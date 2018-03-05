local\_change\_management

Configuration for This resource provides Local Change management status and operations related to Local Change Management. Use file\_upload\_to\_inbox API to upload file required for Local Change Management. resource.

Read/write properties

Read only properties

inbox\_files &lt;String&gt;

Files in Change Management Inbox Directory.

model &lt;String&gt;

Hardware model of appliance.

staged\_sw\_revision &lt;String&gt;

Staged software version on appliance.

staged\_registry\_timestamp &lt;String&gt;

TimeStamp of currently staged registries.

active\_registry\_timestamp &lt;String&gt;

TimeStamp of currently active registries.

staged\_config &lt;String&gt;

Staged config time.

message &lt;String&gt;

Local Change Management command message.

active\_sw\_revision &lt;String&gt;

Currently active software of appliance ..

active\_package\_filename &lt;String&gt;

Filename of currently active package.

staged\_package\_filename &lt;String&gt;

Filename of currently staged package.

active\_config &lt;String&gt;

Active config time ..

id &lt;String&gt;

Id of the appliance.

transfer\_state &lt;String&gt;

transfer state of the local change management process.

Operations

[get (all)](#get_all) [activate](#activate)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_change\_management

Description: Use this operation to get Local Change Management status

HTTP Method: GET

Response Payload: JSON

{"local\_change\_management":\[{ "inbox\_files":&lt;String\_value&gt;

, "model":&lt;String\_value&gt; , "staged\_sw\_revision":&lt;String\_value&gt; , "staged\_registry\_timestamp":&lt;String\_value&gt; , "active\_registry\_timestamp":&lt;String\_value&gt; , "staged\_config":&lt;String\_value&gt; , "message":&lt;String\_value&gt; , "active\_sw\_revision":&lt;String\_value&gt; , "active\_package\_filename":&lt;String\_value&gt; , "staged\_package\_filename":&lt;String\_value&gt; , "active\_config":&lt;String\_value&gt; , "id":&lt;String\_value&gt; , "transfer\_state":&lt;String\_value&gt; }\]}

[activate]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_change\_management?action=activate

Description: Does Local Change Management activate operation

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "local\_change\_management":{}}
