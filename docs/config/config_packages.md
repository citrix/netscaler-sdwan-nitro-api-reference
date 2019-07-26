# config\_packages


<a name="overview"></a>
## Overview
API to get, export to Change Management, compile and delete config packages


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* config\_packages : Operations related to config\_packages 




<a name="paths"></a>
## Paths

<a name="config\_packages-post"></a>
### POST operation for config\_packages
```
POST /config_packages
```


#### Description
Use this operation to compile the configuration package to get audit errors/warnings list.


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*optional*|Select if action is other that ADD|enum (compile, export\_to\_cm)|
|**Body**|**body**  <br>*optional*||[config\_packages\_request\_schema](#config\_packages\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[config\_packages\_post\_success\_schema](#config\_packages\_post\_success\_schema)|
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

* config\_packages


<a name="config\_packages-get"></a>
### Get operation for config\_packages
```
GET /config_packages
```


#### Description
Use this operation to get the config package information


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[config\_packages\_response\_schema](#config\_packages\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_packages


<a name="config\_packages-deletepathparam-delete"></a>
### DELETE operation for config\_packages
```
DELETE /config_packages/{deletePathParam}
```


#### Description
Use this operation to delete a config package


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[config\_packages\_delete\_success\_schema](#config\_packages\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* config\_packages




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="audits"></a>
### audits
Config package compilation results.


|Name|Description|Schema|
|---|---|---|
|**error**  <br>*optional*  <br>*read-only*|List of error messages.|< [error](#audits-error) > array|
|**notice**  <br>*optional*  <br>*read-only*|List of notice messages.|< [notice](#audits-notice) > array|
|**warning**  <br>*optional*  <br>*read-only*|List of warning messages.|< [warning](#audits-warning) > array|

<a name="audits-error"></a>
**error**

|Name|Description|Schema|
|---|---|---|
|**code**  <br>*optional*  <br>*read-only*|Audit code.|string|
|**msg**  <br>*optional*  <br>*read-only*|Audit message.|string|
|**object**  <br>*optional*  <br>*read-only*|Object to which the audit message corresponds to.|string|
|**parentuiid**  <br>*optional*  <br>*read-only*|Unique identifier of parent object.|string|
|**severity**  <br>*optional*  <br>*read-only*|Severity of the audit message.|string|
|**siteuiid**  <br>*optional*  <br>*read-only*|Site unique identifier of the object corresponding to the audit message.|string|
|**uiid**  <br>*optional*  <br>*read-only*|Unique identifier of the object corresponding to the audit message.|string|

<a name="audits-notice"></a>
**notice**

|Name|Description|Schema|
|---|---|---|
|**code**  <br>*optional*  <br>*read-only*|Audit code.|string|
|**msg**  <br>*optional*  <br>*read-only*|Audit message.|string|
|**object**  <br>*optional*  <br>*read-only*|Object to which the audit message corresponds to.|string|
|**parentuiid**  <br>*optional*  <br>*read-only*|Unique identifier of parent object.|string|
|**severity**  <br>*optional*  <br>*read-only*|Severity of the audit message.|string|
|**siteuiid**  <br>*optional*  <br>*read-only*|Site unique identifier of the object corresponding to the audit message.|string|
|**uiid**  <br>*optional*  <br>*read-only*|Unique identifier of the object corresponding to the audit message.|string|

<a name="audits-warning"></a>
**warning**

|Name|Description|Schema|
|---|---|---|
|**code**  <br>*optional*  <br>*read-only*|Audit code.|string|
|**msg**  <br>*optional*  <br>*read-only*|Audit message.|string|
|**object**  <br>*optional*  <br>*read-only*|Object to which the audit message corresponds to.|string|
|**parentuiid**  <br>*optional*  <br>*read-only*|Unique identifier of parent object.|string|
|**severity**  <br>*optional*  <br>*read-only*|Severity of the audit message.|string|
|**siteuiid**  <br>*optional*  <br>*read-only*|Site unique identifier of the object corresponding to the audit message.|string|
|**uiid**  <br>*optional*  <br>*read-only*|Unique identifier of the object corresponding to the audit message.|string|


<a name="config\_packages"></a>
### config\_packages

|Name|Schema|
|---|---|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="config\_packages\_delete\_success\_schema"></a>
### config\_packages\_delete\_success\_schema

|Name|Schema|
|---|---|
|**config\_packages**  <br>*optional*|[config\_packages](#config\_packages\_delete\_success\_schema-config\_packages)|

<a name="config\_packages\_delete\_success\_schema-config\_packages"></a>
**config\_packages**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="config\_packages\_post\_success\_schema"></a>
### config\_packages\_post\_success\_schema

|Name|Schema|
|---|---|
|**config\_packages**  <br>*optional*|[config\_packages](#config\_packages\_post\_success\_schema-config\_packages)|

<a name="config\_packages\_post\_success\_schema-config\_packages"></a>
**config\_packages**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="config\_packages\_put\_success\_schema"></a>
### config\_packages\_put\_success\_schema

|Name|Schema|
|---|---|
|**config\_packages**  <br>*optional*|[config\_packages](#config\_packages\_put\_success\_schema-config\_packages)|

<a name="config\_packages\_put\_success\_schema-config\_packages"></a>
**config\_packages**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="config\_packages\_request\_schema"></a>
### config\_packages\_request\_schema

|Name|Schema|
|---|---|
|**config\_packages**  <br>*optional*|[config\_packages](#config\_packages)|


<a name="config\_packages\_response\_schema"></a>
### config\_packages\_response\_schema
*Type* : < [config\_packages\_response\_schema](#config\_packages\_response\_schema-inline) > array

<a name="config\_packages\_response\_schema-inline"></a>
**config\_packages\_response\_schema**

|Name|Schema|
|---|---|
|**audits**  <br>*optional*|[audits](#audits)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|


<a name="package\_name"></a>
### package\_name
Name of the config package

*Type* : string





