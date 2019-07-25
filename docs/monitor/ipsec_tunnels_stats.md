# ipsec\_tunnels\_stats


<a name="overview"></a>
## Overview
This resource provides IPSec Tunnels Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* ipsec\_tunnels\_stats : Operations related to ipsec\_tunnels\_stats 




<a name="paths"></a>
## Paths

<a name="ipsec\_tunnels\_stats-get"></a>
### Get operation for ipsec\_tunnels\_stats
```
GET /ipsec_tunnels_stats
```


#### Description
Use this operation to get IPSec Tunnels statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ipsec\_tunnels\_stats\_response\_schema](#ipsec\_tunnels\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ipsec\_tunnels\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="mtu"></a>
### MTU
MTU for current IPSec Tunnel

*Type* : integer


<a name="bytes\_dropped"></a>
### bytes\_dropped
Total bytes dropped

*Type* : integer


<a name="ipsec\_tunnels\_stats\_delete\_success\_schema"></a>
### ipsec\_tunnels\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnels\_stats**  <br>*optional*|[ipsec\_tunnels\_stats](#ipsec\_tunnels\_stats\_delete\_success\_schema-ipsec\_tunnels\_stats)|

<a name="ipsec\_tunnels\_stats\_delete\_success\_schema-ipsec\_tunnels\_stats"></a>
**ipsec\_tunnels\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ipsec\_tunnels\_stats\_post\_success\_schema"></a>
### ipsec\_tunnels\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnels\_stats**  <br>*optional*|[ipsec\_tunnels\_stats](#ipsec\_tunnels\_stats\_post\_success\_schema-ipsec\_tunnels\_stats)|

<a name="ipsec\_tunnels\_stats\_post\_success\_schema-ipsec\_tunnels\_stats"></a>
**ipsec\_tunnels\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ipsec\_tunnels\_stats\_put\_success\_schema"></a>
### ipsec\_tunnels\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**ipsec\_tunnels\_stats**  <br>*optional*|[ipsec\_tunnels\_stats](#ipsec\_tunnels\_stats\_put\_success\_schema-ipsec\_tunnels\_stats)|

<a name="ipsec\_tunnels\_stats\_put\_success\_schema-ipsec\_tunnels\_stats"></a>
**ipsec\_tunnels\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ipsec\_tunnels\_stats\_response\_schema"></a>
### ipsec\_tunnels\_stats\_response\_schema
*Type* : < [ipsec\_tunnels\_stats\_response\_schema](#ipsec\_tunnels\_stats\_response\_schema-inline) > array

<a name="ipsec\_tunnels\_stats\_response\_schema-inline"></a>
**ipsec\_tunnels\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**MTU**  <br>*optional*|[MTU](#mtu)|
|**bytes\_dropped**  <br>*optional*|[bytes\_dropped](#bytes\_dropped)|
|**kbps\_received**  <br>*optional*|[kbps\_received](#kbps\_received)|
|**kbps\_sent**  <br>*optional*|[kbps\_sent](#kbps\_sent)|
|**name**  <br>*optional*|[name](#name)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**packets\_sent**  <br>*optional*|[packets\_sent](#packets\_sent)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**state**  <br>*optional*|[state](#state)|


<a name="kbps\_received"></a>
### kbps\_received
Total bytes received

*Type* : integer


<a name="kbps\_sent"></a>
### kbps\_sent
Total bytes received

*Type* : integer


<a name="name"></a>
### name
Name of the IPSec Tunnels

*Type* : string


<a name="packets\_dropped"></a>
### packets\_dropped
Total packets dropped

*Type* : integer


<a name="packets\_received"></a>
### packets\_received
Total packets received

*Type* : integer


<a name="packets\_sent"></a>
### packets\_sent
Total packets sent

*Type* : integer


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
Routing Domain Name to which IPSec Tunnel belong

*Type* : string


<a name="service\_type"></a>
### service\_type
Service Type of the IPSec Tunnel

*Type* : string


<a name="state"></a>
### state
State of the IPSec Tunnels

*Type* : string





