# tacacs\_settings


<a name="overview"></a>
## Overview
These APIs can be used to enable/disable TACACS+, Modify or Get TACACS+ Settings


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* tacacs\_settings : Operations related to tacacs\_settings 




<a name="paths"></a>
## Paths

<a name="tacacs\_settings-get"></a>
### Get operation for tacacs\_settings
```
GET /tacacs_settings
```


#### Description
Get TACACS+ Settings


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[tacacs\_settings\_response\_schema](#tacacs\_settings\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* tacacs\_settings


<a name="tacacs\_settings-put"></a>
### PUT operation for tacacs\_settings
```
PUT /tacacs_settings
```


#### Description
Use this API to modify TACACS+ settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[tacacs\_settings\_request\_schema](#tacacs\_settings\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[tacacs\_settings\_put\_success\_schema](#tacacs\_settings\_put\_success\_schema)|
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

* tacacs\_settings




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="tacacs\_auth\_type"></a>
### tacacs\_auth\_type
TACACS+ server key

*Type* : enum (PAP, ASCII)


<a name="tacacs\_enabled"></a>
### tacacs\_enabled
TACACS+ enable/disable.

*Type* : boolean


<a name="tacacs\_port"></a>
### tacacs\_port
Port of TACACS+ server (Value range 1 to 65535)

*Type* : integer


<a name="tacacs\_port2"></a>
### tacacs\_port2
Port2 of TACACS+ server (Value range 1 to 65535)

*Type* : integer


<a name="tacacs\_port3"></a>
### tacacs\_port3
Port3 of TACACS+ server (Value range 1 to 65535)

*Type* : integer


<a name="tacacs\_server\_ip\_addr"></a>
### tacacs\_server\_ip\_addr
IPADDRESS of TACACS+ server

*Type* : string


<a name="tacacs\_server\_ip\_addr2"></a>
### tacacs\_server\_ip\_addr2
IPADDRESS2 of TACACS+ server

*Type* : string


<a name="tacacs\_server\_ip\_addr3"></a>
### tacacs\_server\_ip\_addr3
IPADDRESS3 of TACACS+ server

*Type* : string


<a name="tacacs\_server\_key"></a>
### tacacs\_server\_key
TACACS+ server key

*Type* : string


<a name="tacacs\_settings"></a>
### tacacs\_settings

|Name|Schema|
|---|---|
|**tacacs\_auth\_type**  <br>*optional*|[tacacs\_auth\_type](#tacacs\_auth\_type)|
|**tacacs\_enabled**  <br>*optional*|[tacacs\_enabled](#tacacs\_enabled)|
|**tacacs\_port**  <br>*optional*|[tacacs\_port](#tacacs\_port)|
|**tacacs\_port2**  <br>*optional*|[tacacs\_port2](#tacacs\_port2)|
|**tacacs\_port3**  <br>*optional*|[tacacs\_port3](#tacacs\_port3)|
|**tacacs\_server\_ip\_addr**  <br>*optional*|[tacacs\_server\_ip\_addr](#tacacs\_server\_ip\_addr)|
|**tacacs\_server\_ip\_addr2**  <br>*optional*|[tacacs\_server\_ip\_addr2](#tacacs\_server\_ip\_addr2)|
|**tacacs\_server\_ip\_addr3**  <br>*optional*|[tacacs\_server\_ip\_addr3](#tacacs\_server\_ip\_addr3)|
|**tacacs\_server\_key**  <br>*optional*|[tacacs\_server\_key](#tacacs\_server\_key)|
|**tacacs\_timeout**  <br>*optional*|[tacacs\_timeout](#tacacs\_timeout)|


<a name="tacacs\_settings\_delete\_success\_schema"></a>
### tacacs\_settings\_delete\_success\_schema

|Name|Schema|
|---|---|
|**tacacs\_settings**  <br>*optional*|[tacacs\_settings](#tacacs\_settings\_delete\_success\_schema-tacacs\_settings)|

<a name="tacacs\_settings\_delete\_success\_schema-tacacs\_settings"></a>
**tacacs\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="tacacs\_settings\_post\_success\_schema"></a>
### tacacs\_settings\_post\_success\_schema

|Name|Schema|
|---|---|
|**tacacs\_settings**  <br>*optional*|[tacacs\_settings](#tacacs\_settings\_post\_success\_schema-tacacs\_settings)|

<a name="tacacs\_settings\_post\_success\_schema-tacacs\_settings"></a>
**tacacs\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="tacacs\_settings\_put\_success\_schema"></a>
### tacacs\_settings\_put\_success\_schema

|Name|Schema|
|---|---|
|**tacacs\_settings**  <br>*optional*|[tacacs\_settings](#tacacs\_settings\_put\_success\_schema-tacacs\_settings)|

<a name="tacacs\_settings\_put\_success\_schema-tacacs\_settings"></a>
**tacacs\_settings**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="tacacs\_settings\_request\_schema"></a>
### tacacs\_settings\_request\_schema

|Name|Schema|
|---|---|
|**tacacs\_settings**  <br>*optional*|[tacacs\_settings](#tacacs\_settings)|


<a name="tacacs\_settings\_response\_schema"></a>
### tacacs\_settings\_response\_schema
*Type* : < [tacacs\_settings\_response\_schema](#tacacs\_settings\_response\_schema-inline) > array

<a name="tacacs\_settings\_response\_schema-inline"></a>
**tacacs\_settings\_response\_schema**

|Name|Schema|
|---|---|
|**tacacs\_auth\_type**  <br>*optional*|[tacacs\_auth\_type](#tacacs\_auth\_type)|
|**tacacs\_enabled**  <br>*optional*|[tacacs\_enabled](#tacacs\_enabled)|
|**tacacs\_port**  <br>*optional*|[tacacs\_port](#tacacs\_port)|
|**tacacs\_port2**  <br>*optional*|[tacacs\_port2](#tacacs\_port2)|
|**tacacs\_port3**  <br>*optional*|[tacacs\_port3](#tacacs\_port3)|
|**tacacs\_server\_ip\_addr**  <br>*optional*|[tacacs\_server\_ip\_addr](#tacacs\_server\_ip\_addr)|
|**tacacs\_server\_ip\_addr2**  <br>*optional*|[tacacs\_server\_ip\_addr2](#tacacs\_server\_ip\_addr2)|
|**tacacs\_server\_ip\_addr3**  <br>*optional*|[tacacs\_server\_ip\_addr3](#tacacs\_server\_ip\_addr3)|
|**tacacs\_server\_key**  <br>*optional*|[tacacs\_server\_key](#tacacs\_server\_key)|
|**tacacs\_timeout**  <br>*optional*|[tacacs\_timeout](#tacacs\_timeout)|


<a name="tacacs\_timeout"></a>
### tacacs\_timeout
TACACS+ timeout in seconds

*Type* : integer





