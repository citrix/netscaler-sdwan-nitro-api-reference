# wan\_optimization\_service\_classes


<a name="overview"></a>
## Overview
API to add, delete, get, modify WAN optimization service classes.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_optimization\_service\_classes : Operations related to wan\_optimization\_service\_classes 




<a name="paths"></a>
## Paths

<a name="wan\_optimization\_service\_classes-post"></a>
### POST operation for wan\_optimization\_service\_classes
```
POST /wan_optimization_service_classes
```


#### Description
Use this operation to add WAN Optimization Service Classes


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_optimization\_service\_classes\_request\_schema](#wan\_optimization\_service\_classes\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[wan\_optimization\_service\_classes\_post\_success\_schema](#wan\_optimization\_service\_classes\_post\_success\_schema)|
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

* wan\_optimization\_service\_classes


<a name="wan\_optimization\_service\_classes-get"></a>
### Get operation for wan\_optimization\_service\_classes
```
GET /wan_optimization_service_classes
```


#### Description
Use this operation to get WAN Optimization Service Classes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_optimization\_service\_classes\_response\_schema](#wan\_optimization\_service\_classes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_service\_classes


<a name="wan\_optimization\_service\_classes-put"></a>
### PUT operation for wan\_optimization\_service\_classes
```
PUT /wan_optimization_service_classes
```


#### Description
Use this operation to modify WAN Optimization Service Classes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_optimization\_service\_classes\_put\_success\_schema](#wan\_optimization\_service\_classes\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_service\_classes


<a name="wan\_optimization\_service\_classes-deletepathparam-delete"></a>
### DELETE operation for wan\_optimization\_service\_classes
```
DELETE /wan_optimization_service_classes/{deletePathParam}
```


#### Description
Use this operation to delete WAN Optimization Service Classes


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[wan\_optimization\_service\_classes\_delete\_success\_schema](#wan\_optimization\_service\_classes\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_optimization\_service\_classes



