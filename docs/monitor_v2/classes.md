classes

Monitoring for This resource provides QoS Classes statistics resource.

Read/write properties

Read only properties

virtual\_path\_service\_name &lt;String&gt;

Name of Virtual path Service.

class\_object &lt;class\_cols\[\]&gt;

Class Stats for each virtual Path Service.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/classes

Description: This resource provides QoS Classes statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"classes":\[{ "virtual\_path\_service\_name":&lt;String\_value&gt;

, "class\_object":\[{ "name":&lt;String\_value&gt; , "dropped\_packets":&lt;String\_value&gt; , "sent\_packets":&lt;String\_value&gt; , "pending\_bytes":&lt;String\_value&gt; , "wait\_ms":&lt;String\_value&gt; , "pending\_packets":&lt;String\_value&gt; , "bandwidth":&lt;String\_value&gt; , "sent\_bytes":&lt;String\_value&gt; , "dropped\_bytes":&lt;String\_value&gt; , "type":&lt;String\_value&gt; , "class\_number":&lt;String\_value&gt; }\]}\]}
