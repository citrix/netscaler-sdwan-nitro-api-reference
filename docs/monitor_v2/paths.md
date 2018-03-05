paths

Monitoring for This resource provides details of all the paths in Appliance resource.

Read/write properties

Read only properties

path\_service\_state &lt;String&gt;

Path Service State.

to\_link &lt;String&gt;

Name of the Path(To Link).

path\_service\_type &lt;String&gt;

Path Service Type.

bandwidth &lt;Float&gt;

Path's Bandwidth in kbps.

packet\_loss &lt;Float&gt;

Path's Packet Loss.

path\_state &lt;String&gt;

Path State.

jitter &lt;Integer&gt;

Path's Jitter value.

congestion &lt;String&gt;

Path's congestion state.

bowt &lt;Integer&gt;

Best One Way Time Latency.

from\_link &lt;String&gt;

Name of the Path(From Link).

mtu &lt;Integer&gt;

Maximum Transferable Unit.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/paths

Description: Use this operation to get Paths Summary. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"paths":\[{ "path\_service\_state":&lt;String\_value&gt;

, "to\_link":&lt;String\_value&gt; , "path\_service\_type":&lt;String\_value&gt; , "bandwidth":&lt;Float\_value&gt; , "packet\_loss":&lt;Float\_value&gt; , "path\_state":&lt;String\_value&gt; , "jitter":&lt;Integer\_value&gt; , "congestion":&lt;String\_value&gt; , "bowt":&lt;Integer\_value&gt; , "from\_link":&lt;String\_value&gt; , "mtu":&lt;Integer\_value&gt; }\]}
