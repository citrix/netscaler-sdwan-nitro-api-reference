# management\_ip


<a name="overview"></a>
## Overview
Get/Set management IP


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* management\_ip : Operations related to management\_ip 




<a name="paths"></a>
## Paths

<a name="management\_ip-get"></a>
### Get operation for management\_ip
```
GET /management_ip
```


#### Description
Get Management IP Info.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[management\_ip\_response\_schema](#management\_ip\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* management\_ip


<a name="management\_ip-put"></a>
### PUT operation for management\_ip
```
PUT /management_ip
```


#### Description
Use this operation to change Management IP of SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[management\_ip\_request\_schema](#management\_ip\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[management\_ip\_put\_success\_schema](#management\_ip\_put\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* management\_ip




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="gateway"></a>
### gateway
Gateway IP of Management IP

*Type* : string


<a name="ip\_address"></a>
### ip\_address
Management IP Of System

*Type* : string


<a name="management\_ip"></a>
### management\_ip

|Name|Schema|
|---|---|
|**gateway**  <br>*optional*|[gateway](#gateway)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**netmask**  <br>*optional*|[netmask](#netmask)|


<a name="management\_ip\_delete\_success\_schema"></a>
### management\_ip\_delete\_success\_schema

|Name|Schema|
|---|---|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip\_delete\_success\_schema-management\_ip)|

<a name="management\_ip\_delete\_success\_schema-management\_ip"></a>
**management\_ip**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="management\_ip\_post\_success\_schema"></a>
### management\_ip\_post\_success\_schema

|Name|Schema|
|---|---|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip\_post\_success\_schema-management\_ip)|

<a name="management\_ip\_post\_success\_schema-management\_ip"></a>
**management\_ip**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="management\_ip\_put\_success\_schema"></a>
### management\_ip\_put\_success\_schema

|Name|Schema|
|---|---|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip\_put\_success\_schema-management\_ip)|

<a name="management\_ip\_put\_success\_schema-management\_ip"></a>
**management\_ip**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="management\_ip\_request\_schema"></a>
### management\_ip\_request\_schema

|Name|Schema|
|---|---|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip)|


<a name="management\_ip\_response\_schema"></a>
### management\_ip\_response\_schema
*Type* : < [management\_ip\_response\_schema](#management\_ip\_response\_schema-inline) > array

<a name="management\_ip\_response\_schema-inline"></a>
**management\_ip\_response\_schema**

|Name|Schema|
|---|---|
|**gateway**  <br>*optional*|[gateway](#gateway)|
|**ip\_address**  <br>*optional*|[ip\_address](#ip\_address)|
|**netmask**  <br>*optional*|[netmask](#netmask)|


<a name="netmask"></a>
### netmask
Subnet mask of Management IP

*Type* : string





