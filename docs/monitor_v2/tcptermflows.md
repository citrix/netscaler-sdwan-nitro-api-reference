tcptermflows

Monitoring for This resource provides details about TCP Terminated flows resource.

Read/write properties

Read only properties

src\_port &lt;String&gt;

Source Port for packets on this flow.

dest\_ip &lt;String&gt;

Destination IP Address for packets on this flow.

from\_wan\_kbps &lt;String&gt;

WAN To LAN kilobits per seconds.

bytes\_pending\_to\_LAN &lt;String&gt;

Number of bytes currently buffered to send to the LAN for this flow.

to\_wan\_kbps &lt;String&gt;

LAN To WAN kilobits per seconds.

src\_ip &lt;String&gt;

Source IP Address for packets on this flow.

age &lt;String&gt;

How long ago this flow was created in milliseconds.

state &lt;String&gt;

Current State of this flow.

bytes\_pending\_to\_WAN &lt;String&gt;

Number of bytes currently buffered to send to the WAN for this flow.

dest\_port &lt;String&gt;

Destination Port for packets on this flow.

ipp &lt;String&gt;

IP Protocol number for packets on this flow.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/tcptermflows

Description: Use this operation to get TCP Termination flows. Filters are supported for this API. max\_stats filter is available as an additional option to filter the flow count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"tcptermflows":\[{ "src\_port":&lt;String\_value&gt;

, "dest\_ip":&lt;String\_value&gt; , "from\_wan\_kbps":&lt;String\_value&gt; , "bytes\_pending\_to\_LAN":&lt;String\_value&gt; , "to\_wan\_kbps":&lt;String\_value&gt; , "src\_ip":&lt;String\_value&gt; , "age":&lt;String\_value&gt; , "state":&lt;String\_value&gt; , "bytes\_pending\_to\_WAN":&lt;String\_value&gt; , "dest\_port":&lt;String\_value&gt; , "ipp":&lt;String\_value&gt; }\]}
