# dynamic\_route


<a name="overview"></a>
## Overview
API to get/add/delete the dynamic route


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* dynamic\_route : Operations related to dynamic\_route 




<a name="paths"></a>
## Paths

<a name="dynamic\_route-post"></a>
### POST operation for dynamic\_route
```
POST /dynamic_route
```


#### Description
Use this operation to add dynamic route IP Information and cost of the routes


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[dynamic\_route\_request\_schema](#dynamic\_route\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[dynamic\_route\_post\_success\_schema](#dynamic\_route\_post\_success\_schema)|
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

* dynamic\_route


<a name="dynamic\_route-get"></a>
### Get operation for dynamic\_route
```
GET /dynamic_route
```


#### Description
Use this operation to get dynamic route IP Information and cost of the routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dynamic\_route\_response\_schema](#dynamic\_route\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_route


<a name="dynamic\_route-put"></a>
### PUT operation for dynamic\_route
```
PUT /dynamic_route
```


#### Description
Use this operation to modify dynamic route IP Information and cost of the routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[dynamic\_route\_put\_success\_schema](#dynamic\_route\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_route


<a name="dynamic\_route-deletepathparam-delete"></a>
### DELETE operation for dynamic\_route
```
DELETE /dynamic_route/{deletePathParam}
```


#### Description
Use this operation to delete dynamic route IP Information and cost of the routes


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[dynamic\_route\_delete\_success\_schema](#dynamic\_route\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dynamic\_route




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="cost"></a>
### cost
Cost of the Route

*Type* : integer


<a name="dynamic\_route"></a>
### dynamic\_route

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**routeip**  <br>*optional*|[routeip](#routeip)|
|**subnet**  <br>*optional*|[subnet](#subnet)|


<a name="dynamic\_route\_delete\_success\_schema"></a>
### dynamic\_route\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_route**  <br>*optional*|[dynamic\_route](#dynamic\_route\_delete\_success\_schema-dynamic\_route)|

<a name="dynamic\_route\_delete\_success\_schema-dynamic\_route"></a>
**dynamic\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dynamic\_route\_post\_success\_schema"></a>
### dynamic\_route\_post\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_route**  <br>*optional*|[dynamic\_route](#dynamic\_route\_post\_success\_schema-dynamic\_route)|

<a name="dynamic\_route\_post\_success\_schema-dynamic\_route"></a>
**dynamic\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dynamic\_route\_put\_success\_schema"></a>
### dynamic\_route\_put\_success\_schema

|Name|Schema|
|---|---|
|**dynamic\_route**  <br>*optional*|[dynamic\_route](#dynamic\_route\_put\_success\_schema-dynamic\_route)|

<a name="dynamic\_route\_put\_success\_schema-dynamic\_route"></a>
**dynamic\_route**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dynamic\_route\_request\_schema"></a>
### dynamic\_route\_request\_schema

|Name|Schema|
|---|---|
|**dynamic\_route**  <br>*optional*|[dynamic\_route](#dynamic\_route)|


<a name="dynamic\_route\_response\_schema"></a>
### dynamic\_route\_response\_schema
*Type* : < [dynamic\_route\_response\_schema](#dynamic\_route\_response\_schema-inline) > array

<a name="dynamic\_route\_response\_schema-inline"></a>
**dynamic\_route\_response\_schema**

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**routeip**  <br>*optional*|[routeip](#routeip)|
|**subnet**  <br>*optional*|[subnet](#subnet)|


<a name="routeip"></a>
### routeip
Route IP Address

*Type* : string


<a name="subnet"></a>
### subnet
Route IP Subnet Information

*Type* : integer





