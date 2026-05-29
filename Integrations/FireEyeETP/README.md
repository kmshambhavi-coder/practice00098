
# FireEyeETP

FireEye Email Threat Prevention Cloud (ETP) is different from traditional email security. It is a complete, cloud-based email security solution that delivers automatic protection from the targeted, spear-phishing attacks. Plus, it includes industry-leading FireEye Advanced Threat Intelligence.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://etp.us.fireeye.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|False|


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
|python_dateutil-2.8.2-py2.py3-none-any.whl|
|arrow-1.4.0-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|tzdata-2026.2-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the FireEye ETP with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### FireEye ETP - Email Alerts Connector
Pull alerts from FireEye ETP. Alerts from FireEye ETP are grouped based on the email ID into one Siemplify Alert.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|alertType|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the FireEye ETP instance.|True|String|https://etp.us.fireeye.com|
|API Key|API Key of the FireEye ETP account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye ETP server is valid.|False|Boolean|False|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Timezone|Timezone of the instance. Default: UTC. Example: +1 will be UTC+1 and -1 will be UTC-1.|False|String||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use|False|String||
|Proxy Username|The proxy username to authenticate with|False|String||
|Proxy Password|The proxy password to authenticate with|False|Password|*****|




