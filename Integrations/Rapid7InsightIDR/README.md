
# Rapid7InsightIDR

Rapid7's InsightIDR is your security center for incident detection and response, authentication monitoring, and endpoint visibility. InsightIDR identifies unauthorized access from external and internal threats and highlights suspicious activity so you don't have to weed through thousands of data streams.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://[region].api.insight.rapid7.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Create Saved Query
Create Rapid7 InsightIDR saved query based on the specified action input parameters. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Name for the new saved query|True|String||
|Statement|A statement to execute in query, should follow LEQL syntax, for example: where(foo=bar)|True|String||
|Time Frame|Specify a time frame in hours for which query should fetch data.|True|String|4|
|Logs|Log names query should execute against. Parameter accepts multiple values as a comma separated string.|False|String||



##### JSON Results
```json
{"id": "xxxxxxxxxx-0003-xxxx-0000-00000000xxxx", "name": "test name", "leql": {"statement": "where(bar=foo)", "during": {"time_range": null, "to": 1608531516963, "from": 1608517116963}}, "logs": ["xxxxxxxx-fb95-xxxx-9810-12b15970xxxx", "xxxxxxxx-db5f-xxxx-b063-7aa2eaaaxxxx"]}
```



#### Delete Saved Query
Delete Rapid7 InsightIDR saved query. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Saved Query ID|ID of the saved query to delete in the format 00000000-0003-7218-0000-000000000000|True|String||



#### List Investigations
List Rapid7 InsightIDR investigations based on the specified action input parameters.  Note: Action is not working with Siemplify entities, only with action input parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Time Frame|Specify a time frame in hours for which to fetch findings.|False|String|4|
|Record limit|Specify how many records can be returned by the action.|False|String|20|
|Include Closed Investigations?|Specify whether to include closed investigations in results or not.|False|Boolean|false|



##### JSON Results
```json
[{"id": "xxxxxxxx-4522-4a6e-9838-81496a0cxxxx", "title": "Process reported as malicious ran on asset xx-srv2016-xxxx.rapidx.local", "status": "OPEN", "source": "ALERT", "assignee": {"name": "Tip Labops", "email": "example@siemplify.co"}, "alerts": [{"type": "Malicious Hash On Asset", "type_description": "A malicious hash was found on an asset.", "first_event_time": "2020-12-02T13:16:14.197Z"}], "created_time": "2020-12-02T13:18:16.758Z"}, {"id": "xxxxxxxx-32bb-4124-a86e-8de5c291xxxx", "title": "Process reported as malicious ran on asset xx-srv2016-xxxx.rapidx.local", "status": "OPEN", "source": "ALERT", "alerts": [{"type": "Malicious Hash On Asset", "type_description": "A malicious hash was found on an asset.", "first_event_time": "2020-12-01T15:03:56.356Z"}], "created_time": "2020-12-01T15:05:24.825Z"}]
```



#### List Saved Queries
List Rapid7 InsightIDR saved queries.  Note: Action is not working with Siemplify entities, only with action input parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record limit|Specify how many records can be returned by the action.|False|String|20|



##### JSON Results
```json
[{"id": "xxxxxxxx-0003-xxxx-0000-00000000xxxx", "name": "MySearch", "leql": {"statement": "where(bar=foo)", "during": {"time_range": null, "to": 1450557608000, "from": 1450557604000}}, "logs": ["xxxxxxxx-8ddd-xxxx-9e15-2dc488f0xxxx", "xxxxxxxx-113e-xxxx-a6b8-ea0be1a4xxxx"]}, {"id": "xxxxxxxx-0003-xxxx-0000-00000000xxxx", "name": "test", "leql": {"statement": "groupby('destination_account')", "during": {"time_range": "Last 5 Minutes", "to": null, "from": null}}, "logs": ["xxxxxxxx-8ddd-xxxx-9e15-2dc488f0xxxx", "xxxxxxxx-113e-xxxx-a6b8-ea0be1a4xxxx", "xxxxxxxx-a7c4-xxxx-b221-d60d260bxxxx", "xxxxxxxx-cf85-xxxx-9ac5-e329b523xxxx"]}]
```



#### Ping
Test connectivity to the Rapid7 InsightIDR service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Run Saved Query
Run a Rapid7 InsightIDR saved query. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Saved Query ID|Because Saved query names are not unique, provide a saved query ID to execute.|True|String||



