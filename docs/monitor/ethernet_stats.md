# ethernet\_stats


<a name="overview"></a>
## Overview
API to get ethernet ports information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* ethernet\_stats : Operations related to ethernet\_stats 




<a name="paths"></a>
## Paths

<a name="ethernet\_stats-get"></a>
### Get operation for ethernet\_stats
```
GET /ethernet_stats
```


#### Description
Use this operation to get ethernet ports


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[ethernet\_stats\_response\_schema](#ethernet\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* ethernet\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bytes\_received"></a>
### bytes\_received
Total bytes received

*Type* : integer


<a name="bytes\_sent"></a>
### bytes\_sent
Total bytes sent

*Type* : integer


<a name="errors"></a>
### errors
Errors

*Type* : integer


<a name="ethernet\_stats\_delete\_success\_schema"></a>
### ethernet\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_stats**  <br>*optional*|[ethernet\_stats](#ethernet\_stats\_delete\_success\_schema-ethernet\_stats)|

<a name="ethernet\_stats\_delete\_success\_schema-ethernet\_stats"></a>
**ethernet\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="ethernet\_stats\_post\_success\_schema"></a>
### ethernet\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_stats**  <br>*optional*|[ethernet\_stats](#ethernet\_stats\_post\_success\_schema-ethernet\_stats)|

<a name="ethernet\_stats\_post\_success\_schema-ethernet\_stats"></a>
**ethernet\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="ethernet\_stats\_put\_success\_schema"></a>
### ethernet\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**ethernet\_stats**  <br>*optional*|[ethernet\_stats](#ethernet\_stats\_put\_success\_schema-ethernet\_stats)|

<a name="ethernet\_stats\_put\_success\_schema-ethernet\_stats"></a>
**ethernet\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="ethernet\_stats\_response\_schema"></a>
### ethernet\_stats\_response\_schema
*Type* : < [ethernet\_stats\_response\_schema](#ethernet\_stats\_response\_schema-inline) > array

<a name="ethernet\_stats\_response\_schema-inline"></a>
**ethernet\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**bytes\_received**  <br>*optional*|[bytes\_received](#bytes\_received)|
|**bytes\_sent**  <br>*optional*|[bytes\_sent](#bytes\_sent)|
|**errors**  <br>*optional*|[errors](#errors)|
|**frames\_received**  <br>*optional*|[frames\_received](#frames\_received)|
|**frames\_sent**  <br>*optional*|[frames\_sent](#frames\_sent)|
|**link\_state**  <br>*optional*|[link\_state](#link\_state)|
|**port\_num**  <br>*optional*|[port\_num](#port\_num)|


<a name="frames\_received"></a>
### frames\_received
The number of frames received

*Type* : integer


<a name="frames\_sent"></a>
### frames\_sent
The number of frames sent

*Type* : integer


<a name="link\_state"></a>
### link\_state
The Link State

*Type* : string


<a name="port\_num"></a>
### port\_num
Ethernet Port

*Type* : string





