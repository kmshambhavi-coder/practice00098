<p align="center"><img src="./Resources/SentinelOneV2.svg" 
     alt="SentinelOneV2" width="200"/></p>

# SentinelOneV2

Endpoint security software that defends every endpoint against every type of attack, at every stage in the threat lifecycle.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{server}.SentinelOne.net/|
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|proto_plus-1.27.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|googleapis_common_protos-1.74.0-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux_2_34_x86_64.whl|
|protobuf-7.34.1-cp310-abi3-manylinux2014_x86_64.whl|
|anyio-4.13.0-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240821-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|arrow-1.3.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|TIPCommon-2.3.4-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|cachetools-6.2.4-py3-none-any.whl|


## Actions
#### Create Device Control Rule
Create a Device Control Rule in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Rule JSON|JSON object of the device control rule.|True|String|{"ruleName": "String","interface": "String","ruleType": "String","action": "String","accessPermission": "String","deviceClass": "String","status": "String"}|
|Scope JSON|JSON object of the scope rule.|True|String|{"accountIds": "String","groupIds": "String","siteIds": "String"}|



##### JSON Results
```json
{"data": {"accessPermission": "Read-Write", "action": "Allow", "bluetoothAddress": null, "createdAt": "2025-10-07T10:40:59.615759Z", "creator": "abc@abc.com (abc@abc.com)", "creatorId": "123", "deviceClass": "FFh", "deviceClassName": "FF Vendor Specific", "deviceId": null, "deviceInformationServiceInfoKey": null, "deviceInformationServiceInfoValue": null, "deviceName": null, "editable": true, "gattService": null, "id": "123", "interface": "USB", "manufacturerName": null, "minorClasses": null, "order": 1, "productId": null, "ruleName": "Test", "ruleType": "class", "scope": "account", "scopeId": "123", "scopeName": "test", "status": "Disabled", "uid": null, "updatedAt": "2025-10-07T10:40:59.613682Z", "vendorId": null, "version": null}}
```



#### Create Hash Blacklist Record
Add hashes to a blacklist in SentinelOne. Note: Only SHA1 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Operating System|Specify the OS for the hash. Possible values: windows, windows_legacy, macos, linux.|True|String|windows|
|Site IDs|Specify a comma-separated list of site ids, where hash needs to be sent to the blacklist.|False|String||
|Group IDs|Specify a comma-separated list of group ids, where hash needs to be sent to the blacklist.|False|String||
|Account IDs|Specify a comma-separated list of account ids, where hash needs to be sent to the blacklist.|False|String||
|Description|Specify additional information related to the hash.|False|String||
|Add to global black list|If enabled, action will add the hash to the global blacklist. Note: when this parameter is enabled, parameters “Site IDs“, “Group IDs“ and “Account IDs“ are ignored.|False|Boolean|False|



##### JSON Results
```json
[{"Entity": "36F9CA40B3CE96FCEE1CF1D4A7222xxxxx", "EntityResult": [{"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group", "value": "36F9CA40B3CE96FCEE1CF1D4A722293xxxx", "source": "user", "updatedAt": "2020-07-02T14:41:20.678280Z", "osType": "windows", "scope": {"groupIds": ["8637125778645xxxx"]}, "type": "white_hash", "id": "9267069797567xxxx", "createdAt": "2020-07-02T14:41:20.678690Z"}, {"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group 2", "value": "36F9CA40B3CE96FCEE1CF1D4A7222xxxx", "source": "user", "updatedAt": "2020-07-02T14:41:20.683858Z", "osType": "windows", "scope": {"groupIds": ["926559911218xxx"]}, "type": "white_hash", "id": "9267069798xxxx", "createdAt": "2020-07-02T14:41:20.684677Z"}]}]
```



#### Create Hash Exclusion Record
Add hash to the exclusion list in SentinelOne. Note: Only SHA1 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Operation System|Specify the OS for the hash. Possible values: windows, windows_legacy, macos, linux.|True|String|windows|
|Site IDs|Specify a comma-separated list of site ids, where hash needs to be sent to the exclusion list.|False|String||
|Group IDs|Specify a comma-separated list of group ids, where hash needs to be sent to the exclusion list.|False|String||
|Account IDs|Specify a comma-separated list of account ids, where hash needs to be sent to the exclusion list.|False|String||
|Description|Specify additional information related to the hash.|False|String||
|Add to global exclusion list|If enabled, action will add the hash to the global exclusion list. Note: when this parameter is enabled, parameters “Site IDs“, “Group IDs“ and “Account IDs“ are ignored.|False|Boolean||



##### JSON Results
```json
[{"Entity": "36F9CA40B3CE96FCEE1CF1D4A72229xxxxx", "EntityResult": [{"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group", "value": "36F9CA40B3CE96FCEE1CF1D4A722293xxxx", "source": "user", "updatedAt": "2020-07-02T14:41:20.678280Z", "osType": "windows", "scope": {"groupIds": ["8637125778645xxxx"]}, "type": "white_hash", "id": "9267069797567xxxx", "createdAt": "2020-07-02T14:41:20.678690Z"}, {"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group 2", "value": "36F9CA40B3CE96FCEE1CF1D4A722293xxxx", "source": "user", "updatedAt": "2020-07-02T14:41:20.683858Z", "osType": "windows", "scope": {"groupIds": ["9265599112181xxxx"]}, "type": "white_hash", "id": "92670697980706xxxx", "createdAt": "2020-07-02T14:41:20.684677Z"}]}]
```



#### Create Path Exclusion Record
Add path to the exclusion list in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Path|Specify the path that needs to be added to the exclusion list.|True|String||
|Operation System|Specify the OS for the path. Possible values: windows, windows_legacy, macos, linux.|True|String|windows|
|Site IDs|Specify a comma-separated list of site ids, where path needs to be sent to the exclusion list.|False|String||
|Group IDs|Specify a comma-separated list of group ids, where path needs to be sent to the exclusion list.|False|String||
|Account IDs|Specify a comma-separated list of account ids, where path needs to be sent to the exclusion list.|False|String||
|Description|Specify additional information related to the path.|False|String||
|Add to global exclusion list|If enabled, action will add the path to the global exclusion list. Note: when this parameter is enabled, parameters “Site IDs“, “Group IDs“ and “Account IDs“ are ignored.|False|Boolean|False|
|Include Subfolders|If enabled, action will include subfolders for the provided path. This feature only works, if user provides folder path and not file path.|False|Boolean||
|Mode|Specify what mode should be used for the excluded path.|False|List|Suppress Alerts|



##### JSON Results
```json
[{"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group", "value": "Test Path", "source": "user", "inject": true, "updatedAt": "2020-07-02T10:47:07.213003Z", "osType": "windows", "scope": {"groupIds": ["863712577864500060"]}, "pathExclusionType": "file", "type": "path", "id": "926589090764579580", "createdAt": "2020-07-02T10:47:07.214956Z", "mode": "suppress"}, {"userName": "user", "description": "Created by Siemplify.", "userId": "8237415437026xxxxx", "scopeName": "Test Group 2", "value": "Test Path", "source": "user", "inject": true, "updatedAt": "2020-07-02T10:47:07.225542Z", "osType": "windows", "scope": {"groupIds": ["926559911218143489"]}, "pathExclusionType": "file", "type": "path", "id": "926589090865242880", "createdAt": "2020-07-02T10:47:07.226877Z", "mode": "suppress"}]
```



#### Delete Device Control Rule
Delete a Device Control Rule in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Rule ID|ID of the rule that needs to be deleted.|True|String||
|Scope Type|Scope type in which the alert is available.|False|List|Account|
|Scope ID|ID of the scope.|True|String||



#### Delete Hash Blacklist Record
Delete hashes from a blacklist in SentinelOne. Note: Only SHA1 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Site IDs|Specify a comma-separated list of site ids, from where the hash needs to be removed.|False|String||
|Group IDs|Specify a comma-separated list of group ids, from where the hash needs to be removed.|False|String||
|Account IDs|Specify a comma-separated list of account ids, from where the hash needs to be removed.|False|String||
|Remove from global black list|If enabled, action will remove the hash from the global black list. Note: when this parameter is enabled, parameters "Site IDs", "Group IDs" and "Account IDs" are ignored.|False|Boolean|false|



#### Disconnect Agent From Network
Disconnect agent from network by it's host name or IP address.
Timeout - 600 Seconds



#### Download Threat File
Download file related to threat in SentinelOne. Note: Your user role must have permissions to Fetch Threat File - Admin, IR Team, SOC.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|Specify the id of the threat for which you want to download the file.|True|String||
|Password|Specify the password for the zip that contains the threat file. Password requirements: At least 10 characters. Three of these: uppercase, lowercase, digits, special symbols. Maximum length is 256 characters.|True|Password|*****|
|Download Folder Path|Specify the path to the folder, where you want to store the threat file.|True|String||
|Overwrite|If enabled, action will overwrite the file with the same name.|False|Boolean|false|



##### JSON Results
```json
{"absolute_path":"files/mim.exe"}
```



#### Enrich Endpoint
Enrich information about the endpoint by IP address or Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight with information about endpoints.|False|Boolean|true|
|Only Infected Endpoints Insights|If enabled, action will only create insights for the infected endpoints.|False|Boolean|true|



