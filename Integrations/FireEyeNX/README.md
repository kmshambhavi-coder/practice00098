
# FireEyeNX

FireEye Network Security is an effective cyber threat protection solution that helps organizations minimize the risk of costly breaches by accurately detecting and immediately stopping advanced, targeted and other evasive attacks hiding in Internet traffic. It facilitates efficient resolution of detected security incidents in minutes with concrete evidence, actionable intelligence and response workflow integration.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://<address>:<port>/|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|TIPCommon-1.0.12.1-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Add IPS Policy Exception
Add IPS Policy Exception in FireEye NX. Note: IP entities are treated as "Attacker IP Address".
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Victim IP Subnet|Specify the IP subnet of the victim that should be used to create a new policy exception. Format: x.x.x.x/xx Example: 10.0.0.1/24|True|String||
|Interface|Specify what interface should be used in policy exceptions.|True|List|ALL|
|Mode|Specify the mode that should be used in the policy exception.|True|List|Block|
|Name|Specify the name for the policy exception. If nothing is specified, action will add policy exception with name Siemplify_{Interface}_{Mode}|False|String||



#### Download Alert Artifacts
Download alert artifacts.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert UUID|Specify the alert uuid from where we need to download artifacts.|True|String||
|Download Path|Specify where the action should save the files.|True|String||



##### JSON Results
```json
{"file_path": "/opt/siemplify/siemplify_server/bin/Scripting/PythonSDK/IntegrationsVirtualEnvironment/FireEyeNX_V1.0/12ec4cfb-43d4-421c-910f-1b0795cxxxxx.zip"}
```



#### Ping
Test connectivity to the FireEye NX with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### FireEye NX - Alerts Connector
Connector ingests FireEye NX alert into Siemplify.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|name|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of FireEye NX server.|True|String|https://x.x.x.x:x|
|Username|Username of the FireEye NX account.|True|String||
|Password|Password of the FireEye NX account.|True|Password|*****|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye NX server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




