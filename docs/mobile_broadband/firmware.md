# firmware


<a name="overview"></a>
## Overview
API to get all firmwares available in the Mobile Broadband device


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* firmware : Operations related to firmware 




<a name="paths"></a>
## Paths

<a name="firmware-get"></a>
### Get operation for firmware
```
GET /firmware
```


#### Description
Use this operation to get the list of Mobile Broadband Firmware


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[firmware\_response\_schema](#firmware\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firmware


<a name="firmware-put"></a>
### PUT operation for firmware
```
PUT /firmware
```


#### Description
Use this operation to update the Firmware in Mobile Broadband Device


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[firmware\_request\_schema](#firmware\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[firmware\_put\_success\_schema](#firmware\_put\_success\_schema)|
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

* firmware


<a name="firmware-deletepathparam-delete"></a>
### DELETE operation for firmware
```
DELETE /firmware/{deletePathParam}
```


#### Description
Use this operation to delete the Firmware in Mobile Broadband Device


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[firmware\_delete\_success\_schema](#firmware\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* firmware




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

|Name|Schema|
|---|---|
|**firmware\_name**  <br>*optional*|[firmware\_name](#firmware\_name)|


<a name="firmware\_delete\_success\_schema"></a>
### firmware\_delete\_success\_schema

|Name|Schema|
|---|---|
|**firmware**  <br>*optional*|[firmware](#firmware\_delete\_success\_schema-firmware)|

<a name="firmware\_delete\_success\_schema-firmware"></a>
**firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="firmware\_name"></a>
### firmware\_name
Name of the firmware. Valid characters are alphabets, digits, underscore(\_), hyphen(-) and dot(.).

*Type* : string


<a name="firmware\_post\_success\_schema"></a>
### firmware\_post\_success\_schema

|Name|Schema|
|---|---|
|**firmware**  <br>*optional*|[firmware](#firmware\_post\_success\_schema-firmware)|

<a name="firmware\_post\_success\_schema-firmware"></a>
**firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="firmware\_put\_success\_schema"></a>
### firmware\_put\_success\_schema

|Name|Schema|
|---|---|
|**firmware**  <br>*optional*|[firmware](#firmware\_put\_success\_schema-firmware)|

<a name="firmware\_put\_success\_schema-firmware"></a>
**firmware**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="firmware\_request\_schema"></a>
### firmware\_request\_schema

|Name|Schema|
|---|---|
|**firmware**  <br>*optional*|[firmware](#firmware)|


<a name="firmware\_response\_schema"></a>
### firmware\_response\_schema
*Type* : < [firmware\_response\_schema](#firmware\_response\_schema-inline) > array

<a name="firmware\_response\_schema-inline"></a>
**firmware\_response\_schema**

|Name|Schema|
|---|---|
|**firmware\_name**  <br>*optional*|[firmware\_name](#firmware\_name)|





