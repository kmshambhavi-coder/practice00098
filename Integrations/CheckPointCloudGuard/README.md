
# CheckPointCloudGuard

CloudGuard is a cloud security posture management solution for cloud environments such as Amazon AWS, Microsoft Azure, and Google Cloud Platform. CloudGuard provides network security policy management and automation for your cloud environment across providers, regions and accounts. Organizations trust CloudGuard to ensure that their network security is well defined and understood, and then to enforce that security policy on a continuous basis. In the event of an unauthorized change, (for example, somebody or something attempts to open network ports) CloudGuard prevents this and instead enforces the configuration you have previously defined.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key ID||True|String||
|API Key Secret||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the Check Point Cloud Guard with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Check Point Cloud Guard - Alerts Connector
Pull alerts from Check Point Cloud Guard.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|alertType|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Key ID|API Key ID of the Check Point Cloud Guard account.|True|String||
|API Key Secret|API Key Secret of the Check Point Cloud Guard account.|True|Password|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|True|Integer|50|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch alerts. Possible values: Low, Medium, High|True|String|Medium|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the CheckPoint Cloud Guard server is valid.|False|Boolean|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




