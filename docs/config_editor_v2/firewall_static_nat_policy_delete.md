firewall\_static\_nat\_policy\_delete

Configuration Editor for API delete configuration for Firewall Static NAT Policy resource.

Read/write properties

package\_name &lt;String&gt;

Config package name using which the API operation should be performed.. Minimum length = 1 Maximum length = 141

id &lt;Integer&gt;

Firewall local policy id.

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 42

Read only properties

Operations

[delete](#delete)

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_static\_nat\_policy\_delete/site\_name=&lt;String&gt;,id=&lt;Integer&gt;,package\_name=&lt;String&gt;

Description: Use this operation to delete the basic and advanced firewall Static NAT Policy

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }
