# application\_routes


<a name="overview"></a>
## Overview
API to get application routes information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* application\_routes : Operations related to application\_routes 




<a name="paths"></a>
## Paths

<a name="application\_routes-get"></a>
### Get operation for application\_routes
```
GET /application_routes
```


#### Description
Use this operation to get application routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[application\_routes\_response\_schema](#application\_routes\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* application\_routes




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="app\_obj\_name"></a>
### app\_obj\_name
Application Object Name

*Type* : string


<a name="app\_route\_type"></a>
### app\_route\_type
The Application Route type. It can be either static or dynamic

*Type* : string


<a name="application\_routes\_delete\_success\_schema"></a>
### application\_routes\_delete\_success\_schema

|Name|Schema|
|---|---|
|**application\_routes**  <br>*optional*|[application\_routes](#application\_routes\_delete\_success\_schema-application\_routes)|

<a name="application\_routes\_delete\_success\_schema-application\_routes"></a>
**application\_routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="application\_routes\_post\_success\_schema"></a>
### application\_routes\_post\_success\_schema

|Name|Schema|
|---|---|
|**application\_routes**  <br>*optional*|[application\_routes](#application\_routes\_post\_success\_schema-application\_routes)|

<a name="application\_routes\_post\_success\_schema-application\_routes"></a>
**application\_routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="application\_routes\_put\_success\_schema"></a>
### application\_routes\_put\_success\_schema

|Name|Schema|
|---|---|
|**application\_routes**  <br>*optional*|[application\_routes](#application\_routes\_put\_success\_schema-application\_routes)|

<a name="application\_routes\_put\_success\_schema-application\_routes"></a>
**application\_routes**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="application\_routes\_response\_schema"></a>
### application\_routes\_response\_schema
*Type* : < [application\_routes\_response\_schema](#application\_routes\_response\_schema-inline) > array

<a name="application\_routes\_response\_schema-inline"></a>
**application\_routes\_response\_schema**

|Name|Schema|
|---|---|
|**app\_obj\_name**  <br>*optional*|[app\_obj\_name](#app\_obj\_name)|
|**app\_route\_type**  <br>*optional*|[app\_route\_type](#app\_route\_type)|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_type**  <br>*optional*|[eligibility\_type](#eligibility\_type)|
|**eligibility\_value**  <br>*optional*|[eligibility\_value](#eligibility\_value)|
|**eligible**  <br>*optional*|[eligible](#eligible)|
|**firewall\_zone**  <br>*optional*|[firewall\_zone](#firewall\_zone)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**hit\_count**  <br>*optional*|[hit\_count](#hit\_count)|
|**reachable**  <br>*optional*|[reachable](#reachable)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service**  <br>*optional*|[service](#service)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="cost"></a>
### cost
A weight to determine Route priority. Lower-cost Routes will be preferred over higher-cost Routes.

*Type* : integer


<a name="eligibility\_type"></a>
### eligibility\_type
The Application Route eligibility type

*Type* : string


<a name="eligibility\_value"></a>
### eligibility\_value
The Application Route eligibility value

*Type* : string


<a name="eligible"></a>
### eligible
The Application Route eligibility

*Type* : string


<a name="firewall\_zone"></a>
### firewall\_zone
The Application Route firewall zone

*Type* : string


<a name="gateway\_ip\_addr"></a>
### gateway\_ip\_addr
The Application Route Gateway IP Address

*Type* : string


<a name="hit\_count"></a>
### hit\_count
The Application Route Hit count

*Type* : integer


<a name="reachable"></a>
### reachable
The Application Route reachablity

*Type* : string


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
The Routing Domain Name

*Type* : string


<a name="service"></a>
### service
The Application Route Service name

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string





