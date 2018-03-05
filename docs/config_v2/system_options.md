system\_options

Configuration for System-Options resource.

Read/write properties

Read only properties

os\_ver &lt;String&gt;

OS Version.

serial\_no &lt;String&gt;

Serial Number of the system.

model &lt;String&gt;

Model Of the system.

service\_uptime &lt;String&gt;

Service up time. Will be shown once Virtual WAN is Enabled.

appliance\_mode &lt;String&gt;

Appliance Mode.

sw\_version &lt;String&gt;

S/W Version The Site is currently running on.

license\_state &lt;Boolean&gt;

The appliance is licensed or not.

system\_time &lt;String&gt;

Shows the current time of system.

appliance\_uptime &lt;String&gt;

Uptime of the appliance (Will be shown once Virtual WAN is enabled).

product &lt;String&gt;

Product name..

site\_name &lt;String&gt;

Site Name.

management\_ip &lt;String&gt;

Management IP Of System.

Operations

[reboot](#reboot) [get (all)](#get_all)

[reboot]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/system\_options?action=reboot

Description: Reboots the SD-WAN Appliance

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "system\_options":{}}

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/system\_options

Description: Get System Information.

HTTP Method: GET

Response Payload: JSON

{"system\_options":\[{ "os\_ver":&lt;String\_value&gt;

, "serial\_no":&lt;String\_value&gt; , "model":&lt;String\_value&gt; , "service\_uptime":&lt;String\_value&gt; , "appliance\_mode":&lt;String\_value&gt; , "sw\_version":&lt;String\_value&gt; , "license\_state":&lt;Boolean\_value&gt; , "system\_time":&lt;String\_value&gt; , "appliance\_uptime":&lt;String\_value&gt; , "product":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "management\_ip":&lt;String\_value&gt; }\]}
