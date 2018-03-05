wanlink

Configuration for API to modify the wanlink standby mode resource.

Read/write properties

wanlink\_name &lt;String&gt;

Wan Link Name.

virtual\_path &lt;String&gt;

Virtual Path Name.

standby\_mode &lt;Boolean&gt;

Standby Mode, 0 for non-standby and 1 for last resort standby.

Read only properties

Operations

[modify](#modify)

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/wanlink

Description: Use this operation to modify wanlink standby mode in SD-WAN Appliance

HTTP Method: PUT

Request Payload: JSON

{"wanlink":{ "wanlink\_name":&lt;String\_value&gt; , "virtual\_path":&lt;String\_value&gt; , "standby\_mode":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "wanlink":\[{ "wanlink\_name":&lt;String\_value&gt;

, "virtual\_path":&lt;String\_value&gt; , "standby\_mode":&lt;Boolean\_value&gt; }\]}
