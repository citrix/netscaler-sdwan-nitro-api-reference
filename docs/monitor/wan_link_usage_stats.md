# wan\_link\_usage\_stats


<a name="overview"></a>
## Overview
This resource provides WAN Links Usage Statistics


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* wan\_link\_usage\_stats : Operations related to wan\_link\_usage\_stats 




<a name="paths"></a>
## Paths

<a name="wan\_link\_usage\_stats-get"></a>
### Get operation for wan\_link\_usage\_stats
```
GET /wan_link_usage_stats
```


#### Description
Use this operation to get WAN Links Usage statistics. Filter and Pagination are supported  for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_link\_usage\_stats\_response\_schema](#wan\_link\_usage\_stats\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_link\_usage\_stats




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="local\_wan\_links"></a>
### local\_wan\_links
Local WAN Links Statistics

*Type* : < [local\_wan\_links](#local\_wan\_links-inline) > array

<a name="local\_wan\_links-inline"></a>
**local\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**congestion**  <br>*optional*  <br>*read-only*|Congestion in the WAN Link|enum (YES, NO, N/A)|
|**delta\_kb**  <br>*optional*  <br>*read-only*|Delta KB in Local WAN Link|number|
|**delta\_packets**  <br>*optional*  <br>*read-only*|Delta packets transferred|number|
|**direction**  <br>*optional*  <br>*read-only*|Direction|enum (Send, Recv)|
|**kbps**  <br>*optional*  <br>*read-only*|kilobytes per second|number|
|**packets**  <br>*optional*  <br>*read-only*|Total packets transferred|integer|
|**permitted\_kbps**  <br>*optional*  <br>*read-only*|kilobytes per second|number|
|**wan\_link\_name**  <br>*optional*  <br>*read-only*|WAN Link name|string|


<a name="on\_demand\_wan\_link\_usage"></a>
### on\_demand\_wan\_link\_usage
On-demand WAN Links Statistics

*Type* : < [on\_demand\_wan\_link\_usage](#on\_demand\_wan\_link\_usage-inline) > array

<a name="on\_demand\_wan\_link\_usage-inline"></a>
**on\_demand\_wan\_link\_usage**

|Name|Description|Schema|
|---|---|---|
|**configured**  <br>*optional*  <br>*read-only*|Whether the WAN Links is configured|string|
|**current\_allowed\_bw\_kbps**  <br>*optional*  <br>*read-only*|Current allowed bandwidth in kbps|number|
|**in\_use**  <br>*optional*  <br>*read-only*|Whether the WAN Link is in use|number|
|**maximum\_allowed\_bw\_kbps**  <br>*optional*  <br>*read-only*|Maximum allowed banddwidth in kbps|number|
|**minimum\_acceptable\_bw\_kbps**  <br>*optional*  <br>*read-only*|Minimum acceptable bandwidth in kbps|number|
|**standby\_priority**  <br>*optional*  <br>*read-only*|Standby Priority|string|
|**virtual\_path\_available\_bandwidth\_kbps**  <br>*optional*  <br>*read-only*|Virtual Path Available Bandwidth in kbps|number|
|**virtual\_path\_name**  <br>*optional*  <br>*read-only*|The name of the Virtual Path|string|
|**virtual\_path\_on\_demand\_bandwidth\_limit\_kbps**  <br>*optional*  <br>*read-only*|Virtual Path On Demand Bandwidth Limit in kbps|number|
|**wan\_link\_name**  <br>*optional*  <br>*read-only*|WAN Link name|string|


<a name="remote\_wan\_links"></a>
### remote\_wan\_links
Remote WAN Links Statistics

*Type* : < [remote\_wan\_links](#remote\_wan\_links-inline) > array

<a name="remote\_wan\_links-inline"></a>
**remote\_wan\_links**

|Name|Description|Schema|
|---|---|---|
|**congestion**  <br>*optional*  <br>*read-only*|Congestion in the WAN Link|enum (YES, NO, N/A)|
|**direction**  <br>*optional*  <br>*read-only*|Direction|enum (Send, Recv)|
|**service**  <br>*optional*  <br>*read-only*|The Service name|string|
|**wan\_link\_name**  <br>*optional*  <br>*read-only*|WAN Link name|string|


<a name="usage\_and\_permitted\_rate"></a>
### usage\_and\_permitted\_rate
Usage and Permitted Rates Statistics

*Type* : < [usage\_and\_permitted\_rate](#usage\_and\_permitted\_rate-inline) > array

<a name="usage\_and\_permitted\_rate-inline"></a>
**usage\_and\_permitted\_rate**

|Name|Description|Schema|
|---|---|---|
|**congestion**  <br>*optional*  <br>*read-only*|Congestion in the WAN Link|enum (YES, NO, N/A)|
|**delta\_packets**  <br>*optional*  <br>*read-only*|Delta packets transferred|integer|
|**delta\_packets\_kb**  <br>*optional*  <br>*read-only*|Delta Packets KB in Local WAN Link|number|
|**direction**  <br>*optional*  <br>*read-only*|Direction|enum (Send, Recv)|
|**kbps**  <br>*optional*  <br>*read-only*|kilobytes per second|number|
|**packets**  <br>*optional*  <br>*read-only*|Total packets transferred|integer|
|**packets\_kb**  <br>*optional*  <br>*read-only*|Total packets kb transferred|number|
|**permitted\_kbps**  <br>*optional*  <br>*read-only*|kilobytes per second|number|
|**service**  <br>*optional*  <br>*read-only*|Service name|string|
|**wan\_link\_name**  <br>*optional*  <br>*read-only*|WAN Link name|string|


<a name="wan\_link\_usage\_stats\_delete\_success\_schema"></a>
### wan\_link\_usage\_stats\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_link\_usage\_stats**  <br>*optional*|[wan\_link\_usage\_stats](#wan\_link\_usage\_stats\_delete\_success\_schema-wan\_link\_usage\_stats)|

<a name="wan\_link\_usage\_stats\_delete\_success\_schema-wan\_link\_usage\_stats"></a>
**wan\_link\_usage\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_link\_usage\_stats\_post\_success\_schema"></a>
### wan\_link\_usage\_stats\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_link\_usage\_stats**  <br>*optional*|[wan\_link\_usage\_stats](#wan\_link\_usage\_stats\_post\_success\_schema-wan\_link\_usage\_stats)|

<a name="wan\_link\_usage\_stats\_post\_success\_schema-wan\_link\_usage\_stats"></a>
**wan\_link\_usage\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_link\_usage\_stats\_put\_success\_schema"></a>
### wan\_link\_usage\_stats\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_link\_usage\_stats**  <br>*optional*|[wan\_link\_usage\_stats](#wan\_link\_usage\_stats\_put\_success\_schema-wan\_link\_usage\_stats)|

<a name="wan\_link\_usage\_stats\_put\_success\_schema-wan\_link\_usage\_stats"></a>
**wan\_link\_usage\_stats**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_link\_usage\_stats\_response\_schema"></a>
### wan\_link\_usage\_stats\_response\_schema
*Type* : < [wan\_link\_usage\_stats\_response\_schema](#wan\_link\_usage\_stats\_response\_schema-inline) > array

<a name="wan\_link\_usage\_stats\_response\_schema-inline"></a>
**wan\_link\_usage\_stats\_response\_schema**

|Name|Schema|
|---|---|
|**local\_wan\_links**  <br>*optional*|[local\_wan\_links](#local\_wan\_links)|
|**on\_demand\_wan\_link\_usage**  <br>*optional*|[on\_demand\_wan\_link\_usage](#on\_demand\_wan\_link\_usage)|
|**remote\_wan\_links**  <br>*optional*|[remote\_wan\_links](#remote\_wan\_links)|
|**usage\_and\_permitted\_rate**  <br>*optional*|[usage\_and\_permitted\_rate](#usage\_and\_permitted\_rate)|





