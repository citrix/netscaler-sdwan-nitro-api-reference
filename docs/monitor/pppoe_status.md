# pppoe\_status


<a name="overview"></a>
## Overview
This resource provides details about PPPOE enabled VNI and status


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* pppoe\_status : Operations related to pppoe\_status 




<a name="paths"></a>
## Paths

<a name="pppoe\_status-get"></a>
### Get operation for pppoe\_status
```
GET /pppoe_status
```


#### Description
Use this operation to get the pppoe session details. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[pppoe\_status\_response\_schema](#pppoe\_status\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* pppoe\_status




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="gateway\_ip\_address"></a>
### gateway\_ip\_address
IP address of the Gateway

*Type* : string


<a name="local\_ip\_address"></a>
### local\_ip\_address
IP address learned for pppoe connection

*Type* : string


<a name="mac\_associated\_with\_gateway\_ip"></a>
### mac\_associated\_with\_gateway\_ip
MAC address associated with local ip

*Type* : string


<a name="pppoe\_status\_delete\_success\_schema"></a>
### pppoe\_status\_delete\_success\_schema

|Name|Schema|
|---|---|
|**pppoe\_status**  <br>*optional*|[pppoe\_status](#pppoe\_status\_delete\_success\_schema-pppoe\_status)|

<a name="pppoe\_status\_delete\_success\_schema-pppoe\_status"></a>
**pppoe\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="pppoe\_status\_post\_success\_schema"></a>
### pppoe\_status\_post\_success\_schema

|Name|Schema|
|---|---|
|**pppoe\_status**  <br>*optional*|[pppoe\_status](#pppoe\_status\_post\_success\_schema-pppoe\_status)|

<a name="pppoe\_status\_post\_success\_schema-pppoe\_status"></a>
**pppoe\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="pppoe\_status\_put\_success\_schema"></a>
### pppoe\_status\_put\_success\_schema

|Name|Schema|
|---|---|
|**pppoe\_status**  <br>*optional*|[pppoe\_status](#pppoe\_status\_put\_success\_schema-pppoe\_status)|

<a name="pppoe\_status\_put\_success\_schema-pppoe\_status"></a>
**pppoe\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="pppoe\_status\_response\_schema"></a>
### pppoe\_status\_response\_schema
*Type* : < [pppoe\_status\_response\_schema](#pppoe\_status\_response\_schema-inline) > array

<a name="pppoe\_status\_response\_schema-inline"></a>
**pppoe\_status\_response\_schema**

|Name|Schema|
|---|---|
|**gateway\_ip\_address**  <br>*optional*|[gateway\_ip\_address](#gateway\_ip\_address)|
|**local\_ip\_address**  <br>*optional*|[local\_ip\_address](#local\_ip\_address)|
|**mac\_associated\_with\_gateway\_ip**  <br>*optional*|[mac\_associated\_with\_gateway\_ip](#mac\_associated\_with\_gateway\_ip)|
|**session\_id**  <br>*optional*|[session\_id](#session\_id)|
|**status**  <br>*optional*|[status](#status)|
|**status\_message**  <br>*optional*|[status\_message](#status\_message)|
|**vni\_name**  <br>*optional*|[vni\_name](#vni\_name)|


<a name="session\_id"></a>
### session\_id
PPPOE session ID

*Type* : string


<a name="status"></a>
### status
PPPOE session status

*Type* : string


<a name="status\_message"></a>
### status\_message
Comment related to the status of PPPOE session

*Type* : string


<a name="vni\_name"></a>
### vni\_name
Name of the Virtual Network Interface

*Type* : string





