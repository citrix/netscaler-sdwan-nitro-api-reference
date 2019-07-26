# applications


<a name="overview"></a>
## Overview
This resource provides details about Applications Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* applications : Operations related to applications 




<a name="paths"></a>
## Paths

<a name="applications-get"></a>
### Get operation for applications
```
GET /applications
```


#### Description
Use this operation to get application details. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[applications\_response\_schema](#applications\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* applications




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application"></a>
### application
Name of the Application

*Type* : string


<a name="applications\_delete\_success\_schema"></a>
### applications\_delete\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_delete\_success\_schema-applications)|

<a name="applications\_delete\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="applications\_post\_success\_schema"></a>
### applications\_post\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_post\_success\_schema-applications)|

<a name="applications\_post\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="applications\_put\_success\_schema"></a>
### applications\_put\_success\_schema

|Name|Schema|
|---|---|
|**applications**  <br>*optional*|[applications](#applications\_put\_success\_schema-applications)|

<a name="applications\_put\_success\_schema-applications"></a>
**applications**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="applications\_response\_schema"></a>
### applications\_response\_schema
*Type* : < [applications\_response\_schema](#applications\_response\_schema-inline) > array

<a name="applications\_response\_schema-inline"></a>
**applications\_response\_schema**

|Name|Schema|
|---|---|
|**application**  <br>*optional*|[application](#application)|
|**bytes\_received**  <br>*optional*|[bytes\_received](#bytes\_received)|
|**bytes\_sent**  <br>*optional*|[bytes\_sent](#bytes\_sent)|
|**family**  <br>*optional*|[family](#family)|
|**total\_bytes**  <br>*optional*|[total\_bytes](#total\_bytes)|


<a name="bytes\_received"></a>
### bytes\_received
Bytes Received for a Application

*Type* : string


<a name="bytes\_sent"></a>
### bytes\_sent
Bytes Sent for a  Application

*Type* : string


<a name="family"></a>
### family
Name of the Application Family

*Type* : string


<a name="total\_bytes"></a>
### total\_bytes
Total bytes(Bytes Sent + Bytes Received) for a Application

*Type* : string





