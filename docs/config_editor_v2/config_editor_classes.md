config\_editor\_classes

Configuration Editor for API to add, modify, delete, and get configuration for Classes resource.

Read/write properties

initial\_share\_percent &lt;Integer&gt;

The maximum share of Virtual Path bandwidth during the Initial Period, as a percentage.

name &lt;String&gt;

The class name.

package\_name &lt;String&gt;

Package name.

virtual\_path\_name &lt;String&gt;

Virtual Path for corresponding class.

initial\_period &lt;Integer&gt;

Duration to apply the Initial Rate before switching to the Sustained Rate, in milliseconds.

id &lt;Integer&gt;

Class ID.

type &lt;String&gt;

Class traffic type. Possible values = \[realtime,interactive,bulk\]

sustained\_share\_percent &lt;Integer&gt;

The maximum share of Virtual Path bandwidth after the Initial Period, as a percentage.

site\_name &lt;String&gt;

Site name for corresponding class.

initial\_rate &lt;Integer&gt;

The maximum rate during the Initial Period, as a percentage or in kbps.

sustained\_rate &lt;Integer&gt;

The maximum rate after the Initial Period, as a percent share of the Virtual Path or in kbps.

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_classes/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the Classes settings

HTTP Method: GET

Response Payload: JSON

{"config\_editor\_classes":\[{ "initial\_share\_percent":&lt;Integer\_value&gt;

, "name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "initial\_period":&lt;Integer\_value&gt; , "id":&lt;Integer\_value&gt; , "type":&lt;String\_value&gt; , "sustained\_share\_percent":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "initial\_rate":&lt;Integer\_value&gt; , "sustained\_rate":&lt;Integer\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/config\_editor\_classes

Description: Use this operation to modify the Classes settings

HTTP Method: PUT

Request Payload: JSON

{"config\_editor\_classes":{ "initial\_share\_percent":&lt;Integer\_value&gt; , "name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "initial\_period":&lt;Integer\_value&gt; , "id":&lt;Integer\_value&gt; , **"type":&lt;String\_value&gt;** , "sustained\_share\_percent":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "initial\_rate":&lt;Integer\_value&gt; , "sustained\_rate":&lt;Integer\_value&gt; }}

Response Payload: JSON

{ "config\_editor\_classes":\[{ "initial\_share\_percent":&lt;Integer\_value&gt;

, "name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "virtual\_path\_name":&lt;String\_value&gt; , "initial\_period":&lt;Integer\_value&gt; , "id":&lt;Integer\_value&gt; , "type":&lt;String\_value&gt; , "sustained\_share\_percent":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "initial\_rate":&lt;Integer\_value&gt; , "sustained\_rate":&lt;Integer\_value&gt; }\]}
