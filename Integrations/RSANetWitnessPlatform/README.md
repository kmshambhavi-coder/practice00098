
# RSANetWitnessPlatform

RSA NetWitness Platform accelerates threat detection and response by collecting and analyzing data across more capture points (logs, packets, netflow and endpoint) and computing platforms (physical, virtual and cloud) and enriching this data with threat intelligence and business context.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Broker API Root||False|None|http://x.x.x.x:50103|
|Broker API Username||False|String||
|Broker API Password||False|Password|*****|
|Concentrator API Root||False|None|http://x.x.x.x:50105|
|Concentrator API Username||False|String||
|Concentrator API Password||False|Password|*****|
|Web API Root||False|None|https://{ip}/rest/api/|
|Web Username||False|String||
|Web Password||False|Password|*****|
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
#### Add Note to Incident
Add Note to Incident in RSA Netwitness. Requires RSA Netwitness Respond license, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify ID of the incident that needs to be updated.|True|String||
|Note|Specify which note should be added to.|True|String||
|Author|Specify the author of the note.|True|String||



#### Enrich Endpoint
Fetch endpoint's system information by its hostname or IP address. Requires RSA Netwitness Respond license, endpoint server service running in the background, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Specify risk threshold for the endpoint. If the endpoint exceeds the threshold, the related entity will be marked as suspicious. If nothing is specified, action won’t check the risk score.|False|String|50|



##### JSON Results
```json
[{"Entity": "RSA-HOST-1", "EntityResult": {"agentId": "575EDC44-BDF9-6D00-FFCD-D354FB64xxxx", "hostName": "RSA-HOST-1", "riskScore": 100, "lastSeenTime": "2020-09-15T13:44:54.949Z", "networkInterfaces_0_name": "Intel(R)82574LGigabitNetworkConnection", "networkInterfaces_0_macAddress": "00:50:56:A2:30:03", "networkInterfaces_0_ipv4": ["172.30.203.145"], "networkInterfaces_0_ipv6": ["fe80::dce6:5825:454a:968d"], "networkInterfaces_0_networkIdv6": ["fe80::"], "networkInterfaces_0_gateway": ["172.30.203.1"], "networkInterfaces_0_dns": ["8.8.8.8"], "networkInterfaces_0_promiscuous": false}}, {"Entity": "172.30.203.145", "EntityResult": {"agentId": "575EDC44-BDF9-6D00-FFCD-D354FB64xxxx", "hostName": "RSA-HOST-1", "riskScore": 100, "lastSeenTime": "2020-09-15T13:44:54.949Z", "networkInterfaces_0_name": "Intel(R)82574LGigabitNetworkConnection", "networkInterfaces_0_macAddress": "00:50:56:A2:30:03", "networkInterfaces_0_ipv4": ["172.30.203.145"], "networkInterfaces_0_ipv6": ["fe80::dce6:5825:454a:968d"], "networkInterfaces_0_networkIdv6": ["fe80::"], "networkInterfaces_0_gateway": ["172.30.203.1"], "networkInterfaces_0_dns": ["8.8.8.8"], "networkInterfaces_0_promiscuous": false}}]
```



#### Enrich File
Fetch information about the file using hashes or file names. Only MD5 and SHA256 are supported. Requires RSA Netwitness Respond license, endpoint server service running in the background, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Risk Score Threshold|Specify risk threshold for the file. If the file exceeds the threshold, the related entity will be marked as suspicious. If nothing is specified, action won’t check the risk score.|False|String|50|



