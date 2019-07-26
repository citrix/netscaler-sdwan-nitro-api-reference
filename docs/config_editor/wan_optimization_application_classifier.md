# wan\_optimization\_application\_classifier


<a name="overview"></a>
## Overview
API to add, delete, get, modify WAN optimization application classifier.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_optimization\_application\_classifier : Operations related to wan\_optimization\_application\_classifier 




<a name="paths"></a>
## Paths

<a name="wan\_optimization\_application\_classifier-post"></a>
### POST operation for wan\_optimization\_application\_classifier
```
POST /wan_optimization_application_classifier
```


#### Description
Use this operation to add WAN Optimization Application Classifiers


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_optimization\_application\_classifier\_request\_schema](#wan\_optimization\_application\_classifier\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[wan\_optimization\_application\_classifier\_post\_success\_schema](#wan\_optimization\_application\_classifier\_post\_success\_schema)|
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

* wan\_optimization\_application\_classifier


<a name="wan\_optimization\_application\_classifier-get"></a>
### Get operation for wan\_optimization\_application\_classifier
```
GET /wan_optimization_application_classifier
```


#### Description
Use this operation to get WAN Optimization Application Classifiers


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_optimization\_application\_classifier\_response\_schema](#wan\_optimization\_application\_classifier\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_application\_classifier


<a name="wan\_optimization\_application\_classifier-put"></a>
### PUT operation for wan\_optimization\_application\_classifier
```
PUT /wan_optimization_application_classifier
```


#### Description
Use this operation to modify WAN Optimization Application Classifiers


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_optimization\_application\_classifier\_put\_success\_schema](#wan\_optimization\_application\_classifier\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_application\_classifier


<a name="wan\_optimization\_application\_classifier-deletepathparam-delete"></a>
### DELETE operation for wan\_optimization\_application\_classifier
```
DELETE /wan_optimization_application_classifier/{deletePathParam}
```


#### Description
Use this operation to delete WAN Optimization Application Classifiers


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[wan\_optimization\_application\_classifier\_delete\_success\_schema](#wan\_optimization\_application\_classifier\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_application\_classifier




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="id"></a>
### id
Auto-generated ID to uniquely identify WAN Optimzation Application Classifiers

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="properties"></a>
### properties
WAN Optimization Application Classifier Properties


|Name|Description|Schema|
|---|---|---|
|**application\_group**  <br>*optional*  <br>*read-only*|WAN Optimization Application Classifier Associated application groups. This list can be added or modified through the wan\_optimization\_application\_classifier\_application\_group APIs|string|
|**wan\_optimization\_application\_classification\_port**  <br>*optional*|Input can be multiple ports or port ranges separated by commas.|string|
|**wan\_optimization\_application\_classification\_type**  <br>*optional*  <br>*read-only*|WAN Optimization Application Classifier Type|string|


<a name="wan\_optimization\_application\_classifier"></a>
### wan\_optimization\_application\_classifier

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**wan\_optimization\_application\_classifier\_name**  <br>*optional*|[wan\_optimization\_application\_classifier\_name](#wan\_optimization\_application\_classifier\_name)|


<a name="wan\_optimization\_application\_classifier\_delete\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier**  <br>*optional*|[wan\_optimization\_application\_classifier](#wan\_optimization\_application\_classifier\_delete\_success\_schema-wan\_optimization\_application\_classifier)|

<a name="wan\_optimization\_application\_classifier\_delete\_success\_schema-wan\_optimization\_application\_classifier"></a>
**wan\_optimization\_application\_classifier**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_name"></a>
### wan\_optimization\_application\_classifier\_name
WAN Optimization Application Classifier name

*Type* : string


<a name="wan\_optimization\_application\_classifier\_post\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier**  <br>*optional*|[wan\_optimization\_application\_classifier](#wan\_optimization\_application\_classifier\_post\_success\_schema-wan\_optimization\_application\_classifier)|

<a name="wan\_optimization\_application\_classifier\_post\_success\_schema-wan\_optimization\_application\_classifier"></a>
**wan\_optimization\_application\_classifier**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_put\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier**  <br>*optional*|[wan\_optimization\_application\_classifier](#wan\_optimization\_application\_classifier\_put\_success\_schema-wan\_optimization\_application\_classifier)|

<a name="wan\_optimization\_application\_classifier\_put\_success\_schema-wan\_optimization\_application\_classifier"></a>
**wan\_optimization\_application\_classifier**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_request\_schema"></a>
### wan\_optimization\_application\_classifier\_request\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier**  <br>*optional*|[wan\_optimization\_application\_classifier](#wan\_optimization\_application\_classifier)|


<a name="wan\_optimization\_application\_classifier\_response\_schema"></a>
### wan\_optimization\_application\_classifier\_response\_schema
*Type* : < [wan\_optimization\_application\_classifier\_response\_schema](#wan\_optimization\_application\_classifier\_response\_schema-inline) > array

<a name="wan\_optimization\_application\_classifier\_response\_schema-inline"></a>
**wan\_optimization\_application\_classifier\_response\_schema**

|Name|Schema|
|---|---|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**properties**  <br>*optional*|[properties](#properties)|
|**wan\_optimization\_application\_classifier\_name**  <br>*optional*|[wan\_optimization\_application\_classifier\_name](#wan\_optimization\_application\_classifier\_name)|





