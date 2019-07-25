# ethernet\_adapters


<a name="overview"></a>
## Overview
View or Modify the Network Adapters through this APIs


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* ethernet\_adapters : Operations related to ethernet\_adapters 




<a name="paths"></a>
## Paths

<a name="ethernet\_adapters-get"></a>
### Get operation for ethernet\_adapters
```
GET /ethernet_adapters
```


#### Description
Use this operation to list all the ethernet adapters


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ethernet\_adapters\_response\_schema](#ethernet\_adapters\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ethernet\_adapters


<a name="ethernet\_adapters-put"></a>
### PUT operation for ethernet\_adapters
```
PUT /ethernet_adapters
```


#### Description
Use this option to modify Autonegotiation, Speed and Duplex settings


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[ethernet\_adapters\_request\_schema](#ethernet\_adapters\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[ethernet\_adapters\_put\_success\_schema](#ethernet\_adapters\_put\_success\_schema)|
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

* ethernet\_adapters




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="autonegotiate"></a>
### autonegotiate
Specifies whether autonegotiation is on or off

*Type* : enum (ON, OFF)


<a name="duplex"></a>
### duplex
Full or Auto

*Type* : enum (FULL, AUTO)


<a name="ethernet\_adapters"></a>
### ethernet\_adapters

|Name|Schema|
|---|---|
|**autonegotiate**  <br>*optional*|[autonegotiate](#autonegotiate)|
|**duplex**  <br>*optional*|[duplex](#duplex)|
|**port\_name**  <br>*optional*|[port\_name](#port\_name)|
|**speed**  <br>*optional*|[speed](#speed)|


<a name="ethernet\_adapters\_delete\_success\_schema"></a>
### ethernet\_adapters\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_adapters**  <br>*optional*|[ethernet\_adapters](#ethernet\_adapters\_delete\_success\_schema-ethernet\_adapters)|

<a name="ethernet\_adapters\_delete\_success\_schema-ethernet\_adapters"></a>
**ethernet\_adapters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ethernet\_adapters\_post\_success\_schema"></a>
### ethernet\_adapters\_post\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_adapters**  <br>*optional*|[ethernet\_adapters](#ethernet\_adapters\_post\_success\_schema-ethernet\_adapters)|

<a name="ethernet\_adapters\_post\_success\_schema-ethernet\_adapters"></a>
**ethernet\_adapters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ethernet\_adapters\_put\_success\_schema"></a>
### ethernet\_adapters\_put\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_adapters**  <br>*optional*|[ethernet\_adapters](#ethernet\_adapters\_put\_success\_schema-ethernet\_adapters)|

<a name="ethernet\_adapters\_put\_success\_schema-ethernet\_adapters"></a>
**ethernet\_adapters**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ethernet\_adapters\_request\_schema"></a>
### ethernet\_adapters\_request\_schema

|Name|Schema|
|---|---|
|**ethernet\_adapters**  <br>*optional*|[ethernet\_adapters](#ethernet\_adapters)|


<a name="ethernet\_adapters\_response\_schema"></a>
### ethernet\_adapters\_response\_schema
*Type* : < [ethernet\_adapters\_response\_schema](#ethernet\_adapters\_response\_schema-inline) > array

<a name="ethernet\_adapters\_response\_schema-inline"></a>
**ethernet\_adapters\_response\_schema**

|Name|Schema|
|---|---|
|**autonegotiate**  <br>*optional*|[autonegotiate](#autonegotiate)|
|**duplex**  <br>*optional*|[duplex](#duplex)|
|**lsp\_state**  <br>*optional*|[lsp\_state](#lsp\_state)|
|**mac\_address**  <br>*optional*|[mac\_address](#mac\_address)|
|**port\_name**  <br>*optional*|[port\_name](#port\_name)|
|**port\_state**  <br>*optional*|[port\_state](#port\_state)|
|**speed**  <br>*optional*|[speed](#speed)|


<a name="lsp\_state"></a>
### lsp\_state
Specifies whether LSP state is up,down or admin\_down when LSP is configured

*Type* : string


<a name="mac\_address"></a>
### mac\_address
Specifies the MAC address of the port

*Type* : string


<a name="port\_name"></a>
### port\_name
Port of the appliance

*Type* : string


<a name="port\_state"></a>
### port\_state
Specifies link state whether it is UP or DOWN

*Type* : enum (ON, OFF)


<a name="speed"></a>
### speed
Specifies the configurable speed

*Type* : enum (10Mb/s, 100Mb/s, 1000Mb/s)





