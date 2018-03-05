firewall\_policy\_template\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Basic and Advanced Firewall settings resource.

Read/write properties

destination\_service\_name &lt;String&gt;

The Destination service that the filter will match.

match\_type &lt;String&gt;

The Application used as match criteria for this Filter.. Possible values = \[ip\_protocol,application,application\_family,application\_objects\]

destination\_port &lt;Integer&gt;

The Destination Port or Port Range that the Filter will match..

application\_objects &lt;String&gt;

The Application used as match criteria for this Filter..

source\_port &lt;Integer&gt;

The Source Port or Port Range that the Filter will match..

ip\_dscp &lt;String&gt;

The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions.. Possible values = \[ANY,DEFAULT,af11,af12,af13,af21,af22,af23,af31,af32,af33,af41,af42,af43,cs1,cs2,cs3,cs4,cs5,cs6,cs7,ef\]

destination\_ip\_address &lt;String&gt;

The Destination IP Address and Subnet Mask that the Filter will match..

source\_service\_type &lt;String&gt;

The Source Service Type that the Filter will match.. Possible values = \[any,local,virtual\_path,internet,intranet,gre\_tunnel,lan\_ipsec\_tunnel,ip\_host,multicast\]

log\_interval &lt;Integer&gt;

The time, in seconds, between logging the number of packets matching the filter (0 = disabled, valid settings are 60-600)..

track\_connection &lt;Boolean&gt;

Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Filter. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation --  proceed with caution if NetScaler SD-WAN is not fully inline..

destination\_service\_type &lt;String&gt;

The Destination Service Type that the Filter will match.. Possible values = \[any,local,virtual\_path,internet,intranet,gre\_tunnel,lan\_ipsec\_tunnel,ip\_host,multicast\]

ip\_protocol\_num &lt;Integer&gt;

The IP Protocol that the Filter will match..

reverse\_also &lt;Boolean&gt;

Click the checkbox to automatically add a copy of this Filter with the Source and Destination settings reversed..

source\_ip\_address &lt;String&gt;

The Source IP Address and Subnet Mask that the Filter will match..

application\_family &lt;String&gt;

The Application used as match criteria for this Filter..

application &lt;String&gt;

The Application used as match criteria for this Filter..

log\_connection\_end &lt;Boolean&gt;

To generate a log when a Connection matching this Filter is deleted..

to\_zones &lt;String&gt;

Select to filter on the zone the packet is destined to. Possible values = \[any,default\_lan\_zone,internet\_zone,untrusted\_internet\_zone\]

action &lt;String&gt;

The Action to take for each packet matching the Filter.. Possible values = \[allow,drop,reject,count\_and\_continue\]

match\_established &lt;Boolean&gt;

To match incoming packets for a Connection to which outgoing packets were allowed..

log\_connection\_start &lt;Boolean&gt;

To generate a log when a new Connection is created by a packet matching this Filter..

source\_service\_name &lt;String&gt;

The Source service that the filter will match.

allow\_fragments &lt;Boolean&gt;

To allow fragmented packets matching the Filter..

from\_zones &lt;String&gt;

Select to filter on the zone the packet originated from. Possible values = \[any,default\_lan\_zone,internet\_zone,untrusted\_internet\_zone\]

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Filters are applied (automatically redistributed)..

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template\_obj

Description: Use this operation to add the local firewall policy settings

HTTP Method: POST

Request Payload: JSON

{"firewall\_policy\_template\_obj": { "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_policy\_template\_obj":{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template\_obj/

Description: Use this operation to delete the local firewall policy settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template\_obj

Description: Use this operation to get the local firewall policy settings

HTTP Method: GET

Response Payload: JSON

{"firewall\_policy\_template\_obj":\[{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template\_obj

Description: Use this operation to modify the local firewall policy settings

HTTP Method: PUT

Request Payload: JSON

{"firewall\_policy\_template\_obj":{ "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_policy\_template\_obj":\[{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\]}
