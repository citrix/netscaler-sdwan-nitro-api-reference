update\_schedule

Configuration for This resource can be used to get software update schedule information and to update software update schedule. resource.

Read/write properties

repeat\_unit &lt;String&gt;

Repeat duration unit.. Possible values = \[hours,days,weeks,months\]

schedule\_window &lt;Integer&gt;

Update schedule window length in hours.. Maximum value = 24

appliance\_type &lt;String&gt;

Appliance type: primary or secondary appliance. Possible values = \[primary,secondary\]

repeat &lt;Integer&gt;

Repeat next update.. Maximum value = 999

site\_name &lt;String&gt;

Site Name.

start\_date\_time &lt;String&gt;

Update schedule start date, time..

Read only properties

message &lt;String&gt;

detailed messgae of command execution..

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/update\_schedule

Description: Use this operation to get software update schedule information.

HTTP Method: GET

Response Payload: JSON

{"update\_schedule":\[{ "repeat\_unit":&lt;String\_value&gt;

, "schedule\_window":&lt;Integer\_value&gt; , "appliance\_type":&lt;String\_value&gt; , "repeat":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "start\_date\_time":&lt;String\_value&gt; , "message":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/update\_schedule

Description: Use this operation to update software update schedule of a site.

HTTP Method: PUT

Request Payload: JSON

{"update\_schedule":{ "repeat\_unit":&lt;String\_value&gt; , "schedule\_window":&lt;Integer\_value&gt; , "appliance\_type":&lt;String\_value&gt; , "repeat":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "start\_date\_time":&lt;String\_value&gt; }}

Response Payload: JSON

{ "update\_schedule":\[{ "repeat\_unit":&lt;String\_value&gt;

, "schedule\_window":&lt;Integer\_value&gt; , "appliance\_type":&lt;String\_value&gt; , "repeat":&lt;Integer\_value&gt; , "site\_name":&lt;String\_value&gt; , "start\_date\_time":&lt;String\_value&gt; , "message":&lt;String\_value&gt; }\]}
