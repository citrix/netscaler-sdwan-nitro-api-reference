# Citrix NetScaler SD-WAN 11.0 - NITRO REST API

## NITRO API

The NetScaler SD-WAN NITRO API allows you to configure and monitor the appliance programmatically. NITRO provides its functionality through Representational State Transfer (REST) interfaces. Therefore, NITRO applications can be developed in any programming language.

**Note**: You must have a basic understanding of the NetScaler SD-WAN appliance before using the NITRO API.

To use the NITRO API, the client application needs only the following:

* Access to a NetScaler SD-WAN system, version 9.3 or later.
* Have a system to generate HTTPS requests (payload in JSON format) to the NetScaler SD-WAN system. You can use any programming language or tool.

The detailed description of all NITRO resources is provided in the tar.gz file that is available for download using NetScaler SD-WAN Graphical User Interface. To download, navigate to **Configuration** > **Appliance Settings** > **NITRO API** and click **Download Nitro API Doc** button.

## How NITRO Works

The NITRO infrastructure consists of a client application and the NITRO Web service running on a NetScaler SD- WAN system. The communication between the client application and the NITRO web service is based on REST architecture using HTTPS.

As shown in the above figure, a NITRO request is executed as follows:

1. The client application sends REST request message to the NITRO web service.
2. The web service processes the REST request message.
3. The NITRO web service returns the corresponding REST response message to the client application.

NITRO APIs are synchronous in nature. This means that the client application waits for a response from the NITRO web service before executing another NITRO API.

## General API Usage

REST (Representational State Transfer) is an architectural style based on simple HTTPS requests and responses between the client and the server. REST is used to query or change the state of objects on the server side. In REST, the server side is modelled as a set of entities where each entity is identified by a unique URL.

Each resource also has a state on which the following operations can be performed:

* **Create**. Clients can create new server-side resources on a "container" resource. You can think of container resources as folders, and child resources as files or subfolders. The calling client provides the state for the resource to be created. The state can be specified in the request by using JSON format. The HTTPS method used for create requests is POST.
* **Read**. Clients can retrieve the state of a resource by specifying its URL with the HTTPS GET method. The response message contains the resource state, expressed in JSON format.
* **Update**. You can update the state of an existing resource by specifying the URL that identifies that object and its new state in JSON, using the PUT HTTPS method.
* **Delete**. You can destroy a resource that exists on the server-side by using the DELETE HTTPS method and the URL identifying the resource to be removed.

In addition to the above four operations, resources can support other operations or actions. These operations use the HTTPS POST method, with the request body (if applicable) in JSON specifying the details of the operation.

## Authenticating NITRO APIs

NetScaler SD-WAN NITRO APIs work on session based session cookie based authentication. Use login NITRO API with HTTPS POST operation to create session cookie. This session cookie should be used in follow on NITRO requests. After execution of all required NITROs, logout of the system using HTTPS DELETE operation on login NITRO resource.

## API Request Content type

NetScaler SD-WAN NITRO APIs which accept input payload as part of the request need the input to be in JSON format with HTTPS request Content-Type application/json.

NITRO API `file_upload_to_inbox` expects file upload operation to be done with `Content-Type multipart/form-data`.

## Example Usage of NITRO APIs

Following examples are demonstrated using curl as the NITRO API client.

### Scenario: Perform Change Management for Configuration Update

**&#49;.** **Login**

```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login"{"username":"<username>","password":"<password>"}}' -v
```

**&#50;.** **Upload config file**

```
curl -X POST -b /tmp/cookies.txt -H "Content-Type:multipart/form-data" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/file_upload_to_inbox?action=file_upload -F file=@<config_file_name> -v
```

**&#51;.** **Verify config**

```
curl -X POST -b /tmp/cookies.txt -H "Content-Type:application/json" –insecure https://<MCN_IP>/sdwan/nitro/v1/config/change_management?action=verify -v
```

Once you get the "message" : "Successful Verification. Results: Network staging validation successful" , you can proceed to the next step.

In case of failed verification, take corrective action as per the detailed error message mentioned in the verify response. After taking the corrective action perform verify operation once again.

**&#52;.** **Stage**

```
curl -X POST -b /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/change_management?action=stage -v
```

