dynamic\_virtual\_path\_obj

Configuration Editor for Dynamic Virtual Path Configuration Object resource.

Read/write properties

maximum\_dynamic\_virtual\_path &lt;Integer&gt;

The Maximum number of Dynamic Virtual Paths allowed between this Site and other Sites connected through an intermediate node..

enable\_dynamic\_virtual\_path &lt;Boolean&gt;

If enabled, Dynamic Virtual Paths will be allowed between this Site and other Sites connected through an intermediate node..

Read only properties

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/dynamic\_virtual\_path\_obj

Description: Use this operation to get the dynamic virtual path configuration object

HTTP Method: GET

Response Payload: JSON

{"dynamic\_virtual\_path\_obj":\[{ "maximum\_dynamic\_virtual\_path":&lt;Integer\_value&gt;

, "enable\_dynamic\_virtual\_path":&lt;Boolean\_value&gt; }\]}
