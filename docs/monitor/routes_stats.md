# routes\_stats


<a name="overview"></a>
## Overview
API to get routes information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* routes\_stats : Operations related to routes\_stats 




<a name="paths"></a>
## Paths

<a name="routes\_stats-get"></a>
### Get operation for routes\_stats
```
GET /routes_stats
```


#### Description
Use this operation to get routes


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[routes\_stats\_response\_schema](#routes\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* routes\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="cost"></a>
### cost
A weight to determine Route priority. Lower-cost Routes will be preferred over higher-cost Routes.

*Type* : integer


<a name="eligibility\_type"></a>
### eligibility\_type
The Route eligibility type

*Type* : string


<a name="eligibility\_value"></a>
### eligibility\_value
The Route eligibility value

*Type* : string


<a name="eligible"></a>
### eligible
The Route eligibility

*Type* : string


<a name="firewall\_zone"></a>
### firewall\_zone
The Route firewall zone

*Type* : string


<a name="gateway\_ip\_addr"></a>
### gateway\_ip\_addr
The Route Gateway IP Address

*Type* : string


<a name="hit\_count"></a>
### hit\_count
The Route Hit count

*Type* : integer


<a name="neighbour\_direct"></a>
### neighbour\_direct
The Route neighbour direct

*Type* : string


<a name="network\_ip\_address"></a>
### network\_ip\_address
Network IP Address

*Type* : string


<a name="protocol"></a>
### protocol
The Routes protocol

*Type* : string


<a name="reachable"></a>
### reachable
The Route reachablity

*Type* : string


<a name="route\_type"></a>
### route\_type
The Route type. It can be either static or dynamic

*Type* : string


<a name="routes\_stats\_delete\_success\_schema"></a>
### routes\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**routes\_stats**  <br>*optional*|[routes\_stats](#routes\_stats\_delete\_success\_schema-routes\_stats)|

<a name="routes\_stats\_delete\_success\_schema-routes\_stats"></a>
**routes\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="routes\_stats\_post\_success\_schema"></a>
### routes\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**routes\_stats**  <br>*optional*|[routes\_stats](#routes\_stats\_post\_success\_schema-routes\_stats)|

<a name="routes\_stats\_post\_success\_schema-routes\_stats"></a>
**routes\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="routes\_stats\_put\_success\_schema"></a>
### routes\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**routes\_stats**  <br>*optional*|[routes\_stats](#routes\_stats\_put\_success\_schema-routes\_stats)|

<a name="routes\_stats\_put\_success\_schema-routes\_stats"></a>
**routes\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="routes\_stats\_response\_schema"></a>
### routes\_stats\_response\_schema
*Type* : < [routes\_stats\_response\_schema](#routes\_stats\_response\_schema-inline) > array

<a name="routes\_stats\_response\_schema-inline"></a>
**routes\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**cost**  <br>*optional*|[cost](#cost)|
|**eligibility\_type**  <br>*optional*|[eligibility\_type](#eligibility\_type)|
|**eligibility\_value**  <br>*optional*|[eligibility\_value](#eligibility\_value)|
|**eligible**  <br>*optional*|[eligible](#eligible)|
|**firewall\_zone**  <br>*optional*|[firewall\_zone](#firewall\_zone)|
|**gateway\_ip\_addr**  <br>*optional*|[gateway\_ip\_addr](#gateway\_ip\_addr)|
|**hit\_count**  <br>*optional*|[hit\_count](#hit\_count)|
|**neighbour\_direct**  <br>*optional*|[neighbour\_direct](#neighbour\_direct)|
|**network\_ip\_address**  <br>*optional*|[network\_ip\_address](#network\_ip\_address)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**reachable**  <br>*optional*|[reachable](#reachable)|
|**route\_type**  <br>*optional*|[route\_type](#route\_type)|
|**routing\_domain\_name**  <br>*optional*|[routing\_domain\_name](#routing\_domain\_name)|
|**service**  <br>*optional*|[service](#service)|
|**site\_ip\_address**  <br>*optional*|[site\_ip\_address](#site\_ip\_address)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|


<a name="routing\_domain\_name"></a>
### routing\_domain\_name
The Routing Domain Name

*Type* : string


<a name="service"></a>
### service
The Route Service name

*Type* : string


<a name="site\_ip\_address"></a>
### site\_ip\_address
The Route Site IP Address

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string





