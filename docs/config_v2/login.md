login

Configuration for Login resource.

Read/write properties

password &lt;String&gt;

Authentication Password.

username &lt;String&gt;

User Name. Minimum length = 1 Maximum length = 64

Read only properties

Operations

[add](#add) [delete](#delete)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/login

Description: Use this operation to Login To SD-WAN Appliance

HTTP Method: POST

Request Payload: JSON

{"login": { "password":&lt;String\_value&gt; , "username":&lt;String\_value&gt; }}

Response Payload: JSON

{ "login":{ "password":&lt;String\_value&gt;

, "username":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/login/

Description: Use this operation to Logout From SD-WAN Appliance

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }
