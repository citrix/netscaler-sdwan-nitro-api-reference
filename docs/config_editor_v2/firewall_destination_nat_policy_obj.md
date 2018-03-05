firewall\_destination\_nat\_policy\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Destination NAT policy settings resource.

Read/write properties

service\_type &lt;String&gt;

The Service Type that the translation applies to.. Possible values = \[local,internet,intranet\]

outside\_network\_ip\_address &lt;String&gt;

The Outside IP Address packets will be translated to (Destination IP Address in the direction selected)..

outside\_port &lt;Integer&gt;

The Outside Port packets will be translated to (Destination port in the direction selected(0: do not NAT the Port))..

direction &lt;String&gt;

The direction, from the Service or Virtual Interface perspective, the translation will operate.. Possible values = \[inbound,outbound\]

inside\_network\_ip\_address &lt;String&gt;

The Inside IP Address and Prefix to translate (Destination IP Address in the direction selected)..

service\_name &lt;String&gt;

The Service Name that the translation applies to..

inside\_port &lt;String&gt;

The Inside Port or port range to translate (Destination port/port range in the direction selected)..

id &lt;Integer&gt;

Firewall destination NATs policy id.

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Filters are applied (automatically redistributed)..

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_destination\_nat\_policy\_obj

Description: Use this operation to add the Destination NAT policy settings

HTTP Method: POST

Request Payload: JSON

{"firewall\_destination\_nat\_policy\_obj": { "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;Integer\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "firewall\_destination\_nat\_policy\_obj":{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;Integer\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_destination\_nat\_policy\_obj/

Description: Use this operation to delete the Destination NAT policy settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_destination\_nat\_policy\_obj

Description: Use this operation to get the Destination NAT policy settings

HTTP Method: GET

Response Payload: JSON

{"firewall\_destination\_nat\_policy\_obj":\[{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;Integer\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_destination\_nat\_policy\_obj

Description: Use this operation to modify the Destination NAT policy settings

HTTP Method: PUT

Request Payload: JSON

{"firewall\_destination\_nat\_policy\_obj":{ "service\_type":&lt;String\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;Integer\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "firewall\_destination\_nat\_policy\_obj":\[{ "service\_type":&lt;String\_value&gt;

, "priority":&lt;Integer\_value&gt; , "outside\_network\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;Integer\_value&gt; , "direction":&lt;String\_value&gt; , "inside\_network\_ip\_address":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; }\]}
