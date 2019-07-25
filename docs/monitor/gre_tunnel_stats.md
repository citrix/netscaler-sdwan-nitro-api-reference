# gre\_tunnel\_stats


<a name="overview"></a>
## Overview
This resource provides GRE Tunnels Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* gre\_tunnel\_stats : Operations related to gre\_tunnel\_stats 




<a name="paths"></a>
## Paths

<a name="gre\_tunnel\_stats-get"></a>
### Get operation for gre\_tunnel\_stats
```
GET /gre_tunnel_stats
```


#### Description
Use this operation to get GRE Tunnels statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[gre\_tunnel\_stats\_response\_schema](#gre\_tunnel\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* gre\_tunnel\_stats




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
MTU of current GRE tunnel

*Type* : integer


<a name="destination\_ip\_address"></a>
### destination\_ip\_address
Destination IP Address of the GRE Tunnel

*Type* : string


<a name="gre\_tunnel\_stats\_delete\_success\_schema"></a>
### gre\_tunnel\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnel\_stats**  <br>*optional*|[gre\_tunnel\_stats](#gre\_tunnel\_stats\_delete\_success\_schema-gre\_tunnel\_stats)|

<a name="gre\_tunnel\_stats\_delete\_success\_schema-gre\_tunnel\_stats"></a>
**gre\_tunnel\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="gre\_tunnel\_stats\_post\_success\_schema"></a>
### gre\_tunnel\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnel\_stats**  <br>*optional*|[gre\_tunnel\_stats](#gre\_tunnel\_stats\_post\_success\_schema-gre\_tunnel\_stats)|

<a name="gre\_tunnel\_stats\_post\_success\_schema-gre\_tunnel\_stats"></a>
**gre\_tunnel\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="gre\_tunnel\_stats\_put\_success\_schema"></a>
### gre\_tunnel\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**gre\_tunnel\_stats**  <br>*optional*|[gre\_tunnel\_stats](#gre\_tunnel\_stats\_put\_success\_schema-gre\_tunnel\_stats)|

<a name="gre\_tunnel\_stats\_put\_success\_schema-gre\_tunnel\_stats"></a>
**gre\_tunnel\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="gre\_tunnel\_stats\_response\_schema"></a>
### gre\_tunnel\_stats\_response\_schema
*Type* : < [gre\_tunnel\_stats\_response\_schema](#gre\_tunnel\_stats\_response\_schema-inline) > array

<a name="gre\_tunnel\_stats\_response\_schema-inline"></a>
**gre\_tunnel\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**MTU**  <br>*optional*|[MTU](#mtu)|
|**destination\_ip\_address**  <br>*optional*|[destination\_ip\_address](#destination\_ip\_address)|
|**kbps\_received**  <br>*optional*|[kbps\_received](#kbps\_received)|
|**kbps\_sent**  <br>*optional*|[kbps\_sent](#kbps\_sent)|
|**keepalive\_reply\_received**  <br>*optional*|[keepalive\_reply\_received](#keepalive\_reply\_received)|
|**keepalive\_reply\_sent**  <br>*optional*|[keepalive\_reply\_sent](#keepalive\_reply\_sent)|
|**keepalive\_request\_sent**  <br>*optional*|[keepalive\_request\_sent](#keepalive\_request\_sent)|
|**name**  <br>*optional*|[name](#name)|
|**packets\_dropped**  <br>*optional*|[packets\_dropped](#packets\_dropped)|
|**packets\_fragmented**  <br>*optional*|[packets\_fragmented](#packets\_fragmented)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**packets\_sent**  <br>*optional*|[packets\_sent](#packets\_sent)|
|**public\_source\_ip\_address**  <br>*optional*|[public\_source\_ip\_address](#public\_source\_ip\_address)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**source\_ip\_address**  <br>*optional*|[source\_ip\_address](#source\_ip\_address)|
|**state**  <br>*optional*|[state](#state)|
|**tunnel\_subnet**  <br>*optional*|[tunnel\_subnet](#tunnel\_subnet)|


<a name="kbps\_received"></a>
### kbps\_received
Total kbps received

*Type* : integer


<a name="kbps\_sent"></a>
### kbps\_sent
Total kbps sent

*Type* : integer


<a name="keepalive\_reply\_received"></a>
### keepalive\_reply\_received
Keepalive reply received

*Type* : integer


<a name="keepalive\_reply\_sent"></a>
### keepalive\_reply\_sent
Keepalive reply sent

*Type* : integer


<a name="keepalive\_request\_sent"></a>
### keepalive\_request\_sent
Keepalive Request Sent

*Type* : integer


<a name="name"></a>
### name
Name of the GRE Tunnel

*Type* : string


<a name="packets\_dropped"></a>
### packets\_dropped
Total packets dropped

*Type* : integer


<a name="packets\_fragmented"></a>
### packets\_fragmented
Total packets fragmented

*Type* : integer


<a name="packets\_received"></a>
### packets\_received
Total packets received

*Type* : integer


<a name="packets\_sent"></a>
### packets\_sent
Total packets sent

*Type* : integer


<a name="public\_source\_ip\_address"></a>
### public\_source\_ip\_address
Public Source IP Address of the GRE Tunnel

*Type* : string


<a name="routing\_domain"></a>
### routing\_domain
Routing Domain to which the GRE Tunnel belongs to

*Type* : string


<a name="source\_ip\_address"></a>
### source\_ip\_address
Source IP Address of the GRE Tunnel

*Type* : string


<a name="state"></a>
### state
Current State of the GRE Tunnel

*Type* : string


<a name="tunnel\_subnet"></a>
### tunnel\_subnet
Tunnel Subnet IP Address of the GRE Tunnel

*Type* : string





