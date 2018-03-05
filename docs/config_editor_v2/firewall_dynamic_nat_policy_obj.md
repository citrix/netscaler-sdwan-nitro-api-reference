firewall\_dynamic\_nat\_policy\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Dynamic NAT policy settings resource.

Read/write properties

port\_forwarding\_rules &lt;port\_forwarding\_rules\_obj\[\]&gt;

Port Forwarding Rules.

enable\_gre\_pptp\_passthrough &lt;Boolean&gt;

To allow a GRE/PPTP session to be translated. Only a single session from the inside network will be permitted..

direction &lt;String&gt;

The direction, from the Service or Virtual Interface perspective, the translation will operate.. Possible values = \[inbound,outbound\]

inside\_network\_ip\_address &lt;String&gt;

The Inside IP Address and Prefix to translate (Source IP Address in the direction selected)..

allow\_related &lt;Boolean&gt;

To allow packets related to a Connection (ICMP error packets)..

service\_name &lt;String&gt;

The Service Name that the translation applies to..

id &lt;Integer&gt;

Firewall dynamic NATs policy id.

inside\_zone &lt;String&gt;

The Inside Zone to translate.. Possible values = \[any,Internet\_Zone,Untrusted\_Internet\_Zone,Default\_LAN\_Zone\]

service\_type &lt;String&gt;

The Service Type that the translation applies to.. Possible values = \[local,internet,intranet\]

outside\_network\_ip\_address &lt;String&gt;

The Outside IP Address and Subnet Mask packets will be translated to (Source IP Address in the direction selected)..

port\_parity &lt;Boolean&gt;

If enabled, outside ports for NAT connections will maintain parity (even if inside port is even, odd if outside port is odd)..

bind\_responder\_route &lt;Boolean&gt;

If enabled, the route for the responder's traffic will be bound to the Source Service..

enable\_ipsec\_passthrough &lt;Boolean&gt;

To allow an IPsec (AH/ESP) session to be translated. Only a single session from the inside network will be permitted..

outside\_zone &lt;String&gt;

The Zone a packet must be destined for to allow translation.. Possible values = \[Internet\_Zone,Untrusted\_Internet\_Zone,Default\_LAN\_Zone\]

type &lt;String&gt;

The type of Dynamic NAT to perform.. Possible values = \[port\_restricted,symmetric\]

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Filters are applied (automatically redistributed)..

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_dynamic\_nat\_policy\_obj

Description: Use this operation to add the Dynamic NAT policy settings

HTTP Method: POST

Request Payload: JSON

{"firewall\_dynamic\_nat\_policy\_obj": { "port\_forwarding\_rules":\[{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\] , "enable\_gre\_pptp\_passthrough":&lt;Boolean\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "allow\_related":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "port\_parity":&lt;Boolean\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "enable\_ipsec\_passthrough":&lt;Boolean\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "type":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_dynamic\_nat\_policy\_obj":{ "priority":&lt;Integer\_value&gt;

, "port\_forwarding\_rules":\[{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\], "enable\_gre\_pptp\_passthrough":&lt;Boolean\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "allow\_related":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "port\_parity":&lt;Boolean\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "enable\_ipsec\_passthrough":&lt;Boolean\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "type":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_dynamic\_nat\_policy\_obj/

Description: Use this operation to delete the Dynamic NAT policy settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_dynamic\_nat\_policy\_obj

Description: Use this operation to get the Dynamic NAT policy settings

HTTP Method: GET

Response Payload: JSON

{"firewall\_dynamic\_nat\_policy\_obj":\[{ "priority":&lt;Integer\_value&gt;

, "port\_forwarding\_rules":\[{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\], "enable\_gre\_pptp\_passthrough":&lt;Boolean\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "allow\_related":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "port\_parity":&lt;Boolean\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "enable\_ipsec\_passthrough":&lt;Boolean\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "type":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_dynamic\_nat\_policy\_obj

Description: Use this operation to modify the Dynamic NAT policy settings

HTTP Method: PUT

Request Payload: JSON

{"firewall\_dynamic\_nat\_policy\_obj":{ "port\_forwarding\_rules":\[{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\] , "enable\_gre\_pptp\_passthrough":&lt;Boolean\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "allow\_related":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "port\_parity":&lt;Boolean\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "enable\_ipsec\_passthrough":&lt;Boolean\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "type":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_dynamic\_nat\_policy\_obj":\[{ "priority":&lt;Integer\_value&gt;

, "port\_forwarding\_rules":\[{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\], "enable\_gre\_pptp\_passthrough":&lt;Boolean\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "allow\_related":&lt;Boolean\_value&gt; , "service\_name":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "inside\_zone":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "port\_parity":&lt;Boolean\_value&gt; , "bind\_responder\_route":&lt;Boolean\_value&gt; , "enable\_ipsec\_passthrough":&lt;Boolean\_value&gt; , "outside\_zone":&lt;String\_value&gt; , "type":&lt;String\_value&gt; }\]}
