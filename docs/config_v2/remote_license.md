remote\_license

Configuration for Remote license configuration resource.

Read/write properties

model\_choices &lt;String&gt;

Model choices available on this device.

remote\_license\_ip &lt;String&gt;

Remote license server IP.

model &lt;String&gt;

Model installed from license.

remote\_license\_port &lt;Integer&gt;

Remote license server port. Minimum value = 1 Maximum value = 65535

Read only properties

Operations

[enable\_remote\_server](#enable_remote_server) [get (all)](#get_all) [modify](#modify)

[enable\_remote\_server]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/remote\_license?action=enable\_remote\_server

Description: Activate the remote license configuration

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "remote\_license":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/remote\_license

Description: Use this operation to get the remote license configuration

HTTP Method: GET

Response Payload: JSON

{"remote\_license":\[{ "model\_choices":&lt;String\_value&gt;

, "remote\_license\_ip":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "remote\_license\_port":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/remote\_license

Description: Update the remote license configuration

HTTP Method: PUT

Request Payload: JSON

{"remote\_license":{ "model\_choices":&lt;String\_value&gt; , "remote\_license\_ip":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "remote\_license\_port":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "remote\_license":\[{ "model\_choices":&lt;String\_value&gt;

, "remote\_license\_ip":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "remote\_license\_port":&lt;Integer\_value&gt; }\]}
