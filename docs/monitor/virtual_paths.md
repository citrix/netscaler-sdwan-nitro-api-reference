# virtual\_paths


<a name="overview"></a>
## Overview
This resource provides details of all the virtual paths in the system


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* virtual\_paths : Operations related to virtual\_paths 




<a name="paths"></a>
## Paths

<a name="virtual\_paths-get"></a>
### Get operation for virtual\_paths
```
GET /virtual_paths
```


#### Description
Use this operation to get Virtual Paths status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_paths\_response\_schema](#virtual\_paths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_paths




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="name"></a>
### name
Name of the Virtual Path

*Type* : string


<a name="status"></a>
### status
Virtual Path Status

*Type* : enum (up, down)


<a name="uptime"></a>
### uptime
Uptime of the Virtual Path

*Type* : string


<a name="virtual\_paths\_delete\_success\_schema"></a>
### virtual\_paths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_delete\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_delete\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_paths\_post\_success\_schema"></a>
### virtual\_paths\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_post\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_post\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_paths\_put\_success\_schema"></a>
### virtual\_paths\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_paths**  <br>*optional*|[virtual\_paths](#virtual\_paths\_put\_success\_schema-virtual\_paths)|

<a name="virtual\_paths\_put\_success\_schema-virtual\_paths"></a>
**virtual\_paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_paths\_response\_schema"></a>
### virtual\_paths\_response\_schema
*Type* : < [virtual\_paths\_response\_schema](#virtual\_paths\_response\_schema-inline) > array

<a name="virtual\_paths\_response\_schema-inline"></a>
**virtual\_paths\_response\_schema**

|Name|Schema|
|---|---|
|**name**  <br>*optional*|[name](#name)|
|**status**  <br>*optional*|[status](#status)|
|**uptime**  <br>*optional*|[uptime](#uptime)|





