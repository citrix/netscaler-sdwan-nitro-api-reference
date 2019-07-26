# ilbflows


<a name="overview"></a>
## Overview
This resource provides details about internet load balancing flows


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* ilbflows : Operations related to ilbflows 




<a name="paths"></a>
## Paths

<a name="ilbflows-get"></a>
### Get operation for ilbflows
```
GET /ilbflows
```


#### Description
Use this operation to get internet load balancing flows. Filters are supported for this API. max\_stats filter is available as an additional option to filter the flow count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ilbflows\_response\_schema](#ilbflows\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ilbflows




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="age"></a>
### age
How long ago this flow was created in milliseconds

*Type* : string


<a name="flowcount"></a>
### flowcount
Number of individual flows between source and destination IP

*Type* : string


<a name="ilbflows\_delete\_success\_schema"></a>
### ilbflows\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ilbflows**  <br>*optional*|[ilbflows](#ilbflows\_delete\_success\_schema-ilbflows)|

<a name="ilbflows\_delete\_success\_schema-ilbflows"></a>
**ilbflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ilbflows\_post\_success\_schema"></a>
### ilbflows\_post\_success\_schema

|Name|Schema|
|---|---|
|**ilbflows**  <br>*optional*|[ilbflows](#ilbflows\_post\_success\_schema-ilbflows)|

<a name="ilbflows\_post\_success\_schema-ilbflows"></a>
**ilbflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ilbflows\_put\_success\_schema"></a>
### ilbflows\_put\_success\_schema

|Name|Schema|
|---|---|
|**ilbflows**  <br>*optional*|[ilbflows](#ilbflows\_put\_success\_schema-ilbflows)|

<a name="ilbflows\_put\_success\_schema-ilbflows"></a>
**ilbflows**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ilbflows\_response\_schema"></a>
### ilbflows\_response\_schema
*Type* : < [ilbflows\_response\_schema](#ilbflows\_response\_schema-inline) > array

<a name="ilbflows\_response\_schema-inline"></a>
**ilbflows\_response\_schema**

|Name|Schema|
|---|---|
|**age**  <br>*optional*|[age](#age)|
|**flowcount**  <br>*optional*|[flowcount](#flowcount)|
|**lanip**  <br>*optional*|[lanip](#lanip)|
|**wanip**  <br>*optional*|[wanip](#wanip)|
|**wanlink**  <br>*optional*|[wanlink](#wanlink)|


<a name="lanip"></a>
### lanip
LAN IP Address for packets on this flow

*Type* : string


<a name="wanip"></a>
### wanip
WAN IP Address for packets on this flow

*Type* : string


<a name="wanlink"></a>
### wanlink
Name of the WAN Link these flows travel through

*Type* : string





