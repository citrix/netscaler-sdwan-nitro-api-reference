# paths


<a name="overview"></a>
## Overview
This resource provides details of all the paths in Appliance


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* paths : Operations related to paths 




<a name="paths"></a>
## Paths

<a name="paths-get"></a>
### Get operation for paths
```
GET /paths
```


#### Description
Use this operation to get Paths Summary. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[paths\_response\_schema](#paths\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* paths




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
Path's congestion state

*Type* : enum (YES, NO)


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

*Type* : integer


<a name="packet\_loss"></a>
### packet\_loss
Path's Packet Loss

*Type* : number


<a name="path\_service\_state"></a>
### path\_service\_state
Path Service State

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="path\_service\_type"></a>
### path\_service\_type
Path Service Type

*Type* : enum (Static, Dynamic)


<a name="path\_state"></a>
### path\_state
Path State

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="paths\_delete\_success\_schema"></a>
### paths\_delete\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_delete\_success\_schema-paths)|

<a name="paths\_delete\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="paths\_post\_success\_schema"></a>
### paths\_post\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_post\_success\_schema-paths)|

<a name="paths\_post\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="paths\_put\_success\_schema"></a>
### paths\_put\_success\_schema

|Name|Schema|
|---|---|
|**paths**  <br>*optional*|[paths](#paths\_put\_success\_schema-paths)|

<a name="paths\_put\_success\_schema-paths"></a>
**paths**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="paths\_response\_schema"></a>
### paths\_response\_schema
*Type* : < [paths\_response\_schema](#paths\_response\_schema-inline) > array

<a name="paths\_response\_schema-inline"></a>
**paths\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth**  <br>*optional*|[bandwidth](#bandwidth)|
|**bowt**  <br>*optional*|[bowt](#bowt)|
|**congestion**  <br>*optional*|[congestion](#congestion)|
|**from\_link**  <br>*optional*|[from\_link](#from\_link)|
|**jitter**  <br>*optional*|[jitter](#jitter)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**packet\_loss**  <br>*optional*|[packet\_loss](#packet\_loss)|
|**path\_service\_state**  <br>*optional*|[path\_service\_state](#path\_service\_state)|
|**path\_service\_type**  <br>*optional*|[path\_service\_type](#path\_service\_type)|
|**path\_state**  <br>*optional*|[path\_state](#path\_state)|
|**to\_link**  <br>*optional*|[to\_link](#to\_link)|


<a name="to\_link"></a>
### to\_link
Name of the Path(To Link)

*Type* : string





