# local\_license


<a name="overview"></a>
## Overview
Local license configuration


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* local\_license : Operations related to local\_license 




<a name="paths"></a>
## Paths

<a name="local\_license-post"></a>
### POST operation for local\_license
```
POST /local_license
```


#### Description
Apply new local license file (already uploaded).  Action will also enable the local license and disbale remote license.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (uninstall\_license, apply\_license, enable\_local\_server, get\_uploaded\_licenses)|
|**Body**|**body**  <br>*optional*||[local\_license\_request\_schema](#local\_license\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[local\_license\_post\_success\_schema](#local\_license\_post\_success\_schema)|
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

* local\_license


<a name="local\_license-get"></a>
### Get operation for local\_license
```
GET /local_license
```


#### Description
Use this operation to get the list of local license files applied


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[local\_license\_response\_schema](#local\_license\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_license




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="file\_name"></a>
### file\_name
File name to be used for apply/uninstall license

*Type* : string


<a name="installed\_files"></a>
### installed\_files
List of license files installed

*Type* : string


<a name="local\_license"></a>
### local\_license

|Name|Schema|
|---|---|
|**file\_name**  <br>*optional*|[file\_name](#file\_name)|


<a name="local\_license\_delete\_success\_schema"></a>
### local\_license\_delete\_success\_schema

|Name|Schema|
|---|---|
|**local\_license**  <br>*optional*|[local\_license](#local\_license\_delete\_success\_schema-local\_license)|

<a name="local\_license\_delete\_success\_schema-local\_license"></a>
**local\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="local\_license\_post\_success\_schema"></a>
### local\_license\_post\_success\_schema

|Name|Schema|
|---|---|
|**local\_license**  <br>*optional*|[local\_license](#local\_license\_post\_success\_schema-local\_license)|

<a name="local\_license\_post\_success\_schema-local\_license"></a>
**local\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="local\_license\_put\_success\_schema"></a>
### local\_license\_put\_success\_schema

|Name|Schema|
|---|---|
|**local\_license**  <br>*optional*|[local\_license](#local\_license\_put\_success\_schema-local\_license)|

<a name="local\_license\_put\_success\_schema-local\_license"></a>
**local\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="local\_license\_request\_schema"></a>
### local\_license\_request\_schema

|Name|Schema|
|---|---|
|**local\_license**  <br>*optional*|[local\_license](#local\_license)|


<a name="local\_license\_response\_schema"></a>
### local\_license\_response\_schema
*Type* : < [local\_license\_response\_schema](#local\_license\_response\_schema-inline) > array

<a name="local\_license\_response\_schema-inline"></a>
**local\_license\_response\_schema**

|Name|Schema|
|---|---|
|**file\_name**  <br>*optional*|[file\_name](#file\_name)|
|**installed\_files**  <br>*optional*|[installed\_files](#installed\_files)|
|**uploaded\_files**  <br>*optional*|[uploaded\_files](#uploaded\_files)|


<a name="uploaded\_files"></a>
### uploaded\_files
List of license files uploaded

*Type* : string





