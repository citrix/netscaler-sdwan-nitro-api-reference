firewall\_connection\_stats

Monitoring for This resource provides Firewall Connection Stats resource.

Read/write properties

Read only properties

destination\_route\_type &lt;String&gt;

Destination Service Type for the connection.

source\_firewall\_zone\_name &lt;String&gt;

Source Zone for the connection.

last\_activity\_ms &lt;String&gt;

Indicates time in milliseconds since last activity on this connection.

dpi\_application\_name &lt;String&gt;

The application for the connection.

destination\_ip\_addr &lt;String&gt;

Destination IP address for the connection.

packets\_received &lt;String&gt;

Packets Received on the connection.

destination\_port &lt;String&gt;

Destination Port for the connection.

source\_port &lt;String&gt;

Source Port for the connection.

receive\_bytes\_dropped &lt;String&gt;

Receive Bytes Dropped on the connection.

state &lt;String&gt;

The State of this connection.

ip\_protocol &lt;String&gt;

IP Protocol for the connection.

bytes\_sent &lt;String&gt;

Bytes Sent on the connection.

packets\_sent &lt;String&gt;

Packets Sent on the connection.

destination\_firewall\_zone\_name &lt;String&gt;

Destination Zone for the connection.

destination\_route\_service\_name &lt;String&gt;

Destination Service Type for the connection.

age\_ms &lt;String&gt;

Age in Milliseconds of the connection.

receive\_packets\_dropped &lt;String&gt;

Receive Packets Dropped on the connection.

bytes\_received &lt;String&gt;

Bytes Received on the connection.

source\_route\_service\_name &lt;String&gt;

Source Service Type for the connection.

source\_route\_type &lt;String&gt;

Source Service Type for the connection.

sent\_packets\_dropped &lt;String&gt;

Sent Packets Dropped on the connection.

source\_ip\_addr &lt;String&gt;

Source IP address for the connection.

routing\_domain\_name &lt;String&gt;

Routing Domain of the connection.

dpi\_family\_name &lt;String&gt;

The family for the connection.

is\_nat &lt;String&gt;

Indicates if this connection makes use of NAT Policies.

sent\_bytes\_dropped &lt;String&gt;

Sent Bytes Dropped on the connection.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/firewall\_connection\_stats

Description: Use this operation to get the Firewall Connection Stats, max\_stats filter is available as an additional option to filter the connection count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"firewall\_connection\_stats":\[{ "destination\_route\_type":&lt;String\_value&gt;

, "source\_firewall\_zone\_name":&lt;String\_value&gt; , "last\_activity\_ms":&lt;String\_value&gt; , "dpi\_application\_name":&lt;String\_value&gt; , "destination\_ip\_addr":&lt;String\_value&gt; , "packets\_received":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "receive\_bytes\_dropped":&lt;String\_value&gt; , "state":&lt;String\_value&gt; , "ip\_protocol":&lt;String\_value&gt; , "bytes\_sent":&lt;String\_value&gt; , "packets\_sent":&lt;String\_value&gt; , "destination\_firewall\_zone\_name":&lt;String\_value&gt; , "destination\_route\_service\_name":&lt;String\_value&gt; , "age\_ms":&lt;String\_value&gt; , "receive\_packets\_dropped":&lt;String\_value&gt; , "bytes\_received":&lt;String\_value&gt; , "source\_route\_service\_name":&lt;String\_value&gt; , "source\_route\_type":&lt;String\_value&gt; , "sent\_packets\_dropped":&lt;String\_value&gt; , "source\_ip\_addr":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "dpi\_family\_name":&lt;String\_value&gt; , "is\_nat":&lt;String\_value&gt; , "sent\_bytes\_dropped":&lt;String\_value&gt; }\]}
