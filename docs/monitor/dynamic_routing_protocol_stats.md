# dynamic\_routing\_protocol\_stats


<a name="overview"></a>
## Overview
This resource provides Dynamic Routing Protocol Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* dynamic\_routing\_protocol\_stats : Operations related to dynamic\_routing\_protocol\_stats 




<a name="paths"></a>
## Paths

<a name="dynamic\_routing\_protocol\_stats-get"></a>
### Get operation for dynamic\_routing\_protocol\_stats
```
GET /dynamic_routing_protocol_stats
```


#### Description
Use this operation to get Dynamic Routing Protocol Statistics


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_routing\_protocol\_stats\_response\_schema](#dynamic\_routing\_protocol\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_routing\_protocol\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bgp\_session"></a>
### bgp\_session
In case of bgp\_state protocol filter by corresponding bgp session. Use all for all bgp sessions

*Type* : string


<a name="data"></a>
### data
Data for routing domain and protocol selected

*Type* : string


<a name="dynamic\_routing\_protocol\_stats"></a>
### dynamic\_routing\_protocol\_stats

|Name|Schema|
|---|---|
|**bgp\_session**  <br>*optional*|[bgp\_session](#bgp\_session)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|


<a name="dynamic\_routing\_protocol\_stats\_delete\_success\_schema"></a>
### dynamic\_routing\_protocol\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_routing\_protocol\_stats**  <br>*optional*|[dynamic\_routing\_protocol\_stats](#dynamic\_routing\_protocol\_stats\_delete\_success\_schema-dynamic\_routing\_protocol\_stats)|

<a name="dynamic\_routing\_protocol\_stats\_delete\_success\_schema-dynamic\_routing\_protocol\_stats"></a>
**dynamic\_routing\_protocol\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_routing\_protocol\_stats\_post\_success\_schema"></a>
### dynamic\_routing\_protocol\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_routing\_protocol\_stats**  <br>*optional*|[dynamic\_routing\_protocol\_stats](#dynamic\_routing\_protocol\_stats\_post\_success\_schema-dynamic\_routing\_protocol\_stats)|

<a name="dynamic\_routing\_protocol\_stats\_post\_success\_schema-dynamic\_routing\_protocol\_stats"></a>
**dynamic\_routing\_protocol\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_routing\_protocol\_stats\_put\_success\_schema"></a>
### dynamic\_routing\_protocol\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_routing\_protocol\_stats**  <br>*optional*|[dynamic\_routing\_protocol\_stats](#dynamic\_routing\_protocol\_stats\_put\_success\_schema-dynamic\_routing\_protocol\_stats)|

<a name="dynamic\_routing\_protocol\_stats\_put\_success\_schema-dynamic\_routing\_protocol\_stats"></a>
**dynamic\_routing\_protocol\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_routing\_protocol\_stats\_request\_schema"></a>
### dynamic\_routing\_protocol\_stats\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_routing\_protocol\_stats**  <br>*optional*|[dynamic\_routing\_protocol\_stats](#dynamic\_routing\_protocol\_stats)|


<a name="dynamic\_routing\_protocol\_stats\_response\_schema"></a>
### dynamic\_routing\_protocol\_stats\_response\_schema
*Type* : < [dynamic\_routing\_protocol\_stats\_response\_schema](#dynamic\_routing\_protocol\_stats\_response\_schema-inline) > array

<a name="dynamic\_routing\_protocol\_stats\_response\_schema-inline"></a>
**dynamic\_routing\_protocol\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**bgp\_session**  <br>*optional*|[bgp\_session](#bgp\_session)|
|**data**  <br>*optional*|[data](#data)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|


<a name="protocol"></a>
### protocol
Protocol for which to get stats for. Either bgp or ospf should be enabled.

*Type* : enum (ospf\_interface, ospf\_state, ospf\_topology, ospf\_lsadb, ospf\_neighbors, bgp\_state, route\_table)


<a name="routing\_domain"></a>
### routing\_domain
Routing domain for which to select stats

*Type* : string





