rules

Monitoring for This resource provides Rules Info resource.

Read/write properties

Read only properties

packets\_dropped &lt;String&gt;

Packets Dropped.

last\_wan\_to\_lan\_latency &lt;String&gt;

Last WAN to LAN Latency.

avg\_wan\_to\_lan\_latency &lt;String&gt;

Avg WAN to LAN Latency.

num &lt;String&gt;

Rule Number.

max\_wan\_to\_lan\_latency &lt;String&gt;

Max WAN to LAN Latency.

min\_wan\_to\_lan\_latency &lt;String&gt;

Min WAN to LAN Latency.

ip\_dscp &lt;String&gt;

DSCP IP.

lan\_to\_wan\_bytes &lt;String&gt;

Lan to WAN bytes.

dst\_ip\_address &lt;String&gt;

Dst IP Address.

lan\_to\_wan\_packets &lt;String&gt;

LAN to WAN Packets.

wan\_to\_lan\_kbps &lt;String&gt;

WAN to LAN Bandwidth.

src\_port &lt;String&gt;

Src Port.

ip\_proto &lt;String&gt;

IP Protocol.

time\_since\_last\_hit &lt;String&gt;

Time Since Last Hit.

bytes\_dropped &lt;String&gt;

Bytes Dropped.

dst\_port &lt;String&gt;

Destination Port.

wan\_to\_lan\_jitter &lt;String&gt;

WAN to LAN Jitter.

service &lt;String&gt;

Service Name.

vlan\_id &lt;String&gt;

VLAN ID.

wan\_to\_lan\_packets &lt;String&gt;

WAN to LAN Packets.

src\_ip\_address &lt;String&gt;

Src IP Address.

site &lt;String&gt;

Site Name.

wan\_to\_lan\_bytes &lt;String&gt;

WAN to LAN Bytes.

wan\_to\_lan\_packets\_lost &lt;String&gt;

WAN to LAN Packets Lost.

routing\_domain\_name &lt;String&gt;

Routing Domain Name.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/rules

Description: Use this operation to get Rules details. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"rules":\[{ "packets\_dropped":&lt;String\_value&gt;

, "last\_wan\_to\_lan\_latency":&lt;String\_value&gt; , "avg\_wan\_to\_lan\_latency":&lt;String\_value&gt; , "num":&lt;String\_value&gt; , "max\_wan\_to\_lan\_latency":&lt;String\_value&gt; , "min\_wan\_to\_lan\_latency":&lt;String\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "lan\_to\_wan\_bytes":&lt;String\_value&gt; , "dst\_ip\_address":&lt;String\_value&gt; , "lan\_to\_wan\_packets":&lt;String\_value&gt; , "wan\_to\_lan\_kbps":&lt;String\_value&gt; , "src\_port":&lt;String\_value&gt; , "ip\_proto":&lt;String\_value&gt; , "time\_since\_last\_hit":&lt;String\_value&gt; , "bytes\_dropped":&lt;String\_value&gt; , "dst\_port":&lt;String\_value&gt; , "wan\_to\_lan\_jitter":&lt;String\_value&gt; , "service":&lt;String\_value&gt; , "vlan\_id":&lt;String\_value&gt; , "wan\_to\_lan\_packets":&lt;String\_value&gt; , "src\_ip\_address":&lt;String\_value&gt; , "site":&lt;String\_value&gt; , "wan\_to\_lan\_bytes":&lt;String\_value&gt; , "wan\_to\_lan\_packets\_lost":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; }\]}
