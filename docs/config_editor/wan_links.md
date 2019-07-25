# wan\_links


<a name="overview"></a>
## Overview
API to add, modify, delete, and get configuration for WAN links


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/config\_editor/  
*Schemes* : HTTP


### Tags

* wan\_links : Operations related to wan\_links 




<a name="paths"></a>
## Paths

<a name="wan\_links-post"></a>
### POST operation for wan\_links
```
POST /wan_links
```


#### Description
Use this operation to add wan links


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[wan\_links\_post\_success\_schema](#wan\_links\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_links


<a name="wan\_links-get"></a>
### Get operation for wan\_links
```
GET /wan_links
```


#### Description
Use this operation to get the list of wan links


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[wan\_links\_response\_schema](#wan\_links\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_links


<a name="wan\_links-put"></a>
### PUT operation for wan\_links
```
PUT /wan_links
```


#### Description
Use this operation to modify a wan link


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[wan\_links\_request\_schema](#wan\_links\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource modified added|[wan\_links\_put\_success\_schema](#wan\_links\_put\_success\_schema)|
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

* wan\_links


<a name="wan\_links-deletepathparam-delete"></a>
### DELETE operation for wan\_links
```
DELETE /wan_links/{deletePathParam}
```


#### Description
Use this operation to delete a wan link


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**deletePathParam**  <br>*required*|Object Primary Key for DELETE operation|object|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource delete added|[wan\_links\_delete\_success\_schema](#wan\_links\_delete\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* wan\_links




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="access\_interfaces"></a>
### access\_interfaces
List of Access Interfaces associated with the wan links group.

*Type* : < [access\_interfaces](#access\_interfaces-inline) > array

<a name="access\_interfaces-inline"></a>
**access\_interfaces**

|Name|Description|Schema|
|---|---|---|
|**conduit\_mode**  <br>*optional*|Determines the priority for Virtual Path traffic on this WAN Link. If set to 'exclude', the Access Interface will only be used for Internet and Intranet traffic|enum (primary, secondary, exclude)|
|**enable\_proxy\_arp**  <br>*optional*|If enabled, the Virtual WAN appliance will reply to ARP requests for the Gateway IP Address when the gateway is unreachable|boolean|
|**gateway\_mac\_addr\_binding**  <br>*optional*|If enabled, the source MAC address of packets received on Internet or Intranet services must match the gateway MAC address|boolean|
|**gw\_ip\_addr**  <br>*optional*|The IP Address of the Gateway router. You cannot configure the Gateway IP Address when the Virtual Appliance is configured to use DHCP Client mode.|string|
|**name**  <br>*optional*|Access Interface name|string|
|**virtual\_interface\_name**  <br>*optional*|Virtual Interface Name|string|
|**virtual\_ip\_addr**  <br>*optional*|The IP Address for the Access Interface Endpoint on the WAN. You cannot configure the IP Address when the Virtual Appliance is configured to use DHCP Client mode.|string|


<a name="access\_type"></a>
### access\_type
The type of network connected to the WAN link

*Type* : enum (public\_internet, private\_intranet, private\_mpls)


<a name="enable\_public\_ip\_learning"></a>
### enable\_public\_ip\_learning
Enable public IP learning

*Type* : boolean


<a name="lan\_to\_wan\_permitted\_rate"></a>
### lan\_to\_wan\_permitted\_rate
LAN to WAN Permitted rate in Kbps

*Type* : integer


<a name="lan\_to\_wan\_physical\_rate"></a>
### lan\_to\_wan\_physical\_rate
LAN to WAN Physical rate in Kbps

*Type* : integer


<a name="mpls\_queues"></a>
### mpls\_queues
List of MPLS Queues associated with the wan links group.

*Type* : < [mpls\_queues](#mpls\_queues-inline) > array

<a name="mpls\_queues-inline"></a>
**mpls\_queues**

|Name|Description|Schema|
|---|---|---|
|**congestion\_threshold**  <br>*optional*|The amount of congestion (in microseconds) after which the MPLS Queue will throttle packet transmission to avoid further congestion|integer|
|**dscp\_tag**  <br>*optional*|The DSCP tag for the MPLS queue  <br>**Default** : `"DEFAULT"`|enum (DEFAULT, af11, af12, af13, af21, af22, af23, af31, af32, af33, af41, af42, af43, cs1, cs2, cs3, cs4, cs5, cs6, cs7, ef)|
|**lan\_to\_wan\_bulk\_eligibility**  <br>*optional*|Allows paths from this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available|boolean|
|**lan\_to\_wan\_interactive\_eligibility**  <br>*optional*|Allows paths from this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available|boolean|
|**lan\_to\_wan\_permitted\_rate\_kbps**  <br>*optional*|The available or allowed rate for LAN to WAN traffic|integer|
|**lan\_to\_wan\_realtime\_eligibility**  <br>*optional*|Allows paths from this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available|boolean|
|**mpls\_queue\_name**  <br>*optional*|The name of the MPLS Queue|string|
|**no\_retag**  <br>*optional*|If enabled, DCSP tags using unmatched Queue will not get retagged to the unmatched Queue tag for LAN to WAN intranet traffic|boolean|
|**tracking\_ip\_address**  <br>*optional*|A virtual IP address that can be pinged to determine the state of the MPLS Queue|string|
|**unmatched**  <br>*optional*|If enabled, DSCP tags not matched by other MPLS Queues will use this queue|boolean|
|**wan\_to\_lan\_bulk\_eligibility**  <br>*optional*|Allows paths to this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available|boolean|
|**wan\_to\_lan\_interactive\_eligibility**  <br>*optional*|Allows paths to this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available.|boolean|
|**wan\_to\_lan\_permitted\_rate\_kbps**  <br>*optional*|The available or allowed rate for WAN to LAN traffic|integer|
|**wan\_to\_lan\_realtime\_eligibility**  <br>*optional*|Allows paths to this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available.|boolean|


<a name="mtu\_size"></a>
### mtu\_size
Maximum taranfer unit size

*Type* : integer


<a name="package\_name"></a>
### package\_name
Config package name using which the wan\_links API operation should be performed.

*Type* : string


<a name="public\_ip"></a>
### public\_ip
Public IP Address of WAN Links

*Type* : string


<a name="site\_name"></a>
### site\_name
Site Name

*Type* : string


<a name="wan\_link\_name"></a>
### wan\_link\_name
WAN Link name

*Type* : string


<a name="wan\_link\_template\_name"></a>
### wan\_link\_template\_name
WAN Link template name

*Type* : string


<a name="wan\_links"></a>
### wan\_links

|Name|Schema|
|---|---|
|**access\_interfaces**  <br>*optional*|[access\_interfaces](#access\_interfaces)|
|**access\_type**  <br>*optional*|[access\_type](#access\_type)|
|**enable\_public\_ip\_learning**  <br>*optional*|[enable\_public\_ip\_learning](#enable\_public\_ip\_learning)|
|**lan\_to\_wan\_permitted\_rate**  <br>*optional*|[lan\_to\_wan\_permitted\_rate](#lan\_to\_wan\_permitted\_rate)|
|**lan\_to\_wan\_physical\_rate**  <br>*optional*|[lan\_to\_wan\_physical\_rate](#lan\_to\_wan\_physical\_rate)|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues)|
|**mtu\_size**  <br>*optional*|[mtu\_size](#mtu\_size)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**public\_ip**  <br>*optional*|[public\_ip](#public\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_link\_template\_name**  <br>*optional*|[wan\_link\_template\_name](#wan\_link\_template\_name)|
|**wan\_to\_lan\_permitted\_rate**  <br>*optional*|[wan\_to\_lan\_permitted\_rate](#wan\_to\_lan\_permitted\_rate)|
|**wan\_to\_lan\_physical\_rate**  <br>*optional*|[wan\_to\_lan\_physical\_rate](#wan\_to\_lan\_physical\_rate)|


<a name="wan\_links\_delete\_success\_schema"></a>
### wan\_links\_delete\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_delete\_success\_schema-wan\_links)|

<a name="wan\_links\_delete\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="wan\_links\_post\_success\_schema"></a>
### wan\_links\_post\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_post\_success\_schema-wan\_links)|

<a name="wan\_links\_post\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="wan\_links\_put\_success\_schema"></a>
### wan\_links\_put\_success\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links\_put\_success\_schema-wan\_links)|

<a name="wan\_links\_put\_success\_schema-wan\_links"></a>
**wan\_links**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="wan\_links\_request\_schema"></a>
### wan\_links\_request\_schema

|Name|Schema|
|---|---|
|**wan\_links**  <br>*optional*|[wan\_links](#wan\_links)|


<a name="wan\_links\_response\_schema"></a>
### wan\_links\_response\_schema
*Type* : < [wan\_links\_response\_schema](#wan\_links\_response\_schema-inline) > array

<a name="wan\_links\_response\_schema-inline"></a>
**wan\_links\_response\_schema**

|Name|Schema|
|---|---|
|**access\_interfaces**  <br>*optional*|[access\_interfaces](#access\_interfaces)|
|**access\_type**  <br>*optional*|[access\_type](#access\_type)|
|**enable\_public\_ip\_learning**  <br>*optional*|[enable\_public\_ip\_learning](#enable\_public\_ip\_learning)|
|**lan\_to\_wan\_permitted\_rate**  <br>*optional*|[lan\_to\_wan\_permitted\_rate](#lan\_to\_wan\_permitted\_rate)|
|**lan\_to\_wan\_physical\_rate**  <br>*optional*|[lan\_to\_wan\_physical\_rate](#lan\_to\_wan\_physical\_rate)|
|**mpls\_queues**  <br>*optional*|[mpls\_queues](#mpls\_queues)|
|**mtu\_size**  <br>*optional*|[mtu\_size](#mtu\_size)|
|**package\_name**  <br>*optional*|[package\_name](#package\_name)|
|**public\_ip**  <br>*optional*|[public\_ip](#public\_ip)|
|**site\_name**  <br>*optional*|[site\_name](#site\_name)|
|**wan\_link\_name**  <br>*optional*|[wan\_link\_name](#wan\_link\_name)|
|**wan\_link\_template\_name**  <br>*optional*|[wan\_link\_template\_name](#wan\_link\_template\_name)|
|**wan\_to\_lan\_permitted\_rate**  <br>*optional*|[wan\_to\_lan\_permitted\_rate](#wan\_to\_lan\_permitted\_rate)|
|**wan\_to\_lan\_physical\_rate**  <br>*optional*|[wan\_to\_lan\_physical\_rate](#wan\_to\_lan\_physical\_rate)|


<a name="wan\_to\_lan\_permitted\_rate"></a>
### wan\_to\_lan\_permitted\_rate
WAN to LAN Permitted rate in Kbps

*Type* : integer


<a name="wan\_to\_lan\_physical\_rate"></a>
### wan\_to\_lan\_physical\_rate
WAN to LAN Physical rate in Kbps

*Type* : integer





