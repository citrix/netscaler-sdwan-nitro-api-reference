# observed\_protocols


<a name="overview"></a>
## Overview
This resource provides details of all the observed protocols.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* observed\_protocols : Operations related to observed\_protocols 




<a name="paths"></a>
## Paths

<a name="observed\_protocols-get"></a>
### Get operation for observed\_protocols
```
GET /observed_protocols
```


#### Description
Use this operation to get Observed Protocol statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[observed\_protocols\_response\_schema](#observed\_protocols\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* observed\_protocols




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="observed\_protocols\_delete\_success\_schema"></a>
### observed\_protocols\_delete\_success\_schema

|Name|Schema|
|---|---|
|**observed\_protocols**  <br>*optional*|[observed\_protocols](#observed\_protocols\_delete\_success\_schema-observed\_protocols)|

<a name="observed\_protocols\_delete\_success\_schema-observed\_protocols"></a>
**observed\_protocols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="observed\_protocols\_post\_success\_schema"></a>
### observed\_protocols\_post\_success\_schema

|Name|Schema|
|---|---|
|**observed\_protocols**  <br>*optional*|[observed\_protocols](#observed\_protocols\_post\_success\_schema-observed\_protocols)|

<a name="observed\_protocols\_post\_success\_schema-observed\_protocols"></a>
**observed\_protocols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="observed\_protocols\_put\_success\_schema"></a>
### observed\_protocols\_put\_success\_schema

|Name|Schema|
|---|---|
|**observed\_protocols**  <br>*optional*|[observed\_protocols](#observed\_protocols\_put\_success\_schema-observed\_protocols)|

<a name="observed\_protocols\_put\_success\_schema-observed\_protocols"></a>
**observed\_protocols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="observed\_protocols\_response\_schema"></a>
### observed\_protocols\_response\_schema
*Type* : < [observed\_protocols\_response\_schema](#observed\_protocols\_response\_schema-inline) > array

<a name="observed\_protocols\_response\_schema-inline"></a>
**observed\_protocols\_response\_schema**

|Name|Schema|
|---|---|
|**port**  <br>*optional*|[port](#port)|
|**protocol**  <br>*optional*|[protocol](#protocol)|
|**rule**  <br>*optional*|[rule](#rule)|
|**rule\_group**  <br>*optional*|[rule\_group](#rule\_group)|
|**service\_instance**  <br>*optional*|[service\_instance](#service\_instance)|
|**service\_type**  <br>*optional*|[service\_type](#service\_type)|
|**wan\_egress\_bytes**  <br>*optional*|[wan\_egress\_bytes](#wan\_egress\_bytes)|
|**wan\_egress\_kbps**  <br>*optional*|[wan\_egress\_kbps](#wan\_egress\_kbps)|
|**wan\_egress\_packets**  <br>*optional*|[wan\_egress\_packets](#wan\_egress\_packets)|
|**wan\_ingress\_bytes**  <br>*optional*|[wan\_ingress\_bytes](#wan\_ingress\_bytes)|
|**wan\_ingress\_kbps**  <br>*optional*|[wan\_ingress\_kbps](#wan\_ingress\_kbps)|
|**wan\_ingress\_packets**  <br>*optional*|[wan\_ingress\_packets](#wan\_ingress\_packets)|


<a name="port"></a>
### port
Port

*Type* : string


<a name="protocol"></a>
### protocol
Name of the protocol

*Type* : enum (UNDEFINED, DISABLED, DEAD, BAD, GOOD)


<a name="rule"></a>
### rule
Name of the Rule

*Type* : string


<a name="rule\_group"></a>
### rule\_group
Name of the rule group

*Type* : string


<a name="service\_instance"></a>
### service\_instance
Service instance

*Type* : integer


<a name="service\_type"></a>
### service\_type
Service type

*Type* : string


<a name="wan\_egress\_bytes"></a>
### wan\_egress\_bytes
Bytes transfered WAN to LAN

*Type* : integer


<a name="wan\_egress\_kbps"></a>
### wan\_egress\_kbps
Transfer rate WAN to LAN kbps

*Type* : number


<a name="wan\_egress\_packets"></a>
### wan\_egress\_packets
Packets transfered WAN to LAN

*Type* : integer


<a name="wan\_ingress\_bytes"></a>
### wan\_ingress\_bytes
Bytes transfered LAN to WAN

*Type* : integer


<a name="wan\_ingress\_kbps"></a>
### wan\_ingress\_kbps
Transfer rate LAN to WAN kbps

*Type* : number


<a name="wan\_ingress\_packets"></a>
### wan\_ingress\_packets
Packets transfered LAN to WAN

*Type* : integer





