# paths\_detailed


<a name="overview"></a>
## Overview
This resource provides detailed summary of all the paths in Appliance


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* paths\_detailed : Operations related to paths\_detailed 




<a name="paths"></a>
## Paths

<a name="paths\_detailed-get"></a>
### Get operation for paths\_detailed
```
GET /paths_detailed
```


#### Description
Use this operation to get detailed Paths Summary. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API .


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[paths\_detailed\_response\_schema](#paths\_detailed\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* paths\_detailed




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bandwidth"></a>
### bandwidth
Path's Bandwidth in kbps

*Type* : number


<a name="bowt"></a>
### bowt
Best One Way Time Latency

*Type* : integer


<a name="congestion"></a>
### congestion
Path's Congestion State

*Type* : enum (YES, NO)


<a name="destination\_port"></a>
### destination\_port
Destination Port Number

*Type* : integer


<a name="duration"></a>
### duration
Duration of Path in Current State (in seconds)

*Type* : string


<a name="from\_link"></a>
### from\_link
Name of the Path(From Link)

*Type* : string


<a name="jitter"></a>
### jitter
Path's Jitter value

*Type* : integer


<a name="mtu"></a>
### mtu
Maximum Transferable Unit

*Type* : string


<a name="packet\_loss"></a>
### packet\_loss
Path's Packet Loss Percentage

*Type* : number


<a name="packets\_ooo"></a>
### packets\_ooo
Packets Out of Order

*Type* : integer


<a name="packets\_received"></a>
### packets\_received
Packets Received

*Type* : integer


<a name="path\_service\_state"></a>
### path\_service\_state
Virtual Path Service State

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="path\_service\_type"></a>
### path\_service\_type
Virtual Path Service Type

*Type* : enum (Static, Dynamic)


<a name="path\_state"></a>
### path\_state
Path State

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="path\_state\_reason"></a>
### path\_state\_reason
Reason of Path State

*Type* : enum (SILENCE, LOSS, PEER, GATEWAY, N/A)


<a name="paths\_detailed\_delete\_success\_schema"></a>
### paths\_detailed\_delete\_success\_schema

|Name|Schema|
|---|---|
|**paths\_detailed**  <br>*optional*|[paths\_detailed](#paths\_detailed\_delete\_success\_schema-paths\_detailed)|

<a name="paths\_detailed\_delete\_success\_schema-paths\_detailed"></a>
**paths\_detailed**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="paths\_detailed\_post\_success\_schema"></a>
### paths\_detailed\_post\_success\_schema

|Name|Schema|
|---|---|
|**paths\_detailed**  <br>*optional*|[paths\_detailed](#paths\_detailed\_post\_success\_schema-paths\_detailed)|

<a name="paths\_detailed\_post\_success\_schema-paths\_detailed"></a>
**paths\_detailed**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="paths\_detailed\_put\_success\_schema"></a>
### paths\_detailed\_put\_success\_schema

|Name|Schema|
|---|---|
|**paths\_detailed**  <br>*optional*|[paths\_detailed](#paths\_detailed\_put\_success\_schema-paths\_detailed)|

<a name="paths\_detailed\_put\_success\_schema-paths\_detailed"></a>
**paths\_detailed**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="paths\_detailed\_response\_schema"></a>
### paths\_detailed\_response\_schema
*Type* : < [paths\_detailed\_response\_schema](#paths\_detailed\_response\_schema-inline) > array

<a name="paths\_detailed\_response\_schema-inline"></a>
**paths\_detailed\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth**  <br>*optional*|[bandwidth](#bandwidth)|
|**bowt**  <br>*optional*|[bowt](#bowt)|
|**congestion**  <br>*optional*|[congestion](#congestion)|
|**destination\_port**  <br>*optional*|[destination\_port](#destination\_port)|
|**duration**  <br>*optional*|[duration](#duration)|
|**from\_link**  <br>*optional*|[from\_link](#from\_link)|
|**jitter**  <br>*optional*|[jitter](#jitter)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**packet\_loss**  <br>*optional*|[packet\_loss](#packet\_loss)|
|**packets\_ooo**  <br>*optional*|[packets\_ooo](#packets\_ooo)|
|**packets\_received**  <br>*optional*|[packets\_received](#packets\_received)|
|**path\_service\_state**  <br>*optional*|[path\_service\_state](#path\_service\_state)|
|**path\_service\_type**  <br>*optional*|[path\_service\_type](#path\_service\_type)|
|**path\_state**  <br>*optional*|[path\_state](#path\_state)|
|**path\_state\_reason**  <br>*optional*|[path\_state\_reason](#path\_state\_reason)|
|**source\_port**  <br>*optional*|[source\_port](#source\_port)|
|**to\_link**  <br>*optional*|[to\_link](#to\_link)|


<a name="source\_port"></a>
### source\_port
Source Port Number

*Type* : integer


<a name="to\_link"></a>
### to\_link
Name of the Path(To Link)

*Type* : string





