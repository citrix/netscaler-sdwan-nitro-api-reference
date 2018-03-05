virtual\_ip\_addresses

Configuration Editor for API to add, modify, delete, and get Virtual IP Address resource.

Read/write properties

is\_private &lt;Boolean&gt;

If enabled, the Virtual IP Address will only be routable on the local Appliance.

is\_identity &lt;Boolean&gt;

If enabled, the Virtual IP Address will be used for IP services.

package\_name &lt;String&gt;

Config package name using which the virtual\_ip\_addresses API operation should be performed.. Minimum length = 1 Maximum length = 141

is\_auto &lt;Boolean&gt;

.

virtual\_interface\_name &lt;String&gt;

Enter one of the associated Virtual Interfaces. Minimum length = 1 Maximum length = 42

ip\_address &lt;String&gt;

IP Address with prefix.

id &lt;Integer&gt;

Auto-generated ID. Use this ID to modify or delete a Virtual IP address.

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 42

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtual\_ip\_addresses

Description: Use this operation to add a Virtual IP address

HTTP Method: POST

Request Payload: JSON

{"virtual\_ip\_addresses": { "is\_private":&lt;Boolean\_value&gt; , "is\_identity":&lt;Boolean\_value&gt; , "package\_name":&lt;String\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "virtual\_ip\_addresses":{ "is\_private":&lt;Boolean\_value&gt;

, "is\_identity":&lt;Boolean\_value&gt; , "package\_name":&lt;String\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtual\_ip\_addresses/package\_name=&lt;String&gt;

Description: Use this operation to delete a Virtual IP address

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtual\_ip\_addresses/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the list of Virtual IP addresses

HTTP Method: GET

Response Payload: JSON

{"virtual\_ip\_addresses":\[{ "is\_private":&lt;Boolean\_value&gt;

, "is\_identity":&lt;Boolean\_value&gt; , "package\_name":&lt;String\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtual\_ip\_addresses

Description: Use this operation to modify a Virtual IP address

HTTP Method: PUT

Request Payload: JSON

{"virtual\_ip\_addresses":{ "is\_private":&lt;Boolean\_value&gt; , "is\_identity":&lt;Boolean\_value&gt; , "package\_name":&lt;String\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "virtual\_ip\_addresses":\[{ "is\_private":&lt;Boolean\_value&gt;

, "is\_identity":&lt;Boolean\_value&gt; , "package\_name":&lt;String\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "virtual\_interface\_name":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}
