# system\_options


<a name="overview"></a>
## Overview
System-Options


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* system\_options : Operations related to system\_options 




<a name="paths"></a>
## Paths

<a name="system\_options-post"></a>
### POST operation for system\_options
```
POST /system_options
```


#### Description
Reboots the SD-WAN Appliance


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (reboot, configuration\_reset, factory\_reset)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[system\_options\_post\_success\_schema](#system\_options\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* system\_options


<a name="system\_options-get"></a>
### Get operation for system\_options
```
GET /system_options
```


#### Description
Get System Information.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[system\_options\_response\_schema](#system\_options\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* system\_options




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_mode"></a>
### appliance\_mode
Appliance Mode

*Type* : enum (MCN, Client)


<a name="appliance\_uptime"></a>
### appliance\_uptime
Uptime of the appliance (Will be shown once Virtual WAN is enabled)

*Type* : string


<a name="license\_state"></a>
### license\_state
The appliance is licensed or not

*Type* : boolean


<a name="management\_ip"></a>
### management\_ip
Management IP Of System

*Type* : string


<a name="model"></a>
### model
Model Of the system

*Type* : string


<a name="os\_ver"></a>
### os\_ver
OS Version

*Type* : string


<a name="product"></a>
### product
Product name.

*Type* : string


<a name="serial\_no"></a>
### serial\_no
Serial Number of the system

*Type* : string


<a name="service\_uptime"></a>
### service\_uptime
Service up time. Will be shown once Virtual WAN is Enabled

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="sw\_version"></a>
### sw\_version
S/W Version The Site is currently running on

*Type* : string


<a name="system\_options\_delete\_success\_schema"></a>
### system\_options\_delete\_success\_schema

|Name|Schema|
|---|---|
|**system\_options**  <br>*optional*|[system\_options](#system\_options\_delete\_success\_schema-system\_options)|

<a name="system\_options\_delete\_success\_schema-system\_options"></a>
**system\_options**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="system\_options\_post\_success\_schema"></a>
### system\_options\_post\_success\_schema

|Name|Schema|
|---|---|
|**system\_options**  <br>*optional*|[system\_options](#system\_options\_post\_success\_schema-system\_options)|

<a name="system\_options\_post\_success\_schema-system\_options"></a>
**system\_options**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="system\_options\_put\_success\_schema"></a>
### system\_options\_put\_success\_schema

|Name|Schema|
|---|---|
|**system\_options**  <br>*optional*|[system\_options](#system\_options\_put\_success\_schema-system\_options)|

<a name="system\_options\_put\_success\_schema-system\_options"></a>
**system\_options**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="system\_options\_response\_schema"></a>
### system\_options\_response\_schema
*Type* : < [system\_options\_response\_schema](#system\_options\_response\_schema-inline) > array

<a name="system\_options\_response\_schema-inline"></a>
**system\_options\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_mode**  <br>*optional*|[appliance\_mode](#appliance\_mode)|
|**appliance\_uptime**  <br>*optional*|[appliance\_uptime](#appliance\_uptime)|
|**license\_state**  <br>*optional*|[license\_state](#license\_state)|
|**management\_ip**  <br>*optional*|[management\_ip](#management\_ip)|
|**model**  <br>*optional*|[model](#model)|
|**os\_ver**  <br>*optional*|[os\_ver](#os\_ver)|
|**product**  <br>*optional*|[product](#product)|
|**serial\_no**  <br>*optional*|[serial\_no](#serial\_no)|
|**service\_uptime**  <br>*optional*|[service\_uptime](#service\_uptime)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**sw\_version**  <br>*optional*|[sw\_version](#sw\_version)|
|**system\_time**  <br>*optional*|[system\_time](#system\_time)|


<a name="system\_time"></a>
### system\_time
Shows the current time of system

*Type* : string





