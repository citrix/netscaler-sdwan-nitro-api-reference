# firewall\_filter\_stats


<a name="overview"></a>
## Overview
This resource provides Firewall Filter Stats


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* firewall\_filter\_stats : Operations related to firewall\_filter\_stats 




<a name="paths"></a>
## Paths

<a name="firewall\_filter\_stats-get"></a>
### Get operation for firewall\_filter\_stats
```
GET /firewall_filter_stats
```


#### Description
Use this operation to get the Firewall Filter Stats,  max\_stats filter is available as an additional option to filter the  count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_filter\_stats\_response\_schema](#firewall\_filter\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_filter\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="action"></a>
### action
The action this policy takes on a possible match

*Type* : string


<a name="allow\_fragments"></a>
### allow\_fragments
Indicates whether fragments matching this filter are allowed

*Type* : enum (0, 1)


<a name="application\_name"></a>
### application\_name
Application for this policy

*Type* : string


<a name="bytes"></a>
### bytes
Total bytes that have matched this policy

*Type* : string


<a name="destination\_firewall\_zone\_name"></a>
### destination\_firewall\_zone\_name
The responding zone used by this policy

*Type* : string


<a name="destination\_ip\_address"></a>
### destination\_ip\_address
Destination IP Address for the policy

*Type* : string


<a name="destination\_port\_or\_icmp\_type"></a>
### destination\_port\_or\_icmp\_type
Responding port ot ICMP code used by this policy

*Type* : string


<a name="destination\_service\_name"></a>
### destination\_service\_name
Destination Service name for the policy

*Type* : string


<a name="destination\_service\_type"></a>
### destination\_service\_type
Destination Service type for the policy

*Type* : string


<a name="dpi\_application\_name"></a>
### dpi\_application\_name
The application for the policy

*Type* : string


<a name="dpi\_family\_name"></a>
### dpi\_family\_name
The family for the policy

*Type* : string


<a name="dscp"></a>
### dscp
DSCP tag used by the policy

*Type* : string


<a name="firewall\_filter\_stats\_delete\_success\_schema"></a>
### firewall\_filter\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_filter\_stats**  <br>*optional*|[firewall\_filter\_stats](#firewall\_filter\_stats\_delete\_success\_schema-firewall\_filter\_stats)|

<a name="firewall\_filter\_stats\_delete\_success\_schema-firewall\_filter\_stats"></a>
**firewall\_filter\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_filter\_stats\_post\_success\_schema"></a>
### firewall\_filter\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_filter\_stats**  <br>*optional*|[firewall\_filter\_stats](#firewall\_filter\_stats\_post\_success\_schema-firewall\_filter\_stats)|

<a name="firewall\_filter\_stats\_post\_success\_schema-firewall\_filter\_stats"></a>
**firewall\_filter\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_filter\_stats\_put\_success\_schema"></a>
### firewall\_filter\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_filter\_stats**  <br>*optional*|[firewall\_filter\_stats](#firewall\_filter\_stats\_put\_success\_schema-firewall\_filter\_stats)|

<a name="firewall\_filter\_stats\_put\_success\_schema-firewall\_filter\_stats"></a>
**firewall\_filter\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_filter\_stats\_response\_schema"></a>
### firewall\_filter\_stats\_response\_schema
*Type* : < [firewall\_filter\_stats\_response\_schema](#firewall\_filter\_stats\_response\_schema-inline) > array

<a name="firewall\_filter\_stats\_response\_schema-inline"></a>
**firewall\_filter\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**action**  <br>*optional*|[action](#action)|
|**allow\_fragments**  <br>*optional*|[allow\_fragments](#allow\_fragments)|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**bytes**  <br>*optional*|[bytes](#bytes)|
|**destination\_firewall\_zone\_name**  <br>*optional*|[destination\_firewall\_zone\_name](#destination\_firewall\_zone\_name)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**destination\_port\_or\_icmp\_type**  <br>*optional*|[destination\_port\_or\_icmp\_type](#destination\_port\_or\_icmp\_type)|
|**destination\_service\_name**  <br>*optional*|[destination\_service\_name](#destination\_service\_name)|
|**destination\_service\_type**  <br>*optional*|[destination\_service\_type](#destination\_service\_type)|
|**dpi\_application\_name**  <br>*optional*|[dpi\_application\_name](#dpi\_application\_name)|
|**dpi\_family\_name**  <br>*optional*|[dpi\_family\_name](#dpi\_family\_name)|
|**dscp**  <br>*optional*|[dscp](#dscp)|
|**ip\_protocol**  <br>*optional*|[ip\_protocol](#ip\_protocol)|
|**log\_connection\_end**  <br>*optional*|[log\_connection\_end](#log\_connection\_end)|
|**log\_connection\_start**  <br>*optional*|[log\_connection\_start](#log\_connection\_start)|
|**match\_established**  <br>*optional*|[match\_established](#match\_established)|
|**packets**  <br>*optional*|[packets](#packets)|
|**port\_or\_icmp\_type**  <br>*optional*|[port\_or\_icmp\_type](#port\_or\_icmp\_type)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**source\_firewall\_zone\_name**  <br>*optional*|[source\_firewall\_zone\_name](#source\_firewall\_zone\_name)|
|**source\_ip\_addr**  <br>*optional*|[source\_ip\_addr](#source\_ip\_addr)|
|**source\_service\_name**  <br>*optional*|[source\_service\_name](#source\_service\_name)|
|**source\_service\_type**  <br>*optional*|[source\_service\_type](#source\_service\_type)|
|**track\_connection**  <br>*optional*|[track\_connection](#track\_connection)|


<a name="ip\_protocol"></a>
### ip\_protocol
IP Protocol for the connection

*Type* : string


<a name="log\_connection\_end"></a>
### log\_connection\_end
Indicates whether the end of connection that match this policy are logged

*Type* : enum (0, 1)


<a name="log\_connection\_start"></a>
### log\_connection\_start
Indicates whether the start of connection that match this policy are logged

*Type* : enum (0, 1)


<a name="match\_established"></a>
### match\_established
Indicates whether packets for an already established connection are matched

*Type* : enum (0, 1)


<a name="packets"></a>
### packets
Total packets that have matched this policy

*Type* : string


<a name="port\_or\_icmp\_type"></a>
### port\_or\_icmp\_type
Originating port ot ICMP code used by this policy

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain Name for the policy

*Type* : string


<a name="source\_firewall\_zone\_name"></a>
### source\_firewall\_zone\_name
The Originating zone used by this policy

*Type* : string


<a name="source\_ip\_addr"></a>
### source\_ip\_addr
Source IP address for the policy

*Type* : string


<a name="source\_service\_name"></a>
### source\_service\_name
Source Service Name for the policy

*Type* : string


<a name="source\_service\_type"></a>
### source\_service\_type
Source Service Type for the policy

*Type* : string


<a name="track\_connection"></a>
### track\_connection
Indicates whether state of the connection matched are tracked

*Type* : enum (0, 1)





