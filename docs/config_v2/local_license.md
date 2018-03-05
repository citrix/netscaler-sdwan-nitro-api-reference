local\_license

Configuration for Local license configuration resource.

Read/write properties

file\_name &lt;String&gt;

File name to be used for apply/uninstall license.

Read only properties

uploaded\_files &lt;String&gt;

List of license files uploaded.

installed\_files &lt;String&gt;

List of license files installed.

Operations

[get\_uploaded\_licenses](#get_uploaded_licenses) [uninstall\_license](#uninstall_license) [get (all)](#get_all) [enable\_local\_server](#enable_local_server) [apply\_license](#apply_license)

[get\_uploaded\_licenses]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_license?action=get\_uploaded\_licenses

Description: Use this operation to get the list of local license files uploaded

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "local\_license":{}}

[uninstall\_license]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_license?action=uninstall\_license

Description: Apply new local license file (already uploaded). Action will also enable the local license and disbale remote license.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "local\_license":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_license

Description: Use this operation to get the list of local license files applied

HTTP Method: GET

Response Payload: JSON

{"local\_license":\[{ "uploaded\_files":&lt;String\_value&gt;

, "file\_name":&lt;String\_value&gt; , "installed\_files":&lt;String\_value&gt; }\]}

[enable\_local\_server]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_license?action=enable\_local\_server

Description: Activate the local license configuration

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "local\_license":{}}

[apply\_license]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_license?action=apply\_license

Description: Apply new local license file (already uploaded). Action will also enable the local license and disbale remote license.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "local\_license":{}}
