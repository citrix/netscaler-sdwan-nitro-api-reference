change\_management

Configuration for This resource provides Change management status and operations related to Change Management. Use file\_upload\_to\_inbox API to upload files for Change Managment Operation. Use get\_package\_file to download packages created by Change Management, to be used in Local Change Management Operation. resource.

Read/write properties

Read only properties

current\_config &lt;String&gt;

Name of the active config..

inbox\_files &lt;String&gt;

Files in Change Management Inbox Directory.

status &lt;String&gt;

This key indicates status of verify action..

sites\_cm\_status &lt;sites\_cm\_info\[\]&gt;

Change management status for Site.

state &lt;String&gt;

Change Management State.

message &lt;String&gt;

Detailed message about API execution..

failure\_reason &lt;String&gt;

This key will be present in the response of verify action. This key indicates failure reason of verify action, if applicable..

activate\_info &lt;String&gt;

Activation information.

network\_staged\_selected\_filename &lt;String&gt;

Network staged config Filename.

Operations

[stage](#stage) [activate\_with\_rollback](#activate_with_rollback) [migrate\_config](#migrate_config) [activate](#activate) [clear\_network\_staging](#clear_network_staging) [verify](#verify) [ignore\_incomplete](#ignore_incomplete) [get (all)](#get_all) [cancel\_stage](#cancel_stage) [clear\_inbox](#clear_inbox)

[stage]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=stage

Description: Start Change Management stage operation

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[activate\_with\_rollback]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=activate\_with\_rollback

Description: Does Change Management activate operation with Rollback enabled. This activation mode ensures, software will revert if an error occurs.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[migrate\_config]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=migrate\_config

Description: Does migrate current config to inbox

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[activate]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=activate

Description: Does Change Management activate operation.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[clear\_network\_staging]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=clear\_network\_staging

Description: This API clears the network staging contents of the Change Management server.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[verify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=verify

Description: Does Change Management verify operation

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[ignore\_incomplete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=ignore\_incomplete

Description: This action can be performed while staging operation is in progress. Issuing this action will ignore incomplete staging action and allows user to proceed with Change Management activation.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management

Description: Use this operation to get Change Management status

HTTP Method: GET

Response Payload: JSON

{"change\_management":\[{ "current\_config":&lt;String\_value&gt;

, "inbox\_files":&lt;String\_value&gt; , "status":&lt;String\_value&gt; , "sites\_cm\_status":\[{ "status":&lt;String\_value&gt; , "staged\_sw\_revision":&lt;String\_value&gt; , "observed\_sw\_revision":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "expected\_interruption":&lt;String\_value&gt; , "appliance\_name":&lt;String\_value&gt; , "staged\_config":&lt;String\_value&gt; , "active\_software":&lt;String\_value&gt; , "expected\_sw\_revision":&lt;String\_value&gt; , "active\_config":&lt;String\_value&gt; , "transfer\_state":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "actual\_interruption\_ms":&lt;String\_value&gt; }\], "state":&lt;String\_value&gt; , "message":&lt;String\_value&gt; , "failure\_reason":&lt;String\_value&gt; , "activate\_info":&lt;String\_value&gt; , "network\_staged\_selected\_filename":&lt;String\_value&gt; }\]}

[cancel\_stage]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=cancel\_stage

Description: Cancel Change Management stage operation

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}

[clear\_inbox]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/change\_management?action=clear\_inbox

Description: Clears Change Management inbox folder

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "change\_management":{}}
