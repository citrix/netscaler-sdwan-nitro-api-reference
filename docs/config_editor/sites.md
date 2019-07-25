# sites


<a name="overview"></a>
## Overview
API to add, modify, delete, and get sites.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* sites : Operations related to sites 




<a name="paths"></a>
## Paths

<a name="sites-post"></a>
### POST operation for sites
```
POST /sites
```


#### Description
Use this operation to add site


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[sites\_post\_success\_schema](#sites\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites


<a name="sites-get"></a>
### Get operation for sites
```
GET /sites
```


#### Description
Use this operation to get the list of sites


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sites\_response\_schema](#sites\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites


<a name="sites-put"></a>
### PUT operation for sites
```
PUT /sites
```


#### Description
Use this operation to modify site


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[sites\_request\_schema](#sites\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[sites\_put\_success\_schema](#sites\_put\_success\_schema)|
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

* sites


<a name="sites-deletepathparam-delete"></a>
### DELETE operation for sites
```
DELETE /sites/{deletePathParam}
```


#### Description
Use this operation to delete a site


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[sites\_delete\_success\_schema](#sites\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sites




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="mode"></a>
### mode
Operating mode of this site

*Type* : enum (primary\_mcn, secondary\_mcn, primary\_rcn, secondary\_rcn, client)


<a name="model"></a>
### model
site model

*Type* : enum (cb210, cb400, cb410, cb1000, cb1100, cb2000, cb2100, cb4000, cb4100, cb5100, cb6100, cbvpx, cbvpxl)


<a name="package\_name"></a>
### package\_name
Config package name using which the site API operation should be performed.

*Type* : string


<a name="persist\_ucast\_refresh\_time\_ms"></a>
### persist\_ucast\_refresh\_time\_ms
Gateway ARP Timer: (ms)

*Type* : integer


<a name="region"></a>
### region
Region to which the site belongs to

*Type* : string


<a name="secure\_key"></a>
### secure\_key
Hexadecimal secure key used for encryption and membership verification in the Virtual WAN network. This field is optional. If the value is not provided, API generates the secure key.

*Type* : string


<a name="site\_location"></a>
### site\_location
Site location.

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="sites"></a>
### sites

|Name|Schema|
|---|---|
|**mode**  <br>*optional*|[mode](#mode)|
|**model**  <br>*optional*|[model](#model)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persist\_ucast\_refresh\_time\_ms**  <br>*optional*|[persist\_ucast\_refresh\_time\_ms](#persist\_ucast\_refresh\_time\_ms)|
|**region**  <br>*optional*|[region](#region)|
|**secure\_key**  <br>*optional*|[secure\_key](#secure\_key)|
|**site\_location**  <br>*optional*|[site\_location](#site\_location)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**user\_ucast\_refresh\_time\_ms**  <br>*optional*|[user\_ucast\_refresh\_time\_ms](#user\_ucast\_refresh\_time\_ms)|


<a name="sites\_delete\_success\_schema"></a>
### sites\_delete\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_delete\_success\_schema-sites)|

<a name="sites\_delete\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="sites\_post\_success\_schema"></a>
### sites\_post\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_post\_success\_schema-sites)|

<a name="sites\_post\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="sites\_put\_success\_schema"></a>
### sites\_put\_success\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites\_put\_success\_schema-sites)|

<a name="sites\_put\_success\_schema-sites"></a>
**sites**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="sites\_request\_schema"></a>
### sites\_request\_schema

|Name|Schema|
|---|---|
|**sites**  <br>*optional*|[sites](#sites)|


<a name="sites\_response\_schema"></a>
### sites\_response\_schema
*Type* : < [sites\_response\_schema](#sites\_response\_schema-inline) > array

<a name="sites\_response\_schema-inline"></a>
**sites\_response\_schema**

|Name|Schema|
|---|---|
|**mode**  <br>*optional*|[mode](#mode)|
|**model**  <br>*optional*|[model](#model)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**persist\_ucast\_refresh\_time\_ms**  <br>*optional*|[persist\_ucast\_refresh\_time\_ms](#persist\_ucast\_refresh\_time\_ms)|
|**region**  <br>*optional*|[region](#region)|
|**secure\_key**  <br>*optional*|[secure\_key](#secure\_key)|
|**site\_location**  <br>*optional*|[site\_location](#site\_location)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**user\_ucast\_refresh\_time\_ms**  <br>*optional*|[user\_ucast\_refresh\_time\_ms](#user\_ucast\_refresh\_time\_ms)|


<a name="user\_ucast\_refresh\_time\_ms"></a>
### user\_ucast\_refresh\_time\_ms
Host ARP Timer: (ms)

*Type* : integer





