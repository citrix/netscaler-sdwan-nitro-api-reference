firewall\_policy\_template

Configuration Editor for API to add, modify, delete, and get configuration for Firewall policy templates resource.

Read/write properties

pre\_appliance\_policies &lt;firewall\_policy\_template\_obj\[\]&gt;

Pre appliance policies.

post\_appliance\_policies &lt;firewall\_policy\_template\_obj\[\]&gt;

Post appliance policies.

firewall\_policy\_template\_name &lt;String&gt;

Firewall policy template name.

package\_name &lt;String&gt;

Config package name using which the firewall policy template API operation should be performed.. Minimum length = 1 Maximum length = 141

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template

Description: Use this operation to add Firewall policy templates

HTTP Method: POST

Request Payload: JSON

{"firewall\_policy\_template": { "pre\_appliance\_policies":\[{ "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\] , "post\_appliance\_policies":\[{ "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\] , "firewall\_policy\_template\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_policy\_template":{ "pre\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "post\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt; , "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "firewall\_policy\_template\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template/package\_name=&lt;String&gt;,firewall\_policy\_template\_name=&lt;String&gt;

Description: Use this operation to delete Firewall policy templates

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the Firewall policy templates

HTTP Method: GET

Response Payload: JSON

{"firewall\_policy\_template":\[{ "pre\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "post\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt; , "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "firewall\_policy\_template\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template

Description: Use this operation to modify the Firewall policy templates

HTTP Method: PUT

Request Payload: JSON

{"firewall\_policy\_template":{ "pre\_appliance\_policies":\[{ "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\] , "post\_appliance\_policies":\[{ "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\] , "firewall\_policy\_template\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "firewall\_policy\_template":\[{ "pre\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt;

, "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "post\_appliance\_policies":\[{ "priority":&lt;Integer\_value&gt; , "destination\_service\_name":&lt;String\_value&gt; , "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;Integer\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;Integer\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "log\_interval":&lt;Integer\_value&gt; , "track\_connection":&lt;Boolean\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "ip\_protocol\_num":&lt;Integer\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "application":&lt;String\_value&gt; , "log\_connection\_end":&lt;Boolean\_value&gt; , "to\_zones":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "match\_established":&lt;Boolean\_value&gt; , "log\_connection\_start":&lt;Boolean\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;Boolean\_value&gt; , "from\_zones":&lt;String\_value&gt; }\], "firewall\_policy\_template\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }\]}
