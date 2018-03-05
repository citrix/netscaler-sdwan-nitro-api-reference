packet\_capture

Diagnostics for Capture and download pcap on different interfaces\[Max File Size 575 MB\] resource.

Read/write properties

summary &lt;packet\_summary\[\]&gt;

Summary of Packets captured.

interface &lt;String&gt;

Interface on which packets have to be captured.

duration &lt;String&gt;

Duration for which packets have to be captured in seconds. Possible values = \[5,10,15,30\]

filter\_str &lt;String&gt;

Filter string is used to determine which packets are captured.

message &lt;String&gt;

Message about the packet capture event.

max\_packets &lt;String&gt;

Max Number of Packets to be captured. Possible values = \[1000,2000,5000,MAX\]

Read only properties

Operations

[add](#add)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/diag/packet\_capture

Description: Use this operation to capture pcap on different interfaces SD-WAN Appliance

HTTP Method: POST

Request Payload: JSON

{"packet\_capture": { "summary":\[{}\] , "interface":&lt;String\_value&gt; , "duration":&lt;String\_value&gt; , "filter\_str":&lt;String\_value&gt; , "message":&lt;String\_value&gt; , "max\_packets":&lt;String\_value&gt; }}

Response Payload: JSON

{ "packet\_capture":{ "summary":\[{ "protocol":&lt;String\_value&gt;

, "src\_port":&lt;String\_value&gt; , "src\_mac":&lt;String\_value&gt; , "number":&lt;String\_value&gt; , "time":&lt;String\_value&gt; , "src\_ip":&lt;String\_value&gt; , "dst\_port":&lt;String\_value&gt; , "dst\_ip":&lt;String\_value&gt; , "length":&lt;String\_value&gt; , "dst\_mac":&lt;String\_value&gt; }\], "interface":&lt;String\_value&gt; , "duration":&lt;String\_value&gt; , "filter\_str":&lt;String\_value&gt; , "message":&lt;String\_value&gt; , "max\_packets":&lt;String\_value&gt; }\]}
