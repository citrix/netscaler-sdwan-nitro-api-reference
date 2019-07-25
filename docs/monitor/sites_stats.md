# sites\_stats


<a name="overview"></a>
## Overview
API to get sites information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* sites\_stats : Operations related to sites\_stats 




<a name="paths"></a>
## Paths

<a name="sites\_stats-get"></a>
### Get operation for sites\_stats
```
GET /sites_stats
```


#### Description
Use this operation to get sites statistics.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sites\_stats\_response\_schema](#sites\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="lan\_to\_wan"></a>
### lan\_to\_wan
LAN to WAN stats.

*Type* : < [lan\_to\_wan](#lan\_to\_wan-inline) > array

<a name="lan\_to\_wan-inline"></a>
**lan\_to\_wan**

|Name|Description|Schema|
|---|---|---|
|**bytes\_dropped**  <br>*optional*  <br>*read-only*|Bytes dropped|number|
|**bytes\_sent**  <br>*optional*  <br>*read-only*|Bytes sent|number|
|**kbps\_dropped**  <br>*optional*  <br>*read-only*|Kilobytes dropped per second|number|
|**kbps\_sent**  <br>*optional*  <br>*read-only*|Kilobytes sent per second|number|
|**packets\_dropped**  <br>*optional*  <br>*read-only*|Packets dropped|integer|
|**packets\_dropped\_per\_sec**  <br>*optional*  <br>*read-only*|Packets dropped per second|number|
|**packets\_sent**  <br>*optional*  <br>*read-only*|Packets sent|integer|
|**packets\_sent\_per\_sec**  <br>*optional*  <br>*read-only*|Packets sent per second|number|
|**service**  <br>*optional*  <br>*read-only*|Service name|string|


<a name="passthrough"></a>
### passthrough
Passthrough stats.

*Type* : < [passthrough](#passthrough-inline) > array

<a name="passthrough-inline"></a>
**passthrough**

|Name|Description|Schema|
|---|---|---|
|**bytes\_dropped**  <br>*optional*  <br>*read-only*|Bytes dropped|number|
|**bytes\_received**  <br>*optional*  <br>*read-only*|Bytes received|number|
|**bytes\_sent**  <br>*optional*  <br>*read-only*|Bytes sent|number|
|**kbps\_dropped**  <br>*optional*  <br>*read-only*|Kilobytes dropped per second|number|
|**kbps\_received**  <br>*optional*  <br>*read-only*|Kilobytes received per second|number|
|**kbps\_sent**  <br>*optional*  <br>*read-only*|Kilobytes sent per second|number|
|**packets\_dropped**  <br>*optional*  <br>*read-only*|Packets dropped|integer|
|**packets\_dropped\_per\_sec**  <br>*optional*  <br>*read-only*|Packets dropped per second|number|
|**packets\_received**  <br>*optional*  <br>*read-only*|Packets received|integer|
|**packets\_received\_per\_sec**  <br>*optional*  <br>*read-only*|Packets received per second|number|
|**packets\_sent**  <br>*optional*  <br>*read-only*|Packets sent|integer|
|**packets\_sent\_per\_sec**  <br>*optional*  <br>*read-only*|Packets sent per second|number|


<a name="sites\_stats\_delete\_success\_schema"></a>
### sites\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sites\_stats**  <br>*optional*|[sites\_stats](#sites\_stats\_delete\_success\_schema-sites\_stats)|

<a name="sites\_stats\_delete\_success\_schema-sites\_stats"></a>
**sites\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sites\_stats\_post\_success\_schema"></a>
### sites\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**sites\_stats**  <br>*optional*|[sites\_stats](#sites\_stats\_post\_success\_schema-sites\_stats)|

<a name="sites\_stats\_post\_success\_schema-sites\_stats"></a>
**sites\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sites\_stats\_put\_success\_schema"></a>
### sites\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**sites\_stats**  <br>*optional*|[sites\_stats](#sites\_stats\_put\_success\_schema-sites\_stats)|

<a name="sites\_stats\_put\_success\_schema-sites\_stats"></a>
**sites\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sites\_stats\_response\_schema"></a>
### sites\_stats\_response\_schema
*Type* : < [sites\_stats\_response\_schema](#sites\_stats\_response\_schema-inline) > array

<a name="sites\_stats\_response\_schema-inline"></a>
**sites\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**lan\_to\_wan**  <br>*optional*|[lan\_to\_wan](#lan\_to\_wan)|
|**passthrough**  <br>*optional*|[passthrough](#passthrough)|
|**wan\_to\_lan**  <br>*optional*|[wan\_to\_lan](#wan\_to\_lan)|


<a name="wan\_to\_lan"></a>
### wan\_to\_lan
WAN to LAN stats.

*Type* : < [wan\_to\_lan](#wan\_to\_lan-inline) > array

<a name="wan\_to\_lan-inline"></a>
**wan\_to\_lan**

|Name|Description|Schema|
|---|---|---|
|**bytes\_dropped**  <br>*optional*  <br>*read-only*|Bytes dropped|number|
|**bytes\_received**  <br>*optional*  <br>*read-only*|Bytes received|number|
|**kbps\_dropped**  <br>*optional*  <br>*read-only*|Kilobytes dropped per second|number|
|**kbps\_received**  <br>*optional*  <br>*read-only*|Kilobytes received per second|number|
|**packets\_dropped**  <br>*optional*  <br>*read-only*|Packets dropped|integer|
|**packets\_dropped\_per\_sec**  <br>*optional*  <br>*read-only*|Packets dropped per second|number|
|**packets\_received**  <br>*optional*  <br>*read-only*|Packets received|integer|
|**packets\_received\_per\_sec**  <br>*optional*  <br>*read-only*|Packets received per second|number|
|**service**  <br>*optional*  <br>*read-only*|Service name|string|





