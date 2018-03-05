port\_forwarding\_rules\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Port forwarding rules resource.

Read/write properties

protocol &lt;String&gt;

The IP protocol to forward.. Possible values = \[both,TCP,UDP\]

outside\_port &lt;String&gt;

The Outside port or port range to forward..

log\_connection\_end &lt;Boolean&gt;

To generate a log when a Connection matching this Rule is deleted..

inside\_network\_ip\_address &lt;String&gt;

The Inside IP address to forward to..

track\_connection &lt;Boolean&gt;

Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets matching this Rule. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation --  proceed with caution if NetScaler SD-WAN is not fully inline..

log\_interval &lt;Integer&gt;

The time, in seconds, between logging the number of packets matching the rule (0 = disabled, valid settings are 60-600)..

inside\_port &lt;String&gt;

The Inside port or port range to forward to. If a range is configured, it must define the name number of ports as the Outside Port..

log\_connection\_start &lt;Boolean&gt;

To generate a log when a new Connection is created by a packet matching this Rule..

allow\_fragments &lt;Boolean&gt;

To enable forwarding of packet fragments..

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/port\_forwarding\_rules\_obj

Description: Use this operation to add the Port forwarding rules

HTTP Method: POST

Request Payload: JSON

{"port\_forwarding\_rules\_obj": { "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "port\_forwarding\_rules\_obj":{ "protocol":&lt;String\_value&gt;

, "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/port\_forwarding\_rules\_obj/

Description: Use this operation to delete the Port forwarding rules

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/port\_forwarding\_rules\_obj

Description: Use this operation to get the Port forwarding rules

HTTP Method: GET

Response Payload: JSON

{"port\_forwarding\_rules\_obj":\[{ "protocol":&lt;String\_value&gt;

, "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/port\_forwarding\_rules\_obj

Description: Use this operation to modify the Port forwarding rules

HTTP Method: PUT

Request Payload: JSON

{"port\_forwarding\_rules\_obj":{ "protocol":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "port\_forwarding\_rules\_obj":\[{ "protocol":&lt;String\_value&gt;

, "outside\_port":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "inside\_port":&lt;String\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; }\]}
