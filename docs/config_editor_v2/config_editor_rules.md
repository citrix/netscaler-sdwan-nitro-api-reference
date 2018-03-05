config\_editor\_rules

Configuration Editor for API to add, modify, delete, and get configuration for Rules resource.

Read/write properties

lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth &lt;Integer&gt;

The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes).

lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth &lt;Integer&gt;

The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes).

lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted..

lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted..

lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit &lt;Integer&gt;

The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited (value is in ms).

lan\_2\_wan\_reassign\_large\_packets\_drop\_limit &lt;Integer&gt;

If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes..

lan\_2\_wan\_general\_class &lt;Integer&gt;

The Class that is to service traffic flows that match this application. The default is Class 9.

wan\_enable\_packet\_aggregation &lt;Boolean&gt;

If enabled, small packets on this flow will be aggregated together into larger packets.

wan\_2\_lan\_enable\_packet\_resequencing &lt;Boolean&gt;

If enabled, traffic flows that match this application should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance..

lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit &lt;Integer&gt;

If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes..

lan\_2\_wan\_general\_large\_packet\_size\_bytes &lt;Integer&gt;

Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets..

lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit &lt;Integer&gt;

If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes..

deep\_packet\_inspection\_enable\_passive\_ftp\_detection &lt;Boolean&gt;

If enabled, processing decisions will be based upon user data. The rule will learn the port used for the FTP data transfer and apply the rule properties to the learned port.

id &lt;Integer&gt;

Id of rule.

rule\_group\_name &lt;String&gt;

A name given to a rule that will allow rule statistics to be summed in groups when they are displayed. All rule statistics for rules with the same Rule Group Name can be viewed together.. Possible values = \[FTP,SMTP,POP3,IMAP,HTTP,TELNET,ICMP,HTTPS,ALTHTTP,SSH,DNS,SNMP,NTP,SNMPTRAP,RDP,IPSEC,RPC,SIP,ICACGPPUDP,ICAUDP,ICACGP,ICA,IPERF,CIFS,LDAP,NETBIOS,GRE,TCP,UDP,Number,RTP,RTCP,DHCP,NFS\]

wan\_transmit\_mode &lt;String&gt;

The method of transmitting and receiving packets. Possible values = \[persistent\_path,load\_balanced\_paths,duplicate\_paths,override\_service\]

wan\_2\_lan\_resequence\_hold\_time &lt;Integer&gt;

The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers (value is in ms).

lan\_2\_wan\_reassign\_class &lt;Integer&gt;

The Class to which flows will be reassigned if the size specified is exceeded. If the default option is selected, packets will not be assigned to an alternate class based on packet size, and will continue to be mapped to the class specified in the General section..

lan\_2\_wan\_general\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted (value is in bytes).

lan\_2\_wan\_general\_drop\_limit &lt;Integer&gt;

The maximum amount of estimated time that packets will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes (Value is in ms).

wan\_enable\_header\_compression\_gre &lt;Boolean&gt;

If enabled, header compression will be used for GRE packets.

wan\_2\_lan\_discard\_late\_resequenced\_packets &lt;Boolean&gt;

After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this to discard, disable this to forward..

wan\_override\_service &lt;String&gt;

The destination service that flows should go to.

lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes &lt;Integer&gt;

Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets..

lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted..

wan\_preferred\_wan\_link &lt;Boolean&gt;

The WAN link that flows should use first.

lan\_2\_wan\_reassign\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.

lan\_2\_wan\_reassign\_large\_packet\_size\_bytes &lt;Integer&gt;

Packets destined for this class which are larger than or equal to this size will follow large packet drop policy. Packets which are smaller than this size will follow small packet drop policy. If this size is set to 0, all packets will be treated as small packets..

wan\_enable\_tcp\_termination &lt;String&gt;

Traffic for this flow will be TCP terminated locally to improve throughput, reducing the round-trip times for acknowledgement packets. If enabled, TCP Termination feature will be used on flows matching this rule. The default is off..

wan\_enable\_header\_compression\_ip\_tcp\_udp &lt;Boolean&gt;

If enabled, header compression will be used for IP, TCP and UDP packets.

lan\_2\_wan\_general\_enable\_red &lt;Boolean&gt;

If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected..

virtual\_path\_name &lt;String&gt;

virtual path name to which the rule belongs to.

lan\_2\_wan\_general\_large\_packets\_drop\_limit &lt;Integer&gt;

