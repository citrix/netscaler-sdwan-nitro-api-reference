applications

Monitoring for This resource provides details about Applications Statistics resource.

Read/write properties

Read only properties

bytes\_received &lt;String&gt;

Bytes Received for a Application.

application &lt;String&gt;

Name of the Application.

total\_bytes &lt;String&gt;

Total bytes(Bytes Sent + Bytes Received) for a Application.

bytes\_sent &lt;String&gt;

Bytes Sent for a Application.

family &lt;String&gt;

Name of the Application Family.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/applications

Description: Use this operation to get application details. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"applications":\[{ "bytes\_received":&lt;String\_value&gt;

, "application":&lt;String\_value&gt; , "total\_bytes":&lt;String\_value&gt; , "bytes\_sent":&lt;String\_value&gt; , "family":&lt;String\_value&gt; }\]}
