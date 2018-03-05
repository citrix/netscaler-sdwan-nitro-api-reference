file\_upload\_to\_inbox

Configuration for File Upload To Inbox resource.

Read/write properties

Read only properties

inbox\_files &lt;String\[\]&gt;

List of files present in inbox after the file upload operation..

Operations

[file\_upload](#file_upload) [upload\_license](#upload_license) [upload\_os\_image](#upload_os_image) [upload\_lcm\_package](#upload_lcm_package)

[file\_upload]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/file\_upload\_to\_inbox?action=file\_upload

Description: Use this operation to Upload software update files (tar.gz and zip), config files and local change management package. To Inbox in SD-WAN Appliance

HTTP Method: POST

Multi-part form data with File Stream

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "file\_upload\_to\_inbox":{}}

[upload\_license]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/file\_upload\_to\_inbox?action=upload\_license

Description: Use this operation to upload a license file to SD-WAN Appliance.Files will be deleted at appliance reboot. Use the local\_license resource to get all uploaded & installed licenses.

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "file\_upload\_to\_inbox":{}}

[upload\_os\_image]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/file\_upload\_to\_inbox?action=upload\_os\_image

Description: Use this operation to upload an OS image file to SD-WAN Appliance

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "file\_upload\_to\_inbox":{}}

[upload\_lcm\_package]{}

URL: http://&lt;MGMT-IP&gt;/sdwan/nitro/v1/config/file\_upload\_to\_inbox?action=upload\_lcm\_package

Description: Use this operation to upload Local Change Management Package

HTTP Method: POST

Request Payload: Request Payload Not Required

Response Payload: JSON

{ "file\_upload\_to\_inbox":{}}