The maximum amount of estimated time that packets larger than or equal to the Large Packet Size will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes..

wan\_2\_lan\_dscp\_tag &lt;String&gt;

The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN.

wan\_persistent\_impedance &lt;Integer&gt;

Use the same path until wait time on the path is longer than the configured value.

lan\_2\_wan\_reassign\_enable\_red &lt;Boolean&gt;

If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected..

site\_name &lt;String&gt;

Site name to which the rule belongs.

lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted.

wan\_track\_performance &lt;Integer&gt;

If enabled, performance of a rule over time will be recorded in a session DB, including loss, latency, jitter and bandwidth used..

lan\_2\_wan\_reassign\_drop\_limit &lt;Integer&gt;

If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes..

lan\_2\_wan\_reassign\_size &lt;Integer&gt;

After a flow is established, if a packet that exceeds this size is detected on the LAN to WAN, then the flow will be moved to the class indicated.

package\_name &lt;String&gt;

Package name to add rule to.

wan\_retransmit\_lost\_packets &lt;Boolean&gt;

If enabled, flows matching this rule will be sent using reliable service to the remote appliance and any packets lost will be retransmitted.

lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit &lt;Integer&gt;

Designates the amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited..

lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red &lt;Boolean&gt;

If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected..

lan\_2\_wan\_tcp\_standalone\_ack\_class &lt;Integer&gt;

The Class that will be used for standalone TCP ACKs. This has no effect on packets that are piggyback ACKs with payload. If the default option is selected, TCP Standalone ACKs will continue to be mapped to the class specified in the General section..

Read only properties

priority &lt;Integer&gt;

The order/precedence in which Rules are applied (automatically redistributed).

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_rules

Description: Use this operation to add the Rules

HTTP Method: POST

Request Payload: JSON

