application\_qos

Configuration Editor for API to add, modify, delete, and get configuration for Application QoS resource.

Read/write properties

match\_type &lt;String&gt;

The mechanism through which this application will be matched (Either a user-defined application, pre-defined applications or groupings of applications). Possible values = \[application\_object,application,application\_family\]

destination\_port &lt;String&gt;

If set, the Destination Port or Port range (eg: 2345-2457) that this rule will match.

application\_objects &lt;String&gt;

The Application Object is a user-defined application, as specified in the Global -  Applications section of this configuration..

source\_port &lt;String&gt;

If set, the Source Port or Port range (eg: 2345-2457) that this rule will match.

virtual\_path\_name &lt;String&gt;

virtual path name to which the application qos belongs to.

retransmit\_lost\_packets &lt;Boolean&gt;

If enabled, flows matching this application will be sent using reliable service to the remote appliance and any packets lost will be retransmitted.

destination\_ip\_address &lt;String&gt;

The Destination IP Address and subnet mask that this rule will match.

wan\_2\_lan\_enable\_packet\_resequencing &lt;Boolean&gt;

If enabled, traffic flows that match this application should be tagged for sequence order, and the packets should be reordered (if necessary) at the WAN to LAN appliance..

lan\_2\_wan\_drop\_limit &lt;Integer&gt;

The maximum amount of estimated time that packets will have to wait in the class scheduler. If the estimated time exceeds this threshold, the packet will be discarded and statistics will be counted. Not valid for Bulk classes (Value is in ms).

lan\_2\_wan\_class &lt;Integer&gt;

The Class that is to service traffic flows that match this application. The default is Class 9.

is\_auto &lt;Boolean&gt;

If set to true, it is a default Application QoS.

transmit\_mode &lt;String&gt;

The method of transmitting and receiving packets. Possible values = \[load\_balance\_paths,persistent\_path,duplicate\_paths\]

id &lt;Integer&gt;

Object id for application qos.

lan\_2\_wan\_drop\_depth &lt;Integer&gt;

If the queue depth exceeds this threshold, the packet will be discarded and statistics will be counted (value is in bytes).

site\_name &lt;String&gt;

Site name to which the application qos belongs.

wan\_2\_lan\_resequence\_hold\_time &lt;Integer&gt;

The maximum delay that a packet may be held awaiting re-sequence. When the timer expires the packet will be sent to the LAN without waiting any further for the pre-requisite sequence numbers (value is in ms).

duplicate\_packets\_disable\_depth &lt;Integer&gt;

The queue depth of the class scheduler at which point duplicate packets will not be generated (value is in bytes).

dscp\_tag &lt;String&gt;

The DSCP tag that will be applied to packets that match this rule on WAN to LAN, before they are sent to the LAN.

application\_family &lt;String&gt;

The Application Family Object is a user-defined application family.

source\_ip\_address &lt;String&gt;

The Source IP Address and subnet mask that this application will match.

persistent\_impedance &lt;Integer&gt;

Use the same path until wait time on the path is longer than the configured value.

package\_name &lt;String&gt;

Package name to add application qos to.

duplicate\_packets\_disable\_limit &lt;Integer&gt;

The amount of time a packet may wait in the queue before duplication is not performed, which prevents duplicate packets from consuming bandwidth when bandwidth is limited (value is in ms).

preferred\_wan\_link &lt;String&gt;

The WAN link that flows should use first.

wan\_2\_lan\_discard\_late\_resequenced\_packets &lt;Boolean&gt;

After a packets sequence timer has expired for a dependent packet, and the packets were permitted to the LAN: If a late packet arrives at WAN to LAN, this property defines what is to be done with it. Enable this checkbox to discard, disable this checkbox to forward..

lan\_2\_wan\_enable\_red &lt;Boolean&gt;

If enabled, Random Early Detection (RED) will discard packets uniformly when congestion is detected..

Read only properties

priority &lt;Integer&gt;

Order of evaluation of the application rule.

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/application\_qos

Description: Use this operation to add the Application QoS

HTTP Method: POST

Request Payload: JSON

{"application\_qos": { "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_class":&lt;Integer\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "transmit\_mode":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_depth":&lt;Integer\_value&gt; , **"site\_name":&lt;String\_value&gt;** , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "persistent\_impedance":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "preferred\_wan\_link":&lt;String\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_enable\_red":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "application\_qos":{ "priority":&lt;Integer\_value&gt;

, "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_class":&lt;Integer\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "transmit\_mode":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_depth":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "persistent\_impedance":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "preferred\_wan\_link":&lt;String\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_enable\_red":&lt;Boolean\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/application\_qos/

Description: Use this operation to delete the Application QoS

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/application\_qos/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the Application QoS settings

HTTP Method: GET

Response Payload: JSON

{"application\_qos":\[{ "priority":&lt;Integer\_value&gt;

, "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_class":&lt;Integer\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "transmit\_mode":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_depth":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "persistent\_impedance":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "preferred\_wan\_link":&lt;String\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_enable\_red":&lt;Boolean\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/application\_qos

Description: Use this operation to modify the Application QoS

HTTP Method: PUT

Request Payload: JSON

{"application\_qos":{ "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_class":&lt;Integer\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "transmit\_mode":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_depth":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "persistent\_impedance":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "preferred\_wan\_link":&lt;String\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_enable\_red":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "application\_qos":\[{ "priority":&lt;Integer\_value&gt;

, "match\_type":&lt;String\_value&gt; , "destination\_port":&lt;String\_value&gt; , "application\_objects":&lt;String\_value&gt; , "source\_port":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "retransmit\_lost\_packets":&lt;Boolean\_value&gt; , "destination\_ip\_address":&lt;String\_value&gt; , "wan\_2\_lan\_enable\_packet\_resequencing":&lt;Boolean\_value&gt; , "lan\_2\_wan\_drop\_limit":&lt;Integer\_value&gt; , "lan\_2\_wan\_class":&lt;Integer\_value&gt; , "is\_auto":&lt;Boolean\_value&gt; , "transmit\_mode":&lt;String\_value&gt; , "id":&lt;Integer\_value&gt; , "lan\_2\_wan\_drop\_depth":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "wan\_2\_lan\_resequence\_hold\_time":&lt;Integer\_value&gt; , "duplicate\_packets\_disable\_depth":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "application\_family":&lt;String\_value&gt; , "source\_ip\_address":&lt;String\_value&gt; , "persistent\_impedance":&lt;Integer\_value&gt; , "package\_name":&lt;String\_value&gt; , "duplicate\_packets\_disable\_limit":&lt;Integer\_value&gt; , "preferred\_wan\_link":&lt;String\_value&gt; , "wan\_2\_lan\_discard\_late\_resequenced\_packets":&lt;Boolean\_value&gt; , "lan\_2\_wan\_enable\_red":&lt;Boolean\_value&gt; }\]}
