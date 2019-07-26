# flows


<a name="overview"></a>
## Overview
This resource provides details about LAN TO WAN and WAN TO LAN flows


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* flows : Operations related to flows 




<a name="paths"></a>
## Paths

<a name="flows-get"></a>
### Get operation for flows
```
GET /flows
```


#### Description
Use this operation to get the LAN TO WAN and WAN TO LAN flows details. Filters are supported for this API, max\_stats filter is available as an additional option to filter the flows count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[flows\_response\_schema](#flows\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* flows




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


<a name="app\_rule\_id"></a>
### app\_rule\_id
ID of the app rule that traffic on this flow is matched

*Type* : string


<a name="application"></a>
### application
Flow's Application name

*Type* : string


<a name="bytes"></a>
### bytes
Number of bytes sent over the life of the flow

*Type* : string


<a name="class\_type"></a>
### class\_type
Type of virtual path class that traffic is using

*Type* : string


<a name="customer\_kbps"></a>
### customer\_kbps
Kilobits per second over period since refresh

*Type* : string


<a name="dest\_ip"></a>
### dest\_ip
Destination IP Address for packets on this flow

*Type* : string


<a name="dest\_port"></a>
### dest\_port
Destination Port for packets on this flow

*Type* : string


<a name="direction"></a>
### direction
Direction for packets on this flow

*Type* : string


<a name="flows\_delete\_success\_schema"></a>
### flows\_delete\_success\_schema

|Name|Schema|
|---|---|
|**flows**  <br>*optional*|[flows](#flows\_delete\_success\_schema-flows)|

<a name="flows\_delete\_success\_schema-flows"></a>
**flows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="flows\_post\_success\_schema"></a>
### flows\_post\_success\_schema

|Name|Schema|
|---|---|
|**flows**  <br>*optional*|[flows](#flows\_post\_success\_schema-flows)|

<a name="flows\_post\_success\_schema-flows"></a>
**flows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="flows\_put\_success\_schema"></a>
### flows\_put\_success\_schema

|Name|Schema|
|---|---|
|**flows**  <br>*optional*|[flows](#flows\_put\_success\_schema-flows)|

<a name="flows\_put\_success\_schema-flows"></a>
**flows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="flows\_response\_schema"></a>
### flows\_response\_schema
*Type* : < [flows\_response\_schema](#flows\_response\_schema-inline) > array

<a name="flows\_response\_schema-inline"></a>
**flows\_response\_schema**

|Name|Schema|
|---|---|
|**age**  <br>*optional*|[age](#age)|
|**app\_rule\_id**  <br>*optional*|[app\_rule\_id](#app\_rule\_id)|
|**application**  <br>*optional*|[application](#application)|
|**bytes**  <br>*optional*|[bytes](#bytes)|
|**class\_type**  <br>*optional*|[class\_type](#class\_type)|
|**customer\_kbps**  <br>*optional*|[customer\_kbps](#customer\_kbps)|
|**dest\_ip**  <br>*optional*|[dest\_ip](#dest\_ip)|
|**dest\_port**  <br>*optional*|[dest\_port](#dest\_port)|
|**direction**  <br>*optional*|[direction](#direction)|
|**hdr\_compression\_bytes**  <br>*optional*|[hdr\_compression\_bytes](#hdr\_compression\_bytes)|
|**hitcount**  <br>*optional*|[hitcount](#hitcount)|
|**ip\_dscp**  <br>*optional*|[ip\_dscp](#ip\_dscp)|
|**ipp**  <br>*optional*|[ipp](#ipp)|
|**ipsec\_overhead\_kbps**  <br>*optional*|[ipsec\_overhead\_kbps](#ipsec\_overhead\_kbps)|
|**lan\_gw\_ip**  <br>*optional*|[lan\_gw\_ip](#lan\_gw\_ip)|
|**packets**  <br>*optional*|[packets](#packets)|
|**path**  <br>*optional*|[path](#path)|
|**pps**  <br>*optional*|[pps](#pps)|
|**rule\_id**  <br>*optional*|[rule\_id](#rule\_id)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**src\_ip**  <br>*optional*|[src\_ip](#src\_ip)|
|**src\_port**  <br>*optional*|[src\_port](#src\_port)|
|**transmission\_type**  <br>*optional*|[transmission\_type](#transmission\_type)|
|**virtual\_path\_overhead\_kbps**  <br>*optional*|[virtual\_path\_overhead\_kbps](#virtual\_path\_overhead\_kbps)|
|**vpathclass**  <br>*optional*|[vpathclass](#vpathclass)|


<a name="hdr\_compression\_bytes"></a>
### hdr\_compression\_bytes
Number of saved bytes to header compression

*Type* : string


<a name="hitcount"></a>
### hitcount
The Number of times this flow has been searched for and found

*Type* : string


<a name="ip\_dscp"></a>
### ip\_dscp
IP DSCP tag setting for packets on this flow

*Type* : string


<a name="ipp"></a>
### ipp
IP Protocol number for packets on this flow

*Type* : string


<a name="ipsec\_overhead\_kbps"></a>
### ipsec\_overhead\_kbps
Kilobits per second over period since refresh

*Type* : string


<a name="lan\_gw\_ip"></a>
### lan\_gw\_ip
IP Address for LAN Gateway

*Type* : string


<a name="packets"></a>
### packets
Number of packets sent over the life of the flow

*Type* : string


<a name="path"></a>
### path
Path that the traffic is currently using

*Type* : string


<a name="pps"></a>
### pps
Packets per second over period since refresh

*Type* : string


<a name="rule\_id"></a>
### rule\_id
ID of the rule that traffic on this flow is matched

*Type* : string


<a name="service\_name"></a>
### service\_name
Flow Service Name

*Type* : string


<a name="service\_type"></a>
### service\_type
Flow Service Type

*Type* : string


<a name="src\_ip"></a>
### src\_ip
Source IP Address for packets on this flow

*Type* : string


<a name="src\_port"></a>
### src\_port
Source Port for packets on this flow

*Type* : string


<a name="transmission\_type"></a>
### transmission\_type
The Transmission Type that the traffic is currently using

*Type* : string


<a name="virtual\_path\_overhead\_kbps"></a>
### virtual\_path\_overhead\_kbps
Kilobits per second over period since refresh

*Type* : string


<a name="vpathclass"></a>
### vpathclass
ID of virtual path class that traffic is using

*Type* : string