{"config\_editor\_rules": { "lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_class":&lt;Integer\_value&gt; , "wan\_enable\_packet\_aggregation":&lt;Boolean\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit":&lt;Integer\_value&gt; , "deep\_packet\_inspection\_enable\_passive\_ftp\_detection":&lt;Boolean\_value&gt; , "id":&lt;Integer\_value&gt; , "rule\_group\_name":&lt;String\_value&gt; , "wan\_transmit\_mode":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_class":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_limit":&lt;Integer\_value&gt; , "wan\_enable\_header\_compression\_gre":&lt;Boolean\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "wan\_override\_service":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "wan\_preferred\_wan\_link":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "wan\_enable\_tcp\_termination":&lt;String\_value&gt; , "wan\_enable\_header\_compression\_ip\_tcp\_udp":&lt;Boolean\_value&gt; , "lan\_2\_wan\_general\_enable\_red":&lt;Boolean\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "lan\_2\_wan\_general\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "wan\_2\_lan\_dscp\_tag":&lt;String\_value&gt; , "wan\_persistent\_impedance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_enable\_red":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth":&lt;Integer\_value&gt; , "wan\_track\_performance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_size":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "wan\_retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_class":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "config\_editor\_rules":{ "priority":&lt;Integer\_value&gt;

, "lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_class":&lt;Integer\_value&gt; , "wan\_enable\_packet\_aggregation":&lt;Boolean\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit":&lt;Integer\_value&gt; , "deep\_packet\_inspection\_enable\_passive\_ftp\_detection":&lt;Boolean\_value&gt; , "id":&lt;Integer\_value&gt; , "rule\_group\_name":&lt;String\_value&gt; , "wan\_transmit\_mode":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_class":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_limit":&lt;Integer\_value&gt; , "wan\_enable\_header\_compression\_gre":&lt;Boolean\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "wan\_override\_service":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "wan\_preferred\_wan\_link":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "wan\_enable\_tcp\_termination":&lt;String\_value&gt; , "wan\_enable\_header\_compression\_ip\_tcp\_udp":&lt;Boolean\_value&gt; , "lan\_2\_wan\_general\_enable\_red":&lt;Boolean\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "lan\_2\_wan\_general\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "wan\_2\_lan\_dscp\_tag":&lt;String\_value&gt; , "wan\_persistent\_impedance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_enable\_red":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth":&lt;Integer\_value&gt; , "wan\_track\_performance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_size":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "wan\_retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_class":&lt;Integer\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_rules/

Description: Use this operation to delete the Rules

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_rules/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the Rules

HTTP Method: GET

Response Payload: JSON

{"config\_editor\_rules":\[{ "priority":&lt;Integer\_value&gt;

, "lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_class":&lt;Integer\_value&gt; , "wan\_enable\_packet\_aggregation":&lt;Boolean\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit":&lt;Integer\_value&gt; , "deep\_packet\_inspection\_enable\_passive\_ftp\_detection":&lt;Boolean\_value&gt; , "id":&lt;Integer\_value&gt; , "rule\_group\_name":&lt;String\_value&gt; , "wan\_transmit\_mode":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_class":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_limit":&lt;Integer\_value&gt; , "wan\_enable\_header\_compression\_gre":&lt;Boolean\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "wan\_override\_service":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "wan\_preferred\_wan\_link":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "wan\_enable\_tcp\_termination":&lt;String\_value&gt; , "wan\_enable\_header\_compression\_ip\_tcp\_udp":&lt;Boolean\_value&gt; , "lan\_2\_wan\_general\_enable\_red":&lt;Boolean\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "lan\_2\_wan\_general\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "wan\_2\_lan\_dscp\_tag":&lt;String\_value&gt; , "wan\_persistent\_impedance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_enable\_red":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth":&lt;Integer\_value&gt; , "wan\_track\_performance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_size":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "wan\_retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_class":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_rules

Description: Use this operation to modify the Rules

HTTP Method: PUT

Request Payload: JSON

{"config\_editor\_rules":{ "lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_class":&lt;Integer\_value&gt; , "wan\_enable\_packet\_aggregation":&lt;Boolean\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit":&lt;Integer\_value&gt; , "deep\_packet\_inspection\_enable\_passive\_ftp\_detection":&lt;Boolean\_value&gt; , "id":&lt;Integer\_value&gt; , "rule\_group\_name":&lt;String\_value&gt; , "wan\_transmit\_mode":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_class":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_limit":&lt;Integer\_value&gt; , "wan\_enable\_header\_compression\_gre":&lt;Boolean\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "wan\_override\_service":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "wan\_preferred\_wan\_link":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "wan\_enable\_tcp\_termination":&lt;String\_value&gt; , "wan\_enable\_header\_compression\_ip\_tcp\_udp":&lt;Boolean\_value&gt; , "lan\_2\_wan\_general\_enable\_red":&lt;Boolean\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "lan\_2\_wan\_general\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "wan\_2\_lan\_dscp\_tag":&lt;String\_value&gt; , "wan\_persistent\_impedance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_enable\_red":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth":&lt;Integer\_value&gt; , "wan\_track\_performance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_size":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "wan\_retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_class":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "config\_editor\_rules":\[{ "priority":&lt;Integer\_value&gt;

, "lan\_2\_wan\_general\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_tcp\_standalone\_ack\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_general\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_class":&lt;Integer\_value&gt; , "wan\_enable\_packet\_aggregation":&lt;Boolean\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_limit":&lt;Integer\_value&gt; , "deep\_packet\_inspection\_enable\_passive\_ftp\_detection":&lt;Boolean\_value&gt; , "id":&lt;Integer\_value&gt; , "rule\_group\_name":&lt;String\_value&gt; , "wan\_transmit\_mode":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_class":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_general\_drop\_limit":&lt;Integer\_value&gt; , "wan\_enable\_header\_compression\_gre":&lt;Boolean\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "wan\_override\_service":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_reassign\_large\_packets\_drop\_depth":&lt;Integer\_value&gt; , "wan\_preferred\_wan\_link":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_drop\_depth":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_large\_packet\_size\_bytes":&lt;Integer\_value&gt; , "wan\_enable\_tcp\_termination":&lt;String\_value&gt; , "wan\_enable\_header\_compression\_ip\_tcp\_udp":&lt;Boolean\_value&gt; , "lan\_2\_wan\_general\_enable\_red":&lt;Boolean\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "lan\_2\_wan\_general\_large\_packets\_drop\_limit":&lt;Integer\_value&gt; , "wan\_2\_lan\_dscp\_tag":&lt;String\_value&gt; , "wan\_persistent\_impedance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_enable\_red":&lt;Boolean\_value&gt; , "site\_name":&lt;String\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_drop\_depth":&lt;Integer\_value&gt; , "wan\_track\_performance":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_reassign\_size":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "wan\_retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_reassign\_duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_enable\_red":&lt;Boolean\_value&gt; , "lan\_2\_wan\_tcp\_standalone\_ack\_class":&lt;Integer\_value&gt; }\]}
