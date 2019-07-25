# wan\_optimization\_application\_classifier\_application\_group


<a name="overview"></a>
## Overview
API to add, delete, get WAN optimization application classifier Groups.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_optimization\_application\_classifier\_application\_group : Operations related to wan\_optimization\_application\_classifier\_application\_group 




<a name="paths"></a>
## Paths

<a name="wan\_optimization\_application\_classifier\_application\_group-post"></a>
### POST operation for wan\_optimization\_application\_classifier\_application\_group
```
POST /wan_optimization_application_classifier_application_group
```


#### Description
Use this operation to add WAN Optimization Application Classifiers associated Application groups


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_optimization\_application\_classifier\_application\_group\_request\_schema](#wan\_optimization\_application\_classifier\_application\_group\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema](#wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema)|
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

* wan\_optimization\_application\_classifier\_application\_group


<a name="wan\_optimization\_application\_classifier\_application\_group-get"></a>
### Get operation for wan\_optimization\_application\_classifier\_application\_group
```
GET /wan_optimization_application_classifier_application_group
```


#### Description
Use this operation to get WAN Optimization Application Classifiers associated Application groups


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_optimization\_application\_classifier\_application\_group\_response\_schema](#wan\_optimization\_application\_classifier\_application\_group\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_application\_classifier\_application\_group


<a name="wan\_optimization\_application\_classifier\_application\_group-deletepathparam-delete"></a>
### DELETE operation for wan\_optimization\_application\_classifier\_application\_group
```
DELETE /wan_optimization_application_classifier_application_group/{deletePathParam}
```


#### Description
Use this operation to delete WAN Optimization Application Classifiers associated Application groups


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema](#wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_application\_classifier\_application\_group




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_group\_name"></a>
### application\_group\_name
WAN Optimization Application Classifier associated Application Group name

*Type* : enum (backup and replication, citrix protocols, content delivery, database and enterprise resource planning (erp) software, custom, directory services, email and collaboration, file server, games, client-server, general classifiers, ip protocols, legacy or non-ip, messaging, host access, infrastructure, middleware, multimedia, network management, peer-to-peer (p2p) applications, routing protocols, security protocols, servers, session, video websites, voice over ip (voip), web)


<a name="id"></a>
### id
Auto-generated ID to uniquely identify WAN Optimization Application Classifier Groups

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="wan\_optimization\_application\_classifier\_application\_group"></a>
### wan\_optimization\_application\_classifier\_application\_group

|Name|Schema|
|---|---|
|**application\_group\_name**  <br>*optional*|[application\_group\_name](#application\_group\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**wan\_optimization\_application\_classifier\_name**  <br>*optional*|[wan\_optimization\_application\_classifier\_name](#wan\_optimization\_application\_classifier\_name)|


<a name="wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier\_application\_group**  <br>*optional*|[wan\_optimization\_application\_classifier\_application\_group](#wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema-wan\_optimization\_application\_classifier\_application\_group)|

<a name="wan\_optimization\_application\_classifier\_application\_group\_delete\_success\_schema-wan\_optimization\_application\_classifier\_application\_group"></a>
**wan\_optimization\_application\_classifier\_application\_group**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier\_application\_group**  <br>*optional*|[wan\_optimization\_application\_classifier\_application\_group](#wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema-wan\_optimization\_application\_classifier\_application\_group)|

<a name="wan\_optimization\_application\_classifier\_application\_group\_post\_success\_schema-wan\_optimization\_application\_classifier\_application\_group"></a>
**wan\_optimization\_application\_classifier\_application\_group**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_application\_group\_put\_success\_schema"></a>
### wan\_optimization\_application\_classifier\_application\_group\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier\_application\_group**  <br>*optional*|[wan\_optimization\_application\_classifier\_application\_group](#wan\_optimization\_application\_classifier\_application\_group\_put\_success\_schema-wan\_optimization\_application\_classifier\_application\_group)|

<a name="wan\_optimization\_application\_classifier\_application\_group\_put\_success\_schema-wan\_optimization\_application\_classifier\_application\_group"></a>
**wan\_optimization\_application\_classifier\_application\_group**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_optimization\_application\_classifier\_application\_group\_request\_schema"></a>
### wan\_optimization\_application\_classifier\_application\_group\_request\_schema

|Name|Schema|
|---|---|
|**wan\_optimization\_application\_classifier\_application\_group**  <br>*optional*|[wan\_optimization\_application\_classifier\_application\_group](#wan\_optimization\_application\_classifier\_application\_group)|


<a name="wan\_optimization\_application\_classifier\_application\_group\_response\_schema"></a>
### wan\_optimization\_application\_classifier\_application\_group\_response\_schema
*Type* : < [wan\_optimization\_application\_classifier\_application\_group\_response\_schema](#wan\_optimization\_application\_classifier\_application\_group\_response\_schema-inline) > array

<a name="wan\_optimization\_application\_classifier\_application\_group\_response\_schema-inline"></a>
**wan\_optimization\_application\_classifier\_application\_group\_response\_schema**

|Name|Schema|
|---|---|
|**application\_group\_name**  <br>*optional*|[application\_group\_name](#application\_group\_name)|
|**id**  <br>*optional*|[id](#id)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**wan\_optimization\_application\_classifier\_name**  <br>*optional*|[wan\_optimization\_application\_classifier\_name](#wan\_optimization\_application\_classifier\_name)|


<a name="wan\_optimization\_application\_classifier\_name"></a>
### wan\_optimization\_application\_classifier\_name
WAN Optimization Application Classifier name

*Type* : string





