# appliance\_certificate


<a name="overview"></a>
## Overview
Appliance Certificate


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* appliance\_certificate : Operations related to appliance\_certificate 




<a name="paths"></a>
## Paths

<a name="appliance\_certificate-post"></a>
### POST operation for appliance\_certificate
```
POST /appliance_certificate
```


#### Description
Use this operation to regenerate SD-WAN Appliance Certificate


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (regenerate\_appliance\_certificate)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[appliance\_certificate\_post\_success\_schema](#appliance\_certificate\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* appliance\_certificate


<a name="appliance\_certificate-get"></a>
### Get operation for appliance\_certificate
```
GET /appliance_certificate
```


#### Description
Use this operation to get details of appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[appliance\_certificate\_response\_schema](#appliance\_certificate\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* appliance\_certificate




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_certificate\_delete\_success\_schema"></a>
### appliance\_certificate\_delete\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate**  <br>*optional*|[appliance\_certificate](#appliance\_certificate\_delete\_success\_schema-appliance\_certificate)|

<a name="appliance\_certificate\_delete\_success\_schema-appliance\_certificate"></a>
**appliance\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="appliance\_certificate\_post\_success\_schema"></a>
### appliance\_certificate\_post\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate**  <br>*optional*|[appliance\_certificate](#appliance\_certificate\_post\_success\_schema-appliance\_certificate)|

<a name="appliance\_certificate\_post\_success\_schema-appliance\_certificate"></a>
**appliance\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="appliance\_certificate\_put\_success\_schema"></a>
### appliance\_certificate\_put\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_certificate**  <br>*optional*|[appliance\_certificate](#appliance\_certificate\_put\_success\_schema-appliance\_certificate)|

<a name="appliance\_certificate\_put\_success\_schema-appliance\_certificate"></a>
**appliance\_certificate**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="appliance\_certificate\_response\_schema"></a>
### appliance\_certificate\_response\_schema
*Type* : < [appliance\_certificate\_response\_schema](#appliance\_certificate\_response\_schema-inline) > array

<a name="appliance\_certificate\_response\_schema-inline"></a>
**appliance\_certificate\_response\_schema**

|Name|Schema|
|---|---|
|**end\_date**  <br>*optional*|[end\_date](#end\_date)|
|**fingerprint**  <br>*optional*|[fingerprint](#fingerprint)|
|**message**  <br>*optional*|[message](#message)|
|**serial\_number**  <br>*optional*|[serial\_number](#serial\_number)|
|**start\_date**  <br>*optional*|[start\_date](#start\_date)|


<a name="end\_date"></a>
### end\_date
Certificate End date

*Type* : string


<a name="fingerprint"></a>
### fingerprint
Certificate Fingerprint

*Type* : string


<a name="message"></a>
### message
Message about the appliance certificate regeneration

*Type* : string


<a name="serial\_number"></a>
### serial\_number
Certificate Serial Number

*Type* : string


<a name="start\_date"></a>
### start\_date
Certificate Start Date

*Type* : string





