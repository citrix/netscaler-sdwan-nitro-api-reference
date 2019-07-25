# dns\_proxy\_stats


<a name="overview"></a>
## Overview
API to get dns proxy statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* dns\_proxy\_stats : Operations related to dns\_proxy\_stats 




<a name="paths"></a>
## Paths

<a name="dns\_proxy\_stats-get"></a>
### Get operation for dns\_proxy\_stats
```
GET /dns_proxy_stats
```


#### Description
Use this operation to get dns forwarder rules


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[dns\_proxy\_stats\_response\_schema](#dns\_proxy\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* dns\_proxy\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="application\_name"></a>
### application\_name
Application Name

*Type* : string


<a name="dns\_proxy\_name"></a>
### dns\_proxy\_name
The DNS Proxy name

*Type* : string


<a name="dns\_proxy\_stats\_delete\_success\_schema"></a>
### dns\_proxy\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy\_stats**  <br>*optional*|[dns\_proxy\_stats](#dns\_proxy\_stats\_delete\_success\_schema-dns\_proxy\_stats)|

<a name="dns\_proxy\_stats\_delete\_success\_schema-dns\_proxy\_stats"></a>
**dns\_proxy\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="dns\_proxy\_stats\_post\_success\_schema"></a>
### dns\_proxy\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy\_stats**  <br>*optional*|[dns\_proxy\_stats](#dns\_proxy\_stats\_post\_success\_schema-dns\_proxy\_stats)|

<a name="dns\_proxy\_stats\_post\_success\_schema-dns\_proxy\_stats"></a>
**dns\_proxy\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="dns\_proxy\_stats\_put\_success\_schema"></a>
### dns\_proxy\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**dns\_proxy\_stats**  <br>*optional*|[dns\_proxy\_stats](#dns\_proxy\_stats\_put\_success\_schema-dns\_proxy\_stats)|

<a name="dns\_proxy\_stats\_put\_success\_schema-dns\_proxy\_stats"></a>
**dns\_proxy\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="dns\_proxy\_stats\_response\_schema"></a>
### dns\_proxy\_stats\_response\_schema
*Type* : < [dns\_proxy\_stats\_response\_schema](#dns\_proxy\_stats\_response\_schema-inline) > array

<a name="dns\_proxy\_stats\_response\_schema-inline"></a>
**dns\_proxy\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**application\_name**  <br>*optional*|[application\_name](#application\_name)|
|**dns\_proxy\_name**  <br>*optional*|[dns\_proxy\_name](#dns\_proxy\_name)|
|**dns\_service\_active**  <br>*optional*|[dns\_service\_active](#dns\_service\_active)|
|**dns\_service\_name**  <br>*optional*|[dns\_service\_name](#dns\_service\_name)|
|**hit\_count**  <br>*optional*|[hit\_count](#hit\_count)|


<a name="dns\_service\_active"></a>
### dns\_service\_active
The DNS service status

*Type* : string


<a name="dns\_service\_name"></a>
### dns\_service\_name
The DNS service name

*Type* : string


<a name="hit\_count"></a>
### hit\_count
The DNS Proxy rule Hit count

*Type* : integer





