# rules


<a name="overview"></a>
## Overview
This resource provides Rules Info


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* rules : Operations related to rules 




<a name="paths"></a>
## Paths

<a name="rules-get"></a>
### Get operation for rules
```
GET /rules
```


#### Description
Use this operation to get Rules details. Filter and Pagination are supported       for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[rules\_response\_schema](#rules\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* rules




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="avg\_wan\_to\_lan\_latency"></a>
### avg\_wan\_to\_lan\_latency
Avg WAN to LAN Latency

*Type* : string


<a name="bytes\_dropped"></a>
### bytes\_dropped
Bytes Dropped

*Type* : string


<a name="dst\_ip\_address"></a>
### dst\_ip\_address
Dst IP Address

*Type* : string


<a name="dst\_port"></a>
### dst\_port
Destination Port

*Type* : string


<a name="ip\_dscp"></a>
### ip\_dscp
DSCP IP

*Type* : string


<a name="ip\_proto"></a>
### ip\_proto
IP Protocol

*Type* : string


<a name="lan\_to\_wan\_bytes"></a>
### lan\_to\_wan\_bytes
Lan to WAN bytes

*Type* : string


<a name="lan\_to\_wan\_packets"></a>
### lan\_to\_wan\_packets
LAN to WAN Packets

*Type* : string


<a name="last\_wan\_to\_lan\_latency"></a>
### last\_wan\_to\_lan\_latency
Last WAN to LAN Latency

*Type* : string


<a name="max\_wan\_to\_lan\_latency"></a>
### max\_wan\_to\_lan\_latency
Max WAN to LAN Latency

*Type* : string


<a name="min\_wan\_to\_lan\_latency"></a>
### min\_wan\_to\_lan\_latency
Min WAN to LAN Latency

*Type* : string


<a name="num"></a>
### num
Rule Number

*Type* : string


<a name="packets\_dropped"></a>
### packets\_dropped
Packets Dropped

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain Name

*Type* : string


<a name="rules\_delete\_success\_schema"></a>
### rules\_delete\_success\_schema

|Name|Schema|
|---|---|
|**rules**  <br>*optional*|[rules](#rules\_delete\_success\_schema-rules)|

<a name="rules\_delete\_success\_schema-rules"></a>
**rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="rules\_post\_success\_schema"></a>
### rules\_post\_success\_schema

|Name|Schema|
|---|---|
|**rules**  <br>*optional*|[rules](#rules\_post\_success\_schema-rules)|

<a name="rules\_post\_success\_schema-rules"></a>
**rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="rules\_put\_success\_schema"></a>
### rules\_put\_success\_schema

|Name|Schema|
|---|---|
|**rules**  <br>*optional*|[rules](#rules\_put\_success\_schema-rules)|

<a name="rules\_put\_success\_schema-rules"></a>
**rules**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="rules\_response\_schema"></a>
### rules\_response\_schema
*Type* : < [rules\_response\_schema](#rules\_response\_schema-inline) > array

<a name="rules\_response\_schema-inline"></a>
**rules\_response\_schema**

|Name|Schema|
|---|---|
|**avg\_wan\_to\_lan\_latency**  <br>*optional*|[avg\_wan\_to\_lan\_latency](#avg\_wan\_to\_lan\_latency)|
|**bytes\_dropped**  <br>*optional*|[bytes\_dropped](#bytes\_dropped)|
|**dst\_ip\_address**  <br>*optional*|[dst\_ip\_address](#dst\_ip\_address)|
|**dst\_port**  <br>*optional*|[dst\_port](#dst\_port)|
|**ip\_dscp**  <br>*optional*|[ip\_dscp](#ip\_dscp)|
|**ip\_proto**  <br>*optional*|[ip\_proto](#ip\_proto)|
|**lan\_to\_wan\_bytes**  <br>*optional*|[lan\_to\_wan\_bytes](#lan\_to\_wan\_bytes)|
|**lan\_to\_wan\_packets**  <br>*optional*|[lan\_to\_wan\_packets](#lan\_to\_wan\_packets)|
|**last\_wan\_to\_lan\_latency**  <br>*optional*|[last\_wan\_to\_lan\_latency](#last\_wan\_to\_lan\_latency)|
|**max\_wan\_to\_lan\_latency**  <br>*optional*|[max\_wan\_to\_lan\_latency](#max\_wan\_to\_lan\_latency)|
|**min\_wan\_to\_lan\_latency**  <br>*optional*|[min\_wan\_to\_lan\_latency](#min\_wan\_to\_lan\_latency)|
|**num**  <br>*optional*|[num](#num)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service**  <br>*optional*|[service](#service)|
|**site**  <br>*optional*|[site](#site)|
|**src\_ip\_address**  <br>*optional*|[src\_ip\_address](#src\_ip\_address)|
|**src\_port**  <br>*optional*|[src\_port](#src\_port)|
|**time\_since\_last\_hit**  <br>*optional*|[time\_since\_last\_hit](#time\_since\_last\_hit)|
|**vlan\_id**  <br>*optional*|[vlan\_id](#vlan\_id)|
|**wan\_to\_lan\_bytes**  <br>*optional*|[wan\_to\_lan\_bytes](#wan\_to\_lan\_bytes)|
|**wan\_to\_lan\_jitter**  <br>*optional*|[wan\_to\_lan\_jitter](#wan\_to\_lan\_jitter)|
|**wan\_to\_lan\_kbps**  <br>*optional*|[wan\_to\_lan\_kbps](#wan\_to\_lan\_kbps)|
|**wan\_to\_lan\_packets**  <br>*optional*|[wan\_to\_lan\_packets](#wan\_to\_lan\_packets)|
|**wan\_to\_lan\_packets\_lost**  <br>*optional*|[wan\_to\_lan\_packets\_lost](#wan\_to\_lan\_packets\_lost)|


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
Src IP Address

*Type* : string


<a name="src\_port"></a>
### src\_port
Src Port

*Type* : string


<a name="time\_since\_last\_hit"></a>
### time\_since\_last\_hit
Time Since Last Hit

*Type* : string


<a name="vlan\_id"></a>
### vlan\_id
VLAN ID

*Type* : string


<a name="wan\_to\_lan\_bytes"></a>
### wan\_to\_lan\_bytes
WAN to LAN Bytes

*Type* : string


<a name="wan\_to\_lan\_jitter"></a>
### wan\_to\_lan\_jitter
WAN to LAN Jitter

*Type* : string


<a name="wan\_to\_lan\_kbps"></a>
### wan\_to\_lan\_kbps
WAN to LAN Bandwidth

*Type* : string


<a name="wan\_to\_lan\_packets"></a>
### wan\_to\_lan\_packets
WAN to LAN Packets

*Type* : string


<a name="wan\_to\_lan\_packets\_lost"></a>
### wan\_to\_lan\_packets\_lost
WAN to LAN Packets Lost

*Type* : string





