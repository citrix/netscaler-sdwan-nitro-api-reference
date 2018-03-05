management\_ip

Configuration for Get/Set management IP resource.

Read/write properties

gateway &lt;String&gt;

Gateway IP of Management IP.

netmask &lt;String&gt;

Subnet mask of Management IP.

ip\_address &lt;String&gt;

Management IP Of System.

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/management\_ip

Description: Get Management IP Info.

HTTP Method: GET

Response Payload: JSON

{"management\_ip":\[{ "gateway":&lt;String\_value&gt;

, "netmask":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/management\_ip

Description: Use this operation to change Management IP of SD-WAN Appliance

HTTP Method: PUT

Request Payload: JSON

{"management\_ip":{ "gateway":&lt;String\_value&gt; , "netmask":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; }}

Response Payload: JSON

{ "management\_ip":\[{ "gateway":&lt;String\_value&gt;

, "netmask":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; }\]}