##### JSON Results
```json
[{"labels": [], "timestamp": 1606991986795, "sequence_number": "32371302194xxxxxxxx", "log_id": "xxxxxxxx-fb95-xxxx-9810-12b1xxxxxxxx", "message": "{\"timestamp\":\"2020-12-03T10:39:41.799Z\",\"hostname\":\"HW-SRV2016-xxxx.RAPIxx.local\",\"event_code\":\"46xx\",\"description\":\"A new process has been created.\",\"subject_user_sid\":\"S-1-5-xx\",\"subject_user_name\":\"HW-SRV2016-xxxx$\",\"subject_domain_name\":\"RAxxxx\",\"subject_logon_id\":\"0x3xx\",\"new_process_id\":\"0x1xx\",\"new_process_name\":\"C:\\\\Windows\\\\Temp\\\\xxxxxxxx-200A-xxxx-9171-C55Axxxxxxxx\\\\DismHost.exe\",\"token_elevation_type\":\"%%19xx\",\"process_id\":\"0x10xx\",\"command_line\":\"C:\\\\Windows\\\\TEMP\\\\xxxx-200A-xxxx-9171-C55Axxxxxxxx\\\\dismhost.exe {xxxxxxxx-12D2-xxxx-AD41-4C0Cxxxxxxxx}\",\"target_user_sid\":\"S-1-x-x\",\"target_user_name\":\"-\",\"target_domain_name\":\"-\",\"target_logon_id\":\"0x0\",\"parent_process_name\":\"C:\\\\Windows\\\\System32\\\\wbem\\\\WmiPrvSE.exe\",\"mandatory_label\":\"S-1-16-1xxxx\",\"source_json\":{\"eventCode\":46xx,\"computerName\":\"HW-SRV2016-xxxx.RAPIxx.local\",\"insertionStrings\":[\"S-1-5-xx\",\"HW-SRV2016-xxxx$\",\"RAxxxx\",\"0x3xx\",\"0x1xx\",\"C:\\\\Windows\\\\Temp\\\\xxxxxxxx-200A-xxxx-9171-C55Axxxxxxxx\\\\DismHost.exe\",\"%%19xx\",\"0x10xx\",\"C:\\\\Windows\\\\TEMP\\\\xxxxxxxx-200A-xxxx-9171-C55Axxxxxxxx\\\\dismhost.exe {xxxxxxxx-12D2-xxxx-AD41-4C0Cxxxxxxxx}\",\"S-1-x-x\",\"-\",\"-\",\"0x0\",\"C:\\\\Windows\\\\System32\\\\wbem\\\\WmiPrvSE.exe\",\"S-1-16-1xxxx\"],\"timeGenerated\":\"20201203103941.799511-000\",\"osVersion\":\"M\"}}", "links": [{"rel": "Context", "href": "https://eu.api.insight.RAPIxx.com/log_search/query/context/32371302194xxxxxxxx?per_page=2&timestamp=1606991986795&log_keys=xxxxxxxx-fb95-xxxx-9810-12b1xxxxxxxx&context_type=SURROUND"}], "sequence_number_str": "32371302194xxxxxxxx"}, {"labels": [], "timestamp": 1606991986799, "sequence_number": "32371302194xxxxxxxx", "log_id": "xxxxxxxx-fb95-xxxx-9810-12b1xxxxxxxx", "message": "{\"timestamp\":\"2020-12-03T10:39:41.113Z\",\"hostname\":\"HW-SRV2016-xxxx.RAPIxx.local\",\"event_code\":\"46xx\",\"description\":\"A new process has been created.\",\"subject_user_sid\":\"S-1-5-xx\",\"subject_user_name\":\"HW-SRV2016-xxxx$\",\"subject_domain_name\":\"RAPIxx\",\"subject_logon_id\":\"0x3xx\",\"new_process_id\":\"S-1-x-x\",\"new_process_name\":\"C:\\\\Windows\\\\System32\\\\wbem\\\\WmiPrvSE.exe\",\"token_elevation_type\":\"%%19xx\",\"process_id\":\"0x3xx\",\"command_line\":\"C:\\\\Windows\\\\system32\\\\wbem\\\\wmiprvse.exe -Embedding\",\"target_user_sid\":\"S-1-x-x\",\"target_user_name\":\"-\",\"target_domain_name\":\"-\",\"target_logon_id\":\"0x0\",\"parent_process_name\":\"C:\\\\Windows\\\\System32\\\\svchost.exe\",\"mandatory_label\":\"S-1-16-1xxxx\",\"source_json\":{\"eventCode\":46xx,\"computerName\":\"HW-SRV2016-xxxx.RAPIxx.local\",\"insertionStrings\":[\"S-1-5-xx\",\"HW-SRV2016-xxxx$\",\"RAPIxx\",\"0x3xx\",\"S-1-x-x\",\"C:\\\\Windows\\\\System32\\\\wbem\\\\WmiPrvSE.exe\",\"%%19xx\",\"0x3xx\",\"C:\\\\Windows\\\\system32\\\\wbem\\\\wmiprvse.exe -Embedding\",\"S-1-x-x\",\"-\",\"-\",\"0x0\",\"C:\\\\Windows\\\\System32\\\\svchost.exe\",\"S-1-16-1xxxx\"],\"timeGenerated\":\"20201203103941.113264-000\",\"osVersion\":\"M\"}}", "links": [{"rel": "Context", "href": "https://eu.api.insight.RAPIxx.com/log_search/query/context/32371302194xxxxxxxx?per_page=2&timestamp=1606991986799&log_keys=xxxxxxxx-fb95-xxxx-9810-12b1xxxxxxxx&context_type=SURROUND"}], "sequence_number_str": "32371302194xxxxxxxx"}]
```



