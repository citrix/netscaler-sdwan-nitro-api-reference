# enable\_disable\_path


<a name="overview"></a>
## Overview
API to enable or disable a path


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* enable\_disable\_path : Operations related to enable\_disable\_path 




<a name="paths"></a>
## Paths

<a name="enable\_disable\_path-put"></a>
### PUT operation for enable\_disable\_path
```
PUT /enable_disable_path
```


#### Description
Use this operation to modify wanlink standby mode in SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[enable\_disable\_path\_request\_schema](#enable\_disable\_path\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[enable\_disable\_path\_put\_success\_schema](#enable\_disable\_path\_put\_success\_schema)|
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

* enable\_disable\_path




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="enable\_disable\_path"></a>
### enable\_disable\_path

|Name|Schema|
|---|---|
|**from\_wan\_link\_name**  <br>*optional*|[from\_wan\_link\_name](#from\_wan\_link\_name)|
|**path\_is\_enabled**  <br>*optional*|[path\_is\_enabled](#path\_is\_enabled)|
|**to\_wan\_link\_name**  <br>*optional*|[to\_wan\_link\_name](#to\_wan\_link\_name)|


<a name="enable\_disable\_path\_delete\_success\_schema"></a>
### enable\_disable\_path\_delete\_success\_schema

|Name|Schema|
|---|---|
|**enable\_disable\_path**  <br>*optional*|[enable\_disable\_path](#enable\_disable\_path\_delete\_success\_schema-enable\_disable\_path)|

<a name="enable\_disable\_path\_delete\_success\_schema-enable\_disable\_path"></a>
**enable\_disable\_path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="enable\_disable\_path\_post\_success\_schema"></a>
### enable\_disable\_path\_post\_success\_schema

|Name|Schema|
|---|---|
|**enable\_disable\_path**  <br>*optional*|[enable\_disable\_path](#enable\_disable\_path\_post\_success\_schema-enable\_disable\_path)|

<a name="enable\_disable\_path\_post\_success\_schema-enable\_disable\_path"></a>
**enable\_disable\_path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="enable\_disable\_path\_put\_success\_schema"></a>
### enable\_disable\_path\_put\_success\_schema

|Name|Schema|
|---|---|
|**enable\_disable\_path**  <br>*optional*|[enable\_disable\_path](#enable\_disable\_path\_put\_success\_schema-enable\_disable\_path)|

<a name="enable\_disable\_path\_put\_success\_schema-enable\_disable\_path"></a>
**enable\_disable\_path**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="enable\_disable\_path\_request\_schema"></a>
### enable\_disable\_path\_request\_schema

|Name|Schema|
|---|---|
|**enable\_disable\_path**  <br>*optional*|[enable\_disable\_path](#enable\_disable\_path)|


<a name="enable\_disable\_path\_response\_schema"></a>
### enable\_disable\_path\_response\_schema
*Type* : < [enable\_disable\_path\_response\_schema](#enable\_disable\_path\_response\_schema-inline) > array

<a name="enable\_disable\_path\_response\_schema-inline"></a>
**enable\_disable\_path\_response\_schema**

|Name|Schema|
|---|---|
|**from\_wan\_link\_name**  <br>*optional*|[from\_wan\_link\_name](#from\_wan\_link\_name)|
|**path\_is\_enabled**  <br>*optional*|[path\_is\_enabled](#path\_is\_enabled)|
|**to\_wan\_link\_name**  <br>*optional*|[to\_wan\_link\_name](#to\_wan\_link\_name)|


<a name="from\_wan\_link\_name"></a>
### from\_wan\_link\_name
From Wan Link Name

*Type* : string


<a name="path\_is\_enabled"></a>
### path\_is\_enabled
Path enabled state, 1 to enable and 0 to disable

*Type* : boolean


<a name="to\_wan\_link\_name"></a>
### to\_wan\_link\_name
To Wan Link Name

*Type* : string





