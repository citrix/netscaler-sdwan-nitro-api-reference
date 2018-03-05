tacacs\_settings

Configuration for These APIs can be used to enable/disable TACACS+, Modify or Get TACACS+ Settings resource.

Read/write properties

tacacs\_port2 &lt;Integer&gt;

Port2 of TACACS+ server (Value range 1 to 65535).

tacacs\_server\_ip\_addr3 &lt;String&gt;

IPADDRESS3 of TACACS+ server.

tacacs\_server\_ip\_addr2 &lt;String&gt;

IPADDRESS2 of TACACS+ server.

tacacs\_enabled &lt;String&gt;

TACACS+ enable/disable. Default value is true.

tacacs\_port &lt;Integer&gt;

Port of TACACS+ server (Value range 1 to 65535).

tacacs\_timeout &lt;Integer&gt;

TACACS+ timeout in seconds. Maximum value = 10

tacacs\_auth\_type &lt;String&gt;

TACACS+ server key. Possible values = \[PAP,ASCII\]

tacacs\_port3 &lt;Integer&gt;

Port3 of TACACS+ server (Value range 1 to 65535).

tacacs\_server\_ip\_addr &lt;String&gt;

IPADDRESS of TACACS+ server.

tacacs\_server\_key &lt;String&gt;

TACACS+ server key.

Read only properties

Operations

[get (all)](#get_all) [modify](#modify)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/tacacs\_settings

Description: Get TACACS+ Settings

HTTP Method: GET

Response Payload: JSON

{"tacacs\_settings":\[{ "tacacs\_port2":&lt;Integer\_value&gt;

, "tacacs\_server\_ip\_addr3":&lt;String\_value&gt; , "tacacs\_server\_ip\_addr2":&lt;String\_value&gt; , "tacacs\_enabled":&lt;String\_value&gt; , "tacacs\_port":&lt;Integer\_value&gt; , "tacacs\_timeout":&lt;Integer\_value&gt; , "tacacs\_auth\_type":&lt;String\_value&gt; , "tacacs\_port3":&lt;Integer\_value&gt; , "tacacs\_server\_ip\_addr":&lt;String\_value&gt; , "tacacs\_server\_key":&lt;String\_value&gt; }\]}

[modify]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/tacacs\_settings

Description: Use this API to modify TACACS+ settings

HTTP Method: PUT

Request Payload: JSON

{"tacacs\_settings":{ "tacacs\_port2":&lt;Integer\_value&gt; , "tacacs\_server\_ip\_addr3":&lt;String\_value&gt; , "tacacs\_server\_ip\_addr2":&lt;String\_value&gt; , "tacacs\_enabled":&lt;String\_value&gt; , "tacacs\_port":&lt;Integer\_value&gt; , "tacacs\_timeout":&lt;Integer\_value&gt; , "tacacs\_auth\_type":&lt;String\_value&gt; , "tacacs\_port3":&lt;Integer\_value&gt; , "tacacs\_server\_ip\_addr":&lt;String\_value&gt; , "tacacs\_server\_key":&lt;String\_value&gt; }}

Response Payload: JSON

{ "tacacs\_settings":\[{ "tacacs\_port2":&lt;Integer\_value&gt;

, "tacacs\_server\_ip\_addr3":&lt;String\_value&gt; , "tacacs\_server\_ip\_addr2":&lt;String\_value&gt; , "tacacs\_enabled":&lt;String\_value&gt; , "tacacs\_port":&lt;Integer\_value&gt; , "tacacs\_timeout":&lt;Integer\_value&gt; , "tacacs\_auth\_type":&lt;String\_value&gt; , "tacacs\_port3":&lt;Integer\_value&gt; , "tacacs\_server\_ip\_addr":&lt;String\_value&gt; , "tacacs\_server\_key":&lt;String\_value&gt; }\]}
