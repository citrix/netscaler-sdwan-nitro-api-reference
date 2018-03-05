os\_partition

Configuration for Os Partition Operations resource.

Read/write properties

Read only properties

active\_os &lt;String&gt;

Current Active OS Partition Version.

backup\_os &lt;String&gt;

Backup OS Partition Version.

partition\_files &lt;String&gt;

List of OS Partition files uploaded.

Operations

[install](#install) [switch](#switch) [clear](#clear) [get (all)](#get_all)

[install]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/os\_partition?action=install

Description: Install the uploaded partition as backup OS

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "os\_partition":{}}

[switch]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/os\_partition?action=switch

Description: Switch Between active and backup OS

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "os\_partition":{}}

[clear]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/os\_partition?action=clear

Description: Deletes Uploaded OS Partition Files

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "os\_partition":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/os\_partition

Description: Use this operation to Get The OS Partition Version

HTTP Method: GET

Response Payload: JSON

{"os\_partition":\[{ "active\_os":&lt;String\_value&gt;

, "backup\_os":&lt;String\_value&gt; , "partition\_files":&lt;String\_value&gt; }\]}
