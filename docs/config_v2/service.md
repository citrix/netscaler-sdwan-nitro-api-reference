service

Configuration for This resource gives service related options resource.

Read/write properties

Read only properties

service\_state &lt;String&gt;

Service state.

message &lt;String&gt;

Message for the action request.

Operations

[restart](#restart) [enable](#enable) [get (all)](#get_all) [disable](#disable)

[restart]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/service?action=restart

Description: Restarts the SD-WAN Service

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "service":{}}

[enable]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/service?action=enable

Description: Enables the SD-WAN Service

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "service":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/service

Description: Use this operation to get SD-WAN Service status

HTTP Method: GET

Response Payload: JSON

{"service":\[{ "service\_state":&lt;String\_value&gt;

, "message":&lt;String\_value&gt; }\]}

[disable]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/service?action=disable

Description: Disables the SD-WAN Service

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "service":{}}
