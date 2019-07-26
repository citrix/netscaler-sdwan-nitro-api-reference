# pcap\_download


<a name="overview"></a>
## Overview
Packet Capture Download


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/download/  
*Schemes* : HTTP


### Tags

* pcap\_download : Operations related to pcap\_download 




<a name="paths"></a>
## Paths

<a name="pcap\_download-get"></a>
### Get operation for pcap\_download
```
GET /pcap_download
```


#### Description
Use this operation to download Packet Capture file


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|No Content|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* pcap\_download




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="pcap\_download\_delete\_success\_schema"></a>
### pcap\_download\_delete\_success\_schema

|Name|Schema|
|---|---|
|**pcap\_download**  <br>*optional*|[pcap\_download](#pcap\_download\_delete\_success\_schema-pcap\_download)|

<a name="pcap\_download\_delete\_success\_schema-pcap\_download"></a>
**pcap\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="pcap\_download\_post\_success\_schema"></a>
### pcap\_download\_post\_success\_schema

|Name|Schema|
|---|---|
|**pcap\_download**  <br>*optional*|[pcap\_download](#pcap\_download\_post\_success\_schema-pcap\_download)|

<a name="pcap\_download\_post\_success\_schema-pcap\_download"></a>
**pcap\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="pcap\_download\_put\_success\_schema"></a>
### pcap\_download\_put\_success\_schema

|Name|Schema|
|---|---|
|**pcap\_download**  <br>*optional*|[pcap\_download](#pcap\_download\_put\_success\_schema-pcap\_download)|

<a name="pcap\_download\_put\_success\_schema-pcap\_download"></a>
**pcap\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|