##### JSON Results
```json
[{"Entity": "34261adf58ac3c8e38724d5fbfba21037d868a2c0b6291e2a61e5a023b55c3f9", "EntityResult": {"firstFileName": "AM_Delta_Patch_1.321.1947.0.exe", "reputationStatus": "KnownGood", "globalRiskScore": 0, "firstSeenTime": "2020-08-23T00:46:25.288Z", "machineOsType": "windows", "signature": {"timeStamp": "2020-08-22T21:01:55.552Z", "thumbprint": "c6573d9ba5efc55b1ad1c59b9cafc33d232b13cc", "context": ["microsoft", "signed", "valid"], "signer": "MicrosoftCorporation"}, "size": 441280, "checksumMd5": "40d93a5ed9d2d55e35857c1f1de162db", "checksumSha1": "3096e9e4ac4cc46dcfa11a053583c2d3e14b14b8", "checksumSha256": "34261adf58ac3c8e38724d5fbfba21037d868a2c0b6291e2a61e5a023b55c3f9", "pe": {"timeStamp": "2020-08-22T20:57:28.000Z", "imageSize": 454656, "numberOfExportedFunctions": 0, "numberOfNamesExported": 0, "numberOfExecuteWriteSections": 0, "context": ["file.exe", "file.arch64", "file.versionInfoPresent", "file.resourceDirectoryPresent", "file.relocationDirectoryPresent", "file.debugDirectoryPresent", "file.tlsDirectoryPresent", "file.richSignaturePresent", "file.companyNameContainsText", "file.descriptionContainsText", "file.versionContainsText", "file.internalNameContainsText", "file.legalCopyrightContainsText", "file.originalFilenameContainsText", "file.productNameContainsText", "file.productVersionContainsText", "file.standardVersionMetaPresent"], "resources": {"originalFileName": "AM_Delta_Patch_1.321.1947.0.exe", "company": "MicrosoftCorporation", "description": "MicrosoftAntimalwareWUStub", "version": null}, "sectionNames": [".text", ".rdata", ".data", ".pdata", ".rsrc", ".reloc"], "importedLibraries": ["ADVAPI32.dll", "KERNEL32.dll", "RPCRT4.dll", "ntdll.dll"]}, "elf": null, "macho": null, "entropy": 7.378079119412321, "format": "pe", "fileStatus": "Neutral", "remediationAction": "Unblock"}}, {"Entity": "AM_Delta_Patch_1.321.1947.0.exe", "EntityResult": {"firstFileName": "AM_Delta_Patch_1.321.1947.0.exe", "reputationStatus": "KnownGood", "globalRiskScore": 0, "firstSeenTime": "2020-08-23T00:46:25.288Z", "machineOsType": "windows", "signature": {"timeStamp": "2020-08-22T21:01:55.552Z", "thumbprint": "c6573d9ba5efc55b1ad1c59b9cafc33d232b13cc", "context": ["microsoft", "signed", "valid"], "signer": "MicrosoftCorporation"}, "size": 441280, "checksumMd5": "40d93a5ed9d2d55e35857c1f1de162db", "checksumSha1": "3096e9e4ac4cc46dcfa11a053583c2d3e14b14b8", "checksumSha256": "34261adf58ac3c8e38724d5fbfba21037d868a2c0b6291e2a61e5a023b55c3f9", "pe": {"timeStamp": "2020-08-22T20:57:28.000Z", "imageSize": 454656, "numberOfExportedFunctions": 0, "numberOfNamesExported": 0, "numberOfExecuteWriteSections": 0, "context": ["file.exe", "file.arch64", "file.versionInfoPresent", "file.resourceDirectoryPresent", "file.relocationDirectoryPresent", "file.debugDirectoryPresent", "file.tlsDirectoryPresent", "file.richSignaturePresent", "file.companyNameContainsText", "file.descriptionContainsText", "file.versionContainsText", "file.internalNameContainsText", "file.legalCopyrightContainsText", "file.originalFilenameContainsText", "file.productNameContainsText", "file.productVersionContainsText", "file.standardVersionMetaPresent"], "resources": {"originalFileName": "AM_Delta_Patch_1.321.1947.0.exe", "company": "MicrosoftCorporation", "description": "MicrosoftAntimalwareWUStub", "version": null}, "sectionNames": [".text", ".rdata", ".data", ".pdata", ".rsrc", ".reloc"], "importedLibraries": ["ADVAPI32.dll", "KERNEL32.dll", "RPCRT4.dll", "ntdll.dll"]}, "elf": null, "macho": null, "entropy": 7.378079119412321, "format": "pe", "fileStatus": "Neutral", "remediationAction": "Unblock"}}]
```



#### Isolate Endpoint
Request endpoint isolation in RSA Netwitness. Requires RSA Netwitness Respond license, endpoint server service running in the background, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|Add comment, which describes the reason behind the isolation request.|True|String||



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Unisolate Endpoint
Request endpoint unisolation in RSA Netwitness. Requires RSA Netwitness Respond license, endpoint server service running in the background, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|Add comment, which describes the reason behind the unisolation request.|True|String||



#### Update Incident
Update Incident in RSA Netwitness. Requires RSA Netwitness Respond license, configured Web Username and Web Password in the integration configuration.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify ID of the incident that needs to be updated.|True|String||
|Status|Specify new status for the incident.|False|List||
|Assignee|Specify new assignee for the incident.|False|String||