##### JSON Results
```json
{"accountId":"XXXXXXXXXXXXXXXXXXXXXX","accountName":"SentinelOne","activeDirectory":{"computerDistinguishedName":"CN=XX-XXXXX,CN=XXXXXXX,DC=XXXXXX,DC=XXXXX","computerMemberOf":[],"lastUserDistinguishedName":"CN=XXXXXX,OU=XXXXXX,OU=PS,OU=XXXXXX","lastUserMemberOf":["CN=XXXXX,OU=XXXXX,OU=XXXXXXXXX,OU=XXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXX","CN=XXXXXXXXX XXXXXXXXX,CN=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXX","CN=XXXXXXXXXt,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXX","CN=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXX","CN=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXX","CN=XXXXXXXXX,OU=XXXXXXXXX,OU=XXXXXXXXX,DC=XXXXXXX,DC=XXXXXX","CN=XXXXXXX,CN=XXXXXXXXX,DC=XXXXXXXXX,DC=XXXXXXXXXX"]},"activeThreats":0,"agentVersion":"4.1.4.82","allowRemoteShell":false,"appsVulnerabilityStatus":"patch_required","computerName":"LP-Test","consoleMigrationStatus":"N/A","coreCount":8,"cpuCount":8,"cpuId":"Intel(R) Core(TM) i7-XXXX CPU @ 1.90GHz","createdAt":"2020-05-31T07:22:14.695136Z","domain":"SIEMPLIFY","encryptedApplications":false,"externalId":"","externalIp":"XXX.XXX.XXX.XXX","groupId":"XXXXXXXXXXXXXXXX","groupIp":"XXX.XXX.XXX.XXX","groupName":"Test Group","id":"XXXXXXXXXXXXXXXXXX","inRemoteShellSession":false,"infected":false,"installerType":".msi","isActive":false,"isDecommissioned":false,"isPendingUninstall":false,"isUninstalled":false,"isUpToDate":true,"lastActiveDate":"2021-01-12T12:59:43.143066Z","lastIpToMgmt":"XXX.XXX.XXX.XXX","lastLoggedInUserName":"xxxx","licenseKey":"","locationType":"fallback","locations":[{"id":"XXXXXXXXXXXXXXXX","name":"Fallback","scope":"global"}],"machineType":"laptop","mitigationMode":"protect","mitigationModeSuspicious":"protect","modelName":"Dell Inc. - Latitude 7490","networkInterfaces":[{"id":"XXXXXXXXXXXXXXXXXXXX","inet":["XXX.XXX.XXX.XXX"],"inet6":["2a10:XXXX:XXXX:0:XXXX:XXXX:XXXX:f01c","2a10:XXXX:XXXX:0:XXXX:XXXX:XXXX:f01c","fe80::XXXX:XXXX:XXXX:f01c"],"name":"Wi-Fi","physical":"d9:XX:XX:XX:h1:4e"},{"id":"XXXXXXXXXXXXXXXXX","inet":["XXX.XXX.XX.XX"],"inet6":["fe80::XXXXX:XXXXX:XXXXX:c22d"],"name":"vEthernet (Default Switch)","physical":"d9:XX:XX:XX:h1:4e"},{"id":"XXXXXXXXXXXXXXXXX","inet":["XX.XX.XX.XX"],"inet6":["XXXX::XXXX:XXXX:XXXX:XXXX","XXXX::XXXX:XXXX:XXXX:XXXX"],"name":"vEthernet (DockerNAT)","physical":"00:XXX:XXX:XX:12:11"}],"networkStatus":"connecting","osArch":"64 bit","osName":"Windows 10 Pro","osRevision":"XXXXXX","osStartTime":"2021-01-03T15:38:32Z","osType":"windows","osUsername":null,"rangerStatus":"NotApplicable","rangerVersion":null,"registeredAt":"2020-05-31T07:22:14.691561Z","scanAbortedAt":null,"scanFinishedAt":"2020-05-31T09:28:53.867014Z","scanStartedAt":"2020-05-31T07:25:37.814972Z","scanStatus":"finished","siteId":"XXXXXXXXXXXXXXXXXX","siteName":"Siemplify.co","threatRebootRequired":false,"totalMemory":34534534,"updatedAt":"2021-01-18T13:33:43.834618Z","userActionsNeeded":[],"uuid":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}
```



