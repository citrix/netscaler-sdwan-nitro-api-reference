# packet\_capture


<a name="overview"></a>
## Overview
Capture and download pcapng on different interfaces[Max File Size 575 MB]


### Version information
*Version* : v2


### URI scheme
*Host* : <MGMT-IP>  
*BasePath* : /sdwan/nitro/v2/diag/  
*Schemes* : HTTP


### Tags

* packet\_capture : Operations related to packet\_capture 




<a name="paths"></a>
## Paths

<a name="packet\_capture-post"></a>
### POST operation for packet\_capture
```
POST /packet_capture
```


#### Description
Use this operation to capture pcap on different interfaces SD-WAN Appliance


#### Parameters

|Type|Name|Schema|
|---|---|---|
|**Body**|**body**  <br>*optional*|[packet\_capture\_request\_schema](#packet\_capture\_request\_schema)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Resource successfully added|[packet\_capture\_post\_success\_schema](#packet\_capture\_post\_success\_schema)|
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

* packet\_capture




<a name="definitions"></a>
## Definitions

<a name="errorschema"></a>
### ErrorSchema

|Name|Schema|
|---|---|
|**errorcode**  <br>*optional*|integer|
|**errormessage**  <br>*optional*|string|


<a name="duration"></a>
### duration
Duration for  which packets have to be captured in seconds

*Type* : enum (5, 10, 15, 30)


<a name="filter\_str"></a>
### filter\_str
Filter string is used to determine which packets are captured

*Type* : string


<a name="interface"></a>
### interface
Interfaces on which packets have to be captured. Multiple Interfaces need to separated using a double hyphen. Ex: MGMT, MGT--1--2, LTE-1--MGMT--1/2, etc.

*Type* : string


<a name="max\_packets"></a>
### max\_packets
Max Number of Packets to be captured

*Type* : enum (1000, 2000, 5000, MAX)


<a name="message"></a>
### message
Message about the packet capture event

*Type* : string


<a name="packet\_capture"></a>
### packet\_capture

|Name|Schema|
|---|---|
|**duration**  <br>*optional*|[duration](#duration)|
|**filter\_str**  <br>*optional*|[filter\_str](#filter\_str)|
|**interface**  <br>*optional*|[interface](#interface)|
|**max\_packets**  <br>*optional*|[max\_packets](#max\_packets)|


<a name="packet\_capture\_delete\_success\_schema"></a>
### packet\_capture\_delete\_success\_schema

|Name|Schema|
|---|---|
|**packet\_capture**  <br>*optional*|[packet\_capture](#packet\_capture\_delete\_success\_schema-packet\_capture)|

<a name="packet\_capture\_delete\_success\_schema-packet\_capture"></a>
**packet\_capture**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource deleted succesfully"`|string|


<a name="packet\_capture\_post\_success\_schema"></a>
### packet\_capture\_post\_success\_schema

|Name|Schema|
|---|---|
|**packet\_capture**  <br>*optional*|[packet\_capture](#packet\_capture\_post\_success\_schema-packet\_capture)|

<a name="packet\_capture\_post\_success\_schema-packet\_capture"></a>
**packet\_capture**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource added succesfully"`|string|


<a name="packet\_capture\_put\_success\_schema"></a>
### packet\_capture\_put\_success\_schema

|Name|Schema|
|---|---|
|**packet\_capture**  <br>*optional*|[packet\_capture](#packet\_capture\_put\_success\_schema-packet\_capture)|

<a name="packet\_capture\_put\_success\_schema-packet\_capture"></a>
**packet\_capture**

|Name|Description|Schema|
|---|---|---|
|**message**  <br>*optional*|**Example** : `"resource modified succesfully"`|string|


<a name="packet\_capture\_request\_schema"></a>
### packet\_capture\_request\_schema

|Name|Schema|
|---|---|
|**packet\_capture**  <br>*optional*|[packet\_capture](#packet\_capture)|


<a name="packet\_capture\_response\_schema"></a>
### packet\_capture\_response\_schema
*Type* : < [packet\_capture\_response\_schema](#packet\_capture\_response\_schema-inline) > array

<a name="packet\_capture\_response\_schema-inline"></a>
**packet\_capture\_response\_schema**

|Name|Schema|
|---|---|
|**duration**  <br>*optional*|[duration](#duration)|
|**filter\_str**  <br>*optional*|[filter\_str](#filter\_str)|
|**interface**  <br>*optional*|[interface](#interface)|
|**max\_packets**  <br>*optional*|[max\_packets](#max\_packets)|
|**message**  <br>*optional*|[message](#message)|
|**summary**  <br>*optional*|[summary](#summary)|


<a name="summary"></a>
### summary
Summary of Packets captured

*Type* : < [summary](#summary-inline) > array

<a name="summary-inline"></a>
**summary**

|Name|Description|Schema|
|---|---|---|
|**dst\_ip**  <br>*optional*  <br>*read-only*|Destination IP of the packet .|string|
|**dst\_mac**  <br>*optional*  <br>*read-only*|Destination MAC of the Packet .|string|
|**dst\_port**  <br>*optional*  <br>*read-only*|Destination Port of the Packet|string|
|**length**  <br>*optional*  <br>*read-only*|Packet length in bytes|string|
|**number**  <br>*optional*  <br>*read-only*|Packet Number|string|
|**protocol**  <br>*optional*  <br>*read-only*|Protocol Used by the packet|string|
|**src\_ip**  <br>*optional*  <br>*read-only*|Source IP of the Packet|string|
|**src\_mac**  <br>*optional*  <br>*read-only*|Source MAC Address of Packet|string|
|**src\_port**  <br>*optional*  <br>*read-only*|Source Port of the Packet|string|
|**time**  <br>*optional*  <br>*read-only*|Packet Time|string|





