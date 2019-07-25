# radius\_settings


<a name="overview"></a>
## Overview
These APIs can be used to enable/disable RADIUS, Modify or Get RADIUS Settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* radius\_settings : Operations related to radius\_settings 




<a name="paths"></a>
## Paths

<a name="radius\_settings-get"></a>
### Get operation for radius\_settings
```
GET /radius_settings
```


#### Description
Get Radius Settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[radius\_settings\_response\_schema](#radius\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* radius\_settings


<a name="radius\_settings-put"></a>
### PUT operation for radius\_settings
```
PUT /radius_settings
```


#### Description
Use this API to modify RADIUS settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[radius\_settings\_request\_schema](#radius\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[radius\_settings\_put\_success\_schema](#radius\_settings\_put\_success\_schema)|
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

* radius\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="radius\_enabled"></a>
### radius\_enabled
RADIUS enable/disable. Default value is true

*Type* : boolean


<a name="radius\_port"></a>
### radius\_port
Port of Radius server (Value range 1 to 65535)

*Type* : integer


<a name="radius\_port2"></a>
### radius\_port2
Port2 of Radius server (Value range 1 to 65535)

*Type* : integer


<a name="radius\_port3"></a>
### radius\_port3
Port3 of Radius server (Value range 1 to 65535)

*Type* : integer


<a name="radius\_server\_ip\_addr"></a>
### radius\_server\_ip\_addr
IPADDRESS of Radius server

*Type* : string


<a name="radius\_server\_ip\_addr2"></a>
### radius\_server\_ip\_addr2
IPADDRESS2 of Radius server

*Type* : string


<a name="radius\_server\_ip\_addr3"></a>
### radius\_server\_ip\_addr3
IPADDRESS3 of Radius server

*Type* : string


<a name="radius\_server\_key"></a>
### radius\_server\_key
Radius server key

*Type* : string


<a name="radius\_settings"></a>
### radius\_settings

|Name|Schema|
|---|---|
|**radius\_enabled**  <br>*optional*|[radius\_enabled](#radius\_enabled)|
|**radius\_port**  <br>*optional*|[radius\_port](#radius\_port)|
|**radius\_port2**  <br>*optional*|[radius\_port2](#radius\_port2)|
|**radius\_port3**  <br>*optional*|[radius\_port3](#radius\_port3)|
|**radius\_server\_ip\_addr**  <br>*optional*|[radius\_server\_ip\_addr](#radius\_server\_ip\_addr)|
|**radius\_server\_ip\_addr2**  <br>*optional*|[radius\_server\_ip\_addr2](#radius\_server\_ip\_addr2)|
|**radius\_server\_ip\_addr3**  <br>*optional*|[radius\_server\_ip\_addr3](#radius\_server\_ip\_addr3)|
|**radius\_server\_key**  <br>*optional*|[radius\_server\_key](#radius\_server\_key)|
|**radius\_timeout**  <br>*optional*|[radius\_timeout](#radius\_timeout)|


<a name="radius\_settings\_delete\_success\_schema"></a>
### radius\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**radius\_settings**  <br>*optional*|[radius\_settings](#radius\_settings\_delete\_success\_schema-radius\_settings)|

<a name="radius\_settings\_delete\_success\_schema-radius\_settings"></a>
**radius\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="radius\_settings\_post\_success\_schema"></a>
### radius\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**radius\_settings**  <br>*optional*|[radius\_settings](#radius\_settings\_post\_success\_schema-radius\_settings)|

<a name="radius\_settings\_post\_success\_schema-radius\_settings"></a>
**radius\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="radius\_settings\_put\_success\_schema"></a>
### radius\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**radius\_settings**  <br>*optional*|[radius\_settings](#radius\_settings\_put\_success\_schema-radius\_settings)|

<a name="radius\_settings\_put\_success\_schema-radius\_settings"></a>
**radius\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="radius\_settings\_request\_schema"></a>
### radius\_settings\_request\_schema

|Name|Schema|
|---|---|
|**radius\_settings**  <br>*optional*|[radius\_settings](#radius\_settings)|


<a name="radius\_settings\_response\_schema"></a>
### radius\_settings\_response\_schema
*Type* : < [radius\_settings\_response\_schema](#radius\_settings\_response\_schema-inline) > array

<a name="radius\_settings\_response\_schema-inline"></a>
**radius\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**radius\_enabled**  <br>*optional*|[radius\_enabled](#radius\_enabled)|
|**radius\_port**  <br>*optional*|[radius\_port](#radius\_port)|
|**radius\_port2**  <br>*optional*|[radius\_port2](#radius\_port2)|
|**radius\_port3**  <br>*optional*|[radius\_port3](#radius\_port3)|
|**radius\_server\_ip\_addr**  <br>*optional*|[radius\_server\_ip\_addr](#radius\_server\_ip\_addr)|
|**radius\_server\_ip\_addr2**  <br>*optional*|[radius\_server\_ip\_addr2](#radius\_server\_ip\_addr2)|
|**radius\_server\_ip\_addr3**  <br>*optional*|[radius\_server\_ip\_addr3](#radius\_server\_ip\_addr3)|
|**radius\_server\_key**  <br>*optional*|[radius\_server\_key](#radius\_server\_key)|
|**radius\_timeout**  <br>*optional*|[radius\_timeout](#radius\_timeout)|


<a name="radius\_timeout"></a>
### radius\_timeout
Radius timeout in seconds

*Type* : integer





