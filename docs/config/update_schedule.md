# update\_schedule


<a name="overview"></a>
## Overview
This resource can be used to get software update schedule information and to update software update schedule.


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config/  
*Schemes* : HTTP


### Tags

* update\_schedule : Operations related to update\_schedule 




<a name="paths"></a>
## Paths

<a name="update\_schedule-get"></a>
### Get operation for update\_schedule
```
GET /update_schedule
```


#### Description
Use this operation to get software update schedule information.


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[update\_schedule\_response\_schema](#update\_schedule\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* update\_schedule


<a name="update\_schedule-put"></a>
### PUT operation for update\_schedule
```
PUT /update_schedule
```


#### Description
Use this operation to update software update schedule of a site.


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[update\_schedule\_request\_schema](#update\_schedule\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[update\_schedule\_put\_success\_schema](#update\_schedule\_put\_success\_schema)|
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

* update\_schedule




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="appliance\_type"></a>
### appliance\_type
Appliance type: primary or secondary appliance

*Type* : enum (primary, secondary)


<a name="message"></a>
### message
detailed messgae of command execution.

*Type* : string


<a name="repeat"></a>
### repeat
Repeat next update.

*Type* : integer


<a name="repeat\_unit"></a>
### repeat\_unit
Repeat duration unit.

*Type* : enum (hours, days, weeks, months)


<a name="schedule\_window"></a>
### schedule\_window
Update schedule window length in hours.

*Type* : integer


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="start\_date\_time"></a>
### start\_date\_time
Update schedule start date, time.

*Type* : string


<a name="update\_schedule"></a>
### update\_schedule

|Name|Schema|
|---|---|
|**appliance\_type**  <br>*optional*|[appliance\_type](#appliance\_type)|
|**repeat**  <br>*optional*|[repeat](#repeat)|
|**repeat\_unit**  <br>*optional*|[repeat\_unit](#repeat\_unit)|
|**schedule\_window**  <br>*optional*|[schedule\_window](#schedule\_window)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**start\_date\_time**  <br>*optional*|[start\_date\_time](#start\_date\_time)|


<a name="update\_schedule\_delete\_success\_schema"></a>
### update\_schedule\_delete\_success\_schema

|Name|Schema|
|---|---|
|**update\_schedule**  <br>*optional*|[update\_schedule](#update\_schedule\_delete\_success\_schema-update\_schedule)|

<a name="update\_schedule\_delete\_success\_schema-update\_schedule"></a>
**update\_schedule**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="update\_schedule\_post\_success\_schema"></a>
### update\_schedule\_post\_success\_schema

|Name|Schema|
|---|---|
|**update\_schedule**  <br>*optional*|[update\_schedule](#update\_schedule\_post\_success\_schema-update\_schedule)|

<a name="update\_schedule\_post\_success\_schema-update\_schedule"></a>
**update\_schedule**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="update\_schedule\_put\_success\_schema"></a>
### update\_schedule\_put\_success\_schema

|Name|Schema|
|---|---|
|**update\_schedule**  <br>*optional*|[update\_schedule](#update\_schedule\_put\_success\_schema-update\_schedule)|

<a name="update\_schedule\_put\_success\_schema-update\_schedule"></a>
**update\_schedule**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="update\_schedule\_request\_schema"></a>
### update\_schedule\_request\_schema

|Name|Schema|
|---|---|
|**update\_schedule**  <br>*optional*|[update\_schedule](#update\_schedule)|


<a name="update\_schedule\_response\_schema"></a>
### update\_schedule\_response\_schema
*Type* : < [update\_schedule\_response\_schema](#update\_schedule\_response\_schema-inline) > array

<a name="update\_schedule\_response\_schema-inline"></a>
**update\_schedule\_response\_schema**

|Name|Schema|
|---|---|
|**appliance\_type**  <br>*optional*|[appliance\_type](#appliance\_type)|
|**message**  <br>*optional*|[message](#message)|
|**repeat**  <br>*optional*|[repeat](#repeat)|
|**repeat\_unit**  <br>*optional*|[repeat\_unit](#repeat\_unit)|
|**schedule\_window**  <br>*optional*|[schedule\_window](#schedule\_window)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**start\_date\_time**  <br>*optional*|[start\_date\_time](#start\_date\_time)|