#### Get Agent Status
Retrieve information about the status of the agents on the endpoints based on the IP or Hostname entity.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "192.168.xx.xx", "EntityResult": {"status": "Not Active"}}]
```



#### Get Application List For Endpoint
Retrieve information about available applications on the endpoint by IP or Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Applications To Return|Specify how many applications to return. If nothing is specified action will return all of the applications.|False|String||



##### JSON Results
```json
[{"Entity": "192.168.xx.xx", "EntityResult": [{"installedDate": "2021-01-06T08:55:56.762000Z", "name": "Mozilla Firefox 84.0.1 (x64 en-US)", "publisher": "xxxx", "size": 211562, "version": "84.0.1"}, {"installedDate": "2020-07-05T09:10:51.735000Z", "name": "7-Zip 19.00 (x64)", "publisher": "xxxx", "size": 5082, "version": "19.00"}]}]
```



#### Get Blacklist
Get a list of all the items available in the blacklist in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hash|Specify a comma-separated list of hashes that need to be checked in blacklist. Only hashes that were found will be returned. If nothing is specified here action will return all hashes. Note: if "Hash" parameter is provided then "Limit" parameter is ignored.|False|String||
|Site IDs|Specify a comma-separated list of site ids, which should be used to return blacklist items.|False|String||
|Group IDs|Specify a comma-separated list of group ids, which should be used to return blacklist items.|False|String||
|Account IDs|Specify a comma-separated list of account ids, which should be used to return blacklist items.|False|String||
|Limit|Specify how many blacklist items should be returned. Note: if "Hash" parameter has values, then this parameter is ignored. Maximum is 1000.|False|String|50|
|Query|Specify the query that needs to be used in order to filter the results.|False|String||
|Use Global Blacklist|If enabled, action will also return hashes from the global blacklist.|False|Boolean|False|



##### JSON Results
```json
[{"userName": "Zivh", "description": "test", "userId": "8237415437026xxxxx", "scopeName": "Siemplify.co", "value": "cf23df2207d99a74fbe169e3eba035e633bxxxxx", "source": "user", "updatedAt": "2020-02-27T15:02:54.686991Z", "osType": "windows", "scope": {"siteIds": ["8237406459034xxxxx"]}, "type": "black_hash", "id": "8353960925573xxxxx", "createdAt": "2020-02-27T15:02:54.687675Z"}, {"description": "Detected by SentinelOne Cloud", "userId": null, "scopeName": "Siemplify.co", "value": "3395856ce81f2b7382dee72602f798b642fxxxxx", "source": "cloud", "updatedAt": "2020-03-18T14:42:02.730095Z", "osType": "linux", "scope": {"siteIds": ["8237406459034xxxxx"]}, "type": "black_hash", "id": "8498811050050xxxxx", "createdAt": "2020-03-18T14:42:02.730449Z"}, {"description": "Detected by SentinelOne Cloud", "userId": null, "scopeName": "Siemplify.co", "value": "df531d66173235167ac502b867f3cae2170xxxxx", "source": "cloud", "updatedAt": "2020-04-08T07:27:35.686775Z", "osType": "linux", "scope": {"siteIds": ["8237406459034xxxxx"]}, "type": "black_hash", "id": "8648827291549xxxxx", "createdAt": "2020-04-08T07:27:35.687168Z"}]
```



#### Get Deep Visibility Query Result
Retrieve information about deep visibility query results. Note: this action should be used in combination with “Initiate Deep Visibility Query“.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query ID|Specify the ID of the query for which you want to return results. This ID is available in the JSON result of the action “Initiate Deep Visibility Query“ as “query_id“ parameter.|True|String||
|Limit|Specify how many events to return. Default: 50. Maximum is 100.|False|String|50|



##### JSON Results
```json
{"res_events":[{"accountId":null,"activeContentFileId":null,"activeContentHash":null,"activeContentPath":null,"activeContentSignedStatus":null,"activeContentType":null,"agentDomain":"WORKGROUP","agentGroupId":"139832xxxxxxxx","agentId":"13984xxxxxxx","agentInfected":false,"agentIp":"185.180.xxx.xxx","agentIsActive":true,"agentIsDecommissioned":false,"agentMachineType":"desktop","agentName":"SentinelOne-H01","agentNetworkStatus":"connected","agentOs":"windows","agentTimestamp":"2022-04-20T19:31:13.095Z","agentUuid":"c356a5exxxxxxxxx","agentVersion":"21.7.5.1080","childProcCount":"0","createdAt":"2022-04-20T19:31:13.095000Z","crossProcCount":"0","crossProcDupRemoteProcHandleCount":"0","crossProcDupThreadHandleCount":"0","crossProcOpenProcCount":"0","crossProcOutOfStorylineCount":"0","crossProcThreadCreateCount":"0","dnsCount":"1","dnsRequest":"config.edge.skype.com","dnsResponse":"type:  5 config.edge.skype.com.trafficmanager.net;type:  5 l-0007.config.skype.com;type:  5 config-edge-skype.l-0007.l-msedge.net;type:  5 l-0007.l-msedge.net;13.107.42.16;","endpointMachineType":"desktop","endpointName":"SentinelOne-H01","endpointOs":"windows","eventIndex":"37","eventTime":"2022-04-20T19:31:13.095Z","eventType":"DNS Resolved","fileIsExecutable":"True","fileMd5":"608ee5e04b780xxxxxxx","fileSha256":"945f276f4055cbcxxxxxxxxx","id":"678236xxxxxxxxx","indicatorBootConfigurationUpdateCount":"0","indicatorEvasionCount":"0","indicatorExploitationCount":"0","indicatorGeneralCount":"0","indicatorInfostealerCount":"0","indicatorInjectionCount":"0","indicatorPersistenceCount":"0","indicatorPostExploitationCount":"0","indicatorRansomwareCount":"0","indicatorReconnaissanceCount":"0","lastActivatedAt":null,"metaEventName":"DNS","moduleCount":"111","netConnCount":"1","netConnInCount":"0","netConnOutCount":"1","objectType":"dns","osSrcChildProcCount":"0","osSrcCrossProcCount":"0","osSrcCrossProcDupRemoteProcHandleCount":"0","osSrcCrossProcDupThreadHandleCount":"0","osSrcCrossProcOpenProcCount":"0","osSrcCrossProcOutOfStorylineCount":"0","osSrcCrossProcThreadCreateCount":"0","osSrcDnsCount":"0","osSrcIndicatorBootConfigurationUpdateCount":"0","osSrcIndicatorEvasionCount":"0","osSrcIndicatorExploitationCount":"0","osSrcIndicatorGeneralCount":"0","osSrcIndicatorInfostealerCount":"0","osSrcIndicatorInjectionCount":"0","osSrcIndicatorPersistenceCount":"0","osSrcIndicatorPostExploitationCount":"0","osSrcIndicatorRansomwareCount":"0","osSrcIndicatorReconnaissanceCount":"0","osSrcModuleCount":"51","osSrcNetConnCount":"0","osSrcNetConnInCount":"0","osSrcNetConnOutCount":"0","osSrcProcActiveContentFileId":null,"osSrcProcActiveContentHash":null,"osSrcProcActiveContentPath":null,"osSrcProcActiveContentSignedStatus":null,"osSrcProcActiveContentType":null,"osSrcProcBinaryisExecutable":"True","osSrcProcCmdLine":"C:\\Windows\\system32\\svchost.exe -k NetworkService -p -s Dnscache","osSrcProcDisplayName":"Host Process for Windows Services","osSrcProcImageMd5":"cd10cb894bexxxxxxxxxxx","osSrcProcImagePath":"C:\\Windows\\System32\\svchost.exe","osSrcProcImageSha1":"1f912d4becxxxxxxxxxxx","osSrcProcImageSha256":"f3feb95e7bcfb0xxxxxxxxxxxxxx","osSrcProcIntegrityLevel":"SYSTEM","osSrcProcIsNative64Bit":"False","osSrcProcIsRedirectCmdProcessor":"False","osSrcProcIsStorylineRoot":"True","osSrcProcName":"svchost.exe","osSrcProcParentActiveContentFileId":null,"osSrcProcParentActiveContentHash":null,"osSrcProcParentActiveContentPath":null,"osSrcProcParentActiveContentSignedStatus":null,"osSrcProcParentActiveContentType":null,"osSrcProcParentCmdLine":null,"osSrcProcParentDisplayName":null,"osSrcProcParentImageMd5":null,"osSrcProcParentImagePath":null,"osSrcProcParentImageSha1":null,"osSrcProcParentImageSha256":null,"osSrcProcParentIntegrityLevel":null,"osSrcProcParentIsNative64Bit":null,"osSrcProcParentIsRedirectCmdProcessor":null,"osSrcProcParentIsStorylineRoot":null,"osSrcProcParentName":null,"osSrcProcParentPid":null,"osSrcProcParentPublisher":null,"osSrcProcParentReasonSignatureInvalid":null,"osSrcProcParentSessionId":null,"osSrcProcParentSignedStatus":null,"osSrcProcParentStartTime":null,"osSrcProcParentStorylineId":null,"osSrcProcParentUid":null,"osSrcProcParentUser":null,"osSrcProcPid":"1960","osSrcProcPublisher":"MICROSOFT WINDOWS PUBLISHER","osSrcProcReasonSignatureInvalid":null,"osSrcProcRelatedToThreat":"False","osSrcProcSessionId":"0","osSrcProcSignedStatus":"signed","osSrcProcStartTime":"2022-04-15T06:30:02.803Z","osSrcProcStorylineId":"E4ABAxxxxxxxxx","osSrcProcSubsystem":"SYS_WIN32","osSrcProcUid":"B87Bxxxxxxxxxx","osSrcProcUser":"NT AUTHORITY\\NETWORK SERVICE","osSrcProcVerifiedStatus":"verified","osSrcRegistryChangeCount":"0","osSrcTgtFileCreationCount":"0","osSrcTgtFileDeletionCount":"0","osSrcTgtFileModificationCount":"0","parentPid":"4420","parentProcessName":"MicrosoftEdgeUpdate.exe","parentProcessStartTime":"2022-04-20T19:31:12.226Z","parentProcessUniqueKey":"F0B60xxxxxxxx","pid":"4452","processCmd":"\"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe\" /ping PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48cmVxdWVzdCBwcm90b2NvbD0iMy4wIiB1cGRhdGVyPSJPbWFoYSIgdXBkYXRlcnZlcnNpb249IjEuMy4xNTcuNjEiIHNoZWxsX3ZlcnNpb249IjEuMy4xNDEuNjMiIGlzbWFjaGluZT0iMSIgc2Vzc2lvbmlkPSJ7MkE5QkQ2NDItNTkzNS00QzNFLUFCMzMtNEQ5REY3QTgxNzI2fSIgdXNlcmlkPSJ7OEM3NEM3RUQtRUI0RS00QTVELUIxQzAtRkFDQUQ5MDQ4NDA3fSIgaW5zdGFsbHNvdXJjZT0ic2NoZWR1bGVyIiByZXF1ZXN0aWQ9Ins2QTQ3M0VCQi1CNDY4LTQ0N0MtOTU4QS05QjA0REVDMUY1MEZ9IiBkZWR1cD0iY3IiIGRvbWFpbmpvaW5lZD0iMCI-PGh3IGxvZ2ljYWxfY3B1cz0iNCIgcGh5c21lbW9yeT0iOCIgZGlza190eXBlPSIyIiBzc2U9IjEiIHNzZTI9IjEiIHNzZTM9IjEiIHNzc2UzPSIxIiBzc2U0MT0iMSIgc3NlNDI9IjEiIGF2eD0iMSIvPjxvcyBwbGF0Zm9ybT0id2luIiB2ZXJzaW9uPSIxMC4wLjE5MDQzLjE2NDUiIHNwPSIiIGFyY2g9Ing2NCIvPjxvZW0gcHJvZHVjdF9tYW51ZmFjdHVyZXI9IlZNd2FyZSwgSW5jLiIgcHJvZHVjdF9uYW1lPSJWTXdhcmU3LDEiLz48ZXhwIGV0YWc9IiZxdW90O3I0NTJ0MStrMlRncS9IWHpqdkZOQlJob3BCV1I5c2JqWHhxZVVESDl1WDA9JnF1b3Q7Ii8-PGFwcCBhcHBpZD0ie0YzQzRGRTAwLUVGRDUtNDAzQi05NTY5LTM5OEEyMEYxQkE0QX0iIHZlcnNpb249IjEuMy4xNTcuNjEiIG5leHR2ZXJzaW9uPSIiIGxhbmc9IiIgYnJhbmQ9IklOQlgiIGNsaWVudD0iIiBjb2hvcnQ9InJyZkAwLjIxIj48dXBkYXRlY2hlY2svPjxwaW5nIHJkPSI1NTg4IiBwaW5nX2ZyZXNobmVzcz0ie0ExRjhFRkJFLTA0M0YtNDlDMy1BNTUwLTAyQzE5Mjk2QjAyNn0iLz48L2FwcD48YXBwIGFwcGlkPSJ7NTZFQjE4RjgtQjAwOC00Q0JELUI2RDItOEM5N0ZFN0U5MDYyfSIgdmVyc2lvbj0iMTAwLjAuMTE4NS40NCIgbmV4dHZlcnNpb249IiIgbGFuZz0iIiBicmFuZD0iSU5CWCIgY2xpZW50PSIiIGV4cGVyaW1lbnRzPSJjb25zZW50PWZhbHNlIiBjb2hvcnQ9InJyZkAwLjMwIj48dXBkYXRlY2hlY2svPjxwaW5nIHJkPSI1NTg4IiBwaW5nX2ZyZXNobmVzcz0iezJDQ0MyQkIxLTQxNDMtNEFCMi05RERGLTE2RDBCNTQzRDdBNX0iLz48L2FwcD48L3JlcXVlc3Q-","processDisplayName":"Microsoft Edge Update","processGroupId":"0BDB0xxxxxxxx","processImagePath":"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe","processImageSha1Hash":"9f76ef75fxxxxxxxxx","processIntegrityLevel":"SYSTEM","processIsRedirectedCommandProcessor":"False","processIsWow64":"True","processName":"MicrosoftEdgeUpdate.exe","processRoot":"False","processSessionId":"0","processStartTime":"2022-04-20T19:31:12.956Z","processSubSystem":"SYS_WIN32","processUniqueKey":"F0B60xxxxxxxx","publisher":"MICROSOFT CORPORATION","registryChangeCount":"13","relatedToThreat":"False","retentionPeriod":null,"rpid":null,"signatureSignedInvalidReason":null,"signedStatus":"signed","siteId":"13983xxxxxxxxx","siteName":"Siemplify-Trial","srcProcActiveContentFileId":null,"srcProcActiveContentHash":null,"srcProcActiveContentPath":null,"srcProcActiveContentSignedStatus":null,"srcProcActiveContentType":null,"srcProcBinaryisExecutable":"True","srcProcCmdLine":"\"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe\" /ping PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48cmVxdWVzdCBwcm90b2NvbD0iMy4wIiB1cGRhdGVyPSJPbWFoYSIgdXBkYXRlcnZlcnNpb249IjEuMy4xNTcuNjEiIHNoZWxsX3ZlcnNpb249IjEuMy4xNDEuNjMiIGlzbWFjaGluZT0iMSIgc2Vzc2lvbmlkPSJ7MkE5QkQ2NDItNTkzNS00QzNFLUFCMzMtNEQ5REY3QTgxNzI2fSIgdXNlcmlkPSJ7OEM3NEM3RUQtRUI0RS00QTVELUIxQzAtRkFDQUQ5MDQ4NDA3fSIgaW5zdGFsbHNvdXJjZT0ic2NoZWR1bGVyIiByZXF1ZXN0aWQ9Ins2QTQ3M0VCQi1CNDY4LTQ0N0MtOTU4QS05QjA0REVDMUY1MEZ9IiBkZWR1cD0iY3IiIGRvbWFpbmpvaW5lZD0iMCI-PGh3IGxvZ2ljYWxfY3B1cz0iNCIgcGh5c21lbW9yeT0iOCIgZGlza190eXBlPSIyIiBzc2U9IjEiIHNzZTI9IjEiIHNzZTM9IjEiIHNzc2UzPSIxIiBzc2U0MT0iMSIgc3NlNDI9IjEiIGF2eD0iMSIvPjxvcyBwbGF0Zm9ybT0id2luIiB2ZXJzaW9uPSIxMC4wLjE5MDQzLjE2NDUiIHNwPSIiIGFyY2g9Ing2NCIvPjxvZW0gcHJvZHVjdF9tYW51ZmFjdHVyZXI9IlZNd2FyZSwgSW5jLiIgcHJvZHVjdF9uYW1lPSJWTXdhcmU3LDEiLz48ZXhwIGV0YWc9IiZxdW90O3I0NTJ0MStrMlRncS9IWHpqdkZOQlJob3BCV1I5c2JqWHhxZVVESDl1WDA9JnF1b3Q7Ii8-PGFwcCBhcHBpZD0ie0YzQzRGRTAwLUVGRDUtNDAzQi05NTY5LTM5OEEyMEYxQkE0QX0iIHZlcnNpb249IjEuMy4xNTcuNjEiIG5leHR2ZXJzaW9uPSIiIGxhbmc9IiIgYnJhbmQ9IklOQlgiIGNsaWVudD0iIiBjb2hvcnQ9InJyZkAwLjIxIj48dXBkYXRlY2hlY2svPjxwaW5nIHJkPSI1NTg4IiBwaW5nX2ZyZXNobmVzcz0ie0ExRjhFRkJFLTA0M0YtNDlDMy1BNTUwLTAyQzE5Mjk2QjAyNn0iLz48L2FwcD48YXBwIGFwcGlkPSJ7NTZFQjE4RjgtQjAwOC00Q0JELUI2RDItOEM5N0ZFN0U5MDYyfSIgdmVyc2lvbj0iMTAwLjAuMTE4NS40NCIgbmV4dHZlcnNpb249IiIgbGFuZz0iIiBicmFuZD0iSU5CWCIgY2xpZW50PSIiIGV4cGVyaW1lbnRzPSJjb25zZW50PWZhbHNlIiBjb2hvcnQ9InJyZkAwLjMwIj48dXBkYXRlY2hlY2svPjxwaW5nIHJkPSI1NTg4IiBwaW5nX2ZyZXNobmVzcz0iezJDQ0MyQkIxLTQxNDMtNEFCMi05RERGLTE2RDBCNTQzRDdBNX0iLz48L2FwcD48L3JlcXVlc3Q-","srcProcDisplayName":"Microsoft Edge Update","srcProcImageMd5":"608ee5e04bxxxxxxxxxx","srcProcImagePath":"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe","srcProcImageSha1":"9f76ef75fb7bxxxxxxxxxxxx","srcProcImageSha256":"945f276f4055cbc95xxxxxxxxx","srcProcIntegrityLevel":"SYSTEM","srcProcIsNative64Bit":"True","srcProcIsRedirectCmdProcessor":"False","srcProcIsStorylineRoot":"False","srcProcName":"MicrosoftEdgeUpdate.exe","srcProcParentActiveContentFileId":null,"srcProcParentActiveContentHash":null,"srcProcParentActiveContentPath":null,"srcProcParentActiveContentSignedStatus":null,"srcProcParentActiveContentType":null,"srcProcParentCmdLine":"\"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe\" /svc","srcProcParentDisplayName":"Microsoft Edge Update","srcProcParentImageMd5":"608ee5e04b780ca18e9266c0ce7da3b2","srcProcParentImagePath":"C:\\Program Files (x86)\\Microsoft\\EdgeUpdate\\MicrosoftEdgeUpdate.exe","srcProcParentImageSha1":"9f76ef75fb7xxxxxxxxxxx","srcProcParentImageSha256":"945f276f4055cbcxxxxxxxxxx","srcProcParentIntegrityLevel":"SYSTEM","srcProcParentIsNative64Bit":"True","srcProcParentIsRedirectCmdProcessor":"False","srcProcParentIsStorylineRoot":"False","srcProcParentName":"MicrosoftEdgeUpdate.exe","srcProcParentPid":"4420","srcProcParentProcUid":"53A793Cxxxxxxxx","srcProcParentPublisher":"MICROSOFT CORPORATION","srcProcParentReasonSignatureInvalid":null,"srcProcParentSessionId":"0","srcProcParentSignedStatus":"signed","srcProcParentStartTime":"2022-04-20T19:31:12.226Z","srcProcParentStorylineId":"0BDBxxxxxxxxx","srcProcParentUid":"53A79xxxxxxxxxx","srcProcParentUser":"NT AUTHORITY\\SYSTEM","srcProcPid":"4452","srcProcPublisher":"MICROSOFT CORPORATION","srcProcReasonSignatureInvalid":null,"srcProcRelatedToThreat":"False","srcProcRpid":null,"srcProcSessionId":"0","srcProcSignedStatus":"signed","srcProcStartTime":"2022-04-20T19:31:12.956Z","srcProcStorylineId":"0BDB0xxxxxxxxxxx","srcProcSubsystem":"SYS_WIN32","srcProcTid":null,"srcProcUid":"F0B6xxxxxxxxx","srcProcUser":"NT AUTHORITY\\SYSTEM","srcProcVerifiedStatus":"verified","storyline":"0BDBxxxxxxxxxx","tgtFileCreationCount":"0","tgtFileDeletionCount":"0","tgtFileModificationCount":"2","tiOriginalEventId":null,"tiOriginalEventIndex":null,"tiOriginalEventTraceId":null,"tid":null,"tiindicatorRelatedEventTime":null,"traceId":"01G147Axxxxxxxxxx","trueContext":"0BDB0xxxxxxxxxx","user":"NT AUTHORITY\\SYSTEM","verifiedStatus":"verified"}]}
```



#### Get Events For Endpoint Hours Back
Retrieve information about the latest events on the endpoint. Works with IP and Hostname entities.Note: this action uses an endpoint that has rate limiting. Only one endpoint can be processed per minute․
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hours Back|Specify how many hours backwards to fetch events.|True|String||
|Events Amount Limit|Specify how many events to return per event type. Default: 50.|False|String|50|
|Include File Events Information|If enabled, action will also query information about file events.|False|Boolean|false|
|Include Indicator Events Information|If enabled, action will also query information about indicator events.|False|Boolean|false|
|Include DNS Events Information|If enabled, action will also query information about DNS events.|False|Boolean|false|
|Include Network Actions Events Information|If enabled, action will also query information about “network actions” events.|False|Boolean|false|
|Include URL Events Information|If enabled, action will also query information about URL events.|False|Boolean|false|
|Include Registry Events Information|If enabled, action will also query information about registry events.|False|Boolean|false|
|Include Scheduled Task Events Information|If enabled, action will also query information about scheduled task events.|False|Boolean|false|



##### JSON Results
```json
[{"EntityResult":{"file_events":[{"k8sNamespace":null,"agentOs":"linux","siteName":"example.com","eventType":"File Rename","pid":"XXXX","fileMd5":null,"containerName":null,"signatureSignedInvalidReason":null,"creation_time_unix_time":1585568500495,"newFileName":"/run/XXXXXXXXX/stub-resolv.conf","agentNetworkStatus":"connected","k8sPodLabels":null,"agentVersion":"3.3.1.14","agentName":"ip-1-1-1-1","relatedToThreat":"False","containerImage":null,"agentId":"XXXXXXXXXXXXXXXXXXXXXXXXXX","id":"XXXXXXXXXXXXXXXXXXXXXXXXX","createdAt":"2020-03-30T11:41:40.495000Z","objectType":"file","hasParent":true,"signedStatus":null,"activeContentFileId":null,"fileSha1":null,"oldFileSha1":null,"fileFullName":"/run/XXXXXXXXX/stub-resolv.conf","fileType":"conf","agentGroupId":"XXXXXXXXXXXXXXXX","agentIsDecommissioned":false,"k8sNamespaceLabels":null,"processName":"systemd-resolved","k8sClusterName":null,"k8sControllerType":null,"tid":null,"agentTimestamp":"2020-03-30T11:41:40.495Z","k8sNode":null,"fileSha256":null,"processStartTime":"2020-03-20T06:15:22.588Z","oldFileName":"/run/XXXXXXXXX/.#stub-resolv.confFRlFnD","verifiedStatus":null,"containerId":null,"oldFileSha256":null,"activeContentType":null,"convictedBy":null,"processUniqueKey":"XXXXXXXXXX-XXXXXXXXX-XXXXX-XXXXX-XXXXXXXXXXX","k8sPodName":null,"agentMachineType":"server","k8sControllerName":null,"parentProcessUniqueKey":"XXXXXXXXXX-XXXXXXXXX-XXXXX-XXXXX-XXXXXXXXXXX","user":null,"fileLocation":null,"agentIp":"XX.XXX.XXXX.XX","agentInfected":false,"fileId":null,"fileCreatedAt":"2020-03-30T11:41:40.495Z","trueContext":"XXXXX-XXXXXX-XXXX-XXXXX-XXXXXXXXXXXX","processDisplayName":"systemd-resolved","publisher":null,"agentIsActive":true,"processGroupId":"XXXXX-XXXXXX-XXXX-XXXXX-XXXXXXXXXXXX","activeContentHash":null,"rpid":null,"agentUuid":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","containerLabels":null,"agentDomain":"","k8sControllerLabels":null,"attributes":[{"section":"Main Attributes","field_id":"agentTimestamp","value":"2020-03-30T11:41:40.495Z","display":"Created At","priority":3,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"agentVersion","value":"3.3.1.14","display":"Agent Version","priority":4,"display_attribute":false,"queryable":true},{"section":"Endpoint Info","field_id":"agentUuid","value":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","display":"Agent UUID","priority":2,"display_attribute":false,"queryable":true},{"section":"Endpoint Info","field_id":"agentName","value":"ip-1-1-1-1","display":"Agent Name","priority":1,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"fileId","value":null,"display":"File Id","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileFullName","value":"/run/XXXXXXXXX/stub-resolv.conf","display":"Full Path","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"trueContext","value":"XXXXX-XXXXXX-XXXX-XXXXX-XXXXXXXXXXXX","display":"True Context","priority":7,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSha1","value":null,"display":"SHA1","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileMD5","value":null,"display":"MD5","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"oldFileName","value":"/run/XXXXXXXXX/.#stub-resolv.confFRlFnD","display":"Old File Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"oldFileMD5","value":null,"display":"Old File MD5","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"oldFileSHA1","value":null,"display":"Old File SHA1","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"oldFileSHA256","value":null,"display":"Old File SHA256","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentOs","value":"linux","display":"Agent OS","priority":3,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"parentPid","value":null,"display":"Parent PID","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessUniqueKey","value":null,"display":"Parent Process UID","priority":null,"display_attribute":true,"queryable":false},{"section":"Main Attributes","field_id":"pid","value":"XXXX","display":"Process ID","priority":5,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processDisplayName","value":"systemd-resolved","display":"Process Display Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processName","value":"systemd-resolved","display":"Process Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processStartTime","value":"2020-03-20T06:15:22.588Z","display":"Process Start Time","priority":null,"display_attribute":false,"queryable":false},{"section":"Main Attributes","field_id":"processUniqueKey","value":"XXXXXXXXXX-XXXXXXXXX-XXXXX-XXXXX-XXXXXXXXXXX","display":"Process UID","priority":6,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"user","value":null,"display":"Process User Name","priority":4,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"rpid","value":null,"display":"Rpid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSHA256","value":null,"display":"SHA256","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signatureSignedInvalidReason","value":null,"display":"Why not verified","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signedStatus","value":null,"display":"Signed Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"publisher","value":null,"display":"Publisher","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"siteName","value":"Siemplify.co","display":"Site Name","priority":6,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"tid","value":null,"display":"Tid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"verifiedStatus","value":null,"display":"Verified Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentMachineType","value":"server","display":"Agent Machine Type","priority":5,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"objectType","value":"file","display":"Object Type","priority":1,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"eventType","value":"File Rename","display":"Event Type","priority":2,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSize","value":null,"display":"File Size","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileType","value":"conf","display":"File Type","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileLocation","value":null,"display":"File Location","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"activeContentFileId","value":null,"display":"Active Content File Id","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentPath","value":null,"display":"Active Content Path","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentHash","value":null,"display":"Active Content Hash","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentSignedStatus","value":null,"display":"Active Content Signed Status","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentType","value":null,"display":"Active Content Type","priority":null,"display_attribute":false,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespace","value":null,"display":"Namespace","priority":3,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sClusterName","value":null,"display":"Cluster name","priority":1,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodName","value":null,"display":"Pod name","priority":8,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerName","value":null,"display":"Container Name","priority":10,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerId","value":null,"display":"Container ID","priority":11,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerImage","value":null,"display":"Container Image","priority":12,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerLabels","value":null,"display":"Container Labels","priority":13,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodLabels","value":null,"display":"Pod Labels","priority":9,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespaceLabels","value":null,"display":"Namespace Labels","priority":4,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNode","value":null,"display":"Node","priority":2,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerLabels","value":null,"display":"Controller Labels","priority":7,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerType","value":null,"display":"Controller Type","priority":5,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerName","value":null,"display":"Controller Name","priority":6,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"convictedBy","value":null,"display":"Convicted By","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"relatedToThreat","value":null,"display":"Related To Threat","priority":8,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"threatStatus","value":null,"display":"threat Status","priority":null,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"siteId","value":null,"display":"Site ID","priority":7,"display_attribute":false,"queryable":true}],"activeContentSignedStatus":null,"fileModifyAt":"2020-03-30T11:41:40.495Z","activeContentPath":null,"oldFileMd5":null,"fileSize":null}],"scheduled_task_events":[],"url_events":[],"dns_events":[],"network_actions_events":[],"indicator_events":[],"registry_events":[],"process_events":[{"k8sNamespace":null,"siteName":"Siemplify.co","eventType":"Process Creation","processIsRedirectedCommandProcessor":"False","parentProcessName":"sh","pid":"XXXXXX","signatureSignedInvalidReason":null,"creation_time_unix_time":1585567021358,"agentNetworkStatus":"connected","k8sPodLabels":null,"agentVersion":"3.3.1.14","processSessionId":"0","agentName":"ip-1-1-1-1","relatedToThreat":"False","containerImage":null,"agentId":"XXXXXXXXXXXXXXXXXXXXXXXXXX","id":"XXXXXXXXXXXXXXXXXX","createdAt":"2020-03-30T11:17:01.358000Z","objectType":"process","hasParent":true,"signedStatus":"unsigned","processCmd":" XXXXXXXXX --report XXXXXXXX.hourly","agentInfected":false,"parentPid":"XXXXX","agentGroupId":"XXXXXXXXXXXXXXXX","agentIsDecommissioned":false,"k8sNamespaceLabels":null,"processName":"XXXXXXXXX","processIsWow64":"False","k8sClusterName":null,"k8sControllerType":null,"processRoot":"False","agentTimestamp":"2020-03-30T11:17:01.358Z","k8sNode":null,"processStartTime":"2020-03-30T11:17:06.594Z","verifiedStatus":null,"containerId":null,"containerName":null,"activeContentFileId":null,"convictedBy":null,"processUniqueKey":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","k8sPodName":null,"agentMachineType":"server","k8sControllerName":null,"parentProcessUniqueKey":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","user":"unknown","agentIp":"XX.XXX.XXXX.XX","activeContentType":null,"md5":null,"publisher":null,"trueContext":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","sha256":null,"parentProcessStartTime":"2020-03-30T11:17:06.592Z","processDisplayName":null,"processIntegrityLevel":"INTEGRITY_LEVEL_UNKNOWN","agentIsActive":true,"processGroupId":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","activeContentHash":null,"agentUuid":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","containerLabels":null,"agentDomain":"","agentOs":"linux","processImagePath":"/bin/XXXX-XXXXX","attributes":[{"section":"Main Attributes","field_id":"agentTimestamp","value":"2020-03-30T11:17:01.358Z","display":"Created At","priority":3,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"agentVersion","value":"3.3.1.14","display":"Agent Version","priority":4,"display_attribute":false,"queryable":true},{"section":"Endpoint Info","field_id":"agentUuid","value":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","display":"Agent UUID","priority":2,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"processCmd","value":" XXXXXXXXX --report XXXXXXXX.hourly","display":"Command Line","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentName","value":"ip-1-1-1-1","display":"Agent Name","priority":1,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"trueContext","value":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","display":"True Context","priority":7,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processImagePath","value":"/bin/XXXXXXXXX","display":"Image Path","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSha1","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"SHA1","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processImageSha1Hash","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"Image SHA1 Hash","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileMD5","value":null,"display":"MD5","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentOs","value":"linux","display":"Agent OS","priority":3,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"parentPid","value":"XXXXX","display":"Parent PID","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessName","value":"sh","display":"Parent Process Name","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessStartTime","value":"2020-03-30T11:17:06.592Z","display":"Parent Process Start Time","priority":null,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"processIntegrityLevel","value":"INTEGRITY_LEVEL_UNKNOWN","display":"Process Integrity Level","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessUniqueKey","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"Parent Process UID","priority":null,"display_attribute":true,"queryable":false},{"section":"Main Attributes","field_id":"pid","value":"XXXXXX","display":"Process ID","priority":5,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processDisplayName","value":null,"display":"Process Display Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processIsRedirectedCommandProcessor","value":"false","display":"Process Is Redirected Command Processor","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processIsWow64","value":"false","display":"Process Is 64 bit","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processName","value":"XXXXXXXXX","display":"Process Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processRoot","value":"false","display":"Process Root","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processSessionId","value":"0","display":"Process Session Id","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processStartTime","value":"2020-03-30T11:17:06.594Z","display":"Process Start Time","priority":null,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"processSubSystem","value":"SUBSYSTEM_UNKNOWN","display":"Process Sub System","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"processUniqueKey","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"Process UID","priority":6,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"user","value":"unknown","display":"Process User Name","priority":4,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"rpid","value":null,"display":"Rpid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSHA256","value":null,"display":"SHA256","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signatureSignedInvalidReason","value":null,"display":"Why not verified","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signedStatus","value":"unsigned","display":"Signed Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"publisher","value":null,"display":"Publisher","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"siteName","value":"example.com","display":"Site Name","priority":6,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"tid","value":null,"display":"Tid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"verifiedStatus","value":null,"display":"Verified Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentMachineType","value":"server","display":"Agent Machine Type","priority":5,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"objectType","value":"process","display":"Object Type","priority":1,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"eventType","value":"Process Creation","display":"Event Type","priority":2,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"activeContentFileId","value":null,"display":"Active Content File Id","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentPath","value":null,"display":"Active Content Path","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentHash","value":null,"display":"Active Content Hash","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentSignedStatus","value":null,"display":"Active Content Signed Status","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentType","value":null,"display":"Active Content Type","priority":null,"display_attribute":false,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespace","value":null,"display":"Namespace","priority":3,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sClusterName","value":null,"display":"Cluster name","priority":1,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodName","value":null,"display":"Pod name","priority":8,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerName","value":null,"display":"Container Name","priority":10,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerId","value":null,"display":"Container ID","priority":11,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerImage","value":null,"display":"Container Image","priority":12,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerLabels","value":null,"display":"Container Labels","priority":13,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodLabels","value":null,"display":"Pod Labels","priority":9,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespaceLabels","value":null,"display":"Namespace Labels","priority":4,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNode","value":null,"display":"Node","priority":2,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerLabels","value":null,"display":"Controller Labels","priority":7,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerType","value":null,"display":"Controller Type","priority":5,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerName","value":null,"display":"Controller Name","priority":6,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"convictedBy","value":null,"display":"Convicted By","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"relatedToThreat","value":null,"display":"Related To Threat","priority":8,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"threatStatus","value":null,"display":"threat Status","priority":null,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"siteId","value":null,"display":"Site ID","priority":7,"display_attribute":false,"queryable":true}],"activeContentSignedStatus":null,"processSubSystem":"SUBSYSTEM_UNKNOWN","activeContentPath":null,"k8sControllerLabels":null,"processImageSha1Hash":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"},{"k8sNamespace":null,"siteName":"example.com","eventType":"Process Creation","processIsRedirectedCommandProcessor":"False","parentProcessName":"cron","pid":"XXXXX","signatureSignedInvalidReason":null,"creation_time_unix_time":1585567021357,"agentNetworkStatus":"connected","k8sPodLabels":null,"agentVersion":"3.3.1.14","processSessionId":"0","agentName":"ip-1-1-1-1","relatedToThreat":"False","containerImage":null,"agentId":"XXXXXXXXXXXXXXXXXXXXXXXXXX","id":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","createdAt":"2020-03-30T11:17:01.357000Z","objectType":"process","hasParent":true,"signedStatus":"unsigned","processCmd":" /bin/sh -c cd / && XXXXXXXXX --report XXXXXXXX.hourly","agentInfected":false,"parentPid":"XXXXX","agentGroupId":"XXXXXXXXXXXXXXXX","agentIsDecommissioned":false,"k8sNamespaceLabels":null,"processName":"sh","processIsWow64":"False","k8sClusterName":null,"k8sControllerType":null,"processRoot":"False","agentTimestamp":"2020-03-30T11:17:01.357Z","k8sNode":null,"processStartTime":"2020-03-30T11:17:06.592Z","verifiedStatus":null,"containerId":null,"containerName":null,"activeContentFileId":null,"convictedBy":null,"processUniqueKey":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","k8sPodName":null,"agentMachineType":"server","k8sControllerName":null,"parentProcessUniqueKey":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","user":"unknown","agentIp":"1.1.1.1","activeContentType":null,"md5":null,"publisher":null,"trueContext":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","sha256":null,"parentProcessStartTime":"2020-03-30T11:17:06.589Z","processDisplayName":null,"processIntegrityLevel":"INTEGRITY_LEVEL_UNKNOWN","agentIsActive":true,"processGroupId":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","activeContentHash":null,"agentUuid":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","containerLabels":null,"agentDomain":"","agentOs":"linux","processImagePath":"/bin/sh","attributes":[{"section":"Main Attributes","field_id":"agentTimestamp","value":"2020-03-30T11:17:01.357Z","display":"Created At","priority":3,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"agentVersion","value":"3.3.1.14","display":"Agent Version","priority":4,"display_attribute":false,"queryable":true},{"section":"Endpoint Info","field_id":"agentUuid","value":"XXXXXXX-XXXXXXXXX-XXXXXXX-XXXXXXX","display":"Agent UUID","priority":2,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"processCmd","value":" /bin/sh -c cd / && XXXXXXXXX --report XXXXXXXX.hourly","display":"Command Line","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentName","value":"ip-1-1-1-1","display":"Agent Name","priority":1,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"trueContext","value":"XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXXXXXXX","display":"True Context","priority":7,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processImagePath","value":"/bin/sh","display":"Image Path","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSha1","value":null,"display":"SHA1","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processImageSha1Hash","value":null,"display":"Image SHA1 Hash","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileMD5","value":null,"display":"MD5","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentOs","value":"linux","display":"Agent OS","priority":3,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"parentPid","value":"XXXXX","display":"Parent PID","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessName","value":"cron","display":"Parent Process Name","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessStartTime","value":"2020-03-30T11:17:06.589Z","display":"Parent Process Start Time","priority":null,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"processIntegrityLevel","value":"INTEGRITY_LEVEL_UNKNOWN","display":"Process Integrity Level","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"parentProcessUniqueKey","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"Parent Process UID","priority":null,"display_attribute":true,"queryable":false},{"section":"Main Attributes","field_id":"pid","value":"XXXXX","display":"Process ID","priority":5,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processDisplayName","value":null,"display":"Process Display Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processIsRedirectedCommandProcessor","value":"false","display":"Process Is Redirected Command Processor","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processIsWow64","value":"false","display":"Process Is 64 bit","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processName","value":"sh","display":"Process Name","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processRoot","value":"false","display":"Process Root","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processSessionId","value":"0","display":"Process Session Id","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"processStartTime","value":"2020-03-30T11:17:06.592Z","display":"Process Start Time","priority":null,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"processSubSystem","value":"SUBSYSTEM_UNKNOWN","display":"Process Sub System","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"processUniqueKey","value":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","display":"Process UID","priority":6,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"user","value":"unknown","display":"Process User Name","priority":4,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"rpid","value":null,"display":"Rpid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"fileSHA256","value":null,"display":"SHA256","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signatureSignedInvalidReason","value":null,"display":"Why not verified","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"signedStatus","value":"unsigned","display":"Signed Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"publisher","value":null,"display":"Publisher","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"siteName","value":"example.com","display":"Site Name","priority":6,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"tid","value":null,"display":"Tid","priority":null,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"verifiedStatus","value":null,"display":"Verified Status","priority":null,"display_attribute":true,"queryable":true},{"section":"Endpoint Info","field_id":"agentMachineType","value":"server","display":"Agent Machine Type","priority":5,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"objectType","value":"process","display":"Object Type","priority":1,"display_attribute":false,"queryable":true},{"section":"Main Attributes","field_id":"eventType","value":"Process Creation","display":"Event Type","priority":2,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"activeContentFileId","value":null,"display":"Active Content File Id","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentPath","value":null,"display":"Active Content Path","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentHash","value":null,"display":"Active Content Hash","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentSignedStatus","value":null,"display":"Active Content Signed Status","priority":null,"display_attribute":false,"queryable":true},{"section":"Other Attributes","field_id":"activeContentType","value":null,"display":"Active Content Type","priority":null,"display_attribute":false,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespace","value":null,"display":"Namespace","priority":3,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sClusterName","value":null,"display":"Cluster name","priority":1,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodName","value":null,"display":"Pod name","priority":8,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerName","value":null,"display":"Container Name","priority":10,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerId","value":null,"display":"Container ID","priority":11,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerImage","value":null,"display":"Container Image","priority":12,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"containerLabels","value":null,"display":"Container Labels","priority":13,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sPodLabels","value":null,"display":"Pod Labels","priority":9,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNamespaceLabels","value":null,"display":"Namespace Labels","priority":4,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sNode","value":null,"display":"Node","priority":2,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerLabels","value":null,"display":"Controller Labels","priority":7,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerType","value":null,"display":"Controller Type","priority":5,"display_attribute":true,"queryable":true},{"section":"Container Attributes","field_id":"k8sControllerName","value":null,"display":"Controller Name","priority":6,"display_attribute":true,"queryable":true},{"section":"Other Attributes","field_id":"convictedBy","value":null,"display":"Convicted By","priority":null,"display_attribute":true,"queryable":true},{"section":"Main Attributes","field_id":"relatedToThreat","value":null,"display":"Related To Threat","priority":8,"display_attribute":false,"queryable":false},{"section":"Other Attributes","field_id":"threatStatus","value":null,"display":"threat Status","priority":null,"display_attribute":false,"queryable":false},{"section":"Endpoint Info","field_id":"siteId","value":null,"display":"Site ID","priority":7,"display_attribute":false,"queryable":true}],"activeContentSignedStatus":null,"processSubSystem":"SUBSYSTEM_UNKNOWN","activeContentPath":null,"k8sControllerLabels":null,"processImageSha1Hash":null}]},"Entity":"ip-1-1-1-1"}]
```



#### Get Group Details
Retrieve detailed information about the provided groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Names|Specify a comma-separated list of group names for which you want to retrieve details.|True|String||



##### JSON Results
```json
[{"EntityResult":{"inherits":"False","name":"Default Group","creator":"Chris Goodman","filterName":"None","updatedAt":"2020-11-07T13:34:05.250729Z","filterId":"None","rank":"None","registrationToken":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","siteId":"XXXXXXXXXXXXXX","isDefault":"True","creatorId":"XXXXXXXXXXXXXXX","totalAgents":"0","type":"static","id":"XXXXXXXXXXXXXXXXXXX","createdAt":"2020-02-11T13:05:37.175034Z"},"Entity":"Default Group"}]
```



#### Get Hash Reputation
Deprecated! Retrieve information about the hashes from SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reputation Threshold|Specify what should be the reputation threshold in order it to be marked as suspicious. If nothing is provided, action will not mark entites as suspicious. Maximum: 10.|False|String|5|
|Create Insight|If enabled, action will create an insight containing information about the reputation.|False|Boolean|true|
|Only Suspicious Hashes Insight|If enabled, action will only create insight for hashes that have higher or equal reputation to “Reputation Threshold“ value.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult":{"data":{"rank":"10"},"is_risky":false},"Entity":"e104ea8908a0c21f245b629dc075ad1dbdea3xxx"},{"EntityResult":{"data":{"rank":"6"},"is_risky":true},"Entity":"df531d66173235167ac502b867f3cae2170adxxx"}]
```



#### Get Site Agents
Get information about agents related to a Site in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Site Name|The name of the site to return.|True|String||
|Max Agents To Return|The maximum number of agents to return. Maximum: 1000.|True|String|100|



##### JSON Results
```json
[{"accountId": "xxxx", "accountName": "xxxx", "activeDirectory": {"computerDistinguishedName": "xxxx", "computerMemberOf": [], "lastUserDistinguishedName": "xxxx", "lastUserMemberOf": [], "userPrincipalName": "xxxx"}, "activeProtection": ["xxxx"], "activeThreats": "10", "agentVersion": "xxxx", "allowRemoteShell": true, "appsVulnerabilityStatus": "xxxx", "cloudProviders": {"GCP": {"cloudAccount": "xxxx", "cloudImage": "xxxx", "cloudInstanceId": "xxxx", "cloudInstanceSize": "xxxx", "cloudLocation": "xxxx", "cloudNetwork": "xxxx", "cloudTags": ["xxxx", "xxxx"], "gcpServiceAccount": "xxxx"}}, "computerName": "xxxx", "consoleMigrationStatus": "N*A", "containerizedWorkloadCounts": null, "coreCount": "2", "cpuCount": "1", "cpuId": "xxxx", "createdAt": "xxxx", "detectionState": null, "domain": "xxxx", "encryptedApplications": false, "externalId": "", "externalIp": "xxxx", "firewallEnabled": false, "firstFullModeTime": null, "fullDiskScanLastUpdatedAt": "xxxx", "groupId": "xxxx", "groupIp": "xxxx", "groupName": "xxxx", "hasContainerizedWorkload": false, "id": "xxxx", "inRemoteShellSession": false, "infected": true, "installerType": "xxxx", "isActive": true, "isAdConnector": false, "isDecommissioned": false, "isHyperAutomate": null, "isPendingUninstall": false, "isUninstalled": false, "isUpToDate": true, "lastActiveDate": "xxxx", "lastIpToMgmt": "xxxx", "lastLoggedInUserName": "xxxx", "lastSuccessfulScanDate": "xxxx", "licenseKey": "xxxx", "locationEnabled": false, "locationType": "xxxx", "locations": null, "machineSid": "xxxx", "machineType": "xxxx", "missingPermissions": [], "mitigationMode": "xxxx", "mitigationModeSuspicious": "xxxx", "modelName": "xxxx", "networkInterfaces": [{"gatewayIp": "xxxx", "gatewayMacAddress": "xxxx", "id": "xxxx", "inet": ["xxxx"], "inet6": ["xxxx"], "name": "xxxx", "physical": "xxxx"}, {"gatewayIp": "xxxx", "gatewayMacAddress": "xxxx", "id": "xxxx", "inet": ["xxxx"], "inet6": [], "name": "xxxx", "physical": "xxxx"}], "networkQuarantineEnabled": false, "networkStatus": "xxxx", "operationalState": "xxxx", "operationalStateExpiration": null, "osArch": "xxxx", "osName": "xxxx", "osRevision": "xxxx", "osStartTime": "xxxx", "osType": "xxxx", "osUsername": "xxxx", "proxyStates": {"console": false, "deepVisibility": false}, "rangerStatus": "xxxx", "rangerVersion": null, "registeredAt": "xxxx", "remoteProfilingState": "xxxx", "remoteProfilingStateExpiration": null, "scanAbortedAt": null, "scanFinishedAt": "xxxx", "scanStartedAt": "xxxx", "scanStatus": "xxxx", "serialNumber": "xxxx", "showAlertIcon": false, "siteId": "xxxx", "siteName": "xxxx", "storageName": null, "storageType": null, "tags": {"sentinelone": [{"assignedAt": "xxxx", "assignedBy": "xxxx", "assignedById": "xxxx", "id": "xxxx", "key": "xxxx", "value": "xxxx"}]}, "threatRebootRequired": false, "totalMemory": "3930", "updatedAt": "xxxx", "userActionsNeeded": [], "uuid": "xxxx"}]
```



#### Get System Status
Fetch system status.
Timeout - 600 Seconds



##### JSON Results
```json
{"system_status": {"data": {"health": "ok"}}, "db_status": {"data": {"health": "ok"}}, "cache_status": {"data": {"health": "ok"}}}
```



#### Get System Version
Fetch system version.
Timeout - 600 Seconds



#### Get Threats
Retrieve information about threats in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mitigation Status|Specify the comma-separated list of threat statuses. Only threats that match the statuses will be returned. Possible values: mitigated, active, blocked, suspicious, suspicious_resolved|False|String||
|Created until|Specify the end time for the threats. Example: 2020-03-02T21:30:13.014874Z|False|String||
|Created from|Specify the start time for the threats. Example: 2020-03-02T21:30:13.014874Z|False|String||
|Resolved Threats|If enabled, action will only return resolved threats.|False|Boolean|false|
|Threat Display Name|Specify a display name of the threat that you want to return. Partial name will also work.|False|String||
|Limit|Specify how many threats to return. Default: 10.|False|String|10|
|API Version|Specify what version of API to use in the action. If nothing is provided connector will use version 2.1. Note: JSON result structure is different between API versions. It is recommended to use the latest one.|False|List|2.0|



##### JSON Results
```json
{"accountId":"XXXXXXXXXXXXXXXXXXXXX","accountName":"SentinelOne","agentComputerName":"desktop-XXXXXXX","agentDomain":"WORKGROUP","agentId":"XXXXXXXXXXXXXXXXXXXXX","agentInfected":false,"agentIp":"42.55.555.444","agentIsActive":false,"agentIsDecommissioned":false,"agentMachineType":"desktop","agentNetworkStatus":"connected","agentOsType":"windows","agentVersion":"X.X.X.XXXX","annotation":null,"automaticallyResolved":false,"browserType":null,"certId":"","classification":"generic.heuristic","classificationSource":"Cloud","classifierName":"MANUAL","cloudVerdict":"provider_unknown","collectionId":"XXXXXXXXXXXXXXXX","commandId":"XXXXXXXXXXXXXXXX","createdAt":"2020-03-02T21:30:13.014874Z","createdDate":"2020-03-02T21:30:12.748000Z","description":"malware detected - not mitigated yet","engines":["manual"],"external_ticket_id":null,"fileContentHash":"fc5aXXXXXXXXXXXXXXXXXXXXX6f399492","fileCreatedDate":null,"fileDisplayName":"GameBar.exe","fileExtensionType":"Executable","fileIsDotNet":null,"fileIsExecutable":true,"fileIsSystem":false,"fileMaliciousContent":null,"fileObjectId":"XXXXXXXXXXXXXXXXX","filePath":"\\Device\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX\\GameBar.exe","fileSha256":null,"fileVerificationType":"NotSigned","fromCloud":false,"fromScan":false,"id":"XXXXXXXXXXXXXXXXX","indicators":[],"initiatedBy":"dvCommand","initiatedByDescription":"Deep Visibility Command","initiatingUserId":"XXXXXXXXXXXXXXXXX","isCertValid":false,"isInteractiveSession":false,"isPartialStory":false,"maliciousGroupId":"XXXXXXXXXXXXXXXXX","maliciousProcessArguments":"-ServerName:App.AppXXXXXXXXXXXXXXXXXX.mca","markedAsBenign":true,"mitigationMode":"protect","mitigationReport":{"kill":{"status":"success"},"network_quarantine":{"status":null},"quarantine":{"status":"success"},"remediate":{"status":null},"rollback":{"status":null},"unquarantine":{"status":"sent"}},"mitigationStatus":"mitigated","publisher":"","rank":2,"resolved":true,"siteId":"XXXXXXXXXXXXXXXXX","siteName":"Siemplify.co","threatAgentVersion":"X.X.X.XXX","threatName":"GameBar.exe","updatedAt":"2020-07-07T17:19:48.260119Z","username":"DESKTOP-XXXXXXX\\diserens","whiteningOptions":[]}
```



#### Initiate Deep Visibility Query
Initiate a Deep Visibility Query search. Returns query id, which should be used in the action "Get Deep Visibility Query Result".
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query for the search.|True|String||
|Start Date|Specify the start date for the search. If nothing is specified, action will fetch events from 30 days ago.|False|String||
|End Date|Specify the end date for the search. If nothing is specified, action will use current time.|False|String||



##### JSON Results
```json
[{"query_id":"q0794f2c18433b38115982b501017c636"}]
```



#### Initiate Full Scan
Initiate a full disk scan on the endpoint in SentinelOne.
Timeout - 600 Seconds



#### List Sites
List available sites in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter sites.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value provided in the "Filter Key" parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the "Filter Key" parameter.|False|String||
|Max Records To Return|Specify how many records to return.|False|String|50|



##### JSON Results
```json
[{"accountId":"43324111xxxxxxxxxx","accountName":"SentinelOne","activeLicenses":1,"createdAt":"2020-02-11T13:05:37.172328Z","creator":"Test Name","creatorId":"43327362xxxxxxxxxx","expiration":"2022-01-11T08:00:00Z","externalId":null,"healthStatus":true,"id":"82374064xxxxxxxxxx","isDefault":false,"name":"Siemplify.co","registrationToken":"eyJ1cmwiOiAiaHR0cHM6Ly91c2VhMS1wYXJ0bmVycy5zZW50aW5lbG9uZS5uZXQiLCAic2l0ZV9rZXkiOiAiNDQzYWU2MGJmMWxxxxxxxxxx","siteType":"Paid","sku":"Complete","state":"active","suite":"Complete","totalLicenses":1000,"unlimitedExpiration":false,"unlimitedLicenses":false,"updatedAt":"2021-08-28T16:07:42.934690Z"}]
```



#### Mark as Threat
Marks suspicious threats as a true positive threat in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat IDs|Specify a comma-separated list of threat IDs that should be marked.|True|String||



##### JSON Results
```json
[{"ID": "8649395079263xxxxx", "marked_as_threat": true}, {"ID": "8846538469000xxxxx", "marked_as_threat": true}, {"ID": "9165158021848xxxxx", "marked_as_threat": true}, {"ID": "9286300562960xxxxx", "marked_as_threat": true}]
```



#### Mitigate Threat
Executes mitigation actions on the threats in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mitigation action|Specify the mitigation actions for the provided threats.|True|List|quarantine|
|Threat IDs|Specify a comma-separated list of threat IDs that should be mitigated.|True|String||



##### JSON Results
```json
[{"mitigated": true, "mitigation_action": "quarantine", "Threat_ID": "9165158021848xxxxx"}, {"mitigated": true, "mitigation_action": "quarantine", "Threat ID": "9286300562960xxxxx"}]
```



#### Move Agents
Move agents to the provided group. This action works with Hostname and IP address entities. Note: the group should be from the same site.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group ID|Specify the ID of the group, where to move the agents.|False|String||
|Group Name|Specify the name of the group, where to move the agents. Note: if both Group ID and Group Name are provided, action will put “Group ID“ in the priority.|False|String||



#### Ping
Test integration connectivity.
Timeout - 600 Seconds



#### Reconnect Agent To The Network
Reconnect disconnected endpoint to the network. Works with Hostname and IP entities.
Timeout - 600 Seconds



#### Resolve Threat
Resolve threats in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat IDs|Specify a comma-separated list of threat IDs that need to be resolved.|True|String||
|Annotation|Specify an annotation describing, why the threat can be resolved.|False|String||



##### JSON Results
```json
[{"resolved": true, "Threat_ID": "8649395079263xxxxx"}, {"resolved": true, "Threat_ID": "8846538469000xxxxx"}, {"resolved": true, "Threat_ID": "9165158021848xxxxx"}, {"resolved": true, "Threat_ID": "9286300562960xxxxx"}]
```



#### Update Alert
Update an alert in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Status|Specify the status for the alert.|False|List|Select One|
|Verdict|Specify the verdict for the alert.|False|List|Select One|



##### JSON Results
```json
{"agentDetectionInfo": {"accountId": "xxxxx", "machineType": "server", "name": "windows-server-xxxxx", "osFamily": "windows", "osName": "Windows Server 2019 Datacenter", "osRevision": "xxxxx", "siteId": "xxxxx", "uuid": "xxxxx", "version": "23.1.2.400"}, "agentRealtimeInfo": {"id": "xxxxx", "infected": true, "isActive": true, "isDecommissioned": false, "machineType": "server", "name": "windows-server-xxxxx", "os": "windows", "uuid": "xxxxx"}, "alertInfo": {"alertId": "xxxxx", "analystVerdict": "False positive", "createdAt": "2024-05-11T01:36:24.673000Z", "dnsRequest": null, "dnsResponse": null, "dstIp": null, "dstPort": null, "dvEventId": "xxxxx", "eventType": "REGVALUEMODIFIED", "hitType": "Events", "incidentStatus": "In progress", "indicatorCategory": null, "indicatorDescription": null, "indicatorName": null, "isEdr": true, "loginAccountDomain": null, "loginAccountSid": null, "loginIsAdministratorEquivalent": null, "loginIsSuccessful": null, "loginType": null, "loginsUserName": null, "modulePath": null, "moduleSha1": null, "netEventDirection": null, "registryKeyPath": "MACHINE\\SYSTEM\\ControlSet001\\Services\\WdFilter\\Security\\Security", "registryOldValue": "xxxxx", "registryOldValueType": "BINARY", "registryPath": "MACHINE\\SYSTEM\\ControlSet001\\Services\\WdFilter\\Security\\Security", "registryValue": "xxxxx", "reportedAt": "2024-05-11T01:36:29.684599Z", "source": "STAR", "srcIp": null, "srcMachineIp": null, "srcPort": null, "tiIndicatorComparisonMethod": null, "tiIndicatorSource": null, "tiIndicatorType": null, "tiIndicatorValue": null, "updatedAt": "2025-05-12T18:41:08.366615Z"}, "containerInfo": {"id": null, "image": null, "labels": null, "name": null}, "kubernetesInfo": {"cluster": null, "controllerKind": null, "controllerLabels": null, "controllerName": null, "namespace": null, "namespaceLabels": null, "node": null, "pod": null, "podLabels": null}, "ruleInfo": {"description": null, "id": "xxxxx", "name": "Registry Value Modified", "queryLang": "1.0", "queryType": "events", "s1ql": "EventType = \"Registry Value Modified\"", "scopeLevel": "account", "severity": "Critical", "treatAsThreat": "UNDEFINED"}, "sourceParentProcessInfo": {"commandline": "C:\\Windows\\system32\\services.exe", "effectiveUser": null, "fileHashMd5": "xxxxx", "fileHashSha1": "xxxxx", "fileHashSha256": "xxxxx", "filePath": "C:\\Windows\\System32\\services.exe", "fileSignerIdentity": "MICROSOFT WINDOWS PUBLISHER", "integrityLevel": "system", "loginUser": null, "name": "services.exe", "pid": "896", "pidStarttime": "2024-04-26T17:33:41.962000Z", "realUser": null, "storyline": "xxxxx", "subsystem": "sys_win32", "uniqueId": "xxxxx", "user": "NT AUTHORITY\\SYSTEM"}, "sourceProcessInfo": {"commandline": "\"C:\\ProgramData\\Microsoft\\Windows Defender\\Platform\\4.18.24030.9-0\\MsMpEng.exe\"", "effectiveUser": null, "fileHashMd5": "xxxxx", "fileHashSha1": "xxxxx", "fileHashSha256": "xxxxx", "filePath": "C:\\ProgramData\\Microsoft\\Windows Defender\\Platform\\4.18.24030.9-0\\MsMpEng.exe", "fileSignerIdentity": "MICROSOFT WINDOWS PUBLISHER", "integrityLevel": "system", "loginUser": null, "name": "MsMpEng.exe", "pid": "3672", "pidStarttime": "2024-04-26T17:34:20.203000Z", "realUser": null, "storyline": "xxxxx", "subsystem": "sys_win32", "uniqueId": "xxxxx", "user": "NT AUTHORITY\\SYSTEM"}, "targetProcessInfo": {"tgtFileCreatedAt": "1970-01-01T00:00:00Z", "tgtFileHashSha1": null, "tgtFileHashSha256": null, "tgtFileId": null, "tgtFileIsSigned": "signed", "tgtFileModifiedAt": "1970-01-01T00:00:00Z", "tgtFileOldPath": null, "tgtFilePath": null, "tgtProcCmdLine": null, "tgtProcImagePath": null, "tgtProcIntegrityLevel": "unknown", "tgtProcName": null, "tgtProcPid": null, "tgtProcSignedStatus": null, "tgtProcStorylineId": null, "tgtProcUid": null, "tgtProcessStartTime": "1970-01-01T00:00:00Z"}}
```



#### Update Analyst Verdict
Update analyst verdict of the threat in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|Specify a comma-separated list of threat ids for which you want to update the analyst verdict.|True|String||
|Analyst Verdict|Specify the analyst verdict.|True|List|Undefined|



#### Update Device Control Rule
Update a Device Control Rule in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Rule ID|ID of the rule that needs to be updated|True|String||
|Rule JSON|JSON object of the device control rule.|True|String|{"ruleName": "String","interface": "String","ruleType": "String","action": "String","accessPermission": "String","deviceClass": "String","status": "String"}|



##### JSON Results
```json
{"data": {"accessPermission": "Read-Write", "action": "Allow", "bluetoothAddress": null, "createdAt": "2025-10-07T10:40:59.615759Z", "creator": "abc@abc.com (abc@abc.com)", "creatorId": "123", "deviceClass": "FFh", "deviceClassName": "FF Vendor Specific", "deviceId": null, "deviceInformationServiceInfoKey": null, "deviceInformationServiceInfoValue": null, "deviceName": null, "editable": true, "gattService": null, "id": "123", "interface": "USB", "manufacturerName": null, "minorClasses": null, "order": 1, "productId": null, "ruleName": "Test", "ruleType": "class", "scope": "account", "scopeId": "123", "scopeName": "test", "status": "Disabled", "uid": null, "updatedAt": "2025-10-07T10:40:59.613682Z", "vendorId": null, "version": null}}
```



#### Add Threat Note
Add a note to the threat in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|Specify the id of the threat for which you want to add a note.|True|String||
|Note|Specify the note that needs to be added to the threat.|True|String||



#### Update Incident Status
Update threat incident status in SentinelOne.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat ID|Specify a comma-separated list of threat ids for which you want to update the incident status.|True|String||
|Status|Specify the incident status.|True|List|Resolved|






## Jobs

#### Sync Alerts
This job will synchronize Google SecOps Alerts and SentinelOne alerts. The job synchronizes status. Requires “SentinelOne Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” you will need to add an “Alert_ID” Alert Context Value for the job to be able to find the correct information.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Environment Name|True|String|Default Environment|
|API Root|True|String||
|API Token|True|Password|*****|
|Max Hours Backwards|False|Integer|24|
|Verify SSL|False|Boolean|true|

#### Sync Threats
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Environment Name|True|String|Default Environment|
|API Root|True|String||
|API Token|True|Password|*****|
|Max Hours Backwards|True|Integer|24|
|Verify SSL|False|Boolean|true|



## Connectors
#### SentinelOne - Alerts Connector
Pull alerts from SentinelOne. Dynamic List works with the “ruleInfo.name” parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Hours Backwards|Amount of hours from where to fetch alerts.|True|Integer|24|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|ruleInfo_name|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|The timeout limit in seconds for the python process running the current script.|True|Integer|180|
|API Root|Address of SentinelOne API root.|True|String||
|API Token|SentinelOne API token.|True|Password|*****|
|Status Filter|Comma-separated list of status that should be ingested. Possible values: Unresolved, In Progress, Resolved. If nothing is provided, the connector will fetch alerts with statuses Unresolved and InProgress.|False|String|Unresolved, In Progress|
|Case Name Template|When provided, connector will add a new key called "custom_case_name" to the Event. It can used to have a customer case name. Please refer to the documentation portal for more details. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. Note: connector will use first Siemplify Event for placeholders. Only keys that have string value will be handled.|False|String||
|Alert Name Template|If provided, connector will use this value for Alert Name. Please refer to the documentation portal for more details. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. Note: connector will use first Siemplify Event for placeholders. Only keys that have string value will be handled. If nothing is provided or user provides an invalid template, connector will use the default alert name.|False|String||
|Lowest Severity To Fetch|Lowest severity of the alerts to fetch. If nothing is provided, the connector will ingest alerts with all severities. Possible Values: Info, Low, Medium, High, Critical.|False|String||
|Max Alerts To Fetch|How many alerts to process per one connector iteration. Maximum: 100.|True|Integer|10|
|Use dynamic list as a blocklist|If enabled, the dynamic list will be used as a blocklist.|False|Boolean|false|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|true|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the SentinelOne server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### SentinelOne - Threats Connector
Pull threats from SentinelOne.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|siemplify_event|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|False|String|threatinfo_classification|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|String|180|
|API Root|Address of SentinelOne API root.|True|String|https://usea1-partners.sentinelone.net/|
|API Token|SentinelOne API token.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Sentinel public cloud server is valid.|False|Boolean|TRUE|
|Fetch Max Days Backwards|Number of days before the first connector iteration to retrieve threats from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|false|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Integer|25|
|Event Object Type Filter|A comma-separated list of event objects that need to be returned alongside threat info. This parameter is used as a filter to only return certain objects. Examples: process,ip,indicators. If nothing is provided, the connector will ingest all event object types.|False|String||
|Event Type Filter|A comma-separated list of event types that need to be returned alongside threat info. This parameter is used as a filter to only return certain event types. Examples: Process Creation, Behavioral Indicators.|False|String||
|Max Events To Return|How many events to return per threat. Maximum: 199.|False|Integer|199|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|FALSE|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|API Version|Specify what version of api to use in the connector. If nothing is provided connector will use version 2.1. Note: Siemplify Event structure is different between API versions. It is recommended to use the latest one. Possible values: 2.0, 2.1.|False|String|2.0|




