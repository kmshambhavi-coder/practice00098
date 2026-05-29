
# Extrahop

ExtraHop provides cloud-native cybersecurity solutions to help enterprises detect and respond to advanced threats—before they compromise your business.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{instance}.extrahop.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyio-4.9.0-py3-none-any.whl|
|certifi-2025.1.31-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|google_api_core-2.24.2-py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|pycryptodome-3.22.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|urllib3-2.3.0-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|protobuf-6.30.2-cp39-abi3-manylinux2014_x86_64.whl|
|google_auth-2.38.0-py2.py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|
|typing_extensions-4.13.0-py3-none-any.whl|
|googleapis_common_protos-1.69.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_api_python_client-2.166.0-py2.py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|TIPCommon-2.2.0-py2.py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the Extrahop with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Update Detection
Update a detection in Extrahop.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Detection ID|Specify the ID of the detection that needs to be updated.|True|String||
|Status|Specify the status for the detection.|False|List|Select One|
|Resolution|Specify the resolution for the detection. Resolution parameter is needed, if Status parameter is set to  "Closed"|False|List|Select One|
|Assign To|Specify the name of the analyst to whom the alert needs to be assigned. If “Unassign '' is provided, action will remove assignment from the alert.|False|String||



##### JSON Results
```json
{"id": 123456789, "start_time": 1742403489782, "update_time": 1744779490793, "title": "LDAP Plaintext Authentication", "description": "test", "risk_score": 45, "type": "unsafe_ldap_auth_individual", "recommended_factors": [], "recommended": false, "categories": ["sec", "sec.hardening"], "properties": {}, "participants": [{"role": "offender", "scanner_service": null, "endpoint": null, "external": false, "object_id": 987654321, "object_type": "device", "object_value": "10.10.0.1", "username": null, "id": 730}, {"role": "offender", "scanner_service": null, "endpoint": "server", "external": false, "object_id": 987654321, "object_type": "device", "object_value": "10.10.0.1", "hostname": "hostname.domain.local", "username": null, "id": 27}], "ticket_id": null, "assignee": "analyst_name", "status": "closed", "resolution": "action_taken", "mitre_tactics": [{"id": "TA0001", "name": "Initial Access", "url": "https://attack.mitre.org/tactics/TA0001"}, {"id": "TA0003", "name": "Persistence", "url": "https://attack.mitre.org/tactics/TA0003"}, {"id": "TA0004", "name": "Privilege Escalation", "url": "https://attack.mitre.org/tactics/TA0004"}, {"id": "TA0005", "name": "Defense Evasion", "url": "https://attack.mitre.org/tactics/TA0005"}, {"id": "TA0006", "name": "Credential Access", "url": "https://attack.mitre.org/tactics/TA0006"}, {"id": "TA0007", "name": "Discovery", "url": "https://attack.mitre.org/tactics/TA0007"}], "mitre_techniques": [{"id": "T1040", "name": "Network Sniffing", "url": "https://example.com", "legacy_ids": ["T1040"]}, {"id": "T1078", "name": "Valid Accounts", "url": "https://example.com", "legacy_ids": ["T1078"]}], "appliance_id": 1, "is_user_created": false, "mod_time": 1742406203932, "create_time": 1742403491994, "url": "https://example.com"}
```









## Connectors
#### Extrahop - Detections Connector
Pull information about detections from Extrahop. Note: whitelist filter works with "type" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|type|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Extrahop instance.|True|String|https://{instance}.api.cloud.extrahop.com|
|Client ID|Client ID of the Extrahop instance.|True|String||
|Client Secret|Client Secret of the Extrahop instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Extrahop server is valid.|False|Boolean|true|
|Lowest Risk Score To Fetch|Lowest risk score that needs to be used to fetch detections. Maximum: 100. If nothing is provided, the connector will ingest detections with all risk scores.|False|Integer||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve detections from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Detections To Fetch|How many detections to process per one connector iteration. Default: 100.|False|Integer|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




