subnets\_obj

Configuration Editor for API to add, delete, and get configuration for subnets resource.

Read/write properties

network &lt;String&gt;

The IP address and mask for the subnet.

routing\_domain &lt;String&gt;

The routing domain.

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/subnets\_obj

Description: Use this operation to add the Destination NAT policy settings

HTTP Method: POST

Request Payload: JSON

{"subnets\_obj": { "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }}

Response Payload: JSON

{ "subnets\_obj":{ "network":&lt;String\_value&gt;

, "routing\_domain":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/subnets\_obj/

Description: Use this operation to delete the Destination NAT policy settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/subnets\_obj

Description: Use this operation to get the Destination NAT policy settings

HTTP Method: GET

Response Payload: JSON

{"subnets\_obj":\[{ "network":&lt;String\_value&gt;

, "routing\_domain":&lt;String\_value&gt; }\]}
