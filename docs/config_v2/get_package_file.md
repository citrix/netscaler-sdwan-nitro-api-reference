get\_package\_file

Configuration for Downloads Package File. Note: Please ensure downloaded package name to be saved in zip format for compatibility resource.

Read/write properties

appliance\_type &lt;String&gt;

Appliance type: primary or secondary appliance. Possible values = \[primary,secondary\]

site\_name &lt;String&gt;

Site Name.

package\_type &lt;String&gt;

Download Package Type. Possible values = \[active,staging\]

Read only properties

Operations

[file\_download](#file_download)

[file\_download]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/get\_package\_file?action=file\_download

Description: Use this operation to Download a package from SD-WAN Appliance

HTTP Method: POST

Request Payload: JSON

{"get\_package\_file": { "appliance\_type":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "package\_type":&lt;String\_value&gt; }}

Response Payload: Binary Stream
