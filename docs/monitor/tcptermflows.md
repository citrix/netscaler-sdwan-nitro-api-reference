# tcptermflows


<a name="overview"></a>
## Overview
This resource provides details about TCP Terminated flows


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* tcptermflows : Operations related to tcptermflows 




<a name="paths"></a>
## Paths

<a name="tcptermflows-get"></a>
### Get operation for tcptermflows
```
GET /tcptermflows
```


#### Description
Use this operation to get TCP Termination flows. Filters are supported for this API. max\_stats filter is available as an additional option to filter the flow count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[tcptermflows\_response\_schema](#tcptermflows\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* tcptermflows




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="age"></a>
### age
How long ago this flow was created in milliseconds

*Type* : string


<a name="bytes\_pending\_to\_lan"></a>
### bytes\_pending\_to\_LAN
Number of bytes currently buffered to send to the LAN for this flow

*Type* : string


<a name="bytes\_pending\_to\_wan"></a>
### bytes\_pending\_to\_WAN
Number of bytes currently buffered to send to the WAN for this flow

*Type* : string


<a name="dest\_ip"></a>
### dest\_ip
Destination IP Address for packets on this flow

*Type* : string


<a name="dest\_port"></a>
### dest\_port
Destination Port for packets on this flow

*Type* : string


<a name="from\_wan\_kbps"></a>
### from\_wan\_kbps
WAN To LAN kilobits per seconds

*Type* : string


<a name="ipp"></a>
### ipp
IP Protocol number for packets on this flow

*Type* : string


<a name="src\_ip"></a>
### src\_ip
Source IP Address for packets on this flow

*Type* : string


<a name="src\_port"></a>
### src\_port
Source Port for packets on this flow

*Type* : string


<a name="state"></a>
### state
Current State of this flow

*Type* : string


<a name="tcptermflows\_delete\_success\_schema"></a>
### tcptermflows\_delete\_success\_schema

|Name|Schema|
|---|---|
|**tcptermflows**  <br>*optional*|[tcptermflows](#tcptermflows\_delete\_success\_schema-tcptermflows)|

<a name="tcptermflows\_delete\_success\_schema-tcptermflows"></a>
**tcptermflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="tcptermflows\_post\_success\_schema"></a>
### tcptermflows\_post\_success\_schema

|Name|Schema|
|---|---|
|**tcptermflows**  <br>*optional*|[tcptermflows](#tcptermflows\_post\_success\_schema-tcptermflows)|

<a name="tcptermflows\_post\_success\_schema-tcptermflows"></a>
**tcptermflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="tcptermflows\_put\_success\_schema"></a>
### tcptermflows\_put\_success\_schema

|Name|Schema|
|---|---|
|**tcptermflows**  <br>*optional*|[tcptermflows](#tcptermflows\_put\_success\_schema-tcptermflows)|

<a name="tcptermflows\_put\_success\_schema-tcptermflows"></a>
**tcptermflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="tcptermflows\_response\_schema"></a>
### tcptermflows\_response\_schema
*Type* : < [tcptermflows\_response\_schema](#tcptermflows\_response\_schema-inline) > array

<a name="tcptermflows\_response\_schema-inline"></a>
**tcptermflows\_response\_schema**

|Name|Schema|
|---|---|
|**age**  <br>*optional*|[age](#age)|
|**bytes\_pending\_to\_LAN**  <br>*optional*|[bytes\_pending\_to\_LAN](#bytes\_pending\_to\_lan)|
|**bytes\_pending\_to\_WAN**  <br>*optional*|[bytes\_pending\_to\_WAN](#bytes\_pending\_to\_wan)|
|**dest\_ip**  <br>*optional*|[dest\_ip](#dest\_ip)|
|**dest\_port**  <br>*optional*|[dest\_port](#dest\_port)|
|**from\_wan\_kbps**  <br>*optional*|[from\_wan\_kbps](#from\_wan\_kbps)|
|**ipp**  <br>*optional*|[ipp](#ipp)|
|**src\_ip**  <br>*optional*|[src\_ip](#src\_ip)|
|**src\_port**  <br>*optional*|[src\_port](#src\_port)|
|**state**  <br>*optional*|[state](#state)|
|**to\_wan\_kbps**  <br>*optional*|[to\_wan\_kbps](#to\_wan\_kbps)|


<a name="to\_wan\_kbps"></a>
### to\_wan\_kbps
LAN To WAN kilobits per seconds

*Type* : string





