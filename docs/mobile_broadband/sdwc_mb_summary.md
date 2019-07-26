# sdwc\_mb\_summary


<a name="overview"></a>
## Overview
API is used by SD-WAN Center to get the Modem/Cellular Network/RF Info/Profile/Call/FirmwareList Information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* sdwc\_mb\_summary : Operations related to sdwc\_mb\_summary 




<a name="paths"></a>
## Paths

<a name="sdwc\_mb\_summary-get"></a>
### Get operation for sdwc\_mb\_summary
```
GET /sdwc_mb_summary
```


#### Description
Use this operation to get the Modem/Cellular Network/RF Info/Profile/Call Statistics/FirmwareList Information  from SD-WAN Appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[sdwc\_mb\_summary\_response\_schema](#sdwc\_mb\_summary\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sdwc\_mb\_summary



