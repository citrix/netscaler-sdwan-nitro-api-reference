# sim


<a name="overview"></a>
## Overview
This resource is to reset Mobile Broadband SIM Module


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/mobile\_broadband/  
*Schemes* : HTTP


### Tags

* sim : Operations related to sim 




<a name="paths"></a>
## Paths

<a name="sim-post"></a>
### POST operation for sim
```
POST /sim
```


#### Description
This operation is to refresh the Mobile Broadband SIM Module


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Query**|**action**  <br>*required*|Select if action is other that ADD|enum (refresh)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[sim\_post\_success\_schema](#sim\_post\_success\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* sim



