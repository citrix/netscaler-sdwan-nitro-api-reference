virtualpaths

Configuration Editor for API to add, modify, delete, and get virtual paths resource.

Read/write properties

local\_site\_name &lt;String&gt;

Local Site name. Minimum length = 1

local\_site &lt;virtual\_path\_site\[\]&gt;

Virtual Path Local Site configuration.

dynamic\_virtual\_path &lt;dynamic\_virtual\_path\_obj\[\]&gt;

Dynamic Virtual Path configuration.

remote\_site\_name &lt;String&gt;

Remote Site name. Minimum length = 1

package\_name &lt;String&gt;

Config package name using which the wan\_links API operation should be performed.. Minimum length = 1 Maximum length = 141

paths &lt;path\_obj\[\]&gt;

Path Configuration for Virtual Paths.

reverse &lt;Boolean&gt;

It should create reverse virtual Path also.

remote\_site &lt;virtual\_path\_site\[\]&gt;

Virtual Path Remote Site configuration.

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtualpaths

Description: Use this operation to add virtual paths

HTTP Method: POST

Request Payload: JSON

{"virtualpaths": { "local\_site\_name":&lt;String\_value&gt; , "local\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\] , "dynamic\_virtual\_path":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt; , "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\] , "remote\_site\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "paths":\[{ "from\_wan\_link\_name":&lt;String\_value&gt; , "ip\_dscp\_tagging":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "reverse\_tracking\_ip\_address":&lt;String\_value&gt; , "bad\_loss\_sensitive":&lt;String\_value&gt; , "from\_site\_name":&lt;String\_value&gt; , "instability\_sensitive":&lt;Boolean\_value&gt; , "to\_site\_name":&lt;String\_value&gt; , "enable\_encryption":&lt;Boolean\_value&gt; , "silence\_period":&lt;Integer\_value&gt; , "static\_path":&lt;Boolean\_value&gt; , "to\_wan\_link\_name":&lt;String\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; }\] , "reverse":&lt;Boolean\_value&gt; , "remote\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\] }}

Response Payload: JSON

{ "virtualpaths":{ "local\_site\_name":&lt;String\_value&gt;

, "local\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\], "dynamic\_virtual\_path":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt; , "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\], "remote\_site\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "paths":\[{ "from\_wan\_link\_name":&lt;String\_value&gt; , "ip\_dscp\_tagging":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "reverse\_tracking\_ip\_address":&lt;String\_value&gt; , "bad\_loss\_sensitive":&lt;String\_value&gt; , "from\_site\_name":&lt;String\_value&gt; , "instability\_sensitive":&lt;Boolean\_value&gt; , "to\_site\_name":&lt;String\_value&gt; , "enable\_encryption":&lt;Boolean\_value&gt; , "silence\_period":&lt;Integer\_value&gt; , "static\_path":&lt;Boolean\_value&gt; , "to\_wan\_link\_name":&lt;String\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; }\], "reverse":&lt;Boolean\_value&gt; , "remote\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\]}\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtualpaths/package\_name=&lt;String&gt;,remote\_site\_name=&lt;String&gt;,local\_site\_name=&lt;String&gt;

Description: Use this operation to delete a virtual paths

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtualpaths/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the list of virtual paths

HTTP Method: GET

Response Payload: JSON

{"virtualpaths":\[{ "local\_site\_name":&lt;String\_value&gt;

, "local\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\], "dynamic\_virtual\_path":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt; , "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\], "remote\_site\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "paths":\[{ "from\_wan\_link\_name":&lt;String\_value&gt; , "ip\_dscp\_tagging":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "reverse\_tracking\_ip\_address":&lt;String\_value&gt; , "bad\_loss\_sensitive":&lt;String\_value&gt; , "from\_site\_name":&lt;String\_value&gt; , "instability\_sensitive":&lt;Boolean\_value&gt; , "to\_site\_name":&lt;String\_value&gt; , "enable\_encryption":&lt;Boolean\_value&gt; , "silence\_period":&lt;Integer\_value&gt; , "static\_path":&lt;Boolean\_value&gt; , "to\_wan\_link\_name":&lt;String\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; }\], "reverse":&lt;Boolean\_value&gt; , "remote\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\]}\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtualpaths

Description: Use this operation to modify a virtual paths

HTTP Method: PUT

Request Payload: JSON

{"virtualpaths":{ "local\_site\_name":&lt;String\_value&gt; , "local\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\] , "dynamic\_virtual\_path":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt; , "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\] , "remote\_site\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "paths":\[{ "from\_wan\_link\_name":&lt;String\_value&gt; , "ip\_dscp\_tagging":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "reverse\_tracking\_ip\_address":&lt;String\_value&gt; , "bad\_loss\_sensitive":&lt;String\_value&gt; , "from\_site\_name":&lt;String\_value&gt; , "instability\_sensitive":&lt;Boolean\_value&gt; , "to\_site\_name":&lt;String\_value&gt; , "enable\_encryption":&lt;Boolean\_value&gt; , "silence\_period":&lt;Integer\_value&gt; , "static\_path":&lt;Boolean\_value&gt; , "to\_wan\_link\_name":&lt;String\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; }\] , "reverse":&lt;Boolean\_value&gt; , "remote\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\] }}

Response Payload: JSON

{ "virtualpaths":\[{ "local\_site\_name":&lt;String\_value&gt;

, "local\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\], "dynamic\_virtual\_path":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt; , "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\], "remote\_site\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "paths":\[{ "from\_wan\_link\_name":&lt;String\_value&gt; , "ip\_dscp\_tagging":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "reverse\_tracking\_ip\_address":&lt;String\_value&gt; , "bad\_loss\_sensitive":&lt;String\_value&gt; , "from\_site\_name":&lt;String\_value&gt; , "instability\_sensitive":&lt;Boolean\_value&gt; , "to\_site\_name":&lt;String\_value&gt; , "enable\_encryption":&lt;Boolean\_value&gt; , "silence\_period":&lt;Integer\_value&gt; , "static\_path":&lt;Boolean\_value&gt; , "to\_wan\_link\_name":&lt;String\_value&gt; , "reverse\_also":&lt;Boolean\_value&gt; }\], "reverse":&lt;Boolean\_value&gt; , "remote\_site":\[{ "route\_cost":&lt;Integer\_value&gt; , "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\]}\]}
