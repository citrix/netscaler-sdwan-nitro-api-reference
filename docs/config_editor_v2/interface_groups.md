interface\_groups

Configuration Editor for API to add, modify, delete, and get interface groups. resource.

Read/write properties

is\_bridged &lt;Boolean&gt;

Enable bridge pairs between the selected interfaces..

eth\_interfaces &lt;String\[\]&gt;

Give interface id to be included in ethernet interface.

package\_name &lt;String&gt;

Config package name using which the site API operation should be performed.. Minimum length = 1 Maximum length = 141

bypass\_mode &lt;String&gt;

The behavior of bridge-paired interfaces in the Interface Group in the event of Appliance/Service restart or failure.. Possible values = \[fail\_to\_wire,fail\_to\_block\]

bridge\_pair &lt;bridge\_pair\_obj\[\]&gt;

Add brige pair associated with the group.

security &lt;String&gt;

The security of the Interface Group's network segment. Trusted segments are generally protected by a firewall.. Possible values = \[trusted,untrusted\]

id &lt;Integer&gt;

.

site\_name &lt;String&gt;

Site Name in which interface group should be added.. Minimum length = 1 Maximum length = 42

virtual\_interfaces &lt;virtual\_interfaces\_obj\[\]&gt;

List of virtual interfaces associated with the interface group..

wccp &lt;Boolean&gt;

Enabling this feature will cause the corresponding routing domain's TCP traffic to be redirected to the SD-WAN Optimization appliance for optimization. The listener should be enabled on interface groups with only ONE ethernet interface..

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/interface\_groups

Description: Use this operation to add interface group

HTTP Method: POST

Request Payload: JSON

{"interface\_groups": { "is\_bridged":&lt;Boolean\_value&gt; , "eth\_interfaces":&lt;String\_value\[\]&gt; , "package\_name":&lt;String\_value&gt; , "bypass\_mode":&lt;String\_value&gt; , "bridge\_pair":\[{ "device\_two":&lt;String\_value&gt; , "lsp\_enabled":&lt;Boolean\_value&gt; , "device\_one":&lt;String\_value&gt; }\] , "security":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "virtual\_interfaces":\[{ "firewall\_zone":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "dhcp\_client":&lt;Boolean\_value&gt; , "routing\_domain":&lt;String\_value&gt; , "vlan\_id":&lt;Integer\_value&gt; }\] , "wccp":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "interface\_groups":{ "is\_bridged":&lt;Boolean\_value&gt;

, "eth\_interfaces":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "bypass\_mode":&lt;String\_value&gt; , "bridge\_pair":\[{ "device\_two":&lt;String\_value&gt; , "lsp\_enabled":&lt;Boolean\_value&gt; , "device\_one":&lt;String\_value&gt; }\], "security":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "virtual\_interfaces":\[{ "firewall\_zone":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "dhcp\_client":&lt;Boolean\_value&gt; , "routing\_domain":&lt;String\_value&gt; , "vlan\_id":&lt;Integer\_value&gt; }\], "wccp":&lt;Boolean\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/interface\_groups/site\_name=&lt;String&gt;,package\_name=&lt;String&gt;

Description: Use this operation to delete an interface group.

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/interface\_groups/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the list of interface groups

HTTP Method: GET

Response Payload: JSON

{"interface\_groups":\[{ "is\_bridged":&lt;Boolean\_value&gt;

, "eth\_interfaces":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "bypass\_mode":&lt;String\_value&gt; , "bridge\_pair":\[{ "device\_two":&lt;String\_value&gt; , "lsp\_enabled":&lt;Boolean\_value&gt; , "device\_one":&lt;String\_value&gt; }\], "security":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "virtual\_interfaces":\[{ "firewall\_zone":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "dhcp\_client":&lt;Boolean\_value&gt; , "routing\_domain":&lt;String\_value&gt; , "vlan\_id":&lt;Integer\_value&gt; }\], "wccp":&lt;Boolean\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/interface\_groups

Description: Use this operation to modify a Virtual IP address

HTTP Method: PUT

Request Payload: JSON

{"interface\_groups":{ "is\_bridged":&lt;Boolean\_value&gt; , "eth\_interfaces":&lt;String\_value\[\]&gt; , "package\_name":&lt;String\_value&gt; , "bypass\_mode":&lt;String\_value&gt; , "bridge\_pair":\[{ "device\_two":&lt;String\_value&gt; , "lsp\_enabled":&lt;Boolean\_value&gt; , "device\_one":&lt;String\_value&gt; }\] , "security":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "virtual\_interfaces":\[{ "firewall\_zone":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "dhcp\_client":&lt;Boolean\_value&gt; , "routing\_domain":&lt;String\_value&gt; , "vlan\_id":&lt;Integer\_value&gt; }\] , "wccp":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "interface\_groups":\[{ "is\_bridged":&lt;Boolean\_value&gt;

, "eth\_interfaces":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "bypass\_mode":&lt;String\_value&gt; , "bridge\_pair":\[{ "device\_two":&lt;String\_value&gt; , "lsp\_enabled":&lt;Boolean\_value&gt; , "device\_one":&lt;String\_value&gt; }\], "security":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "virtual\_interfaces":\[{ "firewall\_zone":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "dhcp\_client":&lt;Boolean\_value&gt; , "routing\_domain":&lt;String\_value&gt; , "vlan\_id":&lt;Integer\_value&gt; }\], "wccp":&lt;Boolean\_value&gt; }\]}
