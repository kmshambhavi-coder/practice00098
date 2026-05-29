
# CBDefense

Next-generation antivirus + EDR in one cloud-delivered platform that stops commodity malware, advanced malware, non-malware attacks and ransomware

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|None|https://<server-address>|
|Api Key||True|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|validators-0.35.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|protobuf-7.34.1-py3-none-any.whl|
|packaging-26.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|pyyaml-6.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|six-1.17.0-py2.py3-none-any.whl|
|prompt_toolkit-3.0.52-py3-none-any.whl|
|cbapi-1.7.10-py2.py3-none-any.whl|
|pygments-2.20.0-py3-none-any.whl|
|solrq-1.1.2-py2.py3-none-any.whl|
|wcwidth-0.6.0-py3-none-any.whl|
|cachetools-7.0.6-py3-none-any.whl|
|pika-1.3.2-py3-none-any.whl|


## Actions
#### Change Policy
Change device policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The new policy name. e.g. TEST_Policy|True|String||



#### Create Policy
Create a new Policy on Cb Defense
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Name for the policy|True|String|None|
|Policy Description|A description of the policy|True|String|None|
|Priority Level|The priority score associated with sensors assigned to this policy. e.g. LOW|True|String||
|Policy Details|The policy details|True|String|None|



#### Delete Policy
Delete a policy from Cb Defense
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Policy name|True|String|None|



#### Delete Rule From Policy
Remove a rule from an existing policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Policy name|True|String|None|
|Rule ID|Rule ID. e.g. 1|True|String|None|



#### Get Device Info
Get information about a device
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"assignedToName": null, "macAddress": null, "adGroupId": 0, "avEngine": "", "avVdfVersion": null, "rootedByAnalyticsTime": null, "linuxKernelVersion": null, "lastExternalIpAddress": "1.1.1.1", "lastDevicePolicyRequestedTime": null, "activationCodeExpiryTime": 1513776891190, "currentSensorPolicyName": null, "organizationName": "test.com", "deviceGuid": null, "loginUserName": null, "lastPolicyUpdatedTime": null, "registeredTime": 1513172091219, "deviceSessionId": null, "lastDevicePolicyChangedTime": null, "windowsPlatform": null, "osVersion": "Windows 10 x64", "firstVirusActivityTime": 0, "avUpdateServers": null, "lastReportedTime": 1520325064134, "middleName": null, "activationCode": null, "deregisteredTime": null, "lastResetTime": 0, "lastInternalIpAddress": "1.1.1.1", "deviceOwnerId": 260377, "avMaster": false, "lastLocation": "OFFSITE", "deviceType": "WINDOWS", "targetPriorityType": "MEDIUM", "encodedActivationCode": null, "lastVirusActivityTime": 0, "avStatus": ["AV_BYPASS"], "sensorStates": ["ACTIVE", "LIVE_RESPONSE_NOT_RUNNING", "LIVE_RESPONSE_NOT_KILLED"], "email": "test", "virtualizationProvider": null, "avPackVersion": null, "assignedToId": null, "scanStatus": null, "name": "HP-01", "policyName": "default", "scanLastActionTime": 0, "vdiBaseDevice": null, "rootedByAnalytics": false, "testId": -1, "avProductVersion": null, "rootedBySensorTime": null, "lastShutdownTime": 1519811818082, "quarantined": false, "createTime": null, "deviceId": 123456, "sensorVersion": "1.1.1.1", "passiveMode": false, "virtualMachine": false, "firstName": null, "uninstallCode": null, "uninstalledTime": null, "messages": null, "policyOverride": false, "organizationId": 1234, "sensorOutOfDate": false, "avAveVersion": null, "status": "REGISTERED", "policyId": 1234, "deviceMetaDataItemList": null, "lastName": null, "originEventHash": null, "avLastScanTime": 0, "rootedBySensor": false, "scanLastCompleteTime": 0, "lastContact": 1520325053567}, "Entity": "HP-01"}]
```



#### Get Events
Get events by entity
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Timeframe of the search. e.g. 3h|True|String||



##### JSON Results
```json
[{"EntityResult": {"0": {"eventId": "00000000000000000000000000000000", "parentApp": {"applicationName": "C: \\Temp\\test.exe", "md5Hash": null, "reputationProperty": null, "effectiveReputation": null, "applicationPath": null, "virusName": null, "effectiveReputationSource": null, "virusCategory": null, "sha256Hash": "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08", "virusSubCategory": null}, "eventTime": 1490617768036, "selectedApp": {"applicationName": "test.exe", "md5Hash": "098f6bcd4621d373cade4e832627b4f6", "reputationProperty": "TRUSTED_WHITE_LIST", "effectiveReputation": null, "applicationPath": "C: \\Temp\\test.exe", "virusName": null, "effectiveReputationSource": null, "virusCategory": null, "sha256Hash": "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08", "virusSubCategory": null}, "attackStage": null, "processDetails": {"userName": "TEST", "interpreterHash": null, "parentCommandLine": "C: \\Temp\\test.exe", "milisSinceProcessStart": 32, "name": "test.exe", "parentPid": 111, "processId": 1234, "interpreterName": null, "commandLine": "temp.exe{5267BC82-9B0D-4F0B-A566-E06CDE5602F1}S-1-5-18: NTAUTHORITY\\Test: Service: ", "parentName": "test.exe", "parentPrivatePid": "772-1489763380982-18", "targetPrivatePid": "2468-1490617768051-975", "targetPid": 12345, "targetCommandLine": "C: \\ProgramFiles(x86)\\Google\\Update\\GoogleUpdate.exe", "privatePid": "2872-1490617768004-974", "targetName": "GoogleUpdate.exe", "fullUserName": "NTAUTHORITY\\TEST"}, "eventType": "SYSTEM_API_CALL", "targetApp": {"applicationName": "C: \\ProgramFiles(x86)\\Google\\Update\\GoogleUpdate.exe", "md5Hash": null, "reputationProperty": "TRUSTED_WHITE_LIST", "effectiveReputation": null, "applicationPath": null, "virusName": null, "effectiveReputationSource": null, "virusCategory": null, "sha256Hash": "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08", "virusSubCategory": null}, "longDescription": "", "threatIndicators": ["SUSPENDED_PROCESS"], "securityEventCode": null, "registryValue": null, "incidentId": null, "shortDescription": "", "createTime": 1490617872232, "alertScore": 0, "alertCategory": null}}, "Entity": "HP-01"}]
```



#### Get Processes
List processes by device
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Timeframe|Timeframe of the search. e.g. 3h|True|String||



##### JSON Results
```json
[{"EntityResult": {"0": {"applicationName": "chrome.exe", "processId": 1234, "numEvents": 111, "applicationPath": null, "privatePid": "3052-1489181082476-30", "sha256Hash": "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08"}}, "Entity": "HP-01"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









