# local\_users


<a name="overview"></a>
## Overview
Add, Delete, Modify or List Local Users through these APIs


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* local\_users : Operations related to local\_users 




<a name="paths"></a>
## Paths

<a name="local\_users-post"></a>
### POST operation for local\_users
```
POST /local_users
```


#### Description
Use this operation to add a local user


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[local\_users\_post\_success\_schema](#local\_users\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_users


<a name="local\_users-get"></a>
### Get operation for local\_users
```
GET /local_users
```


#### Description
Use this operation to get a list of all local users


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[local\_users\_response\_schema](#local\_users\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_users


<a name="local\_users-put"></a>
### PUT operation for local\_users
```
PUT /local_users
```


#### Description
Use this operation to update a local user's password


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[local\_users\_request\_schema](#local\_users\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[local\_users\_put\_success\_schema](#local\_users\_put\_success\_schema)|
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

* local\_users


<a name="local\_users-deletepathparam-delete"></a>
### DELETE operation for local\_users
```
DELETE /local_users/{deletePathParam}
```


#### Description
Use this operation to delete a local user


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[local\_users\_delete\_success\_schema](#local\_users\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* local\_users




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="local\_users"></a>
### local\_users

|Name|Schema|
|---|---|
|**password**  <br>*optional*|[password](#password)|
|**user\_level**  <br>*optional*|[user\_level](#user\_level)|
|**username**  <br>*optional*|[username](#username)|


<a name="local\_users\_delete\_success\_schema"></a>
### local\_users\_delete\_success\_schema

|Name|Schema|
|---|---|
|**local\_users**  <br>*optional*|[local\_users](#local\_users\_delete\_success\_schema-local\_users)|

<a name="local\_users\_delete\_success\_schema-local\_users"></a>
**local\_users**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="local\_users\_post\_success\_schema"></a>
### local\_users\_post\_success\_schema

|Name|Schema|
|---|---|
|**local\_users**  <br>*optional*|[local\_users](#local\_users\_post\_success\_schema-local\_users)|

<a name="local\_users\_post\_success\_schema-local\_users"></a>
**local\_users**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="local\_users\_put\_success\_schema"></a>
### local\_users\_put\_success\_schema

|Name|Schema|
|---|---|
|**local\_users**  <br>*optional*|[local\_users](#local\_users\_put\_success\_schema-local\_users)|

<a name="local\_users\_put\_success\_schema-local\_users"></a>
**local\_users**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="local\_users\_request\_schema"></a>
### local\_users\_request\_schema

|Name|Schema|
|---|---|
|**local\_users**  <br>*optional*|[local\_users](#local\_users)|


<a name="local\_users\_response\_schema"></a>
### local\_users\_response\_schema
*Type* : < [local\_users\_response\_schema](#local\_users\_response\_schema-inline) > array

<a name="local\_users\_response\_schema-inline"></a>
**local\_users\_response\_schema**

|Name|Schema|
|---|---|
|**password**  <br>*optional*|[password](#password)|
|**user\_level**  <br>*optional*|[user\_level](#user\_level)|
|**username**  <br>*optional*|[username](#username)|


<a name="password"></a>
### password
Password of the target user

*Type* : string


<a name="user\_level"></a>
### user\_level
User level of the target user

*Type* : enum (admin, guest)


<a name="username"></a>
### username
Username of the target user

*Type* : string





