firewall\_settings\_delete

Configuration Editor for API delete configuration for Basic and Advanced Firewall settings resource.

Read/write properties

package\_name &lt;String&gt;

Config package name using which the API operation should be performed.. Minimum length = 1 Maximum length = 141

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 42

Read only properties

Operations

[delete](#delete)

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_settings\_delete/site\_name=&lt;String&gt;,package\_name=&lt;String&gt;

Description: Use this operation to delete the basic and advanced firewall settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }
