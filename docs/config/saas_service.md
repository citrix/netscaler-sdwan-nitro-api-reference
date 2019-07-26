# saas\_service


<a name="overview"></a>
## Overview
This resource gives saas gateway service related options


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* saas\_service : Operations related to saas\_service 




<a name="paths"></a>
## Paths

<a name="saas\_service-post"></a>
### POST operation for saas\_service
```
POST /saas_service
```


#### Description
Enables the SD-WAN SaaS Gateway Service


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (enable, disable)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[saas\_service\_post\_success\_schema](#saas\_service\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_service


<a name="saas\_service-get"></a>
### Get operation for saas\_service
```
GET /saas_service
```


#### Description
Use this operation to get SD-WAN SaaS Gateway Service status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[saas\_service\_response\_schema](#saas\_service\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* saas\_service




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="saas\_service\_delete\_success\_schema"></a>
### saas\_service\_delete\_success\_schema

|Name|Schema|
|---|---|
|**saas\_service**  <br>*optional*|[saas\_service](#saas\_service\_delete\_success\_schema-saas\_service)|

<a name="saas\_service\_delete\_success\_schema-saas\_service"></a>
**saas\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="saas\_service\_post\_success\_schema"></a>
### saas\_service\_post\_success\_schema

|Name|Schema|
|---|---|
|**saas\_service**  <br>*optional*|[saas\_service](#saas\_service\_post\_success\_schema-saas\_service)|

<a name="saas\_service\_post\_success\_schema-saas\_service"></a>
**saas\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="saas\_service\_put\_success\_schema"></a>
### saas\_service\_put\_success\_schema

|Name|Schema|
|---|---|
|**saas\_service**  <br>*optional*|[saas\_service](#saas\_service\_put\_success\_schema-saas\_service)|

<a name="saas\_service\_put\_success\_schema-saas\_service"></a>
**saas\_service**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="saas\_service\_response\_schema"></a>
### saas\_service\_response\_schema
*Type* : < [saas\_service\_response\_schema](#saas\_service\_response\_schema-inline) > array

<a name="saas\_service\_response\_schema-inline"></a>
**saas\_service\_response\_schema**

|Name|Schema|
|---|---|
|**saas\_service\_state**  <br>*optional*|[saas\_service\_state](#saas\_service\_state)|


<a name="saas\_service\_state"></a>
### saas\_service\_state
SaaS service state

*Type* : enum (enabled, disabled)





