# upload\_firmware


<a name="overview"></a>
## Overview
This API is to upload the Mobile Broadband firmware


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* upload\_firmware : Operations related to upload\_firmware 




<a name="paths"></a>
## Paths

<a name="upload\_firmware-post"></a>
### POST operation for upload\_firmware
```
POST /upload_firmware
```


#### Description
Use this operation to Upload a firmware to CB210 Mobile Broadband SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**FormData**|**filename**  <br>*optional*|string (binary)|


#### Consumes

* `multipart/form-data`


#### Tags

* upload\_firmware




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="firmware"></a>
### firmware
Firmware package name

*Type* : < string > array


<a name="upload\_firmware\_delete\_success\_schema"></a>
### upload\_firmware\_delete\_success\_schema

|Name|Schema|
|---|---|
|**upload\_firmware**  <br>*optional*|[upload\_firmware](#upload\_firmware\_delete\_success\_schema-upload\_firmware)|

<a name="upload\_firmware\_delete\_success\_schema-upload\_firmware"></a>
**upload\_firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="upload\_firmware\_post\_success\_schema"></a>
### upload\_firmware\_post\_success\_schema

|Name|Schema|
|---|---|
|**upload\_firmware**  <br>*optional*|[upload\_firmware](#upload\_firmware\_post\_success\_schema-upload\_firmware)|

<a name="upload\_firmware\_post\_success\_schema-upload\_firmware"></a>
**upload\_firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="upload\_firmware\_put\_success\_schema"></a>
### upload\_firmware\_put\_success\_schema

|Name|Schema|
|---|---|
|**upload\_firmware**  <br>*optional*|[upload\_firmware](#upload\_firmware\_put\_success\_schema-upload\_firmware)|

<a name="upload\_firmware\_put\_success\_schema-upload\_firmware"></a>
**upload\_firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="upload\_firmware\_response\_schema"></a>
### upload\_firmware\_response\_schema
*Type* : < [upload\_firmware\_response\_schema](#upload\_firmware\_response\_schema-inline) > array

<a name="upload\_firmware\_response\_schema-inline"></a>
**upload\_firmware\_response\_schema**

|Name|Schema|
|---|---|
|**firmware**  <br>*optional*|[firmware](#firmware)|





