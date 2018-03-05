config\_packages

Configuration for API to get, export to Change Management, compile and delete config packages resource.

Read/write properties

package\_name &lt;String&gt;

Name of the config package. Minimum length = 1 Maximum length = 141

Read only properties

audits &lt;audit\_obj&gt;

Config package compilation results..

Operations

[compile](#compile) [add](#add) [delete](#delete) [get (all)](#get_all) [export\_to\_cm](#export_to_cm)

[compile]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/config\_packages?action=compile

Description: Use this operation to compile the configuration package to get audit errors/warnings list.

HTTP Method: POST

{"config\_packages": { "package\_name":&lt;String&gt; }}

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt;}

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/config\_packages

Description: Use this operation to create new configuration package.

HTTP Method: POST

Request Payload: JSON

{"config\_packages": { "package\_name":&lt;String\_value&gt; }}

Response Payload: JSON

{ "config\_packages":{ "package\_name":&lt;String\_value&gt;

, "audits":&lt;audit\_obj\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/config\_packages/package\_name=&lt;String&gt;

Description: Use this operation to delete config package from change management

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/config\_packages

Description: Use this operation to get the config package information

HTTP Method: GET

Response Payload: JSON

{"config\_packages":\[{ "package\_name":&lt;String\_value&gt;

, "audits":&lt;audit\_obj\_value&gt; }\]}

[export\_to\_cm]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/config\_packages?action=export\_to\_cm

Description: Use this operation to export the configuration package to change management

HTTP Method: POST

{"config\_packages": { "package\_name":&lt;String&gt; }}

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt;}
