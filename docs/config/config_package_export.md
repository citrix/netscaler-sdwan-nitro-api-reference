# config\_package\_export


<a name="overview"></a>
## Overview
Export a configuration package from the Config Editor


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* config\_package\_export : Operations related to config\_package\_export 




<a name="paths"></a>
## Paths

<a name="config\_package\_export-post"></a>
### POST operation for config\_package\_export
```
POST /config_package_export
```


#### Description
Use this operation to export and download a config pcakage as a zip file


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[config\_package\_export\_request\_schema](#config\_package\_export\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[config\_package\_export\_post\_success\_schema](#config\_package\_export\_post\_success\_schema)|
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

* config\_package\_export




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="config\_package\_export"></a>
### config\_package\_export

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="config\_package\_export\_delete\_success\_schema"></a>
### config\_package\_export\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_export**  <br>*optional*|[config\_package\_export](#config\_package\_export\_delete\_success\_schema-config\_package\_export)|

<a name="config\_package\_export\_delete\_success\_schema-config\_package\_export"></a>
**config\_package\_export**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_package\_export\_post\_success\_schema"></a>
### config\_package\_export\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_export**  <br>*optional*|[config\_package\_export](#config\_package\_export\_post\_success\_schema-config\_package\_export)|

<a name="config\_package\_export\_post\_success\_schema-config\_package\_export"></a>
**config\_package\_export**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_package\_export\_put\_success\_schema"></a>
### config\_package\_export\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_export**  <br>*optional*|[config\_package\_export](#config\_package\_export\_put\_success\_schema-config\_package\_export)|

<a name="config\_package\_export\_put\_success\_schema-config\_package\_export"></a>
**config\_package\_export**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_package\_export\_request\_schema"></a>
### config\_package\_export\_request\_schema

|Name|Schema|
|---|---|
|**config\_package\_export**  <br>*optional*|[config\_package\_export](#config\_package\_export)|


<a name="config\_package\_export\_response\_schema"></a>
### config\_package\_export\_response\_schema
*Type* : < [config\_package\_export\_response\_schema](#config\_package\_export\_response\_schema-inline) > array

<a name="config\_package\_export\_response\_schema-inline"></a>
**config\_package\_export\_response\_schema**

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="package\_name"></a>
### package\_name
Config package name which has to be exported from the Config Editor

*Type* : string





