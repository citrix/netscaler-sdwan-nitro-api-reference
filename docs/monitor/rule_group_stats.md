# rule\_group\_stats


<a name="overview"></a>
## Overview
This resource provides Rule Groups Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* rule\_group\_stats : Operations related to rule\_group\_stats 




<a name="paths"></a>
## Paths

<a name="rule\_group\_stats-get"></a>
### Get operation for rule\_group\_stats
```
GET /rule_group_stats
```


#### Description
Use this operation to get Rule Group statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[rule\_group\_stats\_response\_schema](#rule\_group\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* rule\_group\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="flows"></a>
### flows
total flows value stat for the rule group

*Type* : integer


<a name="kbps"></a>
### kbps
total kbps value stat for the rule group

*Type* : number


<a name="pps"></a>
### pps
total PPS value for that rule group

*Type* : number


<a name="rule\_group"></a>
### rule\_group
Rule Group Name

*Type* : string


<a name="rule\_group\_stats\_delete\_success\_schema"></a>
### rule\_group\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**rule\_group\_stats**  <br>*optional*|[rule\_group\_stats](#rule\_group\_stats\_delete\_success\_schema-rule\_group\_stats)|

<a name="rule\_group\_stats\_delete\_success\_schema-rule\_group\_stats"></a>
**rule\_group\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="rule\_group\_stats\_post\_success\_schema"></a>
### rule\_group\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**rule\_group\_stats**  <br>*optional*|[rule\_group\_stats](#rule\_group\_stats\_post\_success\_schema-rule\_group\_stats)|

<a name="rule\_group\_stats\_post\_success\_schema-rule\_group\_stats"></a>
**rule\_group\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="rule\_group\_stats\_put\_success\_schema"></a>
### rule\_group\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**rule\_group\_stats**  <br>*optional*|[rule\_group\_stats](#rule\_group\_stats\_put\_success\_schema-rule\_group\_stats)|

<a name="rule\_group\_stats\_put\_success\_schema-rule\_group\_stats"></a>
**rule\_group\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="rule\_group\_stats\_response\_schema"></a>
### rule\_group\_stats\_response\_schema
*Type* : < [rule\_group\_stats\_response\_schema](#rule\_group\_stats\_response\_schema-inline) > array

<a name="rule\_group\_stats\_response\_schema-inline"></a>
**rule\_group\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**flows**  <br>*optional*|[flows](#flows)|
|**kbps**  <br>*optional*|[kbps](#kbps)|
|**pps**  <br>*optional*|[pps](#pps)|
|**rule\_group**  <br>*optional*|[rule\_group](#rule\_group)|





