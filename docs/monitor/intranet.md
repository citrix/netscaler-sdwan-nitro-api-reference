# intranet


<a name="overview"></a>
## Overview
This resource provides details of all intranet


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* intranet : Operations related to intranet 




<a name="paths"></a>
## Paths

<a name="intranet-get"></a>
### Get operation for intranet
```
GET /intranet
```


#### Description
Use this operation to get intranet statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[intranet\_response\_schema](#intranet\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* intranet




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bytes\_recv"></a>
### bytes\_recv
Number of bytes received

*Type* : integer


<a name="bytes\_sent"></a>
### bytes\_sent
Number of bytes sent

*Type* : integer


<a name="intranet\_delete\_success\_schema"></a>
### intranet\_delete\_success\_schema

|Name|Schema|
|---|---|
|**intranet**  <br>*optional*|[intranet](#intranet\_delete\_success\_schema-intranet)|

<a name="intranet\_delete\_success\_schema-intranet"></a>
**intranet**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="intranet\_name"></a>
### intranet\_name
Name of the Intranet

*Type* : string


<a name="intranet\_post\_success\_schema"></a>
### intranet\_post\_success\_schema

|Name|Schema|
|---|---|
|**intranet**  <br>*optional*|[intranet](#intranet\_post\_success\_schema-intranet)|

<a name="intranet\_post\_success\_schema-intranet"></a>
**intranet**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="intranet\_put\_success\_schema"></a>
### intranet\_put\_success\_schema

|Name|Schema|
|---|---|
|**intranet**  <br>*optional*|[intranet](#intranet\_put\_success\_schema-intranet)|

<a name="intranet\_put\_success\_schema-intranet"></a>
**intranet**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="intranet\_response\_schema"></a>
### intranet\_response\_schema
*Type* : < [intranet\_response\_schema](#intranet\_response\_schema-inline) > array

<a name="intranet\_response\_schema-inline"></a>
**intranet\_response\_schema**

|Name|Schema|
|---|---|
|**bytes\_recv**  <br>*optional*|[bytes\_recv](#bytes\_recv)|
|**bytes\_sent**  <br>*optional*|[bytes\_sent](#bytes\_sent)|
|**intranet\_name**  <br>*optional*|[intranet\_name](#intranet\_name)|
|**recv\_packets**  <br>*optional*|[recv\_packets](#recv\_packets)|
|**recv\_rate**  <br>*optional*|[recv\_rate](#recv\_rate)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**sent\_packets**  <br>*optional*|[sent\_packets](#sent\_packets)|
|**sent\_rate**  <br>*optional*|[sent\_rate](#sent\_rate)|


<a name="recv\_packets"></a>
### recv\_packets
Number of packets received

*Type* : integer


<a name="recv\_rate"></a>
### recv\_rate
Receive rate in kbps

*Type* : number


<a name="routing\_domain"></a>
### routing\_domain
Name of the Routing Domain.

*Type* : string


<a name="sent\_packets"></a>
### sent\_packets
Number of packets sent

*Type* : integer


<a name="sent\_rate"></a>
### sent\_rate
Sent rate in kbps

*Type* : number





