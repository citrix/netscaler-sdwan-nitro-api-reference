# firewall\_nat\_stats


<a name="overview"></a>
## Overview
This resource provides Firewall NAT Stats


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* firewall\_nat\_stats : Operations related to firewall\_nat\_stats 




<a name="paths"></a>
## Paths

<a name="firewall\_nat\_stats-get"></a>
### Get operation for firewall\_nat\_stats
```
GET /firewall_nat_stats
```


#### Description
Use this operation to get the Firewall NAT Stats,  max\_stats filter is available as an additional option to filter the nat count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firewall\_nat\_stats\_response\_schema](#firewall\_nat\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firewall\_nat\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="allow\_related"></a>
### allow\_related
Indicates whether this policy allow related ICMP packets

*Type* : enum (0, 1)


<a name="connections"></a>
### connections
Connections that match this policy

*Type* : string


<a name="enable\_gre\_passthrough"></a>
### enable\_gre\_passthrough
Indicates whether this policy allow passthrough of GRE packets

*Type* : enum (0, 1)


<a name="enable\_ipsec\_passthrough"></a>
### enable\_ipsec\_passthrough
Indicates whether this policy allow passthrough of IPSEC packets

*Type* : enum (0, 1)


<a name="firewall\_nat\_stats\_delete\_success\_schema"></a>
### firewall\_nat\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_nat\_stats**  <br>*optional*|[firewall\_nat\_stats](#firewall\_nat\_stats\_delete\_success\_schema-firewall\_nat\_stats)|

<a name="firewall\_nat\_stats\_delete\_success\_schema-firewall\_nat\_stats"></a>
**firewall\_nat\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firewall\_nat\_stats\_post\_success\_schema"></a>
### firewall\_nat\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_nat\_stats**  <br>*optional*|[firewall\_nat\_stats](#firewall\_nat\_stats\_post\_success\_schema-firewall\_nat\_stats)|

<a name="firewall\_nat\_stats\_post\_success\_schema-firewall\_nat\_stats"></a>
**firewall\_nat\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firewall\_nat\_stats\_put\_success\_schema"></a>
### firewall\_nat\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**firewall\_nat\_stats**  <br>*optional*|[firewall\_nat\_stats](#firewall\_nat\_stats\_put\_success\_schema-firewall\_nat\_stats)|

<a name="firewall\_nat\_stats\_put\_success\_schema-firewall\_nat\_stats"></a>
**firewall\_nat\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firewall\_nat\_stats\_response\_schema"></a>
### firewall\_nat\_stats\_response\_schema
*Type* : < [firewall\_nat\_stats\_response\_schema](#firewall\_nat\_stats\_response\_schema-inline) > array

<a name="firewall\_nat\_stats\_response\_schema-inline"></a>
**firewall\_nat\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**allow\_related**  <br>*optional*|[allow\_related](#allow\_related)|
|**connections**  <br>*optional*|[connections](#connections)|
|**enable\_gre\_passthrough**  <br>*optional*|[enable\_gre\_passthrough](#enable\_gre\_passthrough)|
|**enable\_ipsec\_passthrough**  <br>*optional*|[enable\_ipsec\_passthrough](#enable\_ipsec\_passthrough)|
|**inbound\_bytes**  <br>*optional*|[inbound\_bytes](#inbound\_bytes)|
|**inbound\_packets**  <br>*optional*|[inbound\_packets](#inbound\_packets)|
|**inside\_ip\_address**  <br>*optional*|[inside\_ip\_address](#inside\_ip\_address)|
|**inside\_port**  <br>*optional*|[inside\_port](#inside\_port)|
|**ip\_protocol**  <br>*optional*|[ip\_protocol](#ip\_protocol)|
|**masquerade\_parent**  <br>*optional*|[masquerade\_parent](#masquerade\_parent)|
|**nat\_direction**  <br>*optional*|[nat\_direction](#nat\_direction)|
|**outbound\_bytes**  <br>*optional*|[outbound\_bytes](#outbound\_bytes)|
|**outbound\_packets**  <br>*optional*|[outbound\_packets](#outbound\_packets)|
|**outside\_ip\_address**  <br>*optional*|[outside\_ip\_address](#outside\_ip\_address)|
|**outside\_port**  <br>*optional*|[outside\_port](#outside\_port)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service\_name**  <br>*optional*|[service\_name](#service\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**type**  <br>*optional*|[type](#type)|


<a name="inbound\_bytes"></a>
### inbound\_bytes
Total bytes received that have matched this policy

*Type* : string


<a name="inbound\_packets"></a>
### inbound\_packets
Total packets received that have matched this policy

*Type* : string


<a name="inside\_ip\_address"></a>
### inside\_ip\_address
Inside IP Address in use for the policy

*Type* : string


<a name="inside\_port"></a>
### inside\_port
Inside port(s) used by this policy

*Type* : string


<a name="ip\_protocol"></a>
### ip\_protocol
IP Protocol for the policy

*Type* : string


<a name="masquerade\_parent"></a>
### masquerade\_parent
Parent Dynamic NAT policy of this port forwarding NAT policy

*Type* : string


<a name="nat\_direction"></a>
### nat\_direction
The direction of this policy

*Type* : string


<a name="outbound\_bytes"></a>
### outbound\_bytes
Total bytes sent that have matched this policy

*Type* : string


<a name="outbound\_packets"></a>
### outbound\_packets
Total packets sent that have matched this policy

*Type* : string


<a name="outside\_ip\_address"></a>
### outside\_ip\_address
Outside IP Address in use for the policy

*Type* : string


<a name="outside\_port"></a>
### outside\_port
Outside port(s) used by this policy

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain name of the poilicy

*Type* : string


<a name="service\_name"></a>
### service\_name
Service name of this policy

*Type* : string


<a name="service\_type"></a>
### service\_type
Service type this policy

*Type* : string


<a name="type"></a>
### type
Type of NAT used by this policy

*Type* : string





