radius\_settings

Configuration for These APIs can be used to enable/disable RADIUS, Modify or Get RADIUS Settings resource.

Read/write properties

radius\_port &lt;Integer&gt;

Port of Radius server (Value range 1 to 65535).

radius\_enabled &lt;Boolean&gt;

RADIUS enable/disable. Default value is true.

radius\_server\_key &lt;String&gt;

Radius server key.

radius\_server\_ip\_addr3 &lt;String&gt;

IPADDRESS3 of Radius server.

radius\_server\_ip\_addr2 &lt;String&gt;

IPADDRESS2 of Radius server.

radius\_port3 &lt;Integer&gt;

Port3 of Radius server (Value range 1 to 65535).

radius\_timeout &lt;Integer&gt;

Radius timeout in seconds. Maximum value = 10

radius\_port2 &lt;Integer&gt;

Port2 of Radius server (Value range 1 to 65535).

radius\_server\_ip\_addr &lt;String&gt;

IPADDRESS of Radius server.

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/radius\_settings

Description: Get Radius Settings

HTTP Method: GET

Response Payload: JSON

{"radius\_settings":\[{ "radius\_port":&lt;Integer\_value&gt;

, "radius\_enabled":&lt;Boolean\_value&gt; , "radius\_server\_key":&lt;String\_value&gt; , "radius\_server\_ip\_addr3":&lt;String\_value&gt; , "radius\_server\_ip\_addr2":&lt;String\_value&gt; , "radius\_port3":&lt;Integer\_value&gt; , "radius\_timeout":&lt;Integer\_value&gt; , "radius\_port2":&lt;Integer\_value&gt; , "radius\_server\_ip\_addr":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/radius\_settings

Description: Use this API to modify RADIUS settings

HTTP Method: PUT

Request Payload: JSON

{"radius\_settings":{ "radius\_port":&lt;Integer\_value&gt; , "radius\_enabled":&lt;Boolean\_value&gt; , "radius\_server\_key":&lt;String\_value&gt; , "radius\_server\_ip\_addr3":&lt;String\_value&gt; , "radius\_server\_ip\_addr2":&lt;String\_value&gt; , "radius\_port3":&lt;Integer\_value&gt; , "radius\_timeout":&lt;Integer\_value&gt; , "radius\_port2":&lt;Integer\_value&gt; , "radius\_server\_ip\_addr":&lt;String\_value&gt; }}

Response Payload: JSON

{ "radius\_settings":\[{ "radius\_port":&lt;Integer\_value&gt;

, "radius\_enabled":&lt;Boolean\_value&gt; , "radius\_server\_key":&lt;String\_value&gt; , "radius\_server\_ip\_addr3":&lt;String\_value&gt; , "radius\_server\_ip\_addr2":&lt;String\_value&gt; , "radius\_port3":&lt;Integer\_value&gt; , "radius\_timeout":&lt;Integer\_value&gt; , "radius\_port2":&lt;Integer\_value&gt; , "radius\_server\_ip\_addr":&lt;String\_value&gt; }\]}
