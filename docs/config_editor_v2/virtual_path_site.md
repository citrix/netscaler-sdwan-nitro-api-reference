virtual\_path\_site

Configuration Editor for Virtual Path site configuration resource.

Read/write properties

route\_cost &lt;Integer&gt;

This Cost will be added to Routes learned via the Virtual Path.

default\_set &lt;String&gt;

Name of the Virtual Path Default Set that will be used to populate rules and classes for the Virtual Path on the Site.

tracking\_ip\_address &lt;String&gt;

Tracking IP Address.

Read only properties

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/virtual\_path\_site

Description: Use this operation to get the site configuration object

HTTP Method: GET

Response Payload: JSON

{"virtual\_path\_site":\[{ "route\_cost":&lt;Integer\_value&gt;

, "default\_set":&lt;String\_value&gt; , "tracking\_ip\_address":&lt;String\_value&gt; }\]}
