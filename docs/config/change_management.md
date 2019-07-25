# change\_management


<a name="overview"></a>
## Overview
This resource provides Change management status and operations related to Change Management. Use file\_upload\_to\_inbox API to upload files for Change Managment Operation. Use get\_package\_file to download packages created by Change Management, to be used in Local Change Management Operation.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* change\_management : Operations related to change\_management 




<a name="paths"></a>
## Paths

<a name="change\_management-post"></a>
### POST operation for change\_management
```
POST /change_management
```


#### Description
Cancel Change Management stage operation


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (cancel\_stage, verify, activate\_with\_rollback, stage, activate, clear\_inbox, migrate\_config, clear\_network\_staging, ignore\_incomplete)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[change\_management\_post\_success\_schema](#change\_management\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* change\_management


<a name="change\_management-get"></a>
### Get operation for change\_management
```
GET /change_management
```


#### Description
Use this operation to get Change Management status


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[change\_management\_response\_schema](#change\_management\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* change\_management




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="activate\_info"></a>
### activate\_info
Activation information

*Type* : string


<a name="change\_management\_delete\_success\_schema"></a>
### change\_management\_delete\_success\_schema

|Name|Schema|
|---|---|
|**change\_management**  <br>*optional*|[change\_management](#change\_management\_delete\_success\_schema-change\_management)|

<a name="change\_management\_delete\_success\_schema-change\_management"></a>
**change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="change\_management\_post\_success\_schema"></a>
### change\_management\_post\_success\_schema

|Name|Schema|
|---|---|
|**change\_management**  <br>*optional*|[change\_management](#change\_management\_post\_success\_schema-change\_management)|

<a name="change\_management\_post\_success\_schema-change\_management"></a>
**change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="change\_management\_put\_success\_schema"></a>
### change\_management\_put\_success\_schema

|Name|Schema|
|---|---|
|**change\_management**  <br>*optional*|[change\_management](#change\_management\_put\_success\_schema-change\_management)|

<a name="change\_management\_put\_success\_schema-change\_management"></a>
**change\_management**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="change\_management\_response\_schema"></a>
### change\_management\_response\_schema
*Type* : < [change\_management\_response\_schema](#change\_management\_response\_schema-inline) > array

<a name="change\_management\_response\_schema-inline"></a>
**change\_management\_response\_schema**

|Name|Schema|
|---|---|
|**activate\_info**  <br>*optional*|[activate\_info](#activate\_info)|
|**current\_config**  <br>*optional*|[current\_config](#current\_config)|
|**failure\_reason**  <br>*optional*|[failure\_reason](#failure\_reason)|
|**inbox\_files**  <br>*optional*|[inbox\_files](#inbox\_files)|
|**message**  <br>*optional*|[message](#message)|
|**network\_staged\_selected\_filename**  <br>*optional*|[network\_staged\_selected\_filename](#network\_staged\_selected\_filename)|
|**sites\_cm\_status**  <br>*optional*|[sites\_cm\_status](#sites\_cm\_status)|
|**state**  <br>*optional*|[state](#state)|
|**status**  <br>*optional*|[status](#status)|


<a name="current\_config"></a>
### current\_config
Name of the active config.

*Type* : string


<a name="failure\_reason"></a>
### failure\_reason
This key will be present in the response of verify action. This key indicates failure reason of verify action, if applicable.

*Type* : string


<a name="inbox\_files"></a>
### inbox\_files
Files in Change Management Inbox Directory

*Type* : string


<a name="message"></a>
### message
Detailed message about API execution.

*Type* : string


<a name="network\_staged\_selected\_filename"></a>
### network\_staged\_selected\_filename
Network staged config Filename

*Type* : string


<a name="sites\_cm\_status"></a>
### sites\_cm\_status
Change management status for Site

*Type* : < [sites\_cm\_status](#sites\_cm\_status-inline) > array

<a name="sites\_cm\_status-inline"></a>
**sites\_cm\_status**

|Name|Description|Schema|
|---|---|---|
|**active\_config**  <br>*optional*  <br>*read-only*|Active config time .|string|
|**active\_software**  <br>*optional*  <br>*read-only*|Currently active software of appliance .|string|
|**actual\_interruption\_ms**  <br>*optional*  <br>*read-only*|Actual Interruption time for activation|string|
|**appliance\_name**  <br>*optional*  <br>*read-only*|Name of Appliance|string|
|**expected\_interruption**  <br>*optional*  <br>*read-only*|Expected traffic interruption for activation|string|
|**expected\_sw\_revision**  <br>*optional*  <br>*read-only*|Expected software version on appliance|string|
|**model**  <br>*optional*  <br>*read-only*|Hardware model of appliance|string|
|**observed\_sw\_revision**  <br>*optional*  <br>*read-only*|Observed software version on appliance|string|
|**site\_name**  <br>*optional*  <br>*read-only*|Name of site|string|
|**staged\_config**  <br>*optional*  <br>*read-only*|Staged config time|string|
|**staged\_sw\_revision**  <br>*optional*  <br>*read-only*|Staged software version|string|
|**status**  <br>*optional*  <br>*read-only*|Status indicating connected state|string|
|**transfer\_state**  <br>*optional*  <br>*read-only*|transfer state of the change management process|string|


<a name="state"></a>
### state
Change Management State

*Type* : string


<a name="status"></a>
### status
This key indicates status of verify action.

*Type* : string