To perform Stage operation, the change management must be in the “appliance_staging state”.

**API to check the Change Management Status:**

```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/change_management -v
```

**&#53;.** **Activate**

```
curl -X POST -b /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/change_management?action=activate -v
```
Activate can be performed only when the change_management in “activate” or “network_staging” state.

**&#54;.** **Logout**

```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -v
```

### Scenario: Get Application summary for Monitoring API’s

1. **Login**
```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login":{"username":"<username>","password":"<password>"}}' –v
```
2. **Applications**
```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/monitor/applications -v
```
3. **Logout**
```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -
```
 
### Scenario: Get Application summary with filters for Monitoring API’s

1. **Login**
```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login":{"username":"<username>","password":"<password>"}}' –v
```
2. **Applications**
```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" --insecure
https://<MCN_IP>/sdwan/nitro/v1/monitor/applications?filter=family:Network%20Service -v
```
3. **Logout**
```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -v
```

### Scenario: Get Application summary with pagination for Monitoring API’s

1. **Login**
```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login":{"username":"<username>","password":"<password>"}}' –v
```
2. **Applications**
```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/monitor/applications?filter=page_no:1 -v
```

If the page number is not specified in the URL, by default NITRO Server will response for first page. The page size is fixed to 50 and can’t be changed by the NITRO client. JSON Response will contain metadata payload which gives information about number of pages available for the request. Sample response is given below

```json
{
	"applications" : {
		"applications" : [ 
		{
			"application" : "Internet Control Message Protocol", 
			"bytes_received" : "0",
			"bytes_sent" : "19423068",
			"family" : "Network Service",
			"total_bytes" : "19423068"
			} 
		],
		"metadata" : [ 
		{
			"no_of_pages" : "2" 
			}
		] 
	}
}
```

&#51;. **Logout**

```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -v
```

### Scenario: Get Application summary with pagination and filter for Monitoring API’s

1. **Login**
```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login":{"username":"<username>","password":"<password>"}}' –v
```
2. **Applications**
```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" --insecure https://<MCN_IP>/sdwan/nitro/v1/monitor/applications?filter=page_no:2;application:iperf -v
```

If the pagination and filters are specified in the query, then the filters are applied first and the result is paginated. Sample response is given below

```json
{
	"applications" : {
		"applications" : [ 
			{
				"application" : "iperf", 
				"bytes_received" : "0", 
				"bytes_sent" : "19424350", 
				"family" : "Network Management", 
				"total_bytes" : "19423099"
			}
		], "metadata" 
		:[
			{
				"no_of_pages" : "2"
			}
		] 
	}
}
```

&#51;. **Logout**

```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" - - insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -v
```

### Scenario: Get Flow summary with max stats filter for Monitoring API’s
1. **Login**
```
curl -X POST -c /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/config/login --data '{"login":{"username":"<username>","password":"<password>"}}' –v
```
2. **Flows**
```
curl -X GET -b /tmp/cookies.txt -H "Content-Type:application/json" -- insecure https://<MCN_IP>/sdwan/nitro/v1/monitor/flows?filter=max_stats:50 -v
```
3. **Logout**
```
curl -X DELETE -b /tmp/cookies.txt -H "Content-Type:application/json" - - insecure https://<MCN_IP>/sdwan/nitro/v1/config/login -v
```

## Monitoring API Usage Table

Below table will clearly explain about the features (Filters/Paginations/MaxStat Filter) supported by various monitoring API’s.

| Monitoring API Name | Filters | Pagination | Max Stat Filter |
|---|---|---|---|
| `applications` | YES | YES | NO |
| `application_rules` | YES | YES | NO |
| `classes` | YES | YES | NO |
| `firewall_connection_stats` | YES | NO | YES |
| `firewall_filter_stats` | YES | NO | YES |
| `firewall_nat_stats` | YES | NO | YES |
| `flows` | YES | NO | YES |
| `ilbflows` | YES | NO | YES |
| `paths` | YES | YES | NO |
| `rules` | YES | YES | NO |
| `tcptermflows` | YES | NO | YES |
| `virtual_paths` | NO | NO | NO |
| `wanlinkstat` | YES | YES | NO |