# wanlink


<a name="overview"></a>
## Overview
API to modify the wanlink standby mode


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* wanlink : Operations related to wanlink 




<a name="paths"></a>
## Paths

<a name="wanlink-put"></a>
### PUT operation for wanlink
```
PUT /wanlink
```


#### Description
Use this operation to modify wanlink standby mode in SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wanlink\_request\_schema](#wanlink\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wanlink\_put\_success\_schema](#wanlink\_put\_success\_schema)|
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

* wanlink




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="standby\_mode"></a>
### standby\_mode
Standby Mode, 0 for non-standby and 1 for last resort standby

*Type* : boolean


<a name="virtual\_path"></a>
### virtual\_path
Virtual Path Name

*Type* : string


<a name="wanlink"></a>
### wanlink

|Name|Schema|
|---|---|
|**standby\_mode**  <br>*optional*|[standby\_mode](#standby\_mode)|
|**virtual\_path**  <br>*optional*|[virtual\_path](#virtual\_path)|
|**wanlink\_name**  <br>*optional*|[wanlink\_name](#wanlink\_name)|


<a name="wanlink\_delete\_success\_schema"></a>
### wanlink\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wanlink**  <br>*optional*|[wanlink](#wanlink\_delete\_success\_schema-wanlink)|

<a name="wanlink\_delete\_success\_schema-wanlink"></a>
**wanlink**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wanlink\_name"></a>
### wanlink\_name
Wan Link Name

*Type* : string


<a name="wanlink\_post\_success\_schema"></a>
### wanlink\_post\_success\_schema

|Name|Schema|
|---|---|
|**wanlink**  <br>*optional*|[wanlink](#wanlink\_post\_success\_schema-wanlink)|

<a name="wanlink\_post\_success\_schema-wanlink"></a>
**wanlink**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wanlink\_put\_success\_schema"></a>
### wanlink\_put\_success\_schema

|Name|Schema|
|---|---|
|**wanlink**  <br>*optional*|[wanlink](#wanlink\_put\_success\_schema-wanlink)|

<a name="wanlink\_put\_success\_schema-wanlink"></a>
**wanlink**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wanlink\_request\_schema"></a>
### wanlink\_request\_schema

|Name|Schema|
|---|---|
|**wanlink**  <br>*optional*|[wanlink](#wanlink)|


<a name="wanlink\_response\_schema"></a>
### wanlink\_response\_schema
*Type* : < [wanlink\_response\_schema](#wanlink\_response\_schema-inline) > array

<a name="wanlink\_response\_schema-inline"></a>
**wanlink\_response\_schema**

|Name|Schema|
|---|---|
|**standby\_mode**  <br>*optional*|[standby\_mode](#standby\_mode)|
|**virtual\_path**  <br>*optional*|[virtual\_path](#virtual\_path)|
|**wanlink\_name**  <br>*optional*|[wanlink\_name](#wanlink\_name)|





