
# GoogleCloudApi

Google Cloud API integration was designed for you to execute Google Cloud API without the need of writing any code.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Test URL|Test URL that will be used to validate the authentication to Google Cloud API. Uses a GET request.|False|String||
|Service Account Json File Content|Service Account JSON Key that will be used for authentication. Either this parameter or "Workload Identity Email" should be provided. Note: "Service Account JSON Key" authentication has priority.|False|Password|*****|
|Organization ID|ID of the organization that you want to use inside the integration. You can provide {{org_id}} inside your actions to take the value from this parameter.|False|String||
|Project ID|ID of the project that you want to use inside the integration. You can provide {{project_id}} inside your actions to take the value from this parameter.|False|String||
|Quota Project ID|ID of the quota project that will be attached to all of the API requests done by the integration.|False|String||
|Workload Identity Email|Workload identity email that should be used for authentication. Either this parameter or "Service Account JSON Key" should be provided. Note: "Service Account JSON Key" authentication has priority.|False|String||
|OAuth Scopes|Comma-separated list of OAuth scopes necessary to execute Google Cloud API requests.|False|String|https://www.googleapis.com/auth/cloud-platform|
|Verify SSL|If enabled, verify the SSL certificate for all of the connections done by integration.|False|Boolean|true|


#### Dependencies
| |
|-|
|cross/pycryptodomex-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/rsa-4.9-py3-none-any.whl|
|cross/TIPCommon-2.2.2-py2.py3-none-any.whl|
|cross/google_auth-2.34.0-py2.py3-none-any.whl|
|cross/pyparsing-3.1.4-py3-none-any.whl|
|cross/google_api_python_client-2.143.0-py2.py3-none-any.whl|
|cross/requests-2.32.3-py3-none-any.whl|
|cross/certifi-2024.7.4-py3-none-any.whl|
|cross/charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/pyasn1-0.6.0-py2.py3-none-any.whl|
|cross/uritemplate-4.1.1-py2.py3-none-any.whl|
|cross/sniffio-1.3.1-py3-none-any.whl|
|cross/httpcore-1.0.5-py3-none-any.whl|
|cross/protobuf-5.28.0-cp38-abi3-manylinux2014_x86_64.whl|
|cross/proto_plus-1.24.0-py3-none-any.whl|
|cross/soupsieve-2.6-py3-none-any.whl|
|cross/pyasn1_modules-0.4.0-py3-none-any.whl|
|cross/pyzipper-0.3.6-py2.py3-none-any.whl|
|cross/httplib2-0.22.0-py3-none-any.whl|
|cross/idna-3.8-py3-none-any.whl|
|cross/lxml-5.3.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/beautifulsoup4-4.12.3-py3-none-any.whl|
|cross/urllib3-2.2.2-py3-none-any.whl|
|cross/pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|cross/anyio-4.4.0-py3-none-any.whl|
|cross/googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|cross/h11-0.14.0-py3-none-any.whl|
|cross/EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cross/cachetools-5.5.0-py3-none-any.whl|
|cross/google_api_core-2.19.2-py3-none-any.whl|
|cross/httpx-0.27.2-py3-none-any.whl|


## Actions
#### Execute HTTP Request
Execute HTTP request.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Method|Specify the method for the request.|True|List|GET|
|URL Path|Specify the URL that needs to be executed.|True|String|https://|
|URL Params|Specify the parameters for the URL. Any value provided in this parameter will be used alongside the values that are directly provided in the URL path parameters.|False|String|{"URL Field Name": "URL Field Value"}|
|Headers|Specify headers for the HTTP request.|False|String|{"Content-Type": "application/json; charset=utf-8", "Accept": "application/json", "User-Agent" : "GoogleSecOps"}|
|Cookie|Specify the parameters that should be constructed into the "Cookie" header. This parameter will overwrite the cookie provided in the "Headers" parameter.|False|String|{"Cookie_1": "value_1"}|
|Body Payload|Specify body for the HTTP request.|False|String|{"Body Field Name": "Body Field Value"}|
|Expected Response Values|Specify the expected response values. If this parameter is not empty, then action will work in ASYNC mode and action will execute until the expected values will be seen or until timeout. Example input: {"key": "expected value"}|False|String||
|Follow Redirects|If enabled, action will follow the redirects.|False|Boolean|true|
|Fail on 4xx/5xx|If enabled, action will fail, if the status code of the response is 4xx or 5xx.|False|Boolean|true|
|Base64 Output|If enabled, action will convert the response to base64. This is useful when downloading files. Note: JSON result can't be bigger than 15 mb.|False|Boolean|false|
|Fields To Return|Specify what fields to return. Possible values: response_data, redirects, response_code,response_cookies,response_headers,apparent_encoding|True|String|response_data, redirects, response_code,response_cookies,response_headers,apparent_encoding|
|Request Timeout|How long to wait for the server to send data before giving up|True|String|120|
|Save To Case Wall|If enabled, action will save the file and attach it to the case wall. Note: the file will be archived with ".zip" extension. This zip will not be password protected.|False|Boolean|false|
|Password Protect Zip|If enabled, action will add an "infected" password to the zip created with "Save To Case Wall" parameter. Use this, when you are dealing with suspicious files.|False|Boolean|true|



##### JSON Results
```json
{"response_data": [{"id": "123456789012345", "name": "instance-prod-01", "status": "RUNNING", "zone": "us-central1-a", "machineType": "e2-medium", "networkIP": "10.128.0.2"}, {"id": "987654321098765", "name": "instance-dev-db", "status": "STOPPED", "zone": "us-east1-b", "machineType": "n1-standard-1", "networkIP": "10.142.0.5"}, {"id": "567890123456789", "name": "instance-test-web", "status": "SUSPENDED", "zone": "europe-west1-d", "machineType": "e2-micro", "networkIP": "10.150.0.3"}], "redirects": [], "response_code": 200, "response_cookies": {}, "response_headers": {"content-type": "application/json; charset=UTF-8", "date": "Thu, 05 Feb 2026 12:00:00 GMT", "server": "ESF"}, "apparent_encoding": "utf-8"}
```



#### Ping
Test connectivity.
Timeout - 600 Seconds



##### JSON Results
```json
{"endpoint": "https://testendpoint.com"}
```









