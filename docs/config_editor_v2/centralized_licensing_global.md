centralized\_licensing\_global

Configuration Editor for API to modify, get, global settings for centralized licensing resource.

Read/write properties

enable &lt;Boolean&gt;

enable/disable centralized licensing.

remote\_server\_port &lt;Integer&gt;

Remote licensing server port. Maximum value = 65535

remote\_server\_ip &lt;String&gt;

Remote licensing server ip address.

package\_name &lt;String&gt;

Config package name using which the licensing API operation should be performed.. Minimum length = 1 Maximum length = 141

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/centralized\_licensing\_global/package\_name=&lt;package\_name&gt;

Description: Use this operation to get global centralized license properties

HTTP Method: GET

Response Payload: JSON

{"centralized\_licensing\_global":\[{ "enable":&lt;Boolean\_value&gt;

, "remote\_server\_port":&lt;Integer\_value&gt; , "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/centralized\_licensing\_global

Description: Use this operation to modify global centralized license properties

HTTP Method: PUT

Request Payload: JSON

{"centralized\_licensing\_global":{ "enable":&lt;Boolean\_value&gt; , "remote\_server\_port":&lt;Integer\_value&gt; , "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "centralized\_licensing\_global":\[{ "enable":&lt;Boolean\_value&gt;

, "remote\_server\_port":&lt;Integer\_value&gt; , "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; }\]}
