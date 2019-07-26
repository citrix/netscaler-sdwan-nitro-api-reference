# access\_interfaces


<a name="overview"></a>
## Overview
This resource provides Access Interface Stat.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* access\_interfaces : Operations related to access\_interfaces 




<a name="paths"></a>
## Paths

<a name="access\_interfaces-get"></a>
### Get operation for access\_interfaces
```
GET /access_interfaces
```


#### Description
Use this operation to get Access Interface statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[access\_interfaces\_response\_schema](#access\_interfaces\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* access\_interfaces




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="access\_interface"></a>
### access\_interface
Access Interface Stats Array

*Type* : < [access\_interface](#access\_interface-inline) > array

<a name="access\_interface-inline"></a>
**access\_interface**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|WAN Link Access Interface Name|string|
|**ip\_address**  <br>*optional*  <br>*read-only*|WAN Link IP Address|string|
|**last\_arp\_reply\_age**  <br>*optional*  <br>*read-only*|ARP Reply Age|string|
|**mac**  <br>*optional*  <br>*read-only*|WAN Link MAC Address|string|
|**proxy\_arp\_state**  <br>*optional*  <br>*read-only*|WAN Link PROXY State|string|
|**proxy\_ip\_address**  <br>*optional*  <br>*read-only*|WAN Link PROXY IP Address|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|WAN Link Routing Domain|string|
|**wanlink\_name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|


<a name="access\_interfaces\_delete\_success\_schema"></a>
### access\_interfaces\_delete\_success\_schema

|Name|Schema|
|---|---|
|**access\_interfaces**  <br>*optional*|[access\_interfaces](#access\_interfaces\_delete\_success\_schema-access\_interfaces)|

<a name="access\_interfaces\_delete\_success\_schema-access\_interfaces"></a>
**access\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="access\_interfaces\_post\_success\_schema"></a>
### access\_interfaces\_post\_success\_schema

|Name|Schema|
|---|---|
|**access\_interfaces**  <br>*optional*|[access\_interfaces](#access\_interfaces\_post\_success\_schema-access\_interfaces)|

<a name="access\_interfaces\_post\_success\_schema-access\_interfaces"></a>
**access\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="access\_interfaces\_put\_success\_schema"></a>
### access\_interfaces\_put\_success\_schema

|Name|Schema|
|---|---|
|**access\_interfaces**  <br>*optional*|[access\_interfaces](#access\_interfaces\_put\_success\_schema-access\_interfaces)|

<a name="access\_interfaces\_put\_success\_schema-access\_interfaces"></a>
**access\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="access\_interfaces\_response\_schema"></a>
### access\_interfaces\_response\_schema
*Type* : < [access\_interfaces\_response\_schema](#access\_interfaces\_response\_schema-inline) > array

<a name="access\_interfaces\_response\_schema-inline"></a>
**access\_interfaces\_response\_schema**

|Name|Schema|
|---|---|
|**access\_interface**  <br>*optional*|[access\_interface](#access\_interface)|
|**internet\_data\_rates**  <br>*optional*|[internet\_data\_rates](#internet\_data\_rates)|
|**intranet\_data\_rates**  <br>*optional*|[intranet\_data\_rates](#intranet\_data\_rates)|
|**virtual\_path\_data\_rates**  <br>*optional*|[virtual\_path\_data\_rates](#virtual\_path\_data\_rates)|


<a name="internet\_data\_rates"></a>
### internet\_data\_rates
Access Interface Internet Data Rates Array

*Type* : < [internet\_data\_rates](#internet\_data\_rates-inline) > array

<a name="internet\_data\_rates-inline"></a>
**internet\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|Access Interface Name|string|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved. Displayed only for Virtual Path Datarate|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**rcvd\_rate\_kbps**  <br>*optional*  <br>*read-only*|Received rate kbps|number|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain Name. Displayed only for Intranet Datarate|string|
|**sent\_rate\_kbps**  <br>*optional*  <br>*read-only*|Sent rate kbps|number|
|**service\_name**  <br>*optional*  <br>*read-only*|Service Name|string|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|
|**wanlink\_name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|


<a name="intranet\_data\_rates"></a>
### intranet\_data\_rates
Access Interface Intranet Data Rates Array

*Type* : < [intranet\_data\_rates](#intranet\_data\_rates-inline) > array

<a name="intranet\_data\_rates-inline"></a>
**intranet\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|Access Interface Name|string|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved. Displayed only for Virtual Path Datarate|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**rcvd\_rate\_kbps**  <br>*optional*  <br>*read-only*|Received rate kbps|number|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain Name. Displayed only for Intranet Datarate|string|
|**sent\_rate\_kbps**  <br>*optional*  <br>*read-only*|Sent rate kbps|number|
|**service\_name**  <br>*optional*  <br>*read-only*|Service Name|string|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|
|**wanlink\_name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|


<a name="virtual\_path\_data\_rates"></a>
### virtual\_path\_data\_rates
Access Interface Virtual Paths Service Data Rates Array

*Type* : < [virtual\_path\_data\_rates](#virtual\_path\_data\_rates-inline) > array

<a name="virtual\_path\_data\_rates-inline"></a>
**virtual\_path\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|Access Interface Name|string|
|**bytes\_saved**  <br>*optional*  <br>*read-only*|Bytes Saved. Displayed only for Virtual Path Datarate|string|
|**delta\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Delta Bytes Received|string|
|**delta\_bytes\_sent**  <br>*optional*  <br>*read-only*|Delta Bytes Sent|string|
|**delta\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Delta Packets received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Delta Packets sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**rcvd\_rate\_kbps**  <br>*optional*  <br>*read-only*|Received rate kbps|number|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain Name. Displayed only for Intranet Datarate|string|
|**sent\_rate\_kbps**  <br>*optional*  <br>*read-only*|Sent rate kbps|number|
|**service\_name**  <br>*optional*  <br>*read-only*|Service Name|string|
|**total\_bytes\_rcvd**  <br>*optional*  <br>*read-only*|Total Bytes Recieved|string|
|**total\_bytes\_sent**  <br>*optional*  <br>*read-only*|Total Bytes Sent|string|
|**total\_packets\_rcvd**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets Sent|string|
|**wanlink\_name**  <br>*optional*  <br>*read-only*|WAN Link Name|string|





