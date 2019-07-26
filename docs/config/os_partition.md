# os\_partition


<a name="overview"></a>
## Overview
Os Partition Operations


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* os\_partition : Operations related to os\_partition 




<a name="paths"></a>
## Paths

<a name="os\_partition-post"></a>
### POST operation for os\_partition
```
POST /os_partition
```


#### Description
Switch Between active and backup OS


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (switch, install, clear)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[os\_partition\_post\_success\_schema](#os\_partition\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* os\_partition


<a name="os\_partition-get"></a>
### Get operation for os\_partition
```
GET /os_partition
```


#### Description
Use this operation to Get The OS Partition Version


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[os\_partition\_response\_schema](#os\_partition\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* os\_partition




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="active\_os"></a>
### active\_os
Current Active OS Partition Version

*Type* : string


<a name="backup\_os"></a>
### backup\_os
Backup OS Partition Version

*Type* : string


<a name="os\_partition\_delete\_success\_schema"></a>
### os\_partition\_delete\_success\_schema

|Name|Schema|
|---|---|
|**os\_partition**  <br>*optional*|[os\_partition](#os\_partition\_delete\_success\_schema-os\_partition)|

<a name="os\_partition\_delete\_success\_schema-os\_partition"></a>
**os\_partition**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="os\_partition\_post\_success\_schema"></a>
### os\_partition\_post\_success\_schema

|Name|Schema|
|---|---|
|**os\_partition**  <br>*optional*|[os\_partition](#os\_partition\_post\_success\_schema-os\_partition)|

<a name="os\_partition\_post\_success\_schema-os\_partition"></a>
**os\_partition**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="os\_partition\_put\_success\_schema"></a>
### os\_partition\_put\_success\_schema

|Name|Schema|
|---|---|
|**os\_partition**  <br>*optional*|[os\_partition](#os\_partition\_put\_success\_schema-os\_partition)|

<a name="os\_partition\_put\_success\_schema-os\_partition"></a>
**os\_partition**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="os\_partition\_response\_schema"></a>
### os\_partition\_response\_schema
*Type* : < [os\_partition\_response\_schema](#os\_partition\_response\_schema-inline) > array

<a name="os\_partition\_response\_schema-inline"></a>
**os\_partition\_response\_schema**

|Name|Schema|
|---|---|
|**active\_os**  <br>*optional*|[active\_os](#active\_os)|
|**backup\_os**  <br>*optional*|[backup\_os](#backup\_os)|
|**partition\_files**  <br>*optional*|[partition\_files](#partition\_files)|


<a name="partition\_files"></a>
### partition\_files
List of OS Partition files uploaded

*Type* : string





