# service


<a name="overview"></a>
## Overview
This resource gives service related options


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* service : Operations related to service 




<a name="paths"></a>
## Paths

<a name="service-post"></a>
### POST operation for service
```
POST /service
```


#### Description
Disables the SD-WAN Service


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (disable, restart, enable)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[service\_post\_success\_schema](#service\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service


<a name="service-get"></a>
### Get operation for service
```
GET /service
```


#### Description
Use this operation to get SD-WAN Service status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[service\_response\_schema](#service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="message"></a>
### message
Message for the action request

*Type* : string


<a name="service\_delete\_success\_schema"></a>
### service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**service**  <br>*optional*|[service](#service\_delete\_success\_schema-service)|

<a name="service\_delete\_success\_schema-service"></a>
**service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="service\_post\_success\_schema"></a>
### service\_post\_success\_schema

|Name|Schema|
|---|---|
|**service**  <br>*optional*|[service](#service\_post\_success\_schema-service)|

<a name="service\_post\_success\_schema-service"></a>
**service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="service\_put\_success\_schema"></a>
### service\_put\_success\_schema

|Name|Schema|
|---|---|
|**service**  <br>*optional*|[service](#service\_put\_success\_schema-service)|

<a name="service\_put\_success\_schema-service"></a>
**service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="service\_response\_schema"></a>
### service\_response\_schema
*Type* : < [service\_response\_schema](#service\_response\_schema-inline) > array

<a name="service\_response\_schema-inline"></a>
**service\_response\_schema**

|Name|Schema|
|---|---|
|**message**  <br>*optional*|[message](#message)|
|**service\_state**  <br>*optional*|[service\_state](#service\_state)|


<a name="service\_state"></a>
### service\_state
Service state

*Type* : enum (enabled, disabled)





