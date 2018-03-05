region

Configuration Editor for API to add, modify, delete, and get regions resource.

Read/write properties

is\_default &lt;Boolean&gt;

If enabled, the Region will be used as the default Region for the network.

region\_name &lt;String&gt;

Region Name. Minimum length = 1 Maximum length = 32

package\_name &lt;String&gt;

Config package name using which the region API operation should be performed.. Minimum length = 1 Maximum length = 141

region\_description &lt;String&gt;

Region description. Maximum length = 128

force\_internal\_vip\_matching &lt;Boolean&gt;

When enabled, all non-private Virtual IP Addressess in the Region will be forced to match the configured subnets.

id &lt;String&gt;

Config package name using which the region API operation should be performed..

allow\_external\_vip\_matching &lt;Boolean&gt;

When enabled, non-private Virtual IP Addresses from other regions will be allowed to match the configured subnets.

subnets &lt;subnets\_obj\[\]&gt;

Subnets for this region.

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/region

Description: Use this operation to add a region

HTTP Method: POST

Request Payload: JSON

{"region": { "is\_default":&lt;Boolean\_value&gt; , "region\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "region\_description":&lt;String\_value&gt; , "force\_internal\_vip\_matching":&lt;Boolean\_value&gt; , "id":&lt;String\_value&gt; , "allow\_external\_vip\_matching":&lt;Boolean\_value&gt; , "subnets":\[{ "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }\] }}

Response Payload: JSON

{ "region":{ "is\_default":&lt;Boolean\_value&gt;

, "region\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "region\_description":&lt;String\_value&gt; , "force\_internal\_vip\_matching":&lt;Boolean\_value&gt; , "id":&lt;String\_value&gt; , "allow\_external\_vip\_matching":&lt;Boolean\_value&gt; , "subnets":\[{ "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }\]}\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/region/package\_name=&lt;String&gt;,id=&lt;id&gt;

Description: Use this operation to delete a region. This operation also deletes all the sites in the region

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/region/package\_name=&lt;package\_name&gt;

Description: Use this operation to get the regions

HTTP Method: GET

Response Payload: JSON

{"region":\[{ "is\_default":&lt;Boolean\_value&gt;

, "region\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "region\_description":&lt;String\_value&gt; , "force\_internal\_vip\_matching":&lt;Boolean\_value&gt; , "id":&lt;String\_value&gt; , "allow\_external\_vip\_matching":&lt;Boolean\_value&gt; , "subnets":\[{ "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }\]}\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config\_editor/region

Description: Use this operation to modify a region

HTTP Method: PUT

Request Payload: JSON

{"region":{ "is\_default":&lt;Boolean\_value&gt; , "region\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "region\_description":&lt;String\_value&gt; , "force\_internal\_vip\_matching":&lt;Boolean\_value&gt; , "id":&lt;String\_value&gt; , "allow\_external\_vip\_matching":&lt;Boolean\_value&gt; , "subnets":\[{ "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }\] }}

Response Payload: JSON

{ "region":\[{ "is\_default":&lt;Boolean\_value&gt;

, "region\_name":&lt;String\_value&gt; , "package\_name":&lt;String\_value&gt; , "region\_description":&lt;String\_value&gt; , "force\_internal\_vip\_matching":&lt;Boolean\_value&gt; , "id":&lt;String\_value&gt; , "allow\_external\_vip\_matching":&lt;Boolean\_value&gt; , "subnets":\[{ "network":&lt;String\_value&gt; , "routing\_domain":&lt;String\_value&gt; }\]}\]}
