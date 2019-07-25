# ethernet\_mac\_learning\_stats


<a name="overview"></a>
## Overview
This resource provides Ethernet MAC Learning Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* ethernet\_mac\_learning\_stats : Operations related to ethernet\_mac\_learning\_stats 




<a name="paths"></a>
## Paths

<a name="ethernet\_mac\_learning\_stats-get"></a>
### Get operation for ethernet\_mac\_learning\_stats
```
GET /ethernet_mac_learning_stats
```


#### Description
Use this operation to get Ethernet MAC Learning statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ethernet\_mac\_learning\_stats\_response\_schema](#ethernet\_mac\_learning\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ethernet\_mac\_learning\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="age\_ms"></a>
### age\_ms
Reply Age in ms for Ethernet MAC Learning Element

*Type* : integer


<a name="ethernet\_interface"></a>
### ethernet\_interface
Ethernet Interface

*Type* : string


<a name="ethernet\_mac\_learning\_stats\_delete\_success\_schema"></a>
### ethernet\_mac\_learning\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_mac\_learning\_stats**  <br>*optional*|[ethernet\_mac\_learning\_stats](#ethernet\_mac\_learning\_stats\_delete\_success\_schema-ethernet\_mac\_learning\_stats)|

<a name="ethernet\_mac\_learning\_stats\_delete\_success\_schema-ethernet\_mac\_learning\_stats"></a>
**ethernet\_mac\_learning\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ethernet\_mac\_learning\_stats\_post\_success\_schema"></a>
### ethernet\_mac\_learning\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_mac\_learning\_stats**  <br>*optional*|[ethernet\_mac\_learning\_stats](#ethernet\_mac\_learning\_stats\_post\_success\_schema-ethernet\_mac\_learning\_stats)|

<a name="ethernet\_mac\_learning\_stats\_post\_success\_schema-ethernet\_mac\_learning\_stats"></a>
**ethernet\_mac\_learning\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ethernet\_mac\_learning\_stats\_put\_success\_schema"></a>
### ethernet\_mac\_learning\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_mac\_learning\_stats**  <br>*optional*|[ethernet\_mac\_learning\_stats](#ethernet\_mac\_learning\_stats\_put\_success\_schema-ethernet\_mac\_learning\_stats)|

<a name="ethernet\_mac\_learning\_stats\_put\_success\_schema-ethernet\_mac\_learning\_stats"></a>
**ethernet\_mac\_learning\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ethernet\_mac\_learning\_stats\_response\_schema"></a>
### ethernet\_mac\_learning\_stats\_response\_schema
*Type* : < [ethernet\_mac\_learning\_stats\_response\_schema](#ethernet\_mac\_learning\_stats\_response\_schema-inline) > array

<a name="ethernet\_mac\_learning\_stats\_response\_schema-inline"></a>
**ethernet\_mac\_learning\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**age\_ms**  <br>*optional*|[age\_ms](#age\_ms)|
|**ethernet\_interface**  <br>*optional*|[ethernet\_interface](#ethernet\_interface)|
|**hit\_count**  <br>*optional*|[hit\_count](#hit\_count)|
|**interface\_group**  <br>*optional*|[interface\_group](#interface\_group)|
|**mac\_address**  <br>*optional*|[mac\_address](#mac\_address)|
|**vlan**  <br>*optional*|[vlan](#vlan)|


<a name="hit\_count"></a>
### hit\_count
Hit Count for Ethernet MAC Learning Element

*Type* : integer


<a name="interface\_group"></a>
### interface\_group
Interface Group for Ethernet MAC Learning Element

*Type* : integer


<a name="mac\_address"></a>
### mac\_address
MAC Address

*Type* : string


<a name="vlan"></a>
### vlan
VLAN for Ethernet MAC Learning Element

*Type* : integer





