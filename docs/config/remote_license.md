# remote\_license


<a name="overview"></a>
## Overview
Remote license configuration


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* remote\_license : Operations related to remote\_license 




<a name="paths"></a>
## Paths

<a name="remote\_license-post"></a>
### POST operation for remote\_license
```
POST /remote_license
```


#### Description
Activate the remote license configuration


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (enable\_remote\_server)|
|**Body**|**body**  <br>*optional*||[remote\_license\_request\_schema](#remote\_license\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[remote\_license\_post\_success\_schema](#remote\_license\_post\_success\_schema)|
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

* remote\_license


<a name="remote\_license-get"></a>
### Get operation for remote\_license
```
GET /remote_license
```


#### Description
Use this operation to get the remote license configuration


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[remote\_license\_response\_schema](#remote\_license\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* remote\_license


<a name="remote\_license-put"></a>
### PUT operation for remote\_license
```
PUT /remote_license
```


#### Description
Update the remote license configuration


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[remote\_license\_put\_success\_schema](#remote\_license\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* remote\_license




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="model"></a>
### model
Model installed from license

*Type* : string


<a name="model\_choices"></a>
### model\_choices
Model choices available on this device

*Type* : string


<a name="remote\_license"></a>
### remote\_license

|Name|Schema|
|---|---|
|**model**  <br>*optional*|[model](#model)|
|**model\_choices**  <br>*optional*|[model\_choices](#model\_choices)|
|**remote\_license\_ip**  <br>*optional*|[remote\_license\_ip](#remote\_license\_ip)|
|**remote\_license\_port**  <br>*optional*|[remote\_license\_port](#remote\_license\_port)|


<a name="remote\_license\_delete\_success\_schema"></a>
### remote\_license\_delete\_success\_schema

|Name|Schema|
|---|---|
|**remote\_license**  <br>*optional*|[remote\_license](#remote\_license\_delete\_success\_schema-remote\_license)|

<a name="remote\_license\_delete\_success\_schema-remote\_license"></a>
**remote\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="remote\_license\_ip"></a>
### remote\_license\_ip
Remote license server IP

*Type* : string


<a name="remote\_license\_port"></a>
### remote\_license\_port
Remote license server port

*Type* : integer


<a name="remote\_license\_post\_success\_schema"></a>
### remote\_license\_post\_success\_schema

|Name|Schema|
|---|---|
|**remote\_license**  <br>*optional*|[remote\_license](#remote\_license\_post\_success\_schema-remote\_license)|

<a name="remote\_license\_post\_success\_schema-remote\_license"></a>
**remote\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="remote\_license\_put\_success\_schema"></a>
### remote\_license\_put\_success\_schema

|Name|Schema|
|---|---|
|**remote\_license**  <br>*optional*|[remote\_license](#remote\_license\_put\_success\_schema-remote\_license)|

<a name="remote\_license\_put\_success\_schema-remote\_license"></a>
**remote\_license**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="remote\_license\_request\_schema"></a>
### remote\_license\_request\_schema

|Name|Schema|
|---|---|
|**remote\_license**  <br>*optional*|[remote\_license](#remote\_license)|


<a name="remote\_license\_response\_schema"></a>
### remote\_license\_response\_schema
*Type* : < [remote\_license\_response\_schema](#remote\_license\_response\_schema-inline) > array

<a name="remote\_license\_response\_schema-inline"></a>
**remote\_license\_response\_schema**

|Name|Schema|
|---|---|
|**model**  <br>*optional*|[model](#model)|
|**model\_choices**  <br>*optional*|[model\_choices](#model\_choices)|
|**remote\_license\_ip**  <br>*optional*|[remote\_license\_ip](#remote\_license\_ip)|
|**remote\_license\_port**  <br>*optional*|[remote\_license\_port](#remote\_license\_port)|





