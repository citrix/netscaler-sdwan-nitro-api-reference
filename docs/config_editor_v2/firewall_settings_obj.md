firewall\_settings\_obj

Configuration Editor for API to add, modify, delete, and get configuration for Basic and Advanced Firewall settings resource.

Read/write properties

icmp\_idle\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an active ICMP session..

tcp\_closed\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an aborted TCP session..

source\_route\_validation &lt;Boolean&gt;

If enabled, packets will be dropped when received on an interface that differs from the packet's route, as determined by the Source IP address..

policy\_template\_name &lt;String&gt;

This is the name of the Policy Template defined globally whose filters will be included in this site's collection of firewall filters..

tcp\_idle\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an active TCP session..

tcp\_initial\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing a TCP session that has not completed a handshake..

max\_new\_connections\_per\_source &lt;Integer&gt;

The maximum number of non-established Connections to allow per Source IP Address. 0 = unlimited..

untracked\_and\_denied\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing Untracked or Denied Connections..

udp\_idle\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an active UDP session..

tcp\_timewait\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing a terminated TCP session..

default\_track\_connection &lt;Boolean&gt;

Whether or not to enable bidirectional connection state tracking for TCP, UDP and ICMP packets that do not match a filter policy or NAT rule. This feature will block flows which appear illegitimate, due to asymmetric routing or failure of checksum, protocol specific validation --  proceed with caution if NetScaler SD-WAN is not fully inline..

icmp\_initial\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an ICMP session that has not seen traffic in both directions..

generic\_initial\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing a generic session that has not seen traffic in both directions..

default\_firewall\_action &lt;String&gt;

The action for packets that do not match a policy.. Possible values = \[allow,drop\]

udp\_initial\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing a UDP session that has not seen traffic in both directions..

generic\_idle\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing an active generic session..

tcp\_closing\_timeout\_seconds &lt;Integer&gt;

The time, in seconds, to wait for new packets before closing a TCP session after a request to terminate..

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Filters are applied (automatically redistributed)..

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_settings\_obj

Description: Use this operation to add the basic and advanced firewall settings

HTTP Method: POST

Request Payload: JSON

{"firewall\_settings\_obj": { "icmp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closed\_timeout\_seconds":&lt;Integer\_value&gt; , "source\_route\_validation":&lt;Boolean\_value&gt; , "policy\_template\_name":&lt;String\_value&gt; , "tcp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "max\_new\_connections\_per\_source":&lt;Integer\_value&gt; , "untracked\_and\_denied\_timeout\_seconds":&lt;Integer\_value&gt; , "udp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_timewait\_seconds":&lt;Integer\_value&gt; , "default\_track\_connection":&lt;Boolean\_value&gt; , "icmp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "default\_firewall\_action":&lt;String\_value&gt; , "udp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closing\_timeout\_seconds":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "firewall\_settings\_obj":{ "icmp\_idle\_timeout\_seconds":&lt;Integer\_value&gt;

, "tcp\_closed\_timeout\_seconds":&lt;Integer\_value&gt; , "priority":&lt;Integer\_value&gt; , "source\_route\_validation":&lt;Boolean\_value&gt; , "policy\_template\_name":&lt;String\_value&gt; , "tcp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "max\_new\_connections\_per\_source":&lt;Integer\_value&gt; , "untracked\_and\_denied\_timeout\_seconds":&lt;Integer\_value&gt; , "udp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_timewait\_seconds":&lt;Integer\_value&gt; , "default\_track\_connection":&lt;Boolean\_value&gt; , "icmp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "default\_firewall\_action":&lt;String\_value&gt; , "udp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closing\_timeout\_seconds":&lt;Integer\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_settings\_obj/policy\_template\_name=&lt;String&gt;

Description: Use this operation to delete the basic and advanced firewall settings

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_settings\_obj

Description: Use this operation to get the basic and advanced firewall settings

HTTP Method: GET

Response Payload: JSON

{"firewall\_settings\_obj":\[{ "icmp\_idle\_timeout\_seconds":&lt;Integer\_value&gt;

, "tcp\_closed\_timeout\_seconds":&lt;Integer\_value&gt; , "priority":&lt;Integer\_value&gt; , "source\_route\_validation":&lt;Boolean\_value&gt; , "policy\_template\_name":&lt;String\_value&gt; , "tcp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "max\_new\_connections\_per\_source":&lt;Integer\_value&gt; , "untracked\_and\_denied\_timeout\_seconds":&lt;Integer\_value&gt; , "udp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_timewait\_seconds":&lt;Integer\_value&gt; , "default\_track\_connection":&lt;Boolean\_value&gt; , "icmp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "default\_firewall\_action":&lt;String\_value&gt; , "udp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closing\_timeout\_seconds":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/firewall\_settings\_obj

Description: Use this operation to modify the basic and advanced firewall settings

HTTP Method: PUT

Request Payload: JSON

{"firewall\_settings\_obj":{ "icmp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closed\_timeout\_seconds":&lt;Integer\_value&gt; , "source\_route\_validation":&lt;Boolean\_value&gt; , "policy\_template\_name":&lt;String\_value&gt; , "tcp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "max\_new\_connections\_per\_source":&lt;Integer\_value&gt; , "untracked\_and\_denied\_timeout\_seconds":&lt;Integer\_value&gt; , "udp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_timewait\_seconds":&lt;Integer\_value&gt; , "default\_track\_connection":&lt;Boolean\_value&gt; , "icmp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "default\_firewall\_action":&lt;String\_value&gt; , "udp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closing\_timeout\_seconds":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "firewall\_settings\_obj":\[{ "icmp\_idle\_timeout\_seconds":&lt;Integer\_value&gt;

, "tcp\_closed\_timeout\_seconds":&lt;Integer\_value&gt; , "priority":&lt;Integer\_value&gt; , "source\_route\_validation":&lt;Boolean\_value&gt; , "policy\_template\_name":&lt;String\_value&gt; , "tcp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "max\_new\_connections\_per\_source":&lt;Integer\_value&gt; , "untracked\_and\_denied\_timeout\_seconds":&lt;Integer\_value&gt; , "udp\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_timewait\_seconds":&lt;Integer\_value&gt; , "default\_track\_connection":&lt;Boolean\_value&gt; , "icmp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "default\_firewall\_action":&lt;String\_value&gt; , "udp\_initial\_timeout\_seconds":&lt;Integer\_value&gt; , "generic\_idle\_timeout\_seconds":&lt;Integer\_value&gt; , "tcp\_closing\_timeout\_seconds":&lt;Integer\_value&gt; }\]}
