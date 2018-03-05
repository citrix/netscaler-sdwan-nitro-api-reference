dynamic\_route

Configuration for API to get/add/delete the dynamic route resource.

Read/write properties

cost &lt;Integer&gt;

Cost of the Route. Minimum value = 1 Maximum value = 16

routeip &lt;String&gt;

Route IP Address.

subnet &lt;Integer&gt;

Route IP Subnet Information. Minimum value = 1 Maximum value = 32

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/dynamic\_route

Description: Use this operation to add dynamic route IP Information and cost of the routes

HTTP Method: POST

Request Payload: JSON

{"dynamic\_route": { "cost":&lt;Integer\_value&gt; , "routeip":&lt;String\_value&gt; , "subnet":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "dynamic\_route":{ "cost":&lt;Integer\_value&gt;

, "routeip":&lt;String\_value&gt; , "subnet":&lt;Integer\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/dynamic\_route/subnet=&lt;Integer&gt;,routeip=&lt;String&gt;

Description: Use this operation to delete dynamic route IP Information and cost of the routes

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/dynamic\_route

Description: Use this operation to get dynamic route IP Information and cost of the routes

HTTP Method: GET

Response Payload: JSON

{"dynamic\_route":\[{ "cost":&lt;Integer\_value&gt;

, "routeip":&lt;String\_value&gt; , "subnet":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/dynamic\_route

Description: Use this operation to modify dynamic route IP Information and cost of the routes

HTTP Method: PUT

Request Payload: JSON

{"dynamic\_route":{ "cost":&lt;Integer\_value&gt; , "routeip":&lt;String\_value&gt; , "subnet":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "dynamic\_route":\[{ "cost":&lt;Integer\_value&gt;

, "routeip":&lt;String\_value&gt; , "subnet":&lt;Integer\_value&gt; }\]}
