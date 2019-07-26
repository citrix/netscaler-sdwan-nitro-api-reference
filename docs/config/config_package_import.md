# config\_package\_import


<a name="overview"></a>
## Overview
Import a configuration file to the Config Editor


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* config\_package\_import : Operations related to config\_package\_import 




<a name="paths"></a>
## Paths

<a name="config\_package\_import-post"></a>
### POST operation for config\_package\_import
```
POST /config_package_import
```


#### Description
Use this operation to import a file as a configuration package into the Config Editor


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[config\_package\_import\_request\_schema](#config\_package\_import\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[config\_package\_import\_post\_success\_schema](#config\_package\_import\_post\_success\_schema)|
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

* config\_package\_import




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="config\_package\_import"></a>
### config\_package\_import

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="config\_package\_import\_delete\_success\_schema"></a>
### config\_package\_import\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_import**  <br>*optional*|[config\_package\_import](#config\_package\_import\_delete\_success\_schema-config\_package\_import)|

<a name="config\_package\_import\_delete\_success\_schema-config\_package\_import"></a>
**config\_package\_import**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_package\_import\_post\_success\_schema"></a>
### config\_package\_import\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_import**  <br>*optional*|[config\_package\_import](#config\_package\_import\_post\_success\_schema-config\_package\_import)|

<a name="config\_package\_import\_post\_success\_schema-config\_package\_import"></a>
**config\_package\_import**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_package\_import\_put\_success\_schema"></a>
### config\_package\_import\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_package\_import**  <br>*optional*|[config\_package\_import](#config\_package\_import\_put\_success\_schema-config\_package\_import)|

<a name="config\_package\_import\_put\_success\_schema-config\_package\_import"></a>
**config\_package\_import**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_package\_import\_request\_schema"></a>
### config\_package\_import\_request\_schema

|Name|Schema|
|---|---|
|**config\_package\_import**  <br>*optional*|[config\_package\_import](#config\_package\_import)|


<a name="config\_package\_import\_response\_schema"></a>
### config\_package\_import\_response\_schema
*Type* : < [config\_package\_import\_response\_schema](#config\_package\_import\_response\_schema-inline) > array

<a name="config\_package\_import\_response\_schema-inline"></a>
**config\_package\_import\_response\_schema**

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="package\_name"></a>
### package\_name
Config package name to which the uploaded file should be imported.

*Type* : string





