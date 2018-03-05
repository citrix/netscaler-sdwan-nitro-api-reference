ilbflows

Monitoring for This resource provides details about internet load balancing flows resource.

Read/write properties

Read only properties

flowcount &lt;String&gt;

Number of individual flows between source and destination IP.

wanlink &lt;String&gt;

Name of the WAN Link these flows travel through.

wanip &lt;String&gt;

WAN IP Address for packets on this flow.

age &lt;String&gt;

How long ago this flow was created in milliseconds.

lanip &lt;String&gt;

LAN IP Address for packets on this flow.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/ilbflows

Description: Use this operation to get internet load balancing flows. Filters are supported for this API. max\_stats filter is available as an additional option to filter the flow count(50/100/1000). Refer Getting Started Guide where filtering is explained via example of flow summary with max stats filter for monitoring API. Pagination is not supported for this API

HTTP Method: GET

Response Payload: JSON

{"ilbflows":\[{ "flowcount":&lt;String\_value&gt;

, "wanlink":&lt;String\_value&gt; , "wanip":&lt;String\_value&gt; , "age":&lt;String\_value&gt; , "lanip":&lt;String\_value&gt; }\]}
