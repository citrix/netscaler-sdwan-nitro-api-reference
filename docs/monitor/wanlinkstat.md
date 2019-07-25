# wanlinkstat


<a name="overview"></a>
## Overview
This resource provides WAN Link Stat.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* wanlinkstat : Operations related to wanlinkstat 




<a name="paths"></a>
## Paths

<a name="wanlinkstat-get"></a>
### Get operation for wanlinkstat
```
GET /wanlinkstat
```


#### Description
Use this operation to get WAN Link statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wanlinkstat\_response\_schema](#wanlinkstat\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wanlinkstat




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="internet\_data\_rates"></a>
### internet\_data\_rates
Wan Link Internet Data Rates Array

*Type* : < [internet\_data\_rates](#internet\_data\_rates-inline) > array

<a name="internet\_data\_rates-inline"></a>
**internet\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets Received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets Sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|WAN Link Routing Domain Name|string|
|**time\_diff**  <br>*optional*  <br>*read-only*|Time Difference|integer|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|


<a name="intranet\_data\_rates"></a>
### intranet\_data\_rates
Wan Link Internet Data Rates Array

*Type* : < [intranet\_data\_rates](#intranet\_data\_rates-inline) > array

<a name="intranet\_data\_rates-inline"></a>
**intranet\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets Received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets Sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|WAN Link Routing Domain Name|string|
|**time\_diff**  <br>*optional*  <br>*read-only*|Time Difference|integer|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|


<a name="virtual\_path\_data\_rates"></a>
### virtual\_path\_data\_rates
Wan Link Virtual Paths Data Rate Array

*Type* : < [virtual\_path\_data\_rates](#virtual\_path\_data\_rates-inline) > array

<a name="virtual\_path\_data\_rates-inline"></a>
**virtual\_path\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets Received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets Sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|WAN Link Routing Domain Name|string|
|**time\_diff**  <br>*optional*  <br>*read-only*|Time Difference|integer|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|


<a name="wan\_link"></a>
### wan\_link
Wan Link Stats Array

*Type* : < [wan\_link](#wan\_link-inline) > array

<a name="wan\_link-inline"></a>
**wan\_link**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|WAN Link Access Interface Name|string|
|**ip\_address**  <br>*optional*  <br>*read-only*|WAN Link IP Address|string|
|**last\_arp\_reply\_age**  <br>*optional*  <br>*read-only*|ARP Reply Age|string|
|**mac**  <br>*optional*  <br>*read-only*|WAN Link MAC Address|string|
|**proxy\_arp\_state**  <br>*optional*  <br>*read-only*|WAN Link PROXY State|string|
|**proxy\_ip\_address**  <br>*optional*  <br>*read-only*|WAN Link PROXY IP Address|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|WAN Link Routing Domain|string|
|**wl\_name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|


<a name="wanlinkstat\_delete\_success\_schema"></a>
### wanlinkstat\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wanlinkstat**  <br>*optional*|[wanlinkstat](#wanlinkstat\_delete\_success\_schema-wanlinkstat)|

<a name="wanlinkstat\_delete\_success\_schema-wanlinkstat"></a>
**wanlinkstat**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wanlinkstat\_post\_success\_schema"></a>
### wanlinkstat\_post\_success\_schema

|Name|Schema|
|---|---|
|**wanlinkstat**  <br>*optional*|[wanlinkstat](#wanlinkstat\_post\_success\_schema-wanlinkstat)|

<a name="wanlinkstat\_post\_success\_schema-wanlinkstat"></a>
**wanlinkstat**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wanlinkstat\_put\_success\_schema"></a>
### wanlinkstat\_put\_success\_schema

|Name|Schema|
|---|---|
|**wanlinkstat**  <br>*optional*|[wanlinkstat](#wanlinkstat\_put\_success\_schema-wanlinkstat)|

<a name="wanlinkstat\_put\_success\_schema-wanlinkstat"></a>
**wanlinkstat**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wanlinkstat\_response\_schema"></a>
### wanlinkstat\_response\_schema
*Type* : < [wanlinkstat\_response\_schema](#wanlinkstat\_response\_schema-inline) > array

<a name="wanlinkstat\_response\_schema-inline"></a>
**wanlinkstat\_response\_schema**

|Name|Schema|
|---|---|
|**internet\_data\_rates**  <br>*optional*|[internet\_data\_rates](#internet\_data\_rates)|
|**intranet\_data\_rates**  <br>*optional*|[intranet\_data\_rates](#intranet\_data\_rates)|
|**virtual\_path\_data\_rates**  <br>*optional*|[virtual\_path\_data\_rates](#virtual\_path\_data\_rates)|
|**wan\_link**  <br>*optional*|[wan\_link](#wan\_link)|





