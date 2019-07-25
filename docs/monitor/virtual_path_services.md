# virtual\_path\_services


<a name="overview"></a>
## Overview
This resource provides details of all the virtual path services in Appliance


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* virtual\_path\_services : Operations related to virtual\_path\_services 




<a name="paths"></a>
## Paths

<a name="virtual\_path\_services-get"></a>
### Get operation for virtual\_path\_services
```
GET /virtual_path_services
```


#### Description
Use this operation to get Virtual Paths Service statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[virtual\_path\_services\_response\_schema](#virtual\_path\_services\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* virtual\_path\_services




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="best\_jitter"></a>
### best\_jitter
best Jitter value for the virtual path service

*Type* : integer


<a name="bowt"></a>
### bowt
Best One Way Time Latency

*Type* : integer


<a name="from\_site"></a>
### from\_site
Name of the Virtual Path Service(From Site)

*Type* : string


<a name="ipsec\_tunnel\_state"></a>
### ipsec\_tunnel\_state
IPsec tunnel state

*Type* : string


<a name="mtu"></a>
### mtu
Maximum Transferable Unit

*Type* : string


<a name="receive\_rate"></a>
### receive\_rate
receive rate for the virtual path service

*Type* : number


<a name="since\_created"></a>
### since\_created
Time since creation

*Type* : integer


<a name="state"></a>
### state
State of the virtual path service

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="to\_site"></a>
### to\_site
Name of the Virtual Path Service(To Site)

*Type* : string


<a name="virtual\_path\_service\_type"></a>
### virtual\_path\_service\_type
Virtual Path Service Type

*Type* : enum (Static, Dynamic)


<a name="virtual\_path\_services\_delete\_success\_schema"></a>
### virtual\_path\_services\_delete\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_services**  <br>*optional*|[virtual\_path\_services](#virtual\_path\_services\_delete\_success\_schema-virtual\_path\_services)|

<a name="virtual\_path\_services\_delete\_success\_schema-virtual\_path\_services"></a>
**virtual\_path\_services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="virtual\_path\_services\_post\_success\_schema"></a>
### virtual\_path\_services\_post\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_services**  <br>*optional*|[virtual\_path\_services](#virtual\_path\_services\_post\_success\_schema-virtual\_path\_services)|

<a name="virtual\_path\_services\_post\_success\_schema-virtual\_path\_services"></a>
**virtual\_path\_services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="virtual\_path\_services\_put\_success\_schema"></a>
### virtual\_path\_services\_put\_success\_schema

|Name|Schema|
|---|---|
|**virtual\_path\_services**  <br>*optional*|[virtual\_path\_services](#virtual\_path\_services\_put\_success\_schema-virtual\_path\_services)|

<a name="virtual\_path\_services\_put\_success\_schema-virtual\_path\_services"></a>
**virtual\_path\_services**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="virtual\_path\_services\_response\_schema"></a>
### virtual\_path\_services\_response\_schema
*Type* : < [virtual\_path\_services\_response\_schema](#virtual\_path\_services\_response\_schema-inline) > array

<a name="virtual\_path\_services\_response\_schema-inline"></a>
**virtual\_path\_services\_response\_schema**

|Name|Schema|
|---|---|
|**best\_jitter**  <br>*optional*|[best\_jitter](#best\_jitter)|
|**bowt**  <br>*optional*|[bowt](#bowt)|
|**from\_site**  <br>*optional*|[from\_site](#from\_site)|
|**ipsec\_tunnel\_state**  <br>*optional*|[ipsec\_tunnel\_state](#ipsec\_tunnel\_state)|
|**mtu**  <br>*optional*|[mtu](#mtu)|
|**receive\_rate**  <br>*optional*|[receive\_rate](#receive\_rate)|
|**since\_created**  <br>*optional*|[since\_created](#since\_created)|
|**state**  <br>*optional*|[state](#state)|
|**to\_site**  <br>*optional*|[to\_site](#to\_site)|
|**virtual\_path\_service\_type**  <br>*optional*|[virtual\_path\_service\_type](#virtual\_path\_service\_type)|
|**wan\_link\_congested**  <br>*optional*|[wan\_link\_congested](#wan\_link\_congested)|
|**worst\_jitter**  <br>*optional*|[worst\_jitter](#worst\_jitter)|


<a name="wan\_link\_congested"></a>
### wan\_link\_congested
WAN Link congested or not

*Type* : enum (YES, NO)


<a name="worst\_jitter"></a>
### worst\_jitter
Worst Jitter value for the virtual path service

*Type* : integer





