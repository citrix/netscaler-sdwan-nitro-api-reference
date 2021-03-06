# zen\_branch\_maps


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for zen-branch maps


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* zen\_branch\_maps : Operations related to zen\_branch\_maps 




<a name="paths"></a>
## Paths

<a name="zen\_branch\_maps-post"></a>
### POST operation for zen\_branch\_maps
```
POST /zen_branch_maps
```


#### Description
Use this operation to add zen branch map entry


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[zen\_branch\_maps\_request\_schema](#zen\_branch\_maps\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[zen\_branch\_maps\_post\_success\_schema](#zen\_branch\_maps\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* zen\_branch\_maps


<a name="zen\_branch\_maps-get"></a>
### Get operation for zen\_branch\_maps
```
GET /zen_branch_maps
```


#### Description
Use this operation to get the list of zen branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[zen\_branch\_maps\_response\_schema](#zen\_branch\_maps\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* zen\_branch\_maps


<a name="zen\_branch\_maps-put"></a>
### PUT operation for zen\_branch\_maps
```
PUT /zen_branch_maps
```


#### Description
Use this operation to modify a zen branch map entry


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[zen\_branch\_maps\_put\_success\_schema](#zen\_branch\_maps\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* zen\_branch\_maps


<a name="zen\_branch\_maps-deletepathparam-delete"></a>
### DELETE operation for zen\_branch\_maps
```
DELETE /zen_branch_maps/{deletePathParam}
```


#### Description
Use this operation to delete a zen branch map entry


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[zen\_branch\_maps\_delete\_success\_schema](#zen\_branch\_maps\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* zen\_branch\_maps




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="app\_object"></a>
### app\_object
Application object name

*Type* : string


<a name="fqdn\_id"></a>
### fqdn\_id
unique id for the FQDN name

*Type* : integer


<a name="id"></a>
### id
Auto-generated ID. Use this ID to modify or delete a zen\_branch\_map

*Type* : integer


<a name="location\_id"></a>
### location\_id
location id generated by zscaler portal

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the zen branch map API operation should be performed.

*Type* : string


<a name="primary\_vpn"></a>
### primary\_vpn
primary vpn name

*Type* : string


<a name="secondary\_vpn"></a>
### secondary\_vpn
secondary vpn name

*Type* : string


<a name="sitename"></a>
### sitename
Sitename

*Type* : string


<a name="tunnel\_id"></a>
### tunnel\_id
parent key, tunnel-id

*Type* : integer


<a name="vpn\_id"></a>
### vpn\_id
vpn credential id generated by zscaler portal

*Type* : integer


<a name="vpn\_psk"></a>
### vpn\_psk
vpn credential psk for the tunnel

*Type* : string


<a name="wanlink"></a>
### wanlink
wanlink name

*Type* : string


<a name="zen\_branch\_maps"></a>
### zen\_branch\_maps

|Name|Schema|
|---|---|
|**app\_object**  <br>*optional*|[app\_object](#app\_object)|
|**fqdn\_id**  <br>*optional*|[fqdn\_id](#fqdn\_id)|
|**id**  <br>*optional*|[id](#id)|
|**location\_id**  <br>*optional*|[location\_id](#location\_id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_vpn**  <br>*optional*|[primary\_vpn](#primary\_vpn)|
|**secondary\_vpn**  <br>*optional*|[secondary\_vpn](#secondary\_vpn)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|
|**vpn\_id**  <br>*optional*|[vpn\_id](#vpn\_id)|
|**vpn\_psk**  <br>*optional*|[vpn\_psk](#vpn\_psk)|
|**wanlink**  <br>*optional*|[wanlink](#wanlink)|


<a name="zen\_branch\_maps\_delete\_success\_schema"></a>
### zen\_branch\_maps\_delete\_success\_schema

|Name|Schema|
|---|---|
|**zen\_branch\_maps**  <br>*optional*|[zen\_branch\_maps](#zen\_branch\_maps\_delete\_success\_schema-zen\_branch\_maps)|

<a name="zen\_branch\_maps\_delete\_success\_schema-zen\_branch\_maps"></a>
**zen\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="zen\_branch\_maps\_post\_success\_schema"></a>
### zen\_branch\_maps\_post\_success\_schema

|Name|Schema|
|---|---|
|**zen\_branch\_maps**  <br>*optional*|[zen\_branch\_maps](#zen\_branch\_maps\_post\_success\_schema-zen\_branch\_maps)|

<a name="zen\_branch\_maps\_post\_success\_schema-zen\_branch\_maps"></a>
**zen\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="zen\_branch\_maps\_put\_success\_schema"></a>
### zen\_branch\_maps\_put\_success\_schema

|Name|Schema|
|---|---|
|**zen\_branch\_maps**  <br>*optional*|[zen\_branch\_maps](#zen\_branch\_maps\_put\_success\_schema-zen\_branch\_maps)|

<a name="zen\_branch\_maps\_put\_success\_schema-zen\_branch\_maps"></a>
**zen\_branch\_maps**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="zen\_branch\_maps\_request\_schema"></a>
### zen\_branch\_maps\_request\_schema

|Name|Schema|
|---|---|
|**zen\_branch\_maps**  <br>*optional*|[zen\_branch\_maps](#zen\_branch\_maps)|


<a name="zen\_branch\_maps\_response\_schema"></a>
### zen\_branch\_maps\_response\_schema
*Type* : < [zen\_branch\_maps\_response\_schema](#zen\_branch\_maps\_response\_schema-inline) > array

<a name="zen\_branch\_maps\_response\_schema-inline"></a>
**zen\_branch\_maps\_response\_schema**

|Name|Schema|
|---|---|
|**app\_object**  <br>*optional*|[app\_object](#app\_object)|
|**fqdn\_id**  <br>*optional*|[fqdn\_id](#fqdn\_id)|
|**id**  <br>*optional*|[id](#id)|
|**location\_id**  <br>*optional*|[location\_id](#location\_id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**primary\_vpn**  <br>*optional*|[primary\_vpn](#primary\_vpn)|
|**secondary\_vpn**  <br>*optional*|[secondary\_vpn](#secondary\_vpn)|
|**sitename**  <br>*optional*|[sitename](#sitename)|
|**tunnel\_id**  <br>*optional*|[tunnel\_id](#tunnel\_id)|
|**vpn\_id**  <br>*optional*|[vpn\_id](#vpn\_id)|
|**vpn\_psk**  <br>*optional*|[vpn\_psk](#vpn\_psk)|
|**wanlink**  <br>*optional*|[wanlink](#wanlink)|





