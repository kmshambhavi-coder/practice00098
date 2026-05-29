
# F5BIGIPAccessPolicyManager

BIG-IP® Access Policy Manager® (APM) is a flexible, high-performance, centralized access management and security solution that delivers contextual, unified global access to your applications and network as well as to the Internet. It converges and consolidates remote, LAN, and web access and wireless access within a single management interface, while also enabling the quick creation of easy-to-manage, context-based access policies. As a result, BIG-IP APM helps you free up valuable IT resources, ensure the security of your applications and network, and scale quickly and cost-effectively.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|BIG-IP APM Address||True|String|https://{IP-Address}|
|User Name||True|String||
|Password||True|Password|*****|
|Token Timeout (in Seconds)||False|String|36000|
|Verify SSL||False|Boolean|false|


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
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Disconnect Sessions
The action will disconnect the specified sessions from the F5 BIG-IP instance. Action can work using entities or using parameters, according to the Use Case Entities parameter’s value. Supported entities are Address and User Name. NOTE - Filters will be used with an OR logic, so that every session that even one of the parameters, or entities, will be matched in - will be disconnected.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Use Case Entities|Specify whether the action should disconnect sessions using Address and Client IP entities found in the case, or work on the provided parameters only. NOTE - once checked, action will ignore all other parameters in the action|False|Boolean|False|
|Session IDs|Specify specific session IDs you would like to disconnect, in a comma separated list|False|String||
|Logon User Names|Specify Logon User Names you would like to disconnect sessions for, in a comma separated list, so only sessions for these Logon User Names will be disconnected.|False|String||
|Client IPs|Specify Client IPs you would like to disconnect the sessions for,in a comma separated list, so only sessions for these Client IPs will be disconnected.|False|String||



#### List Active Sessions
The action will list all the currently active sessions in the F5 BIG-IP Access Policy Manager.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Limit|Specify the maximum number of entries you would like to get in the action.|False|String||



##### JSON Results
```json
[{"sessionID": "2e9e6xxx", "nestedStats": {"entries": {"clientIp": {"description": "10.0.0.0"}, "logonUser": {"description": "n/a"}}}}]
```



#### Ping
Test connectivity to the F5 BIG-IP Access Policy Manager with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









