# local\_change\_management


<a name="overview"></a>
## Overview
This resource provides  Local Change management status and operations related to Local Change Management. Use file\_upload\_to\_inbox API to upload file required for Local Change Management.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* local\_change\_management : Operations related to local\_change\_management 




<a name="paths"></a>
## Paths

<a name="local\_change\_management-post"></a>
### POST operation for local\_change\_management
```
POST /local_change_management
```


#### Description
Does Local Change Management activate operation


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (activate)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[local\_change\_management\_post\_success\_schema](#local\_change\_management\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_change\_management


<a name="local\_change\_management-get"></a>
### Get operation for local\_change\_management
```
GET /local_change_management
```


#### Description
Use this operation to get Local Change Management status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[local\_change\_management\_response\_schema](#local\_change\_management\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_change\_management




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="active\_config"></a>
### active\_config
Active config time .

*Type* : string


<a name="active\_package\_filename"></a>
### active\_package\_filename
Filename of currently active package

*Type* : string


<a name="active\_registry\_timestamp"></a>
### active\_registry\_timestamp
TimeStamp of currently active registries

*Type* : string


<a name="active\_sw\_revision"></a>
### active\_sw\_revision
Currently active software of appliance .

*Type* : string


<a name="id"></a>
### id
Id of the appliance

*Type* : string


<a name="inbox\_files"></a>
### inbox\_files
Files in Change Management Inbox Directory

*Type* : string


<a name="local\_change\_management\_delete\_success\_schema"></a>
### local\_change\_management\_delete\_success\_schema

|Name|Schema|
|---|---|
|**local\_change\_management**  <br>*optional*|[local\_change\_management](#local\_change\_management\_delete\_success\_schema-local\_change\_management)|

<a name="local\_change\_management\_delete\_success\_schema-local\_change\_management"></a>
**local\_change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="local\_change\_management\_post\_success\_schema"></a>
### local\_change\_management\_post\_success\_schema

|Name|Schema|
|---|---|
|**local\_change\_management**  <br>*optional*|[local\_change\_management](#local\_change\_management\_post\_success\_schema-local\_change\_management)|

<a name="local\_change\_management\_post\_success\_schema-local\_change\_management"></a>
**local\_change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="local\_change\_management\_put\_success\_schema"></a>
### local\_change\_management\_put\_success\_schema

|Name|Schema|
|---|---|
|**local\_change\_management**  <br>*optional*|[local\_change\_management](#local\_change\_management\_put\_success\_schema-local\_change\_management)|

<a name="local\_change\_management\_put\_success\_schema-local\_change\_management"></a>
**local\_change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="local\_change\_management\_response\_schema"></a>
### local\_change\_management\_response\_schema
*Type* : < [local\_change\_management\_response\_schema](#local\_change\_management\_response\_schema-inline) > array

<a name="local\_change\_management\_response\_schema-inline"></a>
**local\_change\_management\_response\_schema**

|Name|Schema|
|---|---|
|**active\_config**  <br>*optional*|[active\_config](#active\_config)|
|**active\_package\_filename**  <br>*optional*|[active\_package\_filename](#active\_package\_filename)|
|**active\_registry\_timestamp**  <br>*optional*|[active\_registry\_timestamp](#active\_registry\_timestamp)|
|**active\_sw\_revision**  <br>*optional*|[active\_sw\_revision](#active\_sw\_revision)|
|**id**  <br>*optional*|[id](#id)|
|**inbox\_files**  <br>*optional*|[inbox\_files](#inbox\_files)|
|**message**  <br>*optional*|[message](#message)|
|**model**  <br>*optional*|[model](#model)|
|**staged\_config**  <br>*optional*|[staged\_config](#staged\_config)|
|**staged\_package\_filename**  <br>*optional*|[staged\_package\_filename](#staged\_package\_filename)|
|**staged\_registry\_timestamp**  <br>*optional*|[staged\_registry\_timestamp](#staged\_registry\_timestamp)|
|**staged\_sw\_revision**  <br>*optional*|[staged\_sw\_revision](#staged\_sw\_revision)|
|**transfer\_state**  <br>*optional*|[transfer\_state](#transfer\_state)|


<a name="message"></a>
### message
Local Change Management command message

*Type* : string


<a name="model"></a>
### model
Hardware model of appliance

*Type* : string


<a name="staged\_config"></a>
### staged\_config
Staged config time

*Type* : string


<a name="staged\_package\_filename"></a>
### staged\_package\_filename
Filename of currently staged package

*Type* : string


<a name="staged\_registry\_timestamp"></a>
### staged\_registry\_timestamp
TimeStamp of currently staged registries

*Type* : string


<a name="staged\_sw\_revision"></a>
### staged\_sw\_revision
Staged software version on appliance

*Type* : string


<a name="transfer\_state"></a>
### transfer\_state
transfer state of the local change management process

*Type* : string