#### Set Investigation Assignee
Set the assignee for the specific Rapid7 InsightIDR investigation. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Investigation ID|ID of investigation to update assignee for. ID should be in the format like 8ec8e324-4522-4a6e-9838-81496a0cadb0.|True|String||
|Assignee email|Email of a new assignee of investigation.|True|String||



##### JSON Results
```json
{"id": "xxxxxxxx-0155-45e5-8dcf-67302f32xxxx", "title": "Process reported as malicious ran on asset xx-srv2016-rpd7.rapixx.local", "status": "OPEN", "source": "ALERT", "assignee": {"name": "Tip Labops", "email": "example@siemplify.co"}, "alerts": [{"type": "Malicious Hash On Asset", "type_description": "A malicious hash was found on an asset.", "first_event_time": "2020-11-30T08:45:23.915Z"}], "created_time": "2020-11-30T08:47:09.291Z"}
```



#### Set Investigation Status
Set the status for the specific Rapid7 InsightIDR investigation. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Investigation ID|ID of investigation to update status for. ID should be in the format like 8ec8e324-4522-4a6e-9838-81496a0cadb0|True|String||
|Status|New Status of investigation.|True|List||



##### JSON Results
```json
{"id": "xxxxxxxx-4522-4a6e-9838-81496a0cxxxx", "title": "Process reported as malicious ran on asset xx-srv2016-rpxx.rapid7.local", "status": "OPEN", "source": "ALERT", "assignee": {"name": "Tip Labops", "email": "example@siemplify.co"}, "alerts": [{"type": "Malicious Hash On Asset", "type_description": "A malicious hash was found on an asset.", "first_event_time": "2020-12-02T13:16:14.197Z"}], "created_time": "2020-12-02T13:18:16.758Z"}
```



#### Update Investigation
Update investigation in Rapid7 InsightIDR. Note: this action was built using API endpoints that are in preview release.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Investigation ID|Specify the ID of the investigation that needs to be updated.|True|String||
|Status|Specify the status for the investigation.|False|List||
|Disposition|Specify the disposition for the investigation.|False|List||



##### JSON Results
```json
{"rrn": "rrn:investigation:eu:d16635a5-xxxx-xxxx-xxxx-67a4fbf26eb4:investigation:PAQBBKR4941D", "organization_id": "d16635a5-xxxx-xxxx-xxxx-67a4fbf26eb4", "title": "Suspicious Process - Malicious Hash On Asset", "source": "ALERT", "status": "OPEN", "priority": "HIGH", "last_accessed": "2022-10-12T13:08:37.650Z", "created_time": "2022-10-12T13:08:37.650Z", "disposition": "NOT_APPLICABLE", "assignee": null, "first_alert_time": "2022-10-12T13:08:37.643Z", "latest_alert_time": "2022-10-12T13:11:43.018Z"}
```









## Connectors
#### Rapid7 InsightIDR - Investigations Connector
This connector was built using API endpoints that are in preview release. Pull information about investigation from Rapid7 InsightIDR. Note: Dynamic list filter works with the "title" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|data_type|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|source|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the Rapid7 InsightIDR instance.|True|String|https://{instance}.api.insight.rapid7.com|
|API Key|API Key of the Rapid7 InsightIDR account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Rapid7 InsightIDR server is valid.|False|Boolean|true|
|Sources|Sources that will be used to fetch investigations. Possible values: User, Alert. If nothing is provided, the connector will ingest investigations from both sources.|False|String|ALERT,USER|
|Lowest Priority To Fetch|The lowest priority that needs to be used to fetch investigations. Possible values: Low, Medium, High, Critical. If nothing is specified, the connector ingests alerts with all severities.|False|String|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve investigations from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Default: 20.|False|Integer|20|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




