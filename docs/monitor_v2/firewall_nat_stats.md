firewall\_nat\_stats

Monitoring for This resource provides Firewall NAT Stats resource.

Read/write properties

Read only properties

nat\_direction &lt;String&gt;

The direction of this policy.

connections &lt;String&gt;

Connections that match this policy.

inbound\_bytes &lt;String&gt;

Total bytes received that have matched this policy.

service\_name &lt;String&gt;

Service name of this policy.

ip\_protocol &lt;String&gt;

IP Protocol for the policy.

allow\_related &lt;String&gt;

Indicates whether this policy allow related ICMP packets.

inside\_ip\_address &lt;String&gt;

Inside IP Address in use for the policy.

enable\_gre\_passthrough &lt;String&gt;

Indicates whether this policy allow passthrough of GRE packets.

service\_type &lt;String&gt;

Service type this policy.

outside\_ip\_address &lt;String&gt;

Outside IP Address in use for the policy.

outside\_port &lt;String&gt;

Outside port(s) used by this policy.

outbound\_bytes &lt;String&gt;

Total bytes sent that have matched this policy.

enable\_ipsec\_passthrough &lt;String&gt;

Indicates whether this policy allow passthrough of IPSEC packets.

inbound\_packets &lt;String&gt;

Total packets received that have matched this policy.

masquerade\_parent &lt;String&gt;

Parent Dynamic NAT policy of this port forwarding NAT policy.

inside\_port &lt;String&gt;

Inside port(s) used by this policy.

type &lt;String&gt;

Type of NAT used by this policy.

outbound\_packets &lt;String&gt;

Total packets sent that have matched this policy.

routing\_domain\_name &lt;String&gt;

Routing Domain name of the poilicy.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/firewall\_nat\_stats

Description: Use this operation to get the Firewall NAT Stats, max\_stats filter is available as an additional option to filter the nat count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"firewall\_nat\_stats":\[{ "nat\_direction":&lt;String\_value&gt;

, "connections":&lt;String\_value&gt; , "inbound\_bytes":&lt;String\_value&gt; , "service\_name":&lt;String\_value&gt; , "ip\_protocol":&lt;String\_value&gt; , "allow\_related":&lt;String\_value&gt; , "inside\_ip\_address":&lt;String\_value&gt; , "enable\_gre\_passthrough":&lt;String\_value&gt; , "service\_type":&lt;String\_value&gt; , "outside\_ip\_address":&lt;String\_value&gt; , "outside\_port":&lt;String\_value&gt; , "outbound\_bytes":&lt;String\_value&gt; , "enable\_ipsec\_passthrough":&lt;String\_value&gt; , "inbound\_packets":&lt;String\_value&gt; , "masquerade\_parent":&lt;String\_value&gt; , "inside\_port":&lt;String\_value&gt; , "type":&lt;String\_value&gt; , "outbound\_packets":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; }\]}
