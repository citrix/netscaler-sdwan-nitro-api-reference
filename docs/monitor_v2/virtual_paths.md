virtual\_paths

Monitoring for This resource provides details of all the virtual paths in the system resource.

Read/write properties

Read only properties

status &lt;String&gt;

Virtual Path Status.

uptime &lt;String&gt;

Uptime of the Virtual Path.

name &lt;String&gt;

Name of the Virtual Path.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/virtual\_paths

Description: Use this operation to get Virtual Paths status

HTTP Method: GET

Response Payload: JSON

{"virtual\_paths":\[{ "status":&lt;String\_value&gt;

, "uptime":&lt;String\_value&gt; , "name":&lt;String\_value&gt; }\]}
