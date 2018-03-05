local\_users

Configuration for Add, Delete, Modify or List Local Users through these APIs resource.

Read/write properties

password &lt;String&gt;

Password of the target user. Minimum length = 1 Maximum length = 256

user\_level &lt;String&gt;

User level of the target user. Possible values = \[admin,guest\]

username &lt;String&gt;

Username of the target user. Minimum length = 1 Maximum length = 64

Read only properties

Operations

[add](#add) [delete](#delete) [get (all)](#get_all) [modify](#modify)

[add]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_users

Description: Use this operation to add a local user

HTTP Method: POST

Request Payload: JSON

{"local\_users": { "password":&lt;String\_value&gt; , "user\_level":&lt;String\_value&gt; , "username":&lt;String\_value&gt; }}

Response Payload: JSON

{ "local\_users":{ "password":&lt;String\_value&gt;

, "user\_level":&lt;String\_value&gt; , "username":&lt;String\_value&gt; }\]}

[delete]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_users/username=&lt;String&gt;

Description: Use this operation to delete a local user

HTTP Method: DELETE

Response Payload: JSON

{ "errorcode": 0, "message": "Done", "severity": &ltString;\_value&gt; }

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_users

Description: Use this operation to get a list of all local users

HTTP Method: GET

Response Payload: JSON

{"local\_users":\[{ "password":&lt;String\_value&gt;

, "user\_level":&lt;String\_value&gt; , "username":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/local\_users

Description: Use this operation to update a local user's password

HTTP Method: PUT

Request Payload: JSON

{"local\_users":{ "password":&lt;String\_value&gt; , "username":&lt;String\_value&gt; }}

Response Payload: JSON

{ "local\_users":\[{ "password":&lt;String\_value&gt;

, "username":&lt;String\_value&gt; }\]}
