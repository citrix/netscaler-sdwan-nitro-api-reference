access\_interface

Configuration Editor for Access Interface object resource.

Read/write properties

virtual\_ip\_addr &lt;String&gt;

The IP Address for the Access Interface Endpoint on the WAN. You cannot configure the IP Address when the Virtual Appliance is configured to use DHCP Client mode..

gw\_ip\_addr &lt;String&gt;

The IP Address of the Gateway router. You cannot configure the Gateway IP Address when the Virtual Appliance is configured to use DHCP Client mode..

virtual\_interface\_name &lt;String&gt;

Virtual Interface Name.

Read only properties

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/access\_interface

Description: Use this operation to get the list of virtual interface objects

HTTP Method: GET

Response Payload: JSON

{"access\_interface":\[{ "virtual\_ip\_addr":&lt;String\_value&gt;

, "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\]}
