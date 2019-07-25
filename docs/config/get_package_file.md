# get\_package\_file


<a name="overview"></a>
## Overview
Downloads Package File. Note: Please ensure downloaded package name to be saved in zip format for compatibility


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* get\_package\_file : Operations related to get\_package\_file 




<a name="paths"></a>
## Paths

<a name="get\_package\_file-post"></a>
### POST operation for get\_package\_file
```
POST /get_package_file
```


#### Description
Use this operation to Download a package from SD-WAN Appliance


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (file\_download)|
|**Body**|**body**  <br>*optional*||[get\_package\_file\_request\_schema](#get\_package\_file\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|File Download successfully|string (binary)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Consumes

* `application/json`


#### Produces

* `application/octet-stream`
* `application/json`


#### Tags

* get\_package\_file




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_type"></a>
### appliance\_type
Appliance type: primary or secondary appliance

*Type* : enum (primary, secondary)


<a name="get\_package\_file"></a>
### get\_package\_file

|Name|Schema|
|---|---|
|**appliance\_type**  <br>*optional*|[appliance\_type](#appliance\_type)|
|**package\_type**  <br>*optional*|[package\_type](#package\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="get\_package\_file\_delete\_success\_schema"></a>
### get\_package\_file\_delete\_success\_schema

|Name|Schema|
|---|---|
|**get\_package\_file**  <br>*optional*|[get\_package\_file](#get\_package\_file\_delete\_success\_schema-get\_package\_file)|

<a name="get\_package\_file\_delete\_success\_schema-get\_package\_file"></a>
**get\_package\_file**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="get\_package\_file\_post\_success\_schema"></a>
### get\_package\_file\_post\_success\_schema

|Name|Schema|
|---|---|
|**get\_package\_file**  <br>*optional*|[get\_package\_file](#get\_package\_file\_post\_success\_schema-get\_package\_file)|

<a name="get\_package\_file\_post\_success\_schema-get\_package\_file"></a>
**get\_package\_file**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="get\_package\_file\_put\_success\_schema"></a>
### get\_package\_file\_put\_success\_schema

|Name|Schema|
|---|---|
|**get\_package\_file**  <br>*optional*|[get\_package\_file](#get\_package\_file\_put\_success\_schema-get\_package\_file)|

<a name="get\_package\_file\_put\_success\_schema-get\_package\_file"></a>
**get\_package\_file**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="get\_package\_file\_request\_schema"></a>
### get\_package\_file\_request\_schema

|Name|Schema|
|---|---|
|**get\_package\_file**  <br>*optional*|[get\_package\_file](#get\_package\_file)|


<a name="get\_package\_file\_response\_schema"></a>
### get\_package\_file\_response\_schema
*Type* : < [get\_package\_file\_response\_schema](#get\_package\_file\_response\_schema-inline) > array

<a name="get\_package\_file\_response\_schema-inline"></a>
**get\_package\_file\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_type**  <br>*optional*|[appliance\_type](#appliance\_type)|
|**package\_type**  <br>*optional*|[package\_type](#package\_type)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="package\_type"></a>
### package\_type
Download Package Type

*Type* : enum (active, staging)


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string





