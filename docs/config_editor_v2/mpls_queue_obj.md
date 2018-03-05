mpls\_queue\_obj

Configuration Editor for MPLS queue objects resource.

Read/write properties

wan\_2\_lan\_permitted\_rate\_kbps &lt;Integer&gt;

The available or allowed rate for WAN to LAN traffic.

dscp\_tag &lt;String&gt;

The DSCP tag for the MPLS queue. Possible values = \[DEFAULT,af11,af12,af13,af21,af22,af23,af31,af32,af33,af41,af42,af43,cs1,cs2,cs3,cs4,cs5,cs6,cs7,ef\]

wan\_2\_lan\_realtime\_eligibility &lt;Boolean&gt;

Allows paths to this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available..

congestion\_threshold &lt;Integer&gt;

The amount of congestion (in microseconds) after which the MPLS Queue will throttle packet transmission to avoid further congestion.

unmatched &lt;Boolean&gt;

If enabled, DSCP tags not matched by other MPLS Queues will use this queue.

lan\_2\_wan\_interactive\_eligibility &lt;Boolean&gt;

Allows paths from this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available.

tracking\_ip\_address &lt;String&gt;

A virtual IP address that can be pinged to determine the state of the MPLS Queue.

mpls\_queue\_name &lt;String&gt;

The name of the MPLS Queue. Minimum length = 1 Maximum length = 32

lan\_2\_wan\_realtime\_eligibility &lt;Boolean&gt;

Allows paths from this WAN Link to transmit realtime traffic. If disabled, these paths will still be considered eligible if no other paths are available.

wan\_2\_lan\_interactive\_eligibility &lt;Boolean&gt;

Allows paths to this WAN Link to transmit interactive traffic. If disabled, these paths will still be considered eligible if no other paths are available..

wan\_2\_lan\_bulk\_eligibility &lt;Boolean&gt;

Allows paths to this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available.

lan\_2\_wan\_bulk\_eligibility &lt;Boolean&gt;

Allows paths from this WAN Link to transmit bulk traffic. If disabled, these paths will still be considered eligible if no other paths are available.

lan\_2\_wan\_permitted\_rate\_kbps &lt;Integer&gt;

The available or allowed rate for LAN to WAN traffic.

no\_retag &lt;Boolean&gt;

If enabled, DCSP tags using unmatched Queue will not get retagged to the unmatched Queue tag for LAN to WAN intranet traffic.

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/mpls\_queue\_obj

Description: Use this operation to add mpls queues

HTTP Method: POST

Request Payload: JSON

{"mpls\_queue\_obj": { "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "mpls\_queue\_obj":{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt;

, "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/mpls\_queue\_obj/mpls\_queue\_name=&lt;String&gt;

Description: Use this operation to delete a mpls queue

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/mpls\_queue\_obj

Description: Use this operation to get the list of mpls queues

HTTP Method: GET

Response Payload: JSON

{"mpls\_queue\_obj":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt;

, "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/mpls\_queue\_obj

Description: Use this operation to modify a mpls queue

HTTP Method: PUT

Request Payload: JSON

{"mpls\_queue\_obj":{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "mpls\_queue\_obj":\[{ "wan\_2\_lan\_permitted\_rate\_kbps":&lt;Integer\_value&gt;

, "dscp\_tag":&lt;String\_value&gt; , "wan\_2\_lan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "congestion\_threshold":&lt;Integer\_value&gt; , "unmatched":&lt;Boolean\_value&gt; , "lan\_2\_wan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; , "mpls\_queue\_name":&lt;String\_value&gt; , "lan\_2\_wan\_realtime\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_interactive\_eligibility":&lt;Boolean\_value&gt; , "wan\_2\_lan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_bulk\_eligibility":&lt;Boolean\_value&gt; , "lan\_2\_wan\_permitted\_rate\_kbps":&lt;Integer\_value&gt; , "no\_retag":&lt;Boolean\_value&gt; }\]}
