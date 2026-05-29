
# FireEyeEX

FireEye Email Security detects and blocks every kind of unwanted email, especially targeted advanced attacks. Time and again, this solution has proven itself capable of detecting corporate email threats in traffic accepted as safe by other products

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|None|https://<address>:<port>|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|defusedxml-0.7.1-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Delete Quarantined Email
Deletes quarantined email.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Queue ID|Specify the queue id of the email that needs to be deleted.|True|String|None|



#### Download Alert Artifacts
Download alert artifacts.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert UUID|Specify the alert uuid from where we need to download artifacts.|True|String|None|
|Download Path|Specify where the action should save the files. If nothing is specified, action will not save the file on the disk. |True|String||



##### JSON Results
```json
[{"file_path": "/tmp/Alert_Artifacts_19d1e07a-2376-4fde-977c-87888e7xxx.zip"}]
```



#### Download Quarantined Email
Downloads quarantined email.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Queue ID|Specify the queue id of the email that needs to be downloaded.|True|String|None|
|Download Path|Specify where the action should save the files. If nothing is specified, action will not save the file on the disk. |True|String||



##### JSON Results
```json
[{"file_path": "/tmp/Quarantined_email_2376-4fde-977c-87888e7xxx.eml"}]
```



#### Ping
Test connectivity to the FireEye EX with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Release Quarantined Email
Releases quarantined email.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Queue ID|Specify the queue id of the email that needs to be released.|True|String|None|



#### List Quarantined Emails
List quarantined emails.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Start Time|If specified, only emails that were created after start time will be returned. If Start Time and End Time are not specified, action returns quarantined emails from the last 24 hours. Format: YYYY-MM-DD'T'HH:MM:SS.SSS-HHMM|False|String||
|End Time|If specified, only emails that were created before end time will be returned.  If Start Time and End Time are not specified, action returns quarantined emails from the last 24 hours. Format: YYYY-MM-DD'T'HH:MM:SS.SSS-HHMM|False|String||
|Sender Filter|If specified, returns all of the quarantined emails only from this sender.|False|String|None|
|Subject Filter|If specified, returns all of the quarantined emails only with this subject.|False|String||
|Max Email to Return|Specify how many emails to return. Limit is 10000. This is FireEye EX limitation.|False|String|None|



##### JSON Results
```json
[{"from": "test.user1@fex2-lab.local", "completed_at": "2020-06-03T15:39:15", "quarantine_path": "/data/email-analysis/quarantine2/2020-06-03/15/49cY3l0dK9zxNgJ", "queue_id": "49cY3l0dK9zxNgJ", "email_uuid": "5f89bf79-32c7-4c61-86ac-f825dd4c6f4a", "message_id": "274ebe82-8576-1ac8-491c-de03e080be89@fex2-lab.local", "subject": "Yura"}]
```









## Connectors
#### FireEye EX - Alerts Connector
FireEye EX - Alerts Connector.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|name|
|Environment Field Name|Describes the name of the field where the environment name is stored.If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of FireEye EX server.|True|String|https://x.x.x.x:x|
|Username|Username of the FireEye EX account.|True|String||
|Password|Password of the FireEye EX account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye EX server is valid.|False|Boolean|True|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Max supported value is 48. This is the FireEye EX limitation.|True|Integer|1|
|Proxy Server Address|The address of the proxy server to use|False|String||
|Proxy Username|The proxy username to authenticate with|False|String||
|Proxy Password|The proxy password to authenticate with|False|Password|*****|




