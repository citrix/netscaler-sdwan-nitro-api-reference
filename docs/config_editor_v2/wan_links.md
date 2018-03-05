wan\_links

Configuration Editor for API to add, modify, delete, and get configuration for WAN links resource.

Read/write properties

lan\_2\_wan\_physical\_rate &lt;Integer&gt;

LAN to WAN Physical rate in Kbps.

access\_interfaces &lt;access\_interface\[\]&gt;

List of Access Interfaces associated with the wan links group..

public\_ip &lt;String&gt;

Public IP Address of WAN Links.

wan\_2\_lan\_permitted\_rate &lt;Integer&gt;

WAN to LAN Permitted rate in Kbps.

lan\_2\_wan\_permitted\_rate &lt;Integer&gt;

LAN to WAN Permitted rate in Kbps.

package\_name &lt;String&gt;

Config package name using which the wan\_links API operation should be performed.. Minimum length = 1 Maximum length = 141

access\_type &lt;String&gt;

The type of network connected to the WAN link. Possible values = \[public\_internet,private\_intranet,private\_mpls\]

mpls\_queues &lt;mpls\_queue\_obj\[\]&gt;

List of MPLS Queues associated with the wan links group..

wan\_2\_lan\_physical\_rate &lt;Integer&gt;

WAN to LAN Physical rate in Kbps.

wan\_link\_name &lt;String&gt;

WAN Link name. Minimum length = 1 Maximum length = 42

enable\_public\_ip\_learning &lt;Boolean&gt;

Enable public IP learning.

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 42

wan\_link\_template\_name &lt;String&gt;

WAN Link template name.

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/wan\_links

Description: Use this operation to add wan links

HTTP Method: POST

Request Payload: JSON

{"wan\_links": { "lan\_2\_wan\_physical\_rate":&lt;Integer\_value&gt; , "access\_interfaces":\[{ "virtual\_ip\_addr":&lt;String\_value&gt; , "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\] , "public\_ip":&lt;String\_value&gt; , "wan\_2\_lan\_permitted\_rate":&lt;Integer\_value&gt; , "lan\_2\_wan\_permitted\_rate":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "access\_type":&lt;String\_value&gt; , "mpls\_queues":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\] , "wan\_2\_lan\_physical\_rate":&lt;Integer\_value&gt; , "wan\_link\_name":&lt;String\_value&gt; , "enable\_public\_ip\_learning":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_link\_template\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "wan\_links":{ "lan\_2\_wan\_physical\_rate":&lt;Integer\_value&gt;

, "access\_interfaces":\[{ "virtual\_ip\_addr":&lt;String\_value&gt; , "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\], "public\_ip":&lt;String\_value&gt; , "wan\_2\_lan\_permitted\_rate":&lt;Integer\_value&gt; , "lan\_2\_wan\_permitted\_rate":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "access\_type":&lt;String\_value&gt; , "mpls\_queues":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\], "wan\_2\_lan\_physical\_rate":&lt;Integer\_value&gt; , "wan\_link\_name":&lt;String\_value&gt; , "enable\_public\_ip\_learning":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_link\_template\_name":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/wan\_links/site\_name=&lt;String&gt;,wan\_link\_name=&lt;String&gt;,package\_name=&lt;String&gt;

Description: Use this operation to delete a wan link

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/wan\_links/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the list of wan links

HTTP Method: GET

Response Payload: JSON

{"wan\_links":\[{ "lan\_2\_wan\_physical\_rate":&lt;Integer\_value&gt;

, "access\_interfaces":\[{ "virtual\_ip\_addr":&lt;String\_value&gt; , "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\], "public\_ip":&lt;String\_value&gt; , "wan\_2\_lan\_permitted\_rate":&lt;Integer\_value&gt; , "lan\_2\_wan\_permitted\_rate":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "access\_type":&lt;String\_value&gt; , "mpls\_queues":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\], "wan\_2\_lan\_physical\_rate":&lt;Integer\_value&gt; , "wan\_link\_name":&lt;String\_value&gt; , "enable\_public\_ip\_learning":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_link\_template\_name":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/wan\_links

Description: Use this operation to modify a wan link

HTTP Method: PUT

Request Payload: JSON

{"wan\_links":{ "lan\_2\_wan\_physical\_rate":&lt;Integer\_value&gt; , "access\_interfaces":\[{ "virtual\_ip\_addr":&lt;String\_value&gt; , "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\] , "public\_ip":&lt;String\_value&gt; , "wan\_2\_lan\_permitted\_rate":&lt;Integer\_value&gt; , "lan\_2\_wan\_permitted\_rate":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "access\_type":&lt;String\_value&gt; , "mpls\_queues":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\] , "wan\_2\_lan\_physical\_rate":&lt;Integer\_value&gt; , "wan\_link\_name":&lt;String\_value&gt; , "enable\_public\_ip\_learning":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_link\_template\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "wan\_links":\[{ "lan\_2\_wan\_physical\_rate":&lt;Integer\_value&gt;

, "access\_interfaces":\[{ "virtual\_ip\_addr":&lt;String\_value&gt; , "gw\_ip\_addr":&lt;String\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; }\], "public\_ip":&lt;String\_value&gt; , "wan\_2\_lan\_permitted\_rate":&lt;Integer\_value&gt; , "lan\_2\_wan\_permitted\_rate":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "access\_type":&lt;String\_value&gt; , "mpls\_queues":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\], "wan\_2\_lan\_physical\_rate":&lt;Integer\_value&gt; , "wan\_link\_name":&lt;String\_value&gt; , "enable\_public\_ip\_learning":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_link\_template\_name":&lt;String\_value&gt; }\]}
