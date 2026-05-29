
# HTTP

Send Http rest api requests

Python Version - 3


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Get Data
Send HTTP get request
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL|The url to send the request to.|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|
|SSL Verification|Whether to verify the SSL certificate of the destination server.|False|Boolean||
|Ignore HTTP Error Codes|If enabled, action should ignore 4xx or 5xx HTTP error codes and not return error.|False|Boolean||
|Headers JSON|JSON object of HTTP headers to be sent with the request.|False|String||



##### JSON Results
```json
{"redirects": ["http://blank.org/"], "response_code": 200, "data": "<html>\n\n<head>\n<title>\nblank\n</title>\n</head>\n\n<body bgcolor=#ffffff text=#2222ff link=#ff0000 vlink=#880000 alink=#00ff00>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<center>\n<a style=\"text-decoration:none\" href=\"blank.html\">.</a>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n</center>\n</body>\n</html>\n"}
```



#### Get URL Data
Send HTTP GET request to URL entities
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Username|Username for basic authentication. Optional.|False|String||
|Password|Password for basic authentication. Optional.|False|Password|*****|
|SSL Verification|Whether to verify the SSL certificate of the destination server.|False|Boolean||



##### JSON Results
```json
[{"EntityResult": {"redirects": ["http://blank.org/"], "data": "<html>\n\n<head>\n<title>\nblank\n</title>\n</head>\n\n<body bgcolor=#ffffff text=#2222ff link=#ff0000 vlink=#880000 alink=#00ff00>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<center>\n<a style=\"text-decoration:none\" href=\"blank.html\">.</a>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n</center>\n</body>\n</html>\n"}, "Entity": "http://blank.org/"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Post Data
Send HTTP post requests
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL|The url to send the request to.|True|String||
|Data|The data to send with the request.|True|String||
|Username|Username|False|String||
|Password|Password|False|Password|*****|
|SSL Verification|Whether to verify the SSL certificate of the destination server.|False|Boolean||
|Headers JSON|JSON object of HTTP headers to be sent with the request.|False|String||
|Content Type|Content Type. If set to application/json the input data must be JSON string.|False|List|None|



##### JSON Results
```json
{"redirects": ["http://blank.org/"], "data": "<html>\n\n<head>\n<title>\nblank\n</title>\n</head>\n\n<body bgcolor=#ffffff text=#2222ff link=#ff0000 vlink=#880000 alink=#00ff00>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<center>\n<a style=\"text-decoration:none\" href=\"blank.html\">.</a>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n<br>\n</center>\n</body>\n</html>\n"}
```









