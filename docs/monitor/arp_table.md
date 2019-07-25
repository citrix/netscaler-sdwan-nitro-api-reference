# arp\_table


<a name="overview"></a>
## Overview
API to get the ARP Table


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* arp\_table : Operations related to arp\_table 




<a name="paths"></a>
## Paths

<a name="arp\_table-get"></a>
### Get operation for arp\_table
```
GET /arp_table
```


#### Description
Use this operation to get ARP Statistics Table


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[arp\_table\_response\_schema](#arp\_table\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* arp\_table




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="arp\_table\_delete\_success\_schema"></a>
### arp\_table\_delete\_success\_schema

|Name|Schema|
|---|---|
|**arp\_table**  <br>*optional*|[arp\_table](#arp\_table\_delete\_success\_schema-arp\_table)|

<a name="arp\_table\_delete\_success\_schema-arp\_table"></a>
**arp\_table**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="arp\_table\_post\_success\_schema"></a>
### arp\_table\_post\_success\_schema

|Name|Schema|
|---|---|
|**arp\_table**  <br>*optional*|[arp\_table](#arp\_table\_post\_success\_schema-arp\_table)|

<a name="arp\_table\_post\_success\_schema-arp\_table"></a>
**arp\_table**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="arp\_table\_put\_success\_schema"></a>
### arp\_table\_put\_success\_schema

|Name|Schema|
|---|---|
|**arp\_table**  <br>*optional*|[arp\_table](#arp\_table\_put\_success\_schema-arp\_table)|

<a name="arp\_table\_put\_success\_schema-arp\_table"></a>
**arp\_table**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="arp\_table\_response\_schema"></a>
### arp\_table\_response\_schema
*Type* : < [arp\_table\_response\_schema](#arp\_table\_response\_schema-inline) > array

<a name="arp\_table\_response\_schema-inline"></a>
**arp\_table\_response\_schema**

|Name|Schema|
|---|---|
|**interface**  <br>*optional*|[interface](#interface)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**mac\_address**  <br>*optional*|[mac\_address](#mac\_address)|
|**reply\_age**  <br>*optional*|[reply\_age](#reply\_age)|
|**routing\_domain**  <br>*optional*|[routing\_domain](#routing\_domain)|
|**state**  <br>*optional*|[state](#state)|
|**type**  <br>*optional*|[type](#type)|
|**vlan**  <br>*optional*|[vlan](#vlan)|


<a name="interface"></a>
### interface
The interface to which ARP Statistics apply

*Type* : integer


<a name="ip\_address"></a>
### ip\_address
The interface IP Address

*Type* : string


<a name="mac\_address"></a>
### mac\_address
The interface MAC Address

*Type* : string


<a name="reply\_age"></a>
### reply\_age
The Interface reply age in milliseconds

*Type* : integer


<a name="routing\_domain"></a>
### routing\_domain
The interface Routing domain

*Type* : string


<a name="state"></a>
### state
The interface state

*Type* : string


<a name="type"></a>
### type
The ARP Stats Type

*Type* : string


<a name="vlan"></a>
### vlan
Virtual LAN Interface identifier

*Type* : integer





