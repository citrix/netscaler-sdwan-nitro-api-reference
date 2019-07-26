# appliance\_ha\_status


<a name="overview"></a>
## Overview
This resource provides the appliance is in active or passive. This is an Internal API used by SD-WAN Center to find the active appliance


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* appliance\_ha\_status : Operations related to appliance\_ha\_status 




<a name="paths"></a>
## Paths

<a name="appliance\_ha\_status-get"></a>
### Get operation for appliance\_ha\_status
```
GET /appliance_ha_status
```


#### Description
Use this operation to get the appliance status.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[appliance\_ha\_status\_response\_schema](#appliance\_ha\_status\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* appliance\_ha\_status




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_ha\_status\_delete\_success\_schema"></a>
### appliance\_ha\_status\_delete\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_ha\_status**  <br>*optional*|[appliance\_ha\_status](#appliance\_ha\_status\_delete\_success\_schema-appliance\_ha\_status)|

<a name="appliance\_ha\_status\_delete\_success\_schema-appliance\_ha\_status"></a>
**appliance\_ha\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="appliance\_ha\_status\_post\_success\_schema"></a>
### appliance\_ha\_status\_post\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_ha\_status**  <br>*optional*|[appliance\_ha\_status](#appliance\_ha\_status\_post\_success\_schema-appliance\_ha\_status)|

<a name="appliance\_ha\_status\_post\_success\_schema-appliance\_ha\_status"></a>
**appliance\_ha\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="appliance\_ha\_status\_put\_success\_schema"></a>
### appliance\_ha\_status\_put\_success\_schema

|Name|Schema|
|---|---|
|**appliance\_ha\_status**  <br>*optional*|[appliance\_ha\_status](#appliance\_ha\_status\_put\_success\_schema-appliance\_ha\_status)|

<a name="appliance\_ha\_status\_put\_success\_schema-appliance\_ha\_status"></a>
**appliance\_ha\_status**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="appliance\_ha\_status\_response\_schema"></a>
### appliance\_ha\_status\_response\_schema
*Type* : < [appliance\_ha\_status\_response\_schema](#appliance\_ha\_status\_response\_schema-inline) > array

<a name="appliance\_ha\_status\_response\_schema-inline"></a>
**appliance\_ha\_status\_response\_schema**

|Name|Schema|
|---|---|
|**is\_active**  <br>*optional*|[is\_active](#is\_active)|
|**status**  <br>*optional*|[status](#status)|


<a name="is\_active"></a>
### is\_active
If it's active, then is\_active will be 1 else it will be 0

*Type* : boolean


<a name="status"></a>
### status
response status

*Type* : string





