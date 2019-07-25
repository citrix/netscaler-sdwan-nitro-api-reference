# license\_info


<a name="overview"></a>
## Overview
License configuration state


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* license\_info : Operations related to license\_info 




<a name="paths"></a>
## Paths

<a name="license\_info-get"></a>
### Get operation for license\_info
```
GET /license_info
```


#### Description
Use this operation to get the current license configuration state


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[license\_info\_response\_schema](#license\_info\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* license\_info




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="action\_required"></a>
### action\_required
Actions required around license like expired-license, bad remote server status

*Type* : string


<a name="license\_expiry"></a>
### license\_expiry
Expiry date of the current installed license

*Type* : string


<a name="license\_info\_delete\_success\_schema"></a>
### license\_info\_delete\_success\_schema

|Name|Schema|
|---|---|
|**license\_info**  <br>*optional*|[license\_info](#license\_info\_delete\_success\_schema-license\_info)|

<a name="license\_info\_delete\_success\_schema-license\_info"></a>
**license\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="license\_info\_post\_success\_schema"></a>
### license\_info\_post\_success\_schema

|Name|Schema|
|---|---|
|**license\_info**  <br>*optional*|[license\_info](#license\_info\_post\_success\_schema-license\_info)|

<a name="license\_info\_post\_success\_schema-license\_info"></a>
**license\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="license\_info\_put\_success\_schema"></a>
### license\_info\_put\_success\_schema

|Name|Schema|
|---|---|
|**license\_info**  <br>*optional*|[license\_info](#license\_info\_put\_success\_schema-license\_info)|

<a name="license\_info\_put\_success\_schema-license\_info"></a>
**license\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="license\_info\_response\_schema"></a>
### license\_info\_response\_schema
*Type* : < [license\_info\_response\_schema](#license\_info\_response\_schema-inline) > array

<a name="license\_info\_response\_schema-inline"></a>
**license\_info\_response\_schema**

|Name|Schema|
|---|---|
|**action\_required**  <br>*optional*|[action\_required](#action\_required)|
|**license\_expiry**  <br>*optional*|[license\_expiry](#license\_expiry)|
|**license\_location**  <br>*optional*|[license\_location](#license\_location)|
|**license\_type**  <br>*optional*|[license\_type](#license\_type)|
|**local\_license\_server\_hostid**  <br>*optional*|[local\_license\_server\_hostid](#local\_license\_server\_hostid)|
|**maintenance\_expiry**  <br>*optional*|[maintenance\_expiry](#maintenance\_expiry)|
|**max\_bw**  <br>*optional*|[max\_bw](#max\_bw)|
|**model**  <br>*optional*|[model](#model)|
|**remote\_license\_ip**  <br>*optional*|[remote\_license\_ip](#remote\_license\_ip)|
|**remote\_license\_port**  <br>*optional*|[remote\_license\_port](#remote\_license\_port)|
|**remote\_license\_status**  <br>*optional*|[remote\_license\_status](#remote\_license\_status)|
|**remote\_server\_status**  <br>*optional*|[remote\_server\_status](#remote\_server\_status)|
|**state**  <br>*optional*|[state](#state)|
|**system\_platform**  <br>*optional*|[system\_platform](#system\_platform)|


<a name="license\_location"></a>
### license\_location
States whether local license or remote license is applied

*Type* : string


<a name="license\_type"></a>
### license\_type
Describes type of license eg. retail, evaluation etc

*Type* : string


<a name="local\_license\_server\_hostid"></a>
### local\_license\_server\_hostid
HostId to be used while requesting license (local)

*Type* : string


<a name="maintenance\_expiry"></a>
### maintenance\_expiry
Maintenance expiry date by the current installed license

*Type* : string


<a name="max\_bw"></a>
### max\_bw
Max bandwidth installed from license

*Type* : string


<a name="model"></a>
### model
Model installed from license

*Type* : string


<a name="remote\_license\_ip"></a>
### remote\_license\_ip
Remote license server IP

*Type* : string


<a name="remote\_license\_port"></a>
### remote\_license\_port
Remote license server port

*Type* : string


<a name="remote\_license\_status"></a>
### remote\_license\_status
Remote license installation status

*Type* : string


<a name="remote\_server\_status"></a>
### remote\_server\_status
Remote license server connectivity status

*Type* : string


<a name="state"></a>
### state
Licensed/Unlicensed

*Type* : string


<a name="system\_platform"></a>
### system\_platform
System platform of device

*Type* : string





