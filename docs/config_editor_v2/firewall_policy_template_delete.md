firewall\_policy\_template\_delete

Configuration Editor for API to delete a firewall template for a site resource.

Read/write properties

template\_name &lt;String&gt;

firewall policy template name.

package\_name &lt;String&gt;

Config package name using which the API operation should be performed.. Minimum length = 1 Maximum length = 141

site\_name &lt;String&gt;

Site Name. Minimum length = 1 Maximum length = 42

Read only properties

Operations

[delete](#delete)

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_policy\_template\_delete/site\_name=&lt;String&gt;,package\_name=&lt;String&gt;,template\_name=&lt;String&gt;

Description: Use this operation to delete the firewall related policy templates

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }
