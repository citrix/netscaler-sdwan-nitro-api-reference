# config\_package\_save\_as


<a name="overview"></a>
## Overview
Rename and Save a configuration package (Save As operation). Allow Overwrite is always enabled in case of API


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* config\_package\_save\_as : Operations related to config\_package\_save\_as 




<a name="paths"></a>
## Paths

<a name="config\_package\_save\_as-post"></a>
### POST operation for config\_package\_save\_as
```
POST /config_package_save_as
```


#### Description
Use this operation to Rename and Save a configuration package (Save As)


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[config\_package\_save\_as\_request\_schema](#config\_package\_save\_as\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[config\_package\_save\_as\_post\_success\_schema](#config\_package\_save\_as\_post\_success\_schema)|
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

* config\_package\_save\_as




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="config\_package\_save\_as"></a>
### config\_package\_save\_as

|Name|Schema|
|---|---|
|**new\_package\_name**  <br>*optional*|[new\_package\_name](#new\_package\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="config\_package\_save\_as\_delete\_success\_schema"></a>
### config\_package\_save\_as\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_save\_as**  <br>*optional*|[config\_package\_save\_as](#config\_package\_save\_as\_delete\_success\_schema-config\_package\_save\_as)|

<a name="config\_package\_save\_as\_delete\_success\_schema-config\_package\_save\_as"></a>
**config\_package\_save\_as**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_package\_save\_as\_post\_success\_schema"></a>
### config\_package\_save\_as\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_save\_as**  <br>*optional*|[config\_package\_save\_as](#config\_package\_save\_as\_post\_success\_schema-config\_package\_save\_as)|

<a name="config\_package\_save\_as\_post\_success\_schema-config\_package\_save\_as"></a>
**config\_package\_save\_as**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_package\_save\_as\_put\_success\_schema"></a>
### config\_package\_save\_as\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_save\_as**  <br>*optional*|[config\_package\_save\_as](#config\_package\_save\_as\_put\_success\_schema-config\_package\_save\_as)|

<a name="config\_package\_save\_as\_put\_success\_schema-config\_package\_save\_as"></a>
**config\_package\_save\_as**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_package\_save\_as\_request\_schema"></a>
### config\_package\_save\_as\_request\_schema

|Name|Schema|
|---|---|
|**config\_package\_save\_as**  <br>*optional*|[config\_package\_save\_as](#config\_package\_save\_as)|


<a name="config\_package\_save\_as\_response\_schema"></a>
### config\_package\_save\_as\_response\_schema
*Type* : < [config\_package\_save\_as\_response\_schema](#config\_package\_save\_as\_response\_schema-inline) > array

<a name="config\_package\_save\_as\_response\_schema-inline"></a>
**config\_package\_save\_as\_response\_schema**

|Name|Schema|
|---|---|
|**new\_package\_name**  <br>*optional*|[new\_package\_name](#new\_package\_name)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="new\_package\_name"></a>
### new\_package\_name
New Config package name.

*Type* : string


<a name="package\_name"></a>
### package\_name
Config package name which has to be renamed.

*Type* : string





