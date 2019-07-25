# sim\_pin\_operations


<a name="overview"></a>
## Overview
This resource is to enable/disable/verify/modify/unblock SIM PIN


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* sim\_pin\_operations : Operations related to sim\_pin\_operations 




<a name="paths"></a>
## Paths

<a name="sim\_pin\_operations-post"></a>
### POST operation for sim\_pin\_operations
```
POST /sim_pin_operations
```


#### Description
Use this operation to unblock SIM


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (unblock\_pin, modify\_pin, enable\_pin, disable\_pin, verify\_pin)|
|**Body**|**body**  <br>*optional*||[sim\_pin\_operations\_request\_schema](#sim\_pin\_operations\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[sim\_pin\_operations\_post\_success\_schema](#sim\_pin\_operations\_post\_success\_schema)|
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

* sim\_pin\_operations




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="confirm\_new\_pin"></a>
### confirm\_new\_pin
Confirm the New SIM PIN for modify operation

*Type* : string


<a name="new\_pin"></a>
### new\_pin
New SIM PIN for modify operation

*Type* : string


<a name="old\_pin"></a>
### old\_pin
Old SIM PIN for modify operation

*Type* : string


<a name="pin"></a>
### pin
SIM PIN for enable/disable/verify/unblock operations

*Type* : string


<a name="puk"></a>
### puk
SIM PUK for unblock operation

*Type* : string


<a name="sim\_pin\_operations"></a>
### sim\_pin\_operations

|Name|Schema|
|---|---|
|**confirm\_new\_pin**  <br>*optional*|[confirm\_new\_pin](#confirm\_new\_pin)|
|**new\_pin**  <br>*optional*|[new\_pin](#new\_pin)|
|**old\_pin**  <br>*optional*|[old\_pin](#old\_pin)|
|**pin**  <br>*optional*|[pin](#pin)|
|**puk**  <br>*optional*|[puk](#puk)|


<a name="sim\_pin\_operations\_delete\_success\_schema"></a>
### sim\_pin\_operations\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_operations**  <br>*optional*|[sim\_pin\_operations](#sim\_pin\_operations\_delete\_success\_schema-sim\_pin\_operations)|

<a name="sim\_pin\_operations\_delete\_success\_schema-sim\_pin\_operations"></a>
**sim\_pin\_operations**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sim\_pin\_operations\_post\_success\_schema"></a>
### sim\_pin\_operations\_post\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_operations**  <br>*optional*|[sim\_pin\_operations](#sim\_pin\_operations\_post\_success\_schema-sim\_pin\_operations)|

<a name="sim\_pin\_operations\_post\_success\_schema-sim\_pin\_operations"></a>
**sim\_pin\_operations**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sim\_pin\_operations\_put\_success\_schema"></a>
### sim\_pin\_operations\_put\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_operations**  <br>*optional*|[sim\_pin\_operations](#sim\_pin\_operations\_put\_success\_schema-sim\_pin\_operations)|

<a name="sim\_pin\_operations\_put\_success\_schema-sim\_pin\_operations"></a>
**sim\_pin\_operations**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sim\_pin\_operations\_request\_schema"></a>
### sim\_pin\_operations\_request\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_operations**  <br>*optional*|[sim\_pin\_operations](#sim\_pin\_operations)|


<a name="sim\_pin\_operations\_response\_schema"></a>
### sim\_pin\_operations\_response\_schema
*Type* : < [sim\_pin\_operations\_response\_schema](#sim\_pin\_operations\_response\_schema-inline) > array

<a name="sim\_pin\_operations\_response\_schema-inline"></a>
**sim\_pin\_operations\_response\_schema**

|Name|Schema|
|---|---|
|**confirm\_new\_pin**  <br>*optional*|[confirm\_new\_pin](#confirm\_new\_pin)|
|**new\_pin**  <br>*optional*|[new\_pin](#new\_pin)|
|**old\_pin**  <br>*optional*|[old\_pin](#old\_pin)|
|**pin**  <br>*optional*|[pin](#pin)|
|**puk**  <br>*optional*|[puk](#puk)|





