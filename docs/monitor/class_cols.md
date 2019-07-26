# class\_cols


<a name="overview"></a>
## Overview
This resource provides Info on QOS Classes


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/monitor/  
*Schemes* : HTTP


### Tags

* class\_cols : Operations related to class\_cols 




<a name="paths"></a>
## Paths

<a name="class\_cols-get"></a>
### Get operation for class\_cols
```
GET /class_cols
```


#### Description
Use this operation to get QOS Class details


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|API Successfully executed|[class\_cols\_response\_schema](#class\_cols\_response\_schema)|
|**400**|Failed: bad input parameter|[ErrorSchema](#errorschema)|
|**401**|Unauthorized: Failed Authentication|[ErrorSchema](#errorschema)|
|**403**|Unauthorized: Forbidden|[ErrorSchema](#errorschema)|
|**405**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**415**|Failed: Data format unacceptable|[ErrorSchema](#errorschema)|
|**500**|Failed: Internal Server Error|[ErrorSchema](#errorschema)|


#### Produces

* `application/json`


#### Tags

* class\_cols




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="bandwidth"></a>
### bandwidth
Bandwidth in kbps

*Type* : string


<a name="class\_cols\_delete\_success\_schema"></a>
### class\_cols\_delete\_success\_schema

|Name|Schema|
|---|---|
|**class\_cols**  <br>*optional*|[class\_cols](#class\_cols\_delete\_success\_schema-class\_cols)|

<a name="class\_cols\_delete\_success\_schema-class\_cols"></a>
**class\_cols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="class\_cols\_post\_success\_schema"></a>
### class\_cols\_post\_success\_schema

|Name|Schema|
|---|---|
|**class\_cols**  <br>*optional*|[class\_cols](#class\_cols\_post\_success\_schema-class\_cols)|

<a name="class\_cols\_post\_success\_schema-class\_cols"></a>
**class\_cols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="class\_cols\_put\_success\_schema"></a>
### class\_cols\_put\_success\_schema

|Name|Schema|
|---|---|
|**class\_cols**  <br>*optional*|[class\_cols](#class\_cols\_put\_success\_schema-class\_cols)|

<a name="class\_cols\_put\_success\_schema-class\_cols"></a>
**class\_cols**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="class\_cols\_response\_schema"></a>
### class\_cols\_response\_schema
*Type* : < [class\_cols\_response\_schema](#class\_cols\_response\_schema-inline) > array

<a name="class\_cols\_response\_schema-inline"></a>
**class\_cols\_response\_schema**

|Name|Schema|
|---|---|
|**bandwidth**  <br>*optional*|[bandwidth](#bandwidth)|
|**class\_number**  <br>*optional*|[class\_number](#class\_number)|
|**dropped\_bytes**  <br>*optional*|[dropped\_bytes](#dropped\_bytes)|
|**dropped\_packets**  <br>*optional*|[dropped\_packets](#dropped\_packets)|
|**name**  <br>*optional*|[name](#name)|
|**pending\_bytes**  <br>*optional*|[pending\_bytes](#pending\_bytes)|
|**pending\_packets**  <br>*optional*|[pending\_packets](#pending\_packets)|
|**sent\_bytes**  <br>*optional*|[sent\_bytes](#sent\_bytes)|
|**sent\_packets**  <br>*optional*|[sent\_packets](#sent\_packets)|
|**type**  <br>*optional*|[type](#type)|
|**wait\_ms**  <br>*optional*|[wait\_ms](#wait\_ms)|


<a name="class\_number"></a>
### class\_number
Class Number

*Type* : string


<a name="dropped\_bytes"></a>
### dropped\_bytes
Dropped Bytes

*Type* : string


<a name="dropped\_packets"></a>
### dropped\_packets
Dropped Packets

*Type* : string


<a name="name"></a>
### name
Class Name

*Type* : string


<a name="pending\_bytes"></a>
### pending\_bytes
Pending Bytes

*Type* : string


<a name="pending\_packets"></a>
### pending\_packets
Pending Packets

*Type* : string


<a name="sent\_bytes"></a>
### sent\_bytes
Sent Bytes

*Type* : string


<a name="sent\_packets"></a>
### sent\_packets
Sent Packets

*Type* : string


<a name="type"></a>
### type
Class Type

*Type* : string


<a name="wait\_ms"></a>
### wait\_ms
Wait time in Milliseconds

*Type* : string





