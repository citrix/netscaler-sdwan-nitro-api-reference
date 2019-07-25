# firewall\_connection\_stats


<a name="overview"></a>
## Overview
This resource provides Firewall Connection Stats


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* firewall\_connection\_stats : Operations related to firewall\_connection\_stats 




<a name="paths"></a>
## Paths

<a name="firewall\_connection\_stats-get"></a>
### Get operation for firewall\_connection\_stats
```
GET /firewall_connection_stats
```


#### Description
Use this operation to get the Firewall Connection Stats, max\_stats filter is available as an additional option to filter the connection count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_connection\_stats\_response\_schema](#firewall\_connection\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_connection\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="age\_ms"></a>
### age\_ms
Age in Milliseconds of the connection

*Type* : string


<a name="bytes\_received"></a>
### bytes\_received
Bytes Received on the connection

*Type* : string


<a name="bytes\_sent"></a>
### bytes\_sent
Bytes Sent on the connection

*Type* : string


<a name="destination\_firewall\_zone\_name"></a>
### destination\_firewall\_zone\_name
Destination Zone for the connection

*Type* : string


<a name="destination\_ip\_addr"></a>
### destination\_ip\_addr
Destination IP address for the connection

*Type* : string


<a name="destination\_port"></a>
### destination\_port
Destination Port for the connection

*Type* : string


<a name="destination\_route\_service\_name"></a>
### destination\_route\_service\_name
Destination Service Type for the connection

*Type* : string


<a name="destination\_route\_type"></a>
### destination\_route\_type
Destination Service Type for the connection

*Type* : string


<a name="dpi\_application\_name"></a>
### dpi\_application\_name
The application for the connection

*Type* : string


<a name="dpi\_family\_name"></a>
### dpi\_family\_name
The family for the connection

*Type* : string


<a name="firewall\_connection\_stats\_delete\_success\_schema"></a>
### firewall\_connection\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_connection\_stats**  <br>*optional*|[firewall\_connection\_stats](#firewall\_connection\_stats\_delete\_success\_schema-firewall\_connection\_stats)|

<a name="firewall\_connection\_stats\_delete\_success\_schema-firewall\_connection\_stats"></a>
**firewall\_connection\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_connection\_stats\_post\_success\_schema"></a>
### firewall\_connection\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_connection\_stats**  <br>*optional*|[firewall\_connection\_stats](#firewall\_connection\_stats\_post\_success\_schema-firewall\_connection\_stats)|

<a name="firewall\_connection\_stats\_post\_success\_schema-firewall\_connection\_stats"></a>
**firewall\_connection\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_connection\_stats\_put\_success\_schema"></a>
### firewall\_connection\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_connection\_stats**  <br>*optional*|[firewall\_connection\_stats](#firewall\_connection\_stats\_put\_success\_schema-firewall\_connection\_stats)|

<a name="firewall\_connection\_stats\_put\_success\_schema-firewall\_connection\_stats"></a>
**firewall\_connection\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_connection\_stats\_response\_schema"></a>
### firewall\_connection\_stats\_response\_schema
*Type* : < [firewall\_connection\_stats\_response\_schema](#firewall\_connection\_stats\_response\_schema-inline) > array

<a name="firewall\_connection\_stats\_response\_schema-inline"></a>
**firewall\_connection\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**age\_ms**  <br>*optional*|[age\_ms](#age\_ms)|
|**bytes\_received**  <br>*optional*|[bytes\_received](#bytes\_received)|
|**bytes\_sent**  <br>*optional*|[bytes\_sent](#bytes\_sent)|
|**destination\_firewall\_zone\_name**  <br>*optional*|[destination\_firewall\_zone\_name](#destination\_firewall\_zone\_name)|
|**destination\_ip\_addr**  <br>*optional*|[destination\_ip\_addr](#destination\_ip\_addr)|
|**destination\_port**  <br>*optional*|[destination\_port](#destination\_port)|
|**destination\_route\_service\_name**  <br>*optional*|[destination\_route\_service\_name](#destination\_route\_service\_name)|
|**destination\_route\_type**  <br>*optional*|[destination\_route\_type](#destination\_route\_type)|
|**dpi\_application\_name**  <br>*optional*|[dpi\_application\_name](#dpi\_application\_name)|
|**dpi\_family\_name**  <br>*optional*|[dpi\_family\_name](#dpi\_family\_name)|
|**ip\_protocol**  <br>*optional*|[ip\_protocol](#ip\_protocol)|
|**is\_nat**  <br>*optional*|[is\_nat](#is\_nat)|
|**last\_activity\_ms**  <br>*optional*|[last\_activity\_ms](#last\_activity\_ms)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**packets\_sent**  <br>*optional*|[packets\_sent](#packets\_sent)|
|**receive\_bytes\_dropped**  <br>*optional*|[receive\_bytes\_dropped](#receive\_bytes\_dropped)|
|**receive\_packets\_dropped**  <br>*optional*|[receive\_packets\_dropped](#receive\_packets\_dropped)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**sent\_bytes\_dropped**  <br>*optional*|[sent\_bytes\_dropped](#sent\_bytes\_dropped)|
|**sent\_packets\_dropped**  <br>*optional*|[sent\_packets\_dropped](#sent\_packets\_dropped)|
|**source\_firewall\_zone\_name**  <br>*optional*|[source\_firewall\_zone\_name](#source\_firewall\_zone\_name)|
|**source\_ip\_addr**  <br>*optional*|[source\_ip\_addr](#source\_ip\_addr)|
|**source\_port**  <br>*optional*|[source\_port](#source\_port)|
|**source\_route\_service\_name**  <br>*optional*|[source\_route\_service\_name](#source\_route\_service\_name)|
|**source\_route\_type**  <br>*optional*|[source\_route\_type](#source\_route\_type)|
|**state**  <br>*optional*|[state](#state)|


<a name="ip\_protocol"></a>
### ip\_protocol
IP Protocol for the connection

*Type* : string


<a name="is\_nat"></a>
### is\_nat
Indicates if this connection makes use of NAT Policies

*Type* : string


<a name="last\_activity\_ms"></a>
### last\_activity\_ms
Indicates time in milliseconds since last activity on this connection

*Type* : string


<a name="packets\_received"></a>
### packets\_received
Packets Received on the connection

*Type* : string


<a name="packets\_sent"></a>
### packets\_sent
Packets Sent on the connection

*Type* : string


<a name="receive\_bytes\_dropped"></a>
### receive\_bytes\_dropped
Receive Bytes Dropped on the connection

*Type* : string


<a name="receive\_packets\_dropped"></a>
### receive\_packets\_dropped
Receive Packets Dropped on the connection

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain of the connection

*Type* : string


<a name="sent\_bytes\_dropped"></a>
### sent\_bytes\_dropped
Sent Bytes Dropped on the connection

*Type* : string


<a name="sent\_packets\_dropped"></a>
### sent\_packets\_dropped
Sent Packets Dropped on the connection

*Type* : string


<a name="source\_firewall\_zone\_name"></a>
### source\_firewall\_zone\_name
Source Zone for the connection

*Type* : string


<a name="source\_ip\_addr"></a>
### source\_ip\_addr
Source IP address for the connection

*Type* : string


<a name="source\_port"></a>
### source\_port
Source Port for the connection

*Type* : string


<a name="source\_route\_service\_name"></a>
### source\_route\_service\_name
Source Service Type for the connection

*Type* : string


<a name="source\_route\_type"></a>
### source\_route\_type
Source Service Type for the connection

*Type* : string


<a name="state"></a>
### state
The State of this connection

*Type* : string





