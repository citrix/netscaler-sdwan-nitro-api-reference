wanlinkstat

Monitoring for This resource provides WAN Link Stat. resource.

Read/write properties

Read only properties

intranet\_data\_rates &lt;wanlink\_datarate\[\]&gt;

Wan Link Internet Data Rates Array.

internet\_data\_rates &lt;wanlink\_datarate\[\]&gt;

Wan Link Internet Data Rates Array.

virtual\_path\_data\_rates &lt;wanlink\_datarate\[\]&gt;

Wan Link Virtual Paths Data Rate Array.

wan\_link &lt;wanlink\_info\[\]&gt;

Wan Link Stats Array.

Operations

[get (all)](#get_all)

[get (all)]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/monitor/wanlinkstat

Description: Use this operation to get WAN Link statistics. Filter and Pagination are supported for this API. Refer Getting Started Guide where filtering and pagination is explained via example of application monitoring API

HTTP Method: GET

Response Payload: JSON

{"wanlinkstat":\[{ "intranet\_data\_rates":\[{ "total\_bytes\_sent":&lt;String\_value&gt;

, "name":&lt;String\_value&gt; , "bytes\_saved":&lt;String\_value&gt; , "delta\_bytes\_rcvd":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "total\_packets\_rcvd":&lt;String\_value&gt; , "total\_bytes\_rcvd":&lt;String\_value&gt; , "delta\_bytes\_sent":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "total\_packets\_sent":&lt;String\_value&gt; }\], "internet\_data\_rates":\[{ "total\_bytes\_sent":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "bytes\_saved":&lt;String\_value&gt; , "delta\_bytes\_rcvd":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "total\_packets\_rcvd":&lt;String\_value&gt; , "total\_bytes\_rcvd":&lt;String\_value&gt; , "delta\_bytes\_sent":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "total\_packets\_sent":&lt;String\_value&gt; }\], "virtual\_path\_data\_rates":\[{ "total\_bytes\_sent":&lt;String\_value&gt; , "name":&lt;String\_value&gt; , "bytes\_saved":&lt;String\_value&gt; , "delta\_bytes\_rcvd":&lt;String\_value&gt; , "direction":&lt;String\_value&gt; , "total\_packets\_rcvd":&lt;String\_value&gt; , "total\_bytes\_rcvd":&lt;String\_value&gt; , "delta\_bytes\_sent":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "total\_packets\_sent":&lt;String\_value&gt; }\], "wan\_link":\[{ "proxy\_ip\_address":&lt;String\_value&gt; , "proxy\_arp\_state":&lt;String\_value&gt; , "ai\_name":&lt;String\_value&gt; , "wl\_name":&lt;String\_value&gt; , "last\_arp\_reply\_age":&lt;String\_value&gt; , "ip\_address":&lt;String\_value&gt; , "routing\_domain\_name":&lt;String\_value&gt; , "mac":&lt;String\_value&gt; }\]}\]}
