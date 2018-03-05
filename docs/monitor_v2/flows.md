flows

Monitoring for This resource provides details about LAN TO WAN and WAN TO LAN flows resource.

Read/write properties

Read only properties

bytes &lt;String&gt;

Number of bytes sent over the life of the flow.

dest\_ip &lt;String&gt;

Destination IP Address for packets on this flow.

packets &lt;String&gt;

Number of packets sent over the life of the flow.

src\_ip &lt;String&gt;

Source IP Address for packets on this flow.

age &lt;String&gt;

How long ago this flow was created in milliseconds.

transmission\_type &lt;String&gt;

The Transmission Type that the traffic is currently using.

ip\_dscp &lt;String&gt;

IP DSCP tag setting for packets on this flow.

direction &lt;String&gt;

Direction for packets on this flow.

service\_name &lt;String&gt;

Flow Service Name.

class\_type &lt;String&gt;

Type of virtual path class that traffic is using.

dest\_port &lt;String&gt;

Destination Port for packets on this flow.

ipp &lt;String&gt;

IP Protocol number for packets on this flow.

vpathclass &lt;String&gt;

ID of virtual path class that traffic is using.

app\_rule\_id &lt;String&gt;

ID of the app rule that traffic on this flow is matched.

service\_type &lt;String&gt;

Flow Service Type.

src\_port &lt;String&gt;

Source Port for packets on this flow.

hitcount &lt;String&gt;

The Number of times this flow has been searched for and found.

pps &lt;String&gt;

Packets per second over period since refresh.

customer\_kbps &lt;String&gt;

Kilobits per second over period since refresh.

path &lt;String&gt;

Path that the traffic is currently using.

rule\_id &lt;String&gt;

ID of the rule that traffic on this flow is matched.

virtual\_path\_overhead\_kbps &lt;String&gt;

Kilobits per second over period since refresh.

ipsec\_overhead\_kbps &lt;String&gt;

Kilobits per second over period since refresh.

hdr\_compression\_bytes &lt;String&gt;

Number of saved bytes to header compression.

lan\_gw\_ip &lt;String&gt;

IP Address for LAN Gateway.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/flows

Description: Use this operation to get the LAN TO WAN and WAN TO LAN flows details. Filters are supported for this API, max\_stats filter is available as an additional option to filter the flows count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"flows":\[{ "bytes":&lt;String\_value&gt;

, "dest\_ip":&lt;String\_value&gt; , "packets":&lt;String\_value&gt; , "src\_ip":&lt;String\_value&gt; , "age":&lt;String\_value&gt; , "transmission\_type":&lt;String\_value&gt; , "ip\_dscp":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "class\_type":&lt;String\_value&gt; , "dest\_port":&lt;String\_value&gt; , "ipp":&lt;String\_value&gt; , "vpathclass":&lt;String\_value&gt; , "app\_rule\_id":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "src\_port":&lt;String\_value&gt; , "hitcount":&lt;String\_value&gt; , "pps":&lt;String\_value&gt; , "customer\_kbps":&lt;String\_value&gt; , "path":&lt;String\_value&gt; , "rule\_id":&lt;String\_value&gt; , "virtual\_path\_overhead\_kbps":&lt;String\_value&gt; , "ipsec\_overhead\_kbps":&lt;String\_value&gt; , "hdr\_compression\_bytes":&lt;String\_value&gt; , "lan\_gw\_ip":&lt;String\_value&gt; }\]}
