firewall\_static\_nat\_policy\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Static NAT policy settings resource.

Read/write properties

service\_type &lt;String&gt;

The Service Type that the translation applies to.. Possible values = \[local,internet,intranet\]

outside\_network\_ip\_address &lt;String&gt;

The Outside IP Address and Subnet Mask packets will be translated to (Source IP Address in the direction selected)..

direction &lt;String&gt;

The direction, from the Service or Virtual Interface perspective, the translation will operate.. Possible values = \[inbound,outbound\]

inside\_network\_ip\_address &lt;String&gt;

The Inside IP Address and Prefix to translate (Source IP Address in the direction selected)..

bind\_responder\_route &lt;Boolean&gt;

If enabled, the route for the responder's traffic will be bound to the Source Service..

service\_name &lt;String&gt;

The Service Name that the translation applies to..

outside\_zone &lt;String&gt;

The Zone a packet must be destined for to allow translation.. Possible values = \[Internet\_Zone,Untrusted\_Internet\_Zone,Default\_LAN\_Zone\]

id &lt;Integer&gt;

Firewall local policy id.

inside\_zone &lt;String&gt;

The Zone a packet must be from to allow translation.. Possible values = \[Internet\_Zone,Untrusted\_Internet\_Zone,Default\_LAN\_Zone\]

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Filters are applied (automatically redistributed)..

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_static\_nat\_policy\_obj

Description: Use this operation to add the Static NAT policy settings

HTTP Method: POST

Request Payload: JSON

{"firewall\_static\_nat\_policy\_obj": { "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_static\_nat\_policy\_obj":{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_static\_nat\_policy\_obj/

Description: Use this operation to delete the Static NAT policy settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_static\_nat\_policy\_obj

Description: Use this operation to get the Static NAT policy settings

HTTP Method: GET

Response Payload: JSON

{"firewall\_static\_nat\_policy\_obj":\[{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_static\_nat\_policy\_obj

Description: Use this operation to modify the Static NAT policy settings

HTTP Method: PUT

Request Payload: JSON

{"firewall\_static\_nat\_policy\_obj":{ "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_static\_nat\_policy\_obj":\[{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; }\]}
