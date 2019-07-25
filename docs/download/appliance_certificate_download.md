# appliance\_certificate\_download


<a name="overview"></a>
## Overview
Appliance Certificate Download


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/download/  
*Schemes* : HTTP


### Tags

* appliance\_certificate\_download : Operations related to appliance\_certificate\_download 




<a name="paths"></a>
## Paths

<a name="appliance\_certificate\_download-get"></a>
### Get operation for appliance\_certificate\_download
```
GET /appliance_certificate_download
```


#### Description
Use this operation to download Appliance Certificate file


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|No Content|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* appliance\_certificate\_download




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_certificate\_download\_delete\_success\_schema"></a>
### appliance\_certificate\_download\_delete\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate\_download**  <br>*optional*|[appliance\_certificate\_download](#appliance\_certificate\_download\_delete\_success\_schema-appliance\_certificate\_download)|

<a name="appliance\_certificate\_download\_delete\_success\_schema-appliance\_certificate\_download"></a>
**appliance\_certificate\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="appliance\_certificate\_download\_post\_success\_schema"></a>
### appliance\_certificate\_download\_post\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate\_download**  <br>*optional*|[appliance\_certificate\_download](#appliance\_certificate\_download\_post\_success\_schema-appliance\_certificate\_download)|

<a name="appliance\_certificate\_download\_post\_success\_schema-appliance\_certificate\_download"></a>
**appliance\_certificate\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="appliance\_certificate\_download\_put\_success\_schema"></a>
### appliance\_certificate\_download\_put\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate\_download**  <br>*optional*|[appliance\_certificate\_download](#appliance\_certificate\_download\_put\_success\_schema-appliance\_certificate\_download)|

<a name="appliance\_certificate\_download\_put\_success\_schema-appliance\_certificate\_download"></a>
**appliance\_certificate\_download**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|