##### JSON Results
```json
{"id": "INC-000", "title": "High Risk Alerts: NetWitness Endpoint for RSA-HOST-1", "summary": "", "priority": "Critical", "riskScore": 90, "status": "Assigned", "alertCount": 16, "averageAlertRiskScore": 90, "sealed": true, "totalRemediationTaskCount": 0, "openRemediationTaskCount": 0, "created": "2020-09-04T08:22:51.456Z", "lastUpdated": "2020-09-17T08:31:13.074Z", "lastUpdatedBy": null, "assignee": "admin", "sources": ["ECAT"], "ruleId": "5ef1b33614c0552a2884cxxx", "firstAlertTime": "2020-08-31T16:09:50.071Z", "categories": [], "journalEntries": null, "createdBy": "High Risk Alerts: NetWitness Endpoint", "deletedAlertCount": 0, "eventCount": 16, "alertMeta": {"SourceIp": [""], "DestinationIp": [""]}}
```



#### Query NetWitness For Events Around IP
Run a query on RSA NetWitness to retreive all events for a specific query (conditions) for a given IP address in the alert
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Hours Backwards|Specify how many hours backwards to fetch events. Default is 1 hour.|False|String|1|
|Max Events To Return|Specify how many events to return. If nothing is specified, action will return 50 events.|False|String|50|



##### JSON Results
```json
[{"EntityResult": [{"payload.req": "110", "ubc.req": "44", "netname": "private dst", "lifetime": "0", "rid": "792830", "payload": "110", "size": "242", "service": "0", "mcb.req": "48", "eth.src": "11:6C:AC:61:11:11", "tcp.flags": "24", "tcp.dstport": "39497", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "792831", "eth.type": "2048", "ip.src": "1.1.1.1", "mcbc.req": "9", "eth.dst": "00:50:56:A5:45:70", "did": "nwappliance5805", "tcp.srcport": "389", "packets": "2", "streams": "1", "time": 1547467411, "entropy.req": "5075", "ip.proto": "6"}, {"payload.req": "110", "ubc.req": "44", "netname": "private dst", "lifetime": "0", "rid": "792830", "payload": "110", "size": "242", "service": "0", "mcb.req": "48", "eth.src": "11:6C:AC:61:11:11", "tcp.flags": "24", "tcp.dstport": "39497", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "2968695", "eth.type": "2048", "ip.src": "1.1.1.1", "mcbc.req": "9", "eth.dst": "00:50:56:A5:45:70", "did": "nwappliance5805", "tcp.srcport": "389", "packets": "2", "streams": "1", "time": 1547467411, "entropy.req": "5075"}], "Entity": "1.1.1.1"}]
```



#### Query NetWitness For Events Around User
Run a query on RSA NetWitness to retreive all events for a specific query (conditions) for a given username in the alert
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Hours Backwards|Specify how many hours backwards to fetch events. Default is 1 hour.|False|String|1|
|Max Events To Return|Specify how many events to return. If nothing is specified, action will return 50 events.|False|String|50|



##### JSON Results
```json
[{"EntityResult": [{"payload.req": "110", "ubc.req": "44", "netname": "private dst", "lifetime": "0", "rid": "792830", "payload": "110", "size": "242", "service": "0", "mcb.req": "48", "mcbc.req": "9", "tcp.dstport": "39497", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "792831", "eth.type": "2048", "ip.src": "1.1.1.1", "tcp.flags": "24", "tcp.srcport": "389", "packets": "2", "user.src": "user", "streams": "1", "time": 1547467411, "entropy.req": "5075", "ip.proto": "6"}, {"payload.req": "111", "ubc.req": "55", "netname": "private dst", "lifetime": "0", "rid": "123", "payload": "123", "size": "242", "service": "0", "mcb.req": "11", "mcbc.req": "9", "tcp.dstport": "39497", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "792831", "eth.type": "2048", "ip.src": "1.1.1.1", "tcp.flags": "24", "tcp.srcport": "389", "packets": "2", "user.src": "user", "streams": "1", "time": 1547467411, "entropy.req": "5075", "ip.proto": "6"}], "Entity": "user"}]
```



#### Run General Query
Run free query and receive event and a PCAP file.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Custom query string.|True|String|None|
|Max Hours Backwards|Specify how many hours backwards to fetch events. Default is 1 hour.|False|String|1|
|Max Events To Return|Specify how many events to return. If nothing is specified, action will return 50 events.|False|String|50|



