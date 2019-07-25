# sites\_cm\_info


<a name="overview"></a>
## Overview
This resource provides Change management info of the sites.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* sites\_cm\_info : Operations related to sites\_cm\_info 




<a name="paths"></a>
## Paths

<a name="sites\_cm\_info-get"></a>
### Get operation for sites\_cm\_info
```
GET /sites_cm_info
```


#### Description
Use this operation to get Change Management status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sites\_cm\_info\_response\_schema](#sites\_cm\_info\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites\_cm\_info




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="active\_config"></a>
### active\_config
Active config time .

*Type* : string


<a name="active\_software"></a>
### active\_software
Currently active software of appliance .

*Type* : string


<a name="actual\_interruption\_ms"></a>
### actual\_interruption\_ms
Actual Interruption time for activation

*Type* : string


<a name="appliance\_name"></a>
### appliance\_name
Name of Appliance

*Type* : string


<a name="expected\_interruption"></a>
### expected\_interruption
Expected traffic interruption for activation

*Type* : string


<a name="expected\_sw\_revision"></a>
### expected\_sw\_revision
Expected software version on appliance

*Type* : string


<a name="model"></a>
### model
Hardware model of appliance

*Type* : string


<a name="observed\_sw\_revision"></a>
### observed\_sw\_revision
Observed software version on appliance

*Type* : string


<a name="site\_name"></a>
### site\_name
Name of site

*Type* : string


<a name="sites\_cm\_info\_delete\_success\_schema"></a>
### sites\_cm\_info\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sites\_cm\_info**  <br>*optional*|[sites\_cm\_info](#sites\_cm\_info\_delete\_success\_schema-sites\_cm\_info)|

<a name="sites\_cm\_info\_delete\_success\_schema-sites\_cm\_info"></a>
**sites\_cm\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sites\_cm\_info\_post\_success\_schema"></a>
### sites\_cm\_info\_post\_success\_schema

|Name|Schema|
|---|---|
|**sites\_cm\_info**  <br>*optional*|[sites\_cm\_info](#sites\_cm\_info\_post\_success\_schema-sites\_cm\_info)|

<a name="sites\_cm\_info\_post\_success\_schema-sites\_cm\_info"></a>
**sites\_cm\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sites\_cm\_info\_put\_success\_schema"></a>
### sites\_cm\_info\_put\_success\_schema

|Name|Schema|
|---|---|
|**sites\_cm\_info**  <br>*optional*|[sites\_cm\_info](#sites\_cm\_info\_put\_success\_schema-sites\_cm\_info)|

<a name="sites\_cm\_info\_put\_success\_schema-sites\_cm\_info"></a>
**sites\_cm\_info**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sites\_cm\_info\_response\_schema"></a>
### sites\_cm\_info\_response\_schema
*Type* : < [sites\_cm\_info\_response\_schema](#sites\_cm\_info\_response\_schema-inline) > array

<a name="sites\_cm\_info\_response\_schema-inline"></a>
**sites\_cm\_info\_response\_schema**

|Name|Schema|
|---|---|
|**active\_config**  <br>*optional*|[active\_config](#active\_config)|
|**active\_software**  <br>*optional*|[active\_software](#active\_software)|
|**actual\_interruption\_ms**  <br>*optional*|[actual\_interruption\_ms](#actual\_interruption\_ms)|
|**appliance\_name**  <br>*optional*|[appliance\_name](#appliance\_name)|
|**expected\_interruption**  <br>*optional*|[expected\_interruption](#expected\_interruption)|
|**expected\_sw\_revision**  <br>*optional*|[expected\_sw\_revision](#expected\_sw\_revision)|
|**model**  <br>*optional*|[model](#model)|
|**observed\_sw\_revision**  <br>*optional*|[observed\_sw\_revision](#observed\_sw\_revision)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**staged\_config**  <br>*optional*|[staged\_config](#staged\_config)|
|**staged\_sw\_revision**  <br>*optional*|[staged\_sw\_revision](#staged\_sw\_revision)|
|**status**  <br>*optional*|[status](#status)|
|**transfer\_state**  <br>*optional*|[transfer\_state](#transfer\_state)|


<a name="staged\_config"></a>
### staged\_config
Staged config time

*Type* : string


<a name="staged\_sw\_revision"></a>
### staged\_sw\_revision
Staged software version

*Type* : string


<a name="status"></a>
### status
Status indicating connected state

*Type* : string


<a name="transfer\_state"></a>
### transfer\_state
transfer state of the change management process

*Type* : string





