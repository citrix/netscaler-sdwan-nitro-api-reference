firewall\_filter\_stats

Monitoring for This resource provides Firewall Filter Stats resource.

Read/write properties

Read only properties

bytes &lt;String&gt;

Total bytes that have matched this policy.

source\_firewall\_zone\_name &lt;String&gt;

The Originating zone used by this policy.

dpi\_application\_name &lt;String&gt;

The application for the policy.

destination\_service\_name &lt;String&gt;

Destination Service name for the policy.

application\_name &lt;String&gt;

Application for this policy.

port\_or\_icmp\_type &lt;String&gt;

Originating port ot ICMP code used by this policy.

packets &lt;String&gt;

Total packets that have matched this policy.

source\_service\_type &lt;String&gt;

Source Service Type for the policy.

destination\_ip\_address &lt;String&gt;

Destination IP Address for the policy.

ip\_protocol &lt;String&gt;

IP Protocol for the connection.

track\_connection &lt;String&gt;

Indicates whether state of the connection matched are tracked.

destination\_service\_type &lt;String&gt;

Destination Service type for the policy.

destination\_firewall\_zone\_name &lt;String&gt;

The responding zone used by this policy.

destination\_port\_or\_icmp\_type &lt;String&gt;

Responding port ot ICMP code used by this policy.

dscp &lt;String&gt;

DSCP tag used by the policy.

log\_connection\_end &lt;String&gt;

Indicates whether the end of connection that match this policy are logged.

action &lt;String&gt;

The action this policy takes on a possible match.

log\_connection\_start &lt;String&gt;

Indicates whether the start of connection that match this policy are logged.

match\_established &lt;String&gt;

Indicates whether packets for an already established connection are matched.

source\_service\_name &lt;String&gt;

Source Service Name for the policy.

source\_ip\_addr &lt;String&gt;

Source IP address for the policy.

routing\_domain\_name &lt;String&gt;

Routing Domain Name for the policy.

allow\_fragments &lt;String&gt;

Indicates whether fragments matching this filter are allowed.

dpi\_family\_name &lt;String&gt;

The family for the policy.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/firewall\_filter\_stats

Description: Use this operation to get the Firewall Filter Stats, max\_stats filter is available as an additional option to filter the count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"firewall\_filter\_stats":\[{ "bytes":&lt;String\_value&gt;

, "source\_firewall\_zone\_name":&lt;String\_value&gt; , "dpi\_application\_name":&lt;String\_value&gt; , "destination\_service\_name":&lt;String\_value&gt; , "application\_name":&lt;String\_value&gt; , "port\_or\_icmp\_type":&lt;String\_value&gt; , "packets":&lt;String\_value&gt; , "source\_service\_type":&lt;String\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "ip\_protocol":&lt;String\_value&gt; , "track\_connection":&lt;String\_value&gt; , "destination\_service\_type":&lt;String\_value&gt; , "destination\_firewall\_zone\_name":&lt;String\_value&gt; , "destination\_port\_or\_icmp\_type":&lt;String\_value&gt; , "dscp":&lt;String\_value&gt; , "log\_connection\_end":&lt;String\_value&gt; , "action":&lt;String\_value&gt; , "log\_connection\_start":&lt;String\_value&gt; , "match\_established":&lt;String\_value&gt; , "source\_service\_name":&lt;String\_value&gt; , "source\_ip\_addr":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "allow\_fragments":&lt;String\_value&gt; , "dpi\_family\_name":&lt;String\_value&gt; }\]}
