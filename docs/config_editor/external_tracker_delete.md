# external\_tracker\_delete


<a name="overview"></a>
## Overview
API to delete configuration for HA external tracker


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* external\_tracker\_delete : Operations related to external\_tracker\_delete 




<a name="paths"></a>
## Paths

<a name="external\_tracker\_delete-deletepathparam-delete"></a>
### DELETE operation for external\_tracker\_delete
```
DELETE /external_tracker_delete/{deletePathParam}
```


#### Description
Use this operation to delete the HA external tracker


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[external\_tracker\_delete\_delete\_success\_schema](#external\_tracker\_delete\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* external\_tracker\_delete




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="external\_tracker\_delete"></a>
### external\_tracker\_delete

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="external\_tracker\_delete\_delete\_success\_schema"></a>
### external\_tracker\_delete\_delete\_success\_schema

|Name|Schema|
|---|---|
|**external\_tracker\_delete**  <br>*optional*|[external\_tracker\_delete](#external\_tracker\_delete\_delete\_success\_schema-external\_tracker\_delete)|

<a name="external\_tracker\_delete\_delete\_success\_schema-external\_tracker\_delete"></a>
**external\_tracker\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="external\_tracker\_delete\_post\_success\_schema"></a>
### external\_tracker\_delete\_post\_success\_schema

|Name|Schema|
|---|---|
|**external\_tracker\_delete**  <br>*optional*|[external\_tracker\_delete](#external\_tracker\_delete\_post\_success\_schema-external\_tracker\_delete)|

<a name="external\_tracker\_delete\_post\_success\_schema-external\_tracker\_delete"></a>
**external\_tracker\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="external\_tracker\_delete\_put\_success\_schema"></a>
### external\_tracker\_delete\_put\_success\_schema

|Name|Schema|
|---|---|
|**external\_tracker\_delete**  <br>*optional*|[external\_tracker\_delete](#external\_tracker\_delete\_put\_success\_schema-external\_tracker\_delete)|

<a name="external\_tracker\_delete\_put\_success\_schema-external\_tracker\_delete"></a>
**external\_tracker\_delete**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="external\_tracker\_delete\_request\_schema"></a>
### external\_tracker\_delete\_request\_schema

|Name|Schema|
|---|---|
|**external\_tracker\_delete**  <br>*optional*|[external\_tracker\_delete](#external\_tracker\_delete)|


<a name="external\_tracker\_delete\_response\_schema"></a>
### external\_tracker\_delete\_response\_schema
*Type* : < [external\_tracker\_delete\_response\_schema](#external\_tracker\_delete\_response\_schema-inline) > array

<a name="external\_tracker\_delete\_response\_schema-inline"></a>
**external\_tracker\_delete\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="id"></a>
### id
HA external tracker id

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the API operation should be performed.

*Type* : string


<a name="site\_name"></a>
### site\_name
The Site Name

*Type* : string





