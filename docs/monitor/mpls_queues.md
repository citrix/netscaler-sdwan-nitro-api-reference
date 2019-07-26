# mpls\_queues


<a name="overview"></a>
## Overview
This resource provides MPLS Queues statistics.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* mpls\_queues : Operations related to mpls\_queues 




<a name="paths"></a>
## Paths

<a name="mpls\_queues-get"></a>
### Get operation for mpls\_queues
```
GET /mpls_queues
```


#### Description
Use this operation to get MPLS Queues statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[mpls\_queues\_response\_schema](#mpls\_queues\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mpls\_queues




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="intranet\_data\_rates"></a>
### intranet\_data\_rates
MPLS Queues Intranet Data Rates Array

*Type* : < [intranet\_data\_rates](#intranet\_data\_rates-inline) > array

<a name="intranet\_data\_rates-inline"></a>
**intranet\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**compression\_bytes\_saved\_recv**  <br>*optional*  <br>*read-only*|IP, TCP, UDP Header compression bytes saved. Displayed only for Virtual Path Datarate|string|
|**compression\_bytes\_saved\_sent**  <br>*optional*  <br>*read-only*|IP, TCP, UDP Header compression bytes saved. Displayed only for Virtual Path Datarate|string|
|**delta\_kB\_recv**  <br>*optional*  <br>*read-only*|Total delta bytes received in kB|string|
|**delta\_kB\_sent**  <br>*optional*  <br>*read-only*|Total delta bytes sent in kB|string|
|**delta\_packets\_recv**  <br>*optional*  <br>*read-only*|Total delta packets received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Total delta packets sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**mismatched\_dscp\_kB\_recv**  <br>*optional*  <br>*read-only*|Mismatched DSCP bytes received in kB|string|
|**mismatched\_dscp\_kB\_sent**  <br>*optional*  <br>*read-only*|Mismatched DSCP bytes sent in kB|string|
|**mismatched\_dscp\_packets\_recv**  <br>*optional*  <br>*read-only*|Mismatched DSCP Packets received|string|
|**mismatched\_dscp\_packets\_sent**  <br>*optional*  <br>*read-only*|Mismatched DSCP Packets sent|string|
|**mpls\_queue\_name**  <br>*optional*  <br>*read-only*|MPLS Queue Name|string|
|**recv\_rate\_kbps**  <br>*optional*  <br>*read-only*|Received rate in kbps|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain Name|string|
|**sent\_rate\_kbps**  <br>*optional*  <br>*read-only*|Sent rate in kbps|string|
|**total\_kB\_recv**  <br>*optional*  <br>*read-only*|Total bytes received in kB|string|
|**total\_kB\_sent**  <br>*optional*  <br>*read-only*|Total bytes sent in kB|string|
|**total\_packets\_recv**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets sent|string|


<a name="mpls\_queue\_data"></a>
### mpls\_queue\_data
MPLS Queues stats array

*Type* : < [mpls\_queue\_data](#mpls\_queue\_data-inline) > array

<a name="mpls\_queue\_data-inline"></a>
**mpls\_queue\_data**

|Name|Description|Schema|
|---|---|---|
|**ai\_name**  <br>*optional*  <br>*read-only*|Access Interface Name|string|
|**ip\_address**  <br>*optional*  <br>*read-only*|MPLS IP Address|string|
|**last\_arp\_reply\_age**  <br>*optional*  <br>*read-only*|ARP Reply Age|string|
|**mac**  <br>*optional*  <br>*read-only*|MPLS MAC Address|string|
|**mpls\_queue\_name**  <br>*optional*  <br>*read-only*|MPLS Queue Name|string|
|**private\_mpls**  <br>*optional*  <br>*read-only*|Private MPLS Name|string|
|**proxy\_address**  <br>*optional*  <br>*read-only*|MPLS Proxy IP Address|string|
|**proxy\_arp\_state**  <br>*optional*  <br>*read-only*|MPLS Proxy State|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain|string|


<a name="mpls\_queues\_delete\_success\_schema"></a>
### mpls\_queues\_delete\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_delete\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_delete\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="mpls\_queues\_post\_success\_schema"></a>
### mpls\_queues\_post\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_post\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_post\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="mpls\_queues\_put\_success\_schema"></a>
### mpls\_queues\_put\_success\_schema

|Name|Schema|
|---|---|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues\_put\_success\_schema-mpls\_queues)|

<a name="mpls\_queues\_put\_success\_schema-mpls\_queues"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="mpls\_queues\_response\_schema"></a>
### mpls\_queues\_response\_schema
*Type* : < [mpls\_queues\_response\_schema](#mpls\_queues\_response\_schema-inline) > array

<a name="mpls\_queues\_response\_schema-inline"></a>
**mpls\_queues\_response\_schema**

|Name|Schema|
|---|---|
|**intranet\_data\_rates**  <br>*optional*|[intranet\_data\_rates](#intranet\_data\_rates)|
|**mpls\_queue\_data**  <br>*optional*|[mpls\_queue\_data](#mpls\_queue\_data)|
|**virtual\_path\_data\_rates**  <br>*optional*|[virtual\_path\_data\_rates](#virtual\_path\_data\_rates)|


<a name="virtual\_path\_data\_rates"></a>
### virtual\_path\_data\_rates
MPLS Queues Virtual Paths Service Data Rates Array

*Type* : < [virtual\_path\_data\_rates](#virtual\_path\_data\_rates-inline) > array

<a name="virtual\_path\_data\_rates-inline"></a>
**virtual\_path\_data\_rates**

|Name|Description|Schema|
|---|---|---|
|**compression\_bytes\_saved\_recv**  <br>*optional*  <br>*read-only*|IP, TCP, UDP Header compression bytes saved. Displayed only for Virtual Path Datarate|string|
|**compression\_bytes\_saved\_sent**  <br>*optional*  <br>*read-only*|IP, TCP, UDP Header compression bytes saved. Displayed only for Virtual Path Datarate|string|
|**delta\_kB\_recv**  <br>*optional*  <br>*read-only*|Total delta bytes received in kB|string|
|**delta\_kB\_sent**  <br>*optional*  <br>*read-only*|Total delta bytes sent in kB|string|
|**delta\_packets\_recv**  <br>*optional*  <br>*read-only*|Total delta packets received|string|
|**delta\_packets\_sent**  <br>*optional*  <br>*read-only*|Total delta packets sent|string|
|**direction**  <br>*optional*  <br>*read-only*|Direction Of Datarate|string|
|**mismatched\_dscp\_kB\_recv**  <br>*optional*  <br>*read-only*|Mismatched DSCP bytes received in kB|string|
|**mismatched\_dscp\_kB\_sent**  <br>*optional*  <br>*read-only*|Mismatched DSCP bytes sent in kB|string|
|**mismatched\_dscp\_packets\_recv**  <br>*optional*  <br>*read-only*|Mismatched DSCP Packets received|string|
|**mismatched\_dscp\_packets\_sent**  <br>*optional*  <br>*read-only*|Mismatched DSCP Packets sent|string|
|**mpls\_queue\_name**  <br>*optional*  <br>*read-only*|MPLS Queue Name|string|
|**recv\_rate\_kbps**  <br>*optional*  <br>*read-only*|Received rate in kbps|string|
|**routing\_domain\_name**  <br>*optional*  <br>*read-only*|Routing Domain Name|string|
|**sent\_rate\_kbps**  <br>*optional*  <br>*read-only*|Sent rate in kbps|string|
|**total\_kB\_recv**  <br>*optional*  <br>*read-only*|Total bytes received in kB|string|
|**total\_kB\_sent**  <br>*optional*  <br>*read-only*|Total bytes sent in kB|string|
|**total\_packets\_recv**  <br>*optional*  <br>*read-only*|Total Packets received|string|
|**total\_packets\_sent**  <br>*optional*  <br>*read-only*|Total Packets sent|string|





