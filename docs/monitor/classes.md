# classes


<a name="overview"></a>
## Overview
This resource provides QoS Classes statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* classes : Operations related to classes 




<a name="paths"></a>
## Paths

<a name="classes-get"></a>
### Get operation for classes
```
GET /classes
```


#### Description
This resource provides QoS Classes statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[classes\_response\_schema](#classes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* classes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="class\_object"></a>
### class\_object
Class Stats for each virtual Path Service

*Type* : < [class\_object](#class\_object-inline) > array

<a name="class\_object-inline"></a>
**class\_object**

|Name|Description|Schema|
|---|---|---|
|**bandwidth**  <br>*optional*  <br>*read-only*|Bandwidth in kbps|string|
|**class\_number**  <br>*optional*  <br>*read-only*|Class Number|string|
|**dropped\_bytes**  <br>*optional*  <br>*read-only*|Dropped Bytes|string|
|**dropped\_packets**  <br>*optional*  <br>*read-only*|Dropped Packets|string|
|**name**  <br>*optional*  <br>*read-only*|Class Name|string|
|**pending\_bytes**  <br>*optional*  <br>*read-only*|Pending Bytes|string|
|**pending\_packets**  <br>*optional*  <br>*read-only*|Pending Packets|string|
|**sent\_bytes**  <br>*optional*  <br>*read-only*|Sent Bytes|string|
|**sent\_packets**  <br>*optional*  <br>*read-only*|Sent Packets|string|
|**type**  <br>*optional*  <br>*read-only*|Class Type|string|
|**wait\_ms**  <br>*optional*  <br>*read-only*|Wait time in Milliseconds|string|


<a name="classes\_delete\_success\_schema"></a>
### classes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_delete\_success\_schema-classes)|

<a name="classes\_delete\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="classes\_post\_success\_schema"></a>
### classes\_post\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_post\_success\_schema-classes)|

<a name="classes\_post\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="classes\_put\_success\_schema"></a>
### classes\_put\_success\_schema

|Name|Schema|
|---|---|
|**classes**  <br>*optional*|[classes](#classes\_put\_success\_schema-classes)|

<a name="classes\_put\_success\_schema-classes"></a>
**classes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="classes\_response\_schema"></a>
### classes\_response\_schema
*Type* : < [classes\_response\_schema](#classes\_response\_schema-inline) > array

<a name="classes\_response\_schema-inline"></a>
**classes\_response\_schema**

|Name|Schema|
|---|---|
|**class\_object**  <br>*optional*|[class\_object](#class\_object)|
|**virtual\_path\_service\_name**  <br>*optional*|[virtual\_path\_service\_name](#virtual\_path\_service\_name)|


<a name="virtual\_path\_service\_name"></a>
### virtual\_path\_service\_name
Name of Virtual path Service

*Type* : string