##### JSON Results
```json
[{"payload.req": "66", "ubc.req": "18", "netname": "multicast dst", "lifetime": "0", "rid": "48908", "payload": "66", "size": "150", "service": "0", "mcb.req": "0", "eth.src": "00:50:56:B5:76:2B", "udp.srcport": "60807", "udp.dstport": "5355", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "48908", "eth.type": "2048", "ip.src": "1.1.1.1", "mcbc.req": "24", "eth.dst": "11:11:5E:11:11:FC", "did": "nwappliance5805", "packets": "2", "streams": "1", "time": 1547047123, "entropy.req": "3498", "ip.proto": "17"}, {"payload.req": "66", "ubc.req": "18", "netname": "multicast dst", "lifetime": "0", "rid": "48908", "payload": "66", "size": "150", "service": "0", "mcb.req": "0", "eth.src": "22:22:22:B2:22:2B", "udp.srcport": "60807", "udp.dstport": "5355", "direction": "lateral", "medium": "1", "ip.dst": "1.1.1.1", "alert": "test App rule", "sessionid": "48908", "eth.type": "2048", "ip.src": "1.1.1.1", "mcbc.req": "24", "eth.dst": "33:44:5E:44:44:FC", "did": "nwappliance5805", "packets": "2", "streams": "1", "time": 1547047331, "entropy.req": "3498", "ip.proto": "17"}]
```



#### Query NetWitness For Events Around Host
Retrieve the latest events related to the hostnames in RSA Netwitness. Requires configuration of Broker API or Concentrator API
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Hours Backwards|Specify how many hours backwards to fetch events. Default is 1 hour.|False|String|1|
|Max Events To Return|Specify how many events to return. If nothing is specified, action will return 50 events.|False|String|50|



##### JSON Results
```json
[{"EntityResult": [{"payload.req": "0", "org.src": "Blue", "domain.src": "test.com", "netname": "other src", "lifetime": "0", "rid": "29", "payload": "0", "size": "66", "country.src": "France", "service": "0", "longdec.src": "-2.2595", "eth.src": "11:1C:1C:11:22:87", "tcp.dstport": "40906", "direction": "inbound", "medium": "1", "ip.dst": "1.1.1.1", "latdec.src": "48.3175", "city.src": "Tr\\u00e9meur", "alert": "test App rule", "sessionid": "29", "eth.type": "2048", "ip.src": "1.1.1.1", "tcp.flags": "20", "eth.dst": "11:11:11:B1:1B:11", "did": "nwappliance5805", "tcp.srcport": "80", "packets": "1", "streams": "1", "time": 1547013286, "ip.proto": "6"}, {"payload.req": "0", "org.src": "Blue", "domain.src": "test.com", "netname": "private dst", "lifetime": "0", "rid": "4401", "payload": "0", "size": "66", "country.src": "France", "service": "0", "longdec.src": "-2.2595", "eth.src": "11:1C:AC:11:11:11", "tcp.dstport": "41156", "direction": "inbound", "medium": "1", "ip.dst": "1.1.1.1", "latdec.src": "48.3175", "city.src": "Tr\\u00e9meur", "alert": "test App rule", "sessionid": "4401", "eth.type": "2048", "ip.src": "1.1.1.1", "tcp.flags": "20", "eth.dst": "00:50:56:B5:1B:43", "did": "nwappliance5805", "tcp.srcport": "80", "packets": "1", "streams": "1", "time": 1547016274}], "Entity": "test.com"}]
```









## Connectors
#### RSA Netwitness Platform - Incidents Connector
Pull incidents from RSA Netwitness Platform.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|true|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|event_type|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Web API Root|Web API Root of the RSA Netwitness Platform instance.|True|String|https://{ip}/rest/api|
|Web Username|Username of the RSA Netwitness Platform account.|True|String||
|Web Password|Password of the RSA Netwitness Platform account.|True|Password|*****|
|Broker API Root|API Root of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. Example: https://{ip}:50103. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|String||
|Broker API Username|API Username of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|String||
|Broker API Password|API Password of the RSA Netwitness broker. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|Password|*****|
|Concentrator API Root|API Root of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. Example: https://{ip}:50105. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|String||
|Concentrator API Username|API Username of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|String||
|Concentrator API Password|API Password of the RSA Netwitness concentrator. Note: broker configuration takes priority over concentrator. If this parameter is provided, the connector will try to fetch more context related to the incident.|False|Password|*****|
|Credential JSON Object|This parameter is needed for storing the data source credentials. This parameter has priority over "Broker API Root", "Broker API Username", "Broker API Password", "Concentrator API Root", "Concentrator API Username", "Concentrator API Password". Please refer to the documentation portal for more details.|False|Password|*****|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Note: connector will wait for the provided time for the updates to incidents.|False|Integer|1|
|Lowest Risk Score To Fetch|Lowest risk score of the incidents to fetch. By default, the connector will ingest all of the incidents. Maximum is 100.|False|Integer||
|Severity Fallback|Specify what should be the fallback severity for the Siemplify Alert, when risk score is not available. Possible values: Informational, Low, Medium, High, Critical.|True|String|Informational|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 100.|False|Integer|10|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the RSA Netwitness Plaform server is valid.|False|Boolean|false|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




