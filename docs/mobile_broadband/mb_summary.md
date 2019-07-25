# mb\_summary


<a name="overview"></a>
## Overview
API to get the Modem/Cellular Network/RF Info/Profile/Call Statistics Information


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* mb\_summary : Operations related to mb\_summary 




<a name="paths"></a>
## Paths

<a name="mb\_summary-get"></a>
### Get operation for mb\_summary
```
GET /mb_summary
```


#### Description
Use this operation to get the Modem/Cellular Network/RF Info/Profile/Call Statistics Information  from SD-WAN Appliance


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[mb\_summary\_response\_schema](#mb\_summary\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* mb\_summary



