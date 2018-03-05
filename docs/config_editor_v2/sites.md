sites

Configuration Editor for API to add, modify, delete, and get sites. resource.

Read/write properties

site\_location &lt;String&gt;

Site location.. Minimum length = 1 Maximum length = 1000

mode &lt;String&gt;

Operating mode of this site. Possible values = \[primary\_mcn,secondary\_mcn,primary\_rcn,secondary\_rcn,client\]

region &lt;String&gt;

Region to which the site belongs to. Minimum length = 1 Maximum length = 42

model &lt;String&gt;

site model. Possible values = \[cb210,cb400,cb410,cb1000,cb2000,cb2100,cb4000,cb4100,cb5100,cbvpx,cbvpxl\]

secure\_key &lt;String&gt;

Hexadecimal secure key used for encryption and membership verification in the Virtual WAN network. This field is optional. If the value is not provided, API generates the secure key.. Minimum length = 8 Maximum length = 32

package\_name &lt;String&gt;

Config package name using which the site API operation should be performed.. Minimum length = 1 Maximum length = 141

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 32

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/sites

Description: Use this operation to add site

HTTP Method: POST

Request Payload: JSON

{"sites": { "site\_location":&lt;String\_value&gt; , "mode":&lt;String\_value&gt; , "region":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "secure\_key":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "sites":{ "site\_location":&lt;String\_value&gt;

, "mode":&lt;String\_value&gt; , "region":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "secure\_key":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/sites/site\_name=&lt;String&gt;,package\_name=&lt;String&gt;

Description: Use this operation to delete a site

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/sites/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the list of sites

HTTP Method: GET

Response Payload: JSON

{"sites":\[{ "site\_location":&lt;String\_value&gt;

, "mode":&lt;String\_value&gt; , "region":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "secure\_key":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/sites

Description: Use this operation to modify site

HTTP Method: PUT

Request Payload: JSON

{"sites":{ "site\_location":&lt;String\_value&gt; , "mode":&lt;String\_value&gt; , "region":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "secure\_key":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "sites":\[{ "site\_location":&lt;String\_value&gt;

, "mode":&lt;String\_value&gt; , "region":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "secure\_key":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; }\]}
