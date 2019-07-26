# apn\_settings


<a name="overview"></a>
## Overview
API to update the Mobile Broadband APN Settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* apn\_settings : Operations related to apn\_settings 




<a name="paths"></a>
## Paths

<a name="apn\_settings-get"></a>
### Get operation for apn\_settings
```
GET /apn_settings
```


#### Description
Use this operation to get the Mobile Broadband APN Settings from SD-WAN Appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[apn\_settings\_response\_schema](#apn\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* apn\_settings


<a name="apn\_settings-put"></a>
### PUT operation for apn\_settings
```
PUT /apn_settings
```


#### Description
Use this operation to update the Mobile Broadband APN Settings in SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[apn\_settings\_request\_schema](#apn\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[apn\_settings\_put\_success\_schema](#apn\_settings\_put\_success\_schema)|
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

* apn\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="apn"></a>
### apn
Name of the Access Point

*Type* : string


<a name="apn\_settings"></a>
### apn\_settings

|Name|Schema|
|---|---|
|**apn**  <br>*optional*|[apn](#apn)|
|**authentication**  <br>*optional*|[authentication](#authentication)|
|**password**  <br>*optional*|[password](#password)|
|**username**  <br>*optional*|[username](#username)|


<a name="apn\_settings\_delete\_success\_schema"></a>
### apn\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**apn\_settings**  <br>*optional*|[apn\_settings](#apn\_settings\_delete\_success\_schema-apn\_settings)|

<a name="apn\_settings\_delete\_success\_schema-apn\_settings"></a>
**apn\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="apn\_settings\_post\_success\_schema"></a>
### apn\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**apn\_settings**  <br>*optional*|[apn\_settings](#apn\_settings\_post\_success\_schema-apn\_settings)|

<a name="apn\_settings\_post\_success\_schema-apn\_settings"></a>
**apn\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="apn\_settings\_put\_success\_schema"></a>
### apn\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**apn\_settings**  <br>*optional*|[apn\_settings](#apn\_settings\_put\_success\_schema-apn\_settings)|

<a name="apn\_settings\_put\_success\_schema-apn\_settings"></a>
**apn\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="apn\_settings\_request\_schema"></a>
### apn\_settings\_request\_schema

|Name|Schema|
|---|---|
|**apn\_settings**  <br>*optional*|[apn\_settings](#apn\_settings)|


<a name="apn\_settings\_response\_schema"></a>
### apn\_settings\_response\_schema
*Type* : < [apn\_settings\_response\_schema](#apn\_settings\_response\_schema-inline) > array

<a name="apn\_settings\_response\_schema-inline"></a>
**apn\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**apn**  <br>*optional*|[apn](#apn)|
|**authentication**  <br>*optional*|[authentication](#authentication)|
|**password**  <br>*optional*|[password](#password)|
|**username**  <br>*optional*|[username](#username)|


<a name="authentication"></a>
### authentication
Authentication for APN. Expected authentications are None, PAP, CHAP and PAPCHAP.

*Type* : enum (None, PAP, CHAP, PAPCHAP)


<a name="password"></a>
### password
Authentication Password for APN.

*Type* : string


<a name="username"></a>
### username
User Name for APN. Valid characters are alphabets, digits, underscore(\_) and hyphen(-) and it should start with an alphabet.

*Type* : string





