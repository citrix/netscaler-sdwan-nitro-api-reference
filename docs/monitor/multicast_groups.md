# multicast\_groups


<a name="overview"></a>
## Overview
This resource provides information about multicast groups.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* multicast\_groups : Operations related to multicast\_groups 




<a name="paths"></a>
## Paths

<a name="multicast\_groups-get"></a>
### Get operation for multicast\_groups
```
GET /multicast_groups
```


#### Description
Use this operation to get information about Multicast Groups.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[multicast\_groups\_response\_schema](#multicast\_groups\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* multicast\_groups




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="multicast\_group"></a>
### multicast\_group
Multicast groups

*Type* : < [multicast\_group](#multicast\_group-inline) > array

<a name="multicast\_group-inline"></a>
**multicast\_group**

|Name|Description|Schema|
|---|---|---|
|**kbps\_received**  <br>*optional*  <br>*read-only*|Kilobytes received per second|number|
|**kbps\_sent**  <br>*optional*  <br>*read-only*|Kilobytes sent per second|number|
|**multicast\_group**  <br>*optional*  <br>*read-only*|Name of the multicast group|string|
|**packets\_received**  <br>*optional*  <br>*read-only*|Packets received|integer|
|**packets\_sent**  <br>*optional*  <br>*read-only*|Packets sent|integer|
|**routing\_domain**  <br>*optional*  <br>*read-only*|Name of the Routing Domain.|string|


<a name="multicast\_group\_destination\_service"></a>
### multicast\_group\_destination\_service
Multicast group destination services

*Type* : < [multicast\_group\_destination\_service](#multicast\_group\_destination\_service-inline) > array

<a name="multicast\_group\_destination\_service-inline"></a>
**multicast\_group\_destination\_service**

|Name|Description|Schema|
|---|---|---|
|**kbps**  <br>*optional*  <br>*read-only*|Kilobytes per second|number|
|**multicast\_group**  <br>*optional*  <br>*read-only*|Name of the multicast group|string|
|**packets**  <br>*optional*  <br>*read-only*|Packets|integer|
|**routing\_domain**  <br>*optional*  <br>*read-only*|Name of the Routing Domain.|string|
|**service\_name**  <br>*optional*  <br>*read-only*|Service name|string|
|**service\_type**  <br>*optional*  <br>*read-only*|Service type|string|


<a name="multicast\_group\_source\_service"></a>
### multicast\_group\_source\_service
Multicast group source services

*Type* : < [multicast\_group\_source\_service](#multicast\_group\_source\_service-inline) > array

<a name="multicast\_group\_source\_service-inline"></a>
**multicast\_group\_source\_service**

|Name|Description|Schema|
|---|---|---|
|**kbps**  <br>*optional*  <br>*read-only*|Kilobytes per second|number|
|**multicast\_group**  <br>*optional*  <br>*read-only*|Name of the multicast group|string|
|**packets**  <br>*optional*  <br>*read-only*|Packets|integer|
|**routing\_domain**  <br>*optional*  <br>*read-only*|Name of the Routing Domain.|string|
|**service\_name**  <br>*optional*  <br>*read-only*|Service name|string|
|**service\_type**  <br>*optional*  <br>*read-only*|Service type|string|


<a name="multicast\_groups\_delete\_success\_schema"></a>
### multicast\_groups\_delete\_success\_schema

|Name|Schema|
|---|---|
|**multicast\_groups**  <br>*optional*|[multicast\_groups](#multicast\_groups\_delete\_success\_schema-multicast\_groups)|

<a name="multicast\_groups\_delete\_success\_schema-multicast\_groups"></a>
**multicast\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="multicast\_groups\_post\_success\_schema"></a>
### multicast\_groups\_post\_success\_schema

|Name|Schema|
|---|---|
|**multicast\_groups**  <br>*optional*|[multicast\_groups](#multicast\_groups\_post\_success\_schema-multicast\_groups)|

<a name="multicast\_groups\_post\_success\_schema-multicast\_groups"></a>
**multicast\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="multicast\_groups\_put\_success\_schema"></a>
### multicast\_groups\_put\_success\_schema

|Name|Schema|
|---|---|
|**multicast\_groups**  <br>*optional*|[multicast\_groups](#multicast\_groups\_put\_success\_schema-multicast\_groups)|

<a name="multicast\_groups\_put\_success\_schema-multicast\_groups"></a>
**multicast\_groups**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="multicast\_groups\_response\_schema"></a>
### multicast\_groups\_response\_schema
*Type* : < [multicast\_groups\_response\_schema](#multicast\_groups\_response\_schema-inline) > array

<a name="multicast\_groups\_response\_schema-inline"></a>
**multicast\_groups\_response\_schema**

|Name|Schema|
|---|---|
|**multicast\_group**  <br>*optional*|[multicast\_group](#multicast\_group)|
|**multicast\_group\_destination\_service**  <br>*optional*|[multicast\_group\_destination\_service](#multicast\_group\_destination\_service)|
|**multicast\_group\_source\_service**  <br>*optional*|[multicast\_group\_source\_service](#multicast\_group\_source\_service)|





