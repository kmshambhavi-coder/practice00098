
# GoogleForms

Google Forms is a survey administration software included as part of the free, web-based Google Docs Editors suite offered by Google.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Delegated Email|An email address to use for the impersonation and access control.|True|String||
|Service Account JSON|The content of the service account key JSON file.|True|Password|*****|
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to Google Forms is valid.|False|Boolean||


#### Dependencies
| |
|-|
|certifi-2024.8.30-py3-none-any.whl|
|google_auth-2.36.0-py2.py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests-2.32.3-py3-none-any.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|charset_normalizer-3.4.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|proto_plus-1.25.0-py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|
|google_api_python_client-2.154.0-py2.py3-none-any.whl|
|google_api_core-2.23.0-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|googleapis_common_protos-1.66.0-py2.py3-none-any.whl|
|TIPCommon-2.0.4-py2.py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|


## Actions
#### Ping
Use the Ping action to test the connectivity to Google Forms.
Timeout - 600 Seconds









## Connectors
#### Google Forms  - Responses Connector
Pull responses from Google Forms.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The name of the field where the product name is stored.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|event_type|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment.|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the Environment Field Name field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value .* to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|The timeout limit in seconds for the Python process running the current script.|True|Integer|180|
|Delegated Email|An email address to use for the impersonation and access control.|True|String||
|Service Account JSON|The content of the service account key JSON file.|True|Password|*****|
|Form IDs To Track|A comma-separated list of Google Forms IDs to track for responses. To retrieve a form's unique ID, open the form in the Forms editor (not the public response link) and copy the string located between /d/ and /edit in the full address shown in your browser's bar.|True|String||
|Alert Severity|Severity of the alert created out of responses. Supported values: Informational, Low, Medium, High, Critical.|False|String|Low|
|Max Hours Backwards|A number of hours before the first connector iteration to retrieve responses from. This parameter applies either to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp.|True|Integer|1|
|Max Responses To Fetch|The maximum number of responses to process for every connector iteration. The maximum value is 100.|False|Integer|100|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation.|False|Boolean|false|
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to Google Forms is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




