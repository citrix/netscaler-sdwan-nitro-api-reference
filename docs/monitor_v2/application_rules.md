application\_rules

Monitoring for This resource provides Application Rules Info resource.

Read/write properties

Read only properties

packets\_dropped &lt;String&gt;

Number of Packets Dropped.

num &lt;String&gt;

Rule Number.

application\_object &lt;String&gt;

Application Object Name.

dpi\_family &lt;String&gt;

DPI Family Name.

lan\_to\_wan\_bytes &lt;String&gt;

Lan to WAN bytes.

dst\_ip\_address &lt;String&gt;

Destination IP Address.

lan\_to\_wan\_packets &lt;String&gt;

LAN to WAN Packets.

src\_port &lt;String&gt;

Source Port.

dpi\_application &lt;String&gt;

DPI Application Name.

wan\_to\_lan\_kbps &lt;String&gt;

WAN to LAN Bandwidth in kbps.

time\_since\_last\_hit &lt;String&gt;

Time Since Last Hit.

bytes\_dropped &lt;String&gt;

Bytes Dropped.

dst\_port &lt;String&gt;

Destination Port.

service &lt;String&gt;

Service Name.

wan\_to\_lan\_packets &lt;String&gt;

WAN to LAN Packets.

src\_ip\_address &lt;String&gt;

Source IP Address.

site &lt;String&gt;

Site Name.

wan\_to\_lan\_bytes &lt;String&gt;

WAN to LAN Bytes.

routing\_domain\_name &lt;String&gt;

Routing Domain Name.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/application\_rules

Description: Use this operation to get Application rules details.Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"application\_rules":\[{ "packets\_dropped":&lt;String\_value&gt;

, "num":&lt;String\_value&gt; , "application\_object":&lt;String\_value&gt; , "dpi\_family":&lt;String\_value&gt; , "lan\_to\_wan\_bytes":&lt;String\_value&gt; , "dst\_ip\_address":&lt;String\_value&gt; , "lan\_to\_wan\_packets":&lt;String\_value&gt; , "src\_port":&lt;String\_value&gt; , "dpi\_application":&lt;String\_value&gt; , "wan\_to\_lan\_kbps":&lt;String\_value&gt; , "time\_since\_last\_hit":&lt;String\_value&gt; , "bytes\_dropped":&lt;String\_value&gt; , "dst\_port":&lt;String\_value&gt; , "service":&lt;String\_value&gt; , "wan\_to\_lan\_packets":&lt;String\_value&gt; , "src\_ip\_address":&lt;String\_value&gt; , "site":&lt;String\_value&gt; , "wan\_to\_lan\_bytes":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; }\]}
