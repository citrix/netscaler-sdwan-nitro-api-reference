# sim\_pin\_summary


<a name="overview"></a>
## Overview
This resource is to get SIM PIN summary


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* sim\_pin\_summary : Operations related to sim\_pin\_summary 




<a name="paths"></a>
## Paths

<a name="sim\_pin\_summary-get"></a>
### Get operation for sim\_pin\_summary
```
GET /sim_pin_summary
```


#### Description
Use this operation to get the Mobile Broadband SIM PIN Settings from SD-WAN Appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sim\_pin\_summary\_response\_schema](#sim\_pin\_summary\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sim\_pin\_summary




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="pin\_state"></a>
### pin\_state
SIM PIN state

*Type* : string


<a name="pin\_tries"></a>
### pin\_tries
Number of PIN tries remaining

*Type* : string


<a name="puk\_tries"></a>
### puk\_tries
Number of PUK tries remaining

*Type* : string


<a name="sim\_pin\_summary\_delete\_success\_schema"></a>
### sim\_pin\_summary\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_summary**  <br>*optional*|[sim\_pin\_summary](#sim\_pin\_summary\_delete\_success\_schema-sim\_pin\_summary)|

<a name="sim\_pin\_summary\_delete\_success\_schema-sim\_pin\_summary"></a>
**sim\_pin\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sim\_pin\_summary\_post\_success\_schema"></a>
### sim\_pin\_summary\_post\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_summary**  <br>*optional*|[sim\_pin\_summary](#sim\_pin\_summary\_post\_success\_schema-sim\_pin\_summary)|

<a name="sim\_pin\_summary\_post\_success\_schema-sim\_pin\_summary"></a>
**sim\_pin\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sim\_pin\_summary\_put\_success\_schema"></a>
### sim\_pin\_summary\_put\_success\_schema

|Name|Schema|
|---|---|
|**sim\_pin\_summary**  <br>*optional*|[sim\_pin\_summary](#sim\_pin\_summary\_put\_success\_schema-sim\_pin\_summary)|

<a name="sim\_pin\_summary\_put\_success\_schema-sim\_pin\_summary"></a>
**sim\_pin\_summary**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sim\_pin\_summary\_response\_schema"></a>
### sim\_pin\_summary\_response\_schema
*Type* : < [sim\_pin\_summary\_response\_schema](#sim\_pin\_summary\_response\_schema-inline) > array

<a name="sim\_pin\_summary\_response\_schema-inline"></a>
**sim\_pin\_summary\_response\_schema**

|Name|Schema|
|---|---|
|**pin\_state**  <br>*optional*|[pin\_state](#pin\_state)|
|**pin\_tries**  <br>*optional*|[pin\_tries](#pin\_tries)|
|**puk\_tries**  <br>*optional*|[puk\_tries](#puk\_tries)|





