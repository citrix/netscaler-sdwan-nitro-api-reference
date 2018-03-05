license\_info

Configuration for License configuration state resource.

Read/write properties

Read only properties

license\_location &lt;String&gt;

States whether local license or remote license is applied.

local\_license\_server\_hostid &lt;String&gt;

HostId to be used while requesting license (local).

action\_required &lt;String&gt;

Actions required around license like expired-license, bad remote server status.

maintenance\_expiry &lt;String&gt;

Maintenance expiry date by the current installed license.

remote\_license\_ip &lt;String&gt;

Remote license server IP.

license\_type &lt;String&gt;

Describes type of license eg. retail, evaluation etc.

max\_bw &lt;String&gt;

Max bandwidth installed from license.

model &lt;String&gt;

Model installed from license.

system\_platform &lt;String&gt;

System platform of device.

remote\_license\_port &lt;String&gt;

Remote license server port.

remote\_license\_status &lt;String&gt;

Remote license installation status.

state &lt;String&gt;

Licensed/Unlicensed.

license\_expiry &lt;String&gt;

Expiry date of the current installed license.

remote\_server\_status &lt;String&gt;

Remote license server connectivity status.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/license\_info

Description: Use this operation to get the current license configuration state

HTTP Method: GET

Response Payload: JSON

{"license\_info":\[{ "license\_location":&lt;String\_value&gt;

, "local\_license\_server\_hostid":&lt;String\_value&gt; , "action\_required":&lt;String\_value&gt; , "maintenance\_expiry":&lt;String\_value&gt; , "remote\_license\_ip":&lt;String\_value&gt; , "license\_type":&lt;String\_value&gt; , "max\_bw":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "system\_platform":&lt;String\_value&gt; , "remote\_license\_port":&lt;String\_value&gt; , "remote\_license\_status":&lt;String\_value&gt; , "state":&lt;String\_value&gt; , "license\_expiry":&lt;String\_value&gt; , "remote\_server\_status":&lt;String\_value&gt; }\]}
