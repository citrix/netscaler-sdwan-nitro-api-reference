# file\_upload\_to\_inbox


<a name="overview"></a>
## Overview
File Upload To Inbox


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* file\_upload\_to\_inbox : Operations related to file\_upload\_to\_inbox 




<a name="paths"></a>
## Paths

<a name="file\_upload\_to\_inbox-post"></a>
### POST operation for file\_upload\_to\_inbox
```
POST /file_upload_to_inbox
```


#### Description
Use this operation to upload a saas gateway data image to SD-WAN Appliance.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**FormData**|**filename**  <br>*optional*|string (binary)|


#### Consumes

* `multipart/form-data`


#### Tags

* file\_upload\_to\_inbox




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="file\_upload\_to\_inbox\_delete\_success\_schema"></a>
### file\_upload\_to\_inbox\_delete\_success\_schema

|Name|Schema|
|---|---|
|**file\_upload\_to\_inbox**  <br>*optional*|[file\_upload\_to\_inbox](#file\_upload\_to\_inbox\_delete\_success\_schema-file\_upload\_to\_inbox)|

<a name="file\_upload\_to\_inbox\_delete\_success\_schema-file\_upload\_to\_inbox"></a>
**file\_upload\_to\_inbox**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="file\_upload\_to\_inbox\_post\_success\_schema"></a>
### file\_upload\_to\_inbox\_post\_success\_schema

|Name|Schema|
|---|---|
|**file\_upload\_to\_inbox**  <br>*optional*|[file\_upload\_to\_inbox](#file\_upload\_to\_inbox\_post\_success\_schema-file\_upload\_to\_inbox)|

<a name="file\_upload\_to\_inbox\_post\_success\_schema-file\_upload\_to\_inbox"></a>
**file\_upload\_to\_inbox**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="file\_upload\_to\_inbox\_put\_success\_schema"></a>
### file\_upload\_to\_inbox\_put\_success\_schema

|Name|Schema|
|---|---|
|**file\_upload\_to\_inbox**  <br>*optional*|[file\_upload\_to\_inbox](#file\_upload\_to\_inbox\_put\_success\_schema-file\_upload\_to\_inbox)|

<a name="file\_upload\_to\_inbox\_put\_success\_schema-file\_upload\_to\_inbox"></a>
**file\_upload\_to\_inbox**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="file\_upload\_to\_inbox\_response\_schema"></a>
### file\_upload\_to\_inbox\_response\_schema
*Type* : < [file\_upload\_to\_inbox\_response\_schema](#file\_upload\_to\_inbox\_response\_schema-inline) > array

<a name="file\_upload\_to\_inbox\_response\_schema-inline"></a>
**file\_upload\_to\_inbox\_response\_schema**

|Name|Schema|
|---|---|
|**inbox\_files**  <br>*optional*|[inbox\_files](#inbox\_files)|


<a name="inbox\_files"></a>
### inbox\_files
List of files present in inbox after the file upload operation.

*Type* : < string > array





