centralized\_licensing\_site

Configuration Editor for API to modify, get, site settings for centralized licensing for sites resource.

Read/write properties

remote\_server\_port &lt;Integer&gt;

Remote server port. Maximum value = 65535

remote\_server\_ip &lt;String&gt;

Remote licensing server ip address.

package\_name &lt;String&gt;

Config package name using which the centralized licensing operation should be performed.. Minimum length = 1 Maximum length = 141

license\_server\_location &lt;String&gt;

The location of the license server. Possible values = \[LOCAL,CENTRAL\]

site\_name &lt;String&gt;

Site Name for which centralized licensing properties need to be set. Minimum length = 1 Maximum length = 32

appliance\_edition &lt;String&gt;

Edition of the appliance. SE is Stanadard Edition, EE is Enterprise Edition, PER-HOUR is on an hourly basis. Possible values = \[SE,EE,PER-HOUR\]

license\_rate &lt;String&gt;

License rate. Possible values = \[10,20,50,100,150,200,250,300,500,1000,1500,2000,3000,4000,5000,auto\]

override\_global &lt;Boolean&gt;

enable/disable overriding global centralized licensing settings.

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/centralized\_licensing\_site/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the centralized licensing settings for this site

HTTP Method: GET

Response Payload: JSON

{"centralized\_licensing\_site":\[{ "remote\_server\_port":&lt;Integer\_value&gt;

, "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "license\_server\_location":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "appliance\_edition":&lt;String\_value&gt; , "license\_rate":&lt;String\_value&gt; , "override\_global":&lt;Boolean\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/centralized\_licensing\_site

Description: Use this operation to modify the centralized licensing settings for this site

HTTP Method: PUT

Request Payload: JSON

{"centralized\_licensing\_site":{ "remote\_server\_port":&lt;Integer\_value&gt; , "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "license\_server\_location":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "appliance\_edition":&lt;String\_value&gt; , "license\_rate":&lt;String\_value&gt; , "override\_global":&lt;Boolean\_value&gt; }}

Response Payload: JSON

{ "centralized\_licensing\_site":\[{ "remote\_server\_port":&lt;Integer\_value&gt;

, "remote\_server\_ip":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "license\_server\_location":&lt;String\_value&gt; , "site\_name":&lt;String\_value&gt; , "appliance\_edition":&lt;String\_value&gt; , "license\_rate":&lt;String\_value&gt; , "override\_global":&lt;Boolean\_value&gt; }\]}
