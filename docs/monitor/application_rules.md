# application\_rules


<a name="overview"></a>
## Overview
This resource provides Application Rules Info


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* application\_rules : Operations related to application\_rules 




<a name="paths"></a>
## Paths

<a name="application\_rules-get"></a>
### Get operation for application\_rules
```
GET /application_rules
```


#### Description
Use this operation to get Application rules details.Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_rules\_response\_schema](#application\_rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_rules




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_object"></a>
### application\_object
Application Object Name

*Type* : string


<a name="application\_rules\_delete\_success\_schema"></a>
### application\_rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_rules**  <br>*optional*|[application\_rules](#application\_rules\_delete\_success\_schema-application\_rules)|

<a name="application\_rules\_delete\_success\_schema-application\_rules"></a>
**application\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_rules\_post\_success\_schema"></a>
### application\_rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_rules**  <br>*optional*|[application\_rules](#application\_rules\_post\_success\_schema-application\_rules)|

<a name="application\_rules\_post\_success\_schema-application\_rules"></a>
**application\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_rules\_put\_success\_schema"></a>
### application\_rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_rules**  <br>*optional*|[application\_rules](#application\_rules\_put\_success\_schema-application\_rules)|

<a name="application\_rules\_put\_success\_schema-application\_rules"></a>
**application\_rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_rules\_response\_schema"></a>
### application\_rules\_response\_schema
*Type* : < [application\_rules\_response\_schema](#application\_rules\_response\_schema-inline) > array

<a name="application\_rules\_response\_schema-inline"></a>
**application\_rules\_response\_schema**

|Name|Schema|
|---|---|
|**application\_object**  <br>*optional*|[application\_object](#application\_object)|
|**bytes\_dropped**  <br>*optional*|[bytes\_dropped](#bytes\_dropped)|
|**dpi\_application**  <br>*optional*|[dpi\_application](#dpi\_application)|
|**dpi\_family**  <br>*optional*|[dpi\_family](#dpi\_family)|
|**dst\_ip\_address**  <br>*optional*|[dst\_ip\_address](#dst\_ip\_address)|
|**dst\_port**  <br>*optional*|[dst\_port](#dst\_port)|
|**lan\_to\_wan\_bytes**  <br>*optional*|[lan\_to\_wan\_bytes](#lan\_to\_wan\_bytes)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**num**  <br>*optional*|[num](#num)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service**  <br>*optional*|[service](#service)|
|**site**  <br>*optional*|[site](#site)|
|**src\_ip\_address**  <br>*optional*|[src\_ip\_address](#src\_ip\_address)|
|**src\_port**  <br>*optional*|[src\_port](#src\_port)|
|**time\_since\_last\_hit**  <br>*optional*|[time\_since\_last\_hit](#time\_since\_last\_hit)|
|**wan\_to\_lan\_bytes**  <br>*optional*|[wan\_to\_lan\_bytes](#wan\_to\_lan\_bytes)|
|**wan\_to\_lan\_kbps**  <br>*optional*|[wan\_to\_lan\_kbps](#wan\_to\_lan\_kbps)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|


<a name="bytes\_dropped"></a>
### bytes\_dropped
Bytes Dropped

*Type* : string


<a name="dpi\_application"></a>
### dpi\_application
DPI Application Name

*Type* : string


<a name="dpi\_family"></a>
### dpi\_family
DPI Family Name

*Type* : string


<a name="dst\_ip\_address"></a>
### dst\_ip\_address
Destination IP Address

*Type* : string


<a name="dst\_port"></a>
### dst\_port
Destination Port

*Type* : string


<a name="lan\_to\_wan\_bytes"></a>
### lan\_to\_wan\_bytes
Lan to WAN bytes

*Type* : string


<a name="lan\_to\_wan\_packets"></a>
### lan\_to\_wan\_packets
LAN to WAN Packets

*Type* : string


<a name="num"></a>
### num
Rule Number

*Type* : string


<a name="packets\_dropped"></a>
### packets\_dropped
Number of Packets Dropped

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain Name

*Type* : string


<a name="service"></a>
### service
Service Name

*Type* : string


<a name="site"></a>
### site
Site Name

*Type* : string


<a name="src\_ip\_address"></a>
### src\_ip\_address
Source IP Address

*Type* : string


<a name="src\_port"></a>
### src\_port
Source Port

*Type* : string


<a name="time\_since\_last\_hit"></a>
### time\_since\_last\_hit
Time Since Last Hit

*Type* : string


<a name="wan\_to\_lan\_bytes"></a>
### wan\_to\_lan\_bytes
WAN to LAN Bytes

*Type* : string


<a name="wan\_to\_lan\_kbps"></a>
### wan\_to\_lan\_kbps
WAN to LAN Bandwidth in kbps

*Type* : string


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
WAN to LAN Packets

*Type* : string





