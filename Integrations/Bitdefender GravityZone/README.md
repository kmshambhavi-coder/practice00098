
# Bitdefender GravityZone

Bitdefender Control Center API's allow developers and SOC's to automate business workflows. Docs: https://github.com/snags141/SiemplifyIntegration_BitdefenderGravityZone

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|API Key generated under "My Account"|True|Password|*****|
|Access URL|Access URL for Control Center API|True|String|https://cloud.gravityzone.bitdefender.com/api|
|Verify SSL|Verify SSL when making requests|False|Boolean|false|


#### Dependencies
| |
|-|
|requests-2.32.4-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|


## Actions
#### Blocklist - Add Hashes
Use this method to add one or more file hashes to the Blocklist. Hashes supported: SHA256, MD5.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hash List|A comma-separated list of SHA256 or MD5 hashes.|True|String|hash1,hash2|
|Source Info|A description for the hashes.|True|String|Determined to be malicious.|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Blocklist - List Items
This method lists all the hashes that are present in the blocklist.
Timeout - 600 Seconds



##### JSON Results
```json
{"items": [{"companyId": "5b680f6fb1a43d860a7b23c8", "hash": "098f6bcd4621d373cade4e832627b4f6", "hashType": 2, "id": "5b7ac19bb1a43dfb107b23c6", "source": 3, "sourceInfo": "Added from public API"}, {"filename": "file.txt", "hash": "f696282aa4cd4f614aa995190cf442fe", "hashType": 2, "id": "5b7ac19bb1a43dfb107b23c7", "source": 1, "sourceInfo": "Added from incident 1"}]}
```



#### Blocklist - Remove Item
This method removes an item from the Blocklist, identified by its ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hash ID|The ID of the item in the Blocklist to be deleted|True|String|Eg: 0df7568c-59c1-48e0-a31b-18d83e6d9810|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Create Scan Task
This method creates a task to isolate the specified endpoint.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Target IDs|A list with the IDs of the targets to scan. The target ID can designate an endpoint or a container.|True|String|targetId1,targetId2|
|Scan Type|The type of scan. Available options are: 1 - quick scan; 2 - full scan; 3 - memory scan; 4 - custom scan|True|List|Quick|
|Task Name|The name of the task. If the parameter is not passed, the name will be automatically generated.|False|String|None|
|Custom Scan - Depth|The scan profile. Available options: 1 - aggressive; 2 - normal; 3 - permissive. This parameter is only used when scan type is Custom|False|List|Normal|
|Custom Scan - Paths|Comma-separated list of target paths to be scanned. This parameter is only used when scan type is Custom|False|String|LocalDrives|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Create Scan Task by MAC Address
Use this method to generate a scan task for managed endpoints identified by their MAC address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|MAC Addresses|The list of mac addresses of the endpoints to be scanned. You can specify at most 100 MAC addresses at once|True|String|macaddr1,macaddr2|
|Scan Type|The type of scan. Available options are: 1 - quick scan; 2 - full scan; 3 - memory scan; 4 - custom scan|True|List|Quick|
|Task Name|The name of the task. If the parameter is not passed, the name will be automatically generated.|False|String|None|
|Custom Scan - Depth|The scan profile. Available options: 1 - aggressive; 2 - normal; 3 - permissive. This parameter is only used when scan type is Custom|False|List|Normal|
|Custom Scan - Paths|Comma-separated list of target paths to be scanned. This parameter is only used when scan type is Custom|False|String|LocalDrives|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Get Custom Groups List
This method retrieves the list of groups under a specified group.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Parent ID|Parent group ID for which the child groups will be listed. 'Computers and Groups' and 'Deleted' groups are returned if the passed parameter is null.|False|String||



##### JSON Results
```json
{"items": [{"id": "5582c385b1a43deb7f7b23c6", "name": "myGroup1"}, {"id": "5582d3b3b1a43d897f7b23c8", "name": "myGroup2"}]}
```



#### Get Endpoints List
Get list of endpoints
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter - SSID|The SSID (Active Directory SID of the endpoint) used to filter the endpoints regardless of their protection status.|False|String|None|
|Filter - Depth - All Items Recursively|Boolean to filter all endpoints recursively within the Network Inventory of a company.|False|Boolean|false|
|Filter - Security Servers|Boolean to filter all Security Servers|False|Boolean|false|
|Filter - Managed Relays|Boolean to filter all endpoints with Relay role. |False|Boolean|false|
|Filter - Managed Exchange Servers|Boolean to filter all protected Exchange servers.|False|Boolean|false|
|Parent ID|The ID of the target company or group. If not specified or set with a company ID, the method returns only the endpoints under Computers and Groups.|False|String|None|
|Endpoints|Select whether to return only managed endpoints, unmanaged endpoints, or all endpoints.|True|List|All|
|Filter - Managed with BEST|Boolean to filter all endpoints with the security agent installed on them.|False|Boolean|false|
|Filter - Name|A string for filtering the items by name. Minimum required string length is three characters.|False|String|None|
|Filter - MAC Addresses|Comma-separated list of MAC addresses used to filter the endpoints regardless of their protection status.|False|String|None|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237335"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Get Hourly Usage for EC2 Instances
This method exposes the hourly usage for each Amazon instance category (micro, medium etc.).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Target Month|The month for which the usage is returned. The month will be provided in the following format: mm/yyyy. The default value is the current month.|True|String|01/2020|



##### JSON Results
```json
{"result": {"micro": 11, "medium": 157}}
```



#### Get Managed Endpoint Details
This method returns detailed information, such as: details to identify the endpoint and the security agent, the status of installed protection modules.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Endpoint ID|The ID of the endpoint for which the details will be returned|True|String|oBFA8Ie3Oh4iXCtyr5Z9iw|



##### JSON Results
```json
{"result": {"id": "54a28b41b1a43d89367b23fd", "name": "WIN-TGQDU499RS4", "companyId": "5575a235d2172c65038b454e", "operatingSystem": "Windows Server 2008 R2 Datacenter", "state": 1, "ip": "1.1.1.1", "lastSeen": "2015-06-22T13:46:59", "machineType": 1, "agent": {"engineVersion": "7.61184", "primaryEngine": 1, "fallbackEngine": 2, "lastUpdate": "2015-06-22T13:40:06", "licensed": 1, "productOutdated": false, "productUpdateDisabled": false, "productVersion": "1.1.1.1", "signatureOutdated": false, "signatureUpdateDisabled": false, "type": 3}, "group": {"id": "5575a235d2172c65038b456d", "name": "Custom Groups"}, "malwareStatus": {"detection": false, "infected": false}, "modules": {"advancedThreatControl": false, "antimalware": false, "contentControl": false, "deviceControl": false, "firewall": false, "powerUser": false, "networkAttackDefense": false}, "policy": {"id": "5121da426803fa2d0e000017", "applied": true, "name": "Default policy"}, "label": "endpoint label", "moveState": 1, "riskScore": {"value": "81%", "impact": "High", "misconfigurations": "70%", "appVulnerabilities": "11%", "humanRisks": "19%"}}}
```



#### Get Network Inventory Items
This method returns network inventory items. Note - Some filters require a specific license to be active, otherwise they are ignored, resulting in an inaccurate API response. The field name works with partial matching.
The filter returns the items whose names are exact match or start with the specified value. To use the specified value as a suffix, use the asterisk symbol (*).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter - Name|A string for filtering the items by name. Minimum required string length is three characters.|False|String|None|
|Filter - MAC Addresses|Comma-separated list of MAC addresses used to filter the endpoints regardless of their protection status.|False|String|None|
|Filter - SSID|The SSID (Active Directory SID of the endpoint) used to filter the endpoints regardless of their protection status.|False|String|None|
|Filter - Depth - All Items Recursively|Boolean to filter all endpoints recursively within the Network Inventory of a company.|False|Boolean|false|
|Filter - Security Servers|Boolean to filter all Security Servers|False|Boolean|false|
|Filter - Managed Relays|Boolean to filter all endpoints with Relay role. |False|Boolean|false|
|Filter - Managed Exchange Servers|Boolean to filter all protected Exchange servers.|False|Boolean|false|
|Filter - Managed with BEST|Boolean to filter all endpoints with the security agent installed on them.|False|Boolean|false|
|Filter - Virtual Machines|Boolean to filter all virtual machines.|False|Boolean|false|
|Filter - Computers|Boolean to filter all computers.|False|Boolean|false|
|Filter - EC2 Instances|Boolean to filter all Amazon EC2 Instances.|False|Boolean|false|
|Filter - Groups|Boolean to filter all custom groups of endpoints.|False|Boolean|false|
|Parent ID|The ID of the container for which the network items will be returned.|False|String|None|



##### JSON Results
```json
{"result": {"id": "21a295eeb1a43d8b497b24b7", "name": "Computer", "type": 5, "parentId": "21a295eeb1a43d8b497b24b7", "companyId": "21a295eeb1a43d8b497b24b7", "details": {"label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 2, "operatingSystemVersion": "Windows Server", "ip": "1.1.1.1", "macs": ["324935237346"], "ssid": ""}}}
```



#### Get Scan Tasks List
This method returns the list of scan tasks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task Status|The status of the task.|True|List|All|
|Task Name|Use an asterisk in front to search its appearance anywhere in the name. If omitted, only returns results where the name starts with the keyword|False|String|None|



##### JSON Results
```json
{"result": [{"id": "21a295eeb1a43d8b497b23b7", "name": "task 1", "status": 1, "startDate": "2015-08-21T23:48:16"}, {"id": "21a295eeb1a43d8b497b23b8", "name": "task 2", "status": 1, "startDate": "2015-08-21T10:21:15"}]}
```



#### Isolate Endpoint
This method creates a task to isolate the specified endpoint.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Endpoint ID|The ID of the endpoint for which the details will be returned|True|String|oBFA8Ie3Oh4iXCtyr5Z9iw|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Policies - List All
This method retrieves the list of available policies.
Timeout - 600 Seconds



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Policy 1", "companyId": "55896b87b7894d0f367b23c6", "companyName": "Company Test"}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Policy 2", "companyId": "55896b87b7894d0f367b23c6", "companyName": "Company Test"}]}
```



#### Quarantine - Add File
This method creates a new task to add a file to quarantine.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|The absolute file path on disk. This can be at most 4096 characters in length and should have the format suitable to the target's operating system.|True|String|C:\Users\Public\malicious.exe|
|Endpoint IDs|A list with the IDs of the target endpoints. Max 100 targets at once. Only endpoints having the EDR Sensor module active are considered valid targets.|True|String|targetId1,targetId2|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Quarantine - Get Items List
This method retrieves the list of quarantined items available for a company. An item can be a file or an Microsoft Exchange object.
The filter fields Threat Name, File Path, and IP Address work with partial matching.
The filter returns the items which are exact match or start with the specified value.
To use the specified value as a suffix, use the asterisk symbol (*). For example:
If filePath is C:\temp, the API returns all items originating from this folder, including sub-folders.
If filePath is *myfile.exe, then the API returns a list of all myfile.exe files from anywhere on the system.
The Exchange filters require a valid license key for Security for Exchange.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service|Allowed services are: computers, for "Computers and Virtual Machines" or exchange, for "Security for Exchange"|True|List|Computers|
|Filter - Threat Name|Filters the quarantined items by threat name.This filter is available for computers and exchange services.|False|String|None|
|Filter - Start Date|Filters the items that quarantined after the specified date. Format for startDate is in ISO 8601.The filter is available for computers and exchange.|False|String|None|
|Filter - End Date|Filters the items quarantined before the specified date.Format for startDate is in ISO 8601.The filter is available for computers and exchange.|False|String|None|
|Filter - File Path|Filters the quarantined items by file path. This filter is available for computers service.|False|String|None|
|Filter - IP Address|Filters the quarantine items by IP address. This filter is available for computers service.|False|String|None|
|Filter - Action Status|Filters the quarantine items by action status. "Pending Save" Is only available to the Exchange Service.|False|List|None|
|Endpoint ID|ID of the computer for which you want to retrieve the quarantined items. If not passed, he method returns the items quarantined in the entire network.|False|String|None|



##### JSON Results
```json
{"items": [{"id": "5d3968e0f23f730ecb0f68c2", "quarantinedOn": "2019-07-28T11:31:28", "actionStatus": 1, "companyId": "55896b87b7894d0f367b23c6", "endpointId": "5d36c255f23f730fa91944e2", "endpointName": "Computer 1", "endpointIP": "1.1.1.1", "canBeRestored": false, "canBeRemoved": false, "threatName": "Virus 0", "details": {"filePath": "c:\\Virus0\\virus0.exe"}}]}
```



#### Quarantine - Remove Items
This method creates a new task to remove items from quarantine.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service|Allowed services are: computers, for "Computers and Virtual Machines" or exchange, for "Security for Exchange"|True|List|Computers|
|Quarantine Item IDs|Comma-separated list of quarantine items IDs. The maximum number of items that can be removed once is 100.|True|String|itemId1,itemId2|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Quarantine - Restore Exchange Items
This method creates a new task to restore items from the quarantine for Exchange Servers.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|EWS URL|The Exchange Web Services URL .The EWS URL is necessary when the Exchange Autodiscovery does not work.|False|String|None|
|Email|The email address of the Exchange user. This parameter is necessary when the email address is different from the username.|False|String|None|
|Password|The password of an Exchange user|True|Password|*****|
|Username|The username of an Microsoft Exchange user. The username must include the domain name.|True|String|username|
|Quarantine Item IDs|Comma-separated list of quarantine items IDs. The maximum number of items that can be removed once is 100.|True|String|itemId1,itemId2|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Quarantine - Restore Items
This method creates a new task to restore items from the quarantine.

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Location to Restore|The absolute path to the folder where the items will be restored. If the parameter is not set, the original location will be used.|False|String|None|
|Quarantine Item IDs|Comma-separated list of quarantine items IDs. The maximum number of items that can be removed once is 100.|True|String|itemId1,itemId2|
|Service|Allowed services are: computers, for "Computers and Virtual Machines" or exchange, for "Security for Exchange"|True|List|Computers|
|Add Exclusion in Policy|Exclude the files to be restored from future scans. Exclusions do not apply to items with the Default Policy assigned.|False|Boolean|false|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Reports - Get Download Links
This method returns an Object with information regarding the report availability for download and the corresponding download links.
The instant report is created one time only and available for download for less than 24 hours.
Scheduled reports are generated periodically and all report instances are saved in the GravityZone database.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report ID|The report ID to fetch|True|String|reportId|



##### JSON Results
```json
{"result": {"readyForDownload": true, "allInstancesUrl": "https://gravityzone.bitdefender.com/api/v1.0/http/downloadReportZip?reportId=5645cba6f12a9a8c5e8b4748&allInstances=1&serviceType=1", "lastInstanceUrl": "https://gravityzone.bitdefender.com/api/v1.0/http/downloadReportZip?reportId=5645cba6f12a9a8c5e8b4748&allInstances=0&serviceType=1"}}
```



#### Reports - List All
This method returns the list of scheduled reports, according to the parameters received.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Name|The name of the report.|False|String|None|
|Report Type|The report type.|False|List||



##### JSON Results
```json
{"items": [{"id": "5638cdceb1a43d46137b23c6", "name": "My report 1", "occurrence": 2, "type": 2}, {"id": "5638d7f8b1a43d49137b23c9", "name": "My report 2", "occurrence": 4, "type": 2}, {"id": "563b271bb1a43d21077b23c8", "name": "My report 3", "occurrence": 4, "type": 2}, {"id": "563a289eb1a43d2f617b23c6", "name": "My report 4", "occurrence": 2, "type": 2}]}
```



#### Restore Isolated Endpoint
This method creates a task to restore the specified endpoint from isolation.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Endpoint ID|The ID of the endpoint for which the details will be returned|True|String|oBFA8Ie3Oh4iXCtyr5Z9iw|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Set Endpoint Label
This method sets a new label to an endpoint.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Label|A string representing the label. The maximum allowed length is 64 characters. Enter an empty string to reset a previously set label.|True|String|Some label|
|Endpoint ID|The ID of the endpoint for which the details will be returned|True|String|oBFA8Ie3Oh4iXCtyr5Z9iw|



##### JSON Results
```json
{"items": [{"id": "21a295eeb1a43d8b497b23b7", "name": "Endpoint 1", "label": "endpoint 1", "fqdn": "endpoint1.local", "groupId": "5a5f4d36b1a43d5f097b23bb", "isManaged": true, "machineType": 1, "operatingSystemVersion": "Windows Server 2016", "ip": "1.1.1.1", "macs": ["324935237225"], "ssid": ""}, {"id": "23a295d8b1a43d7c4a7b23c9", "name": "Endpoint 2", "machineType": 1, "label": "endpoint 2", "fqdn": "endpoint2.local", "groupId": "5a4f4d46b1a53d5f197b23aa", "isManaged": true, "operatingSystemVersion": "Windows 7", "ip": "1.1.1.1", "macs": ["325935237445"], "ssid": ""}]}
```



#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Policies - Get Details
This method retrieves all information related to a security policy.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy ID|The ID of the policy to be queried.|True|String|5e1023820d21ea80605bf919|



##### JSON Results
```json
{"result": {"id": "5121da426803fa2d0e000017", "name": "Default policy", "createdBy": "root+us@bitdefender.com", "createDate": "None", "lastModifyDate": "2015-10-29T12:27:57", "settings": {"antimalware": {"onAccess": {"onAccessScanning": {"enable": true, "profile": 2, "settings": {"general": {"fileTypes": {"scanLocalFile": {"enable": true, "settings": {"fileType": 1, "extensions": ""}}, "scanNetworkFile": {"enable": true, "settings": {"fileType": 1, "extensions": ""}}, "limitFile": {"enable": false, "size": 20}}, "archives": {"enable": false, "limitArchiveSize": 10, "maximumArchiveDepth": 2}, "miscellaneous": {"scanBootSectors": true, "scanOnlyNewChangeFiles": true, "scanForKeyloggers": true, "scanPUA": true, "deferredScanning": true}, "scanAction": {"infectedFiles": {"action": 1, "then": 4}, "suspectFiles": {"action": 0, "then": 0}}}, "advanced": {"onAccessUnix": true, "onAccessUnixPaths": ["/home", "/bin", "/sbin", "/usr", "/etc"]}}}, "ransomwareProtection": {"enable": false}, "virusControl": {"enable": true, "profile": 2, "defaultAction": 3}}, "onDemand": {"scanTask": [], "deviceScanning": {"enable": true, "settings": {"automaticallyScanCdDvd": true, "automaticallyScanUsb": true, "scanDevices": {"enable": false, "maxim": 0}}, "scanProfile": 2, "scanSettings": {"fileTypes": 1, "extensions": [], "archives": {"enable": true, "settings": {"limitArchiveSize": 10, "maximumArchiveDepth": 16}, "scanEmail": true}, "miscellaneous": {"scanBoot": false, "scanRegistry": false, "scanRootkits": true, "ignoreKeyloggers": true, "scanMemory": false, "scanCookie": false, "scanNewChanged": true, "scanPUA": true, "scanNetworkFiles": true}, "action": {"whenInfected": {"action": 2, "then": 4}, "whenSuspect": {"action": 1, "then": 1}, "whenRootKitAction": 2}}}, "contextualScan": {"scanProfile": 4, "scanSettings": {"archives": {"enable": true, "settings": {"limitArchiveSize": 10, "maximumArchiveDepth": 16}, "scanEmail": true}, "miscellaneous": {"scanBoot": false, "scanRegistry": false, "scanRootkits": false, "ignoreKeyloggers": false, "scanMemory": false, "scanCookie": false, "scanNewChanged": true, "scanPUA": true, "scanNetworkFiles": true}, "action": {"whenInfected": {"action": 2, "then": 4}, "whenSuspect": {"action": 4, "then": 1}, "whenRootKitAction": 2}}}}, "settings": {"activateExclusions": {"enable": false, "exclusionsItems": []}, "useBuiltInExclusions": true, "deleteFilesOlderThan": 30, "submitQuarantined": {"enable": true, "hours": 1}, "rescanQuarantine": true, "copyFilesToQuarantineBeforeDisinfect": true, "allowUserQuarantineActions": true}, "securityServers": {"affinityRule": false, "svaIps": [], "useSSL": false, "enableOnDemandSlots": false, "svaProxy": {"profile": 1}, "serverOrder": "priority"}, "dynamicThreatDefense": {"enable": true, "actionforLocal": 5, "actionforNetwork": 2, "targetedAttack": {"enable": true, "detectionLevel": 2}, "suspiciousFilesAndNetworkTraffic": {"enable": true, "detectionLevel": 2}, "exploits": {"enable": true, "detectionLevel": 2}, "ransomware": {"enable": true, "detectionLevel": 2}, "grayware": {"enable": true, "detectionLevel": 2}, "enableGlobalReportingForFiles": false, "enableGlobalReportingForNetwork": false}, "antiExploit": {"enable": true, "predefinedApplications": [{"details": {"applicationName": "7-Zip Archiver Console", "status": 1, "processName": ["7z.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "7-Zip Archiver GUI", "status": 1, "processName": ["7zG.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Acrobat Reader", "status": 1, "processName": ["Acrobat.exe", "Acrord32.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Foxit Reader", "status": 1, "processName": ["FoxitReader.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Libre Office, Open Office", "status": 1, "processName": ["Soffice.bin"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Microsoft Word", "status": 1, "processName": ["Winword.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Microsoft Excel", "status": 1, "processName": ["Excel.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Microsoft PowerPoint", "status": 1, "processName": ["Powerpnt.exe", "Pptview.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Microsoft Outlook", "status": 1, "processName": ["Outlook.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Microsoft Equation Editor", "status": 1, "processName": ["Eqnedt32.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": true, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Conflict Resolution for Access", "status": 1, "processName": ["Acecnflt.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Office, Filter Loader", "status": 1, "processName": ["Fltldr.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Microsoft Internet Explorer", "status": 1, "processName": ["Iexplore.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Mozilla Firefox", "status": 1, "processName": ["Firefox.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Mozilla Thunderbird", "status": 1, "processName": ["Thunderbird.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Opera Browser", "status": 1, "processName": ["Opera*.exe", "Launcher*.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Apple Safari", "status": 1, "processName": ["Safari.exe", "WebKit2WebProcess.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "Flash Player Container", "status": 1, "processName": ["FlashPlayerPlugin*.exe", "Plugin-container.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}, {"details": {"applicationName": "WinRAR Archiver GUI", "status": 1, "processName": ["WinRAR.exe"]}, "exploitDetectionTechniques": [{"enable": true, "name": 1, "action": 1}, {"enable": true, "name": 2, "action": 1}, {"enable": true, "name": 3, "action": 1}, {"enable": true, "name": 4, "action": 1}, {"enable": true, "name": 5, "action": 1}, {"enable": true, "name": 6, "action": 1}, {"enable": true, "name": 7, "action": 1}, {"enable": true, "name": 8, "action": 1}, {"enable": true, "name": 9, "action": 1}, {"enable": true, "name": 10, "action": 1}, {"enable": true, "name": 11, "action": 1}, {"enable": true, "name": 12, "action": 1}, {"enable": true, "name": 13, "action": 1}, {"enable": true, "name": 14, "action": 1}, {"enable": true, "name": 15, "action": 1}, {"enable": true, "name": 18, "action": 1}, {"enable": true, "name": 19, "action": 1}, {"enable": true, "name": 20, "action": 1}, {"enable": false, "name": 16, "action": 1}, {"enable": true, "name": 17, "action": 1}]}], "customApplications": [], "systemWideDetections": {"privilegeEscalationStatus": true, "privilegeEscalation": 1, "lsassMemoryAccessFromUnknownProcess": 3, "lsassMemoryAccessFromUnknownProcessStatus": true}}, "onExecute": {"commandLineScanning": {"enable": true}, "ransomwareRemediation": {"enable": false, "localAttack": {"enable": true}, "remoteAttack": {"enable": false}, "restore": {"mode": 2}}, "theta": {"enabled": true}}}, "contentControl": {"webAccess": {"enable": false, "profileType": 3, "useExceptions": true, "webRules": [], "scheduler": []}, "webCategoriesFilter": {"enable": false, "profileType": 3, "treatAsExceptions": false, "enableDetailedAlerts": true}, "antiphishing": {"enable": true, "settings": {"protectionAgainstFraud": true, "protectionAgainstPhishing": true}, "defaultAction": 1}, "application": {"enable": false, "rules": []}, "dataProtection": {"enable": false, "rules": [], "exclusions": []}, "traffic": {"enable": true, "enableExclusions": false, "trafficScan": {"incomingEmails": false, "outgoingEmails": false, "webTraffic": true, "enable": true}, "exclusions": []}, "networkMonitor": {"enable": true, "attackTechniques": [{"enable": true, "name": 1, "action": 3}, {"enable": true, "name": 2, "action": 3}, {"enable": true, "name": 5, "action": 3}, {"enable": true, "name": 3, "action": 3}, {"enable": true, "name": 4, "action": 3}], "attackTechniquesReportOnly": [{"enable": true, "name": 1, "action": 0}, {"enable": true, "name": 2, "action": 0}, {"enable": true, "name": 5, "action": 0}, {"enable": true, "name": 3, "action": 0}, {"enable": true, "name": 4, "action": 0}]}}, "deviceControl": {"dataLossPrevention": {"enable": false, "rules": [{"ruleName": "Bluetooth Devices", "deviceClass": 1, "permissions": {"ALL": 1}}, {"ruleName": "CDROM Drives", "deviceClass": 2, "permissions": {"ALL": 1}}, {"ruleName": "Floppy Disk Drives", "deviceClass": 4, "permissions": {"ALL": 1}}, {"ruleName": "IEEE 1284 4", "deviceClass": 5, "permissions": {"ALL": 1}}, {"ruleName": "IEEE 1394", "deviceClass": 6, "permissions": {"ALL": 1}}, {"ruleName": "Imaging Devices", "deviceClass": 7, "permissions": {"ALL": 1}}, {"ruleName": "Modems", "deviceClass": 8, "permissions": {"ALL": 1}}, {"ruleName": "Tape Drives", "deviceClass": 10, "permissions": {"ALL": 1}}, {"ruleName": "Windows Portable", "deviceClass": 12, "permissions": {"ALL": 1}}, {"ruleName": "LPT/COM Ports", "deviceClass": 13, "permissions": {"ALL": 1}}, {"ruleName": "SCSI Raid", "deviceClass": 14, "permissions": {"ALL": 1}}, {"ruleName": "Printers", "deviceClass": 16, "permissions": {"ALL": 1}}, {"ruleName": "Network Adapters", "deviceClass": 18, "permissions": {"ALL": 1}}, {"ruleName": "Wireless Network Adapters", "deviceClass": 19, "permissions": {"ALL": 1}}, {"ruleName": "Internal Storage", "deviceClass": 20, "permissions": {"ALL": 1}}, {"ruleName": "External Storage", "deviceClass": 21, "permissions": {"ALL": 1}}]}, "dataLossPreventionExceptions": {"enable": false, "rules": []}}, "exchange": {"antimalware": {"enable": true, "exclusions": [], "rules": [{"name": "Default rule", "active": true, "default": true, "scope": {"applyTo": 4, "from": 1, "to": 1}, "settings": {"scanMode": 1, "extensions": [], "maximumSizeEnabled": false, "maximumSize": 3, "maximumDepthEnabled": true, "maximumDepth": 4, "scanPUA": true}, "actions": {"infected": {"action": 2, "then": 4}, "suspected": {"action": 1, "then": 1}, "stopIfMatched": true, "unscannable": {"action": 1, "then": 1}}}], "scanTasks": [], "settings": {"appendFooter": true, "footerText": "This email was scanned by Bitdefender", "infectedText": "The $FILENAME attachment was infected with $VIRUS. The attachment was deleted by Bitdefender.", "quarantinedText": "The $FILENAME attachment was infected with $VIRUS. The attachment was moved to quarantine by Bitdefender.", "unscannableInfectedText": "The $FILENAME attachment could not be scanned. The attachment was deleted by Bitdefender.", "unscannableQuarantinedText": "The $FILENAME attachment could not be scanned. The attachment was moved to quarantine by Bitdefender."}}, "antispam": {"enable": true, "settings": {"rblDnsAddress": "", "rblDnsMsTimeout": 500, "rblServers": []}, "whiteList": {"enable": true, "list": []}, "rules": [{"name": "Default Rule", "default": true, "active": true, "scope": {"applyTo": 1, "from": 1, "to": 1}, "aggressivity": 2, "filters": {"asian": false, "cyrillic": false, "fapMaterial": true, "url": true, "rbl": false, "cloud": true, "heuristic": true}, "checkAuthConnections": false, "actions": {"type": 1, "exchangeSCL": true, "modifySubject": true, "modifySubjectText": "[SPAM]", "appendHeader": false, "headerName": "X-Bitdefender-Spam", "headerValue": "${score}", "saveMailToDisk": false, "archiveToAccount": false, "stopIfMatched": true}}]}, "antispoofing": {"enable": false, "domainIpList": []}, "blackList": {"enable": false, "list": []}, "contentControl": {"attachmentFiltering": {"enable": false, "settings": {"replacementText": "A Bitdefender attachment filtering rule detected the $FILENAME attachment and deleted it. Contact your email administrator for more information."}, "exclusions": {"trustedSenders": [], "trustedRecipients": [], "excludeOnlyIfAllRecipientsAreTrusted": false}, "rules": []}, "contentFiltering": {"enable": false, "exclusions": {"trustedSenders": [], "trustedRecipients": [], "excludeOnlyIfAllRecipientsAreTrusted": false}, "rules": []}}, "quarantine": {"deleteFilesOlderThan": 15}, "userGroups": []}, "firewall": {"advanced": {"createAgresiveRules": false, "createRulesForAppsBlockedByIDS": true, "ignoreSignedProcesses": true, "monitorProcessChanges": true, "protectionLevel": 4, "rule": [{"defaultRule": 1, "ruleType": 1, "details": {"name": "Incoming ICMP", "applictionPath": "system", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": ""}, "directlyConnected": {"enable": false}, "protocol": 4, "customProtocol": "1", "direction": 1, "ipVersion": 2}, "permission": {"home": true, "public": true, "setPermission": 1}, "type": 1, "ruleId": "a29eb5d3-2e97-4e4e-92cc-071a3de7d6f0"}, {"defaultRule": 1, "ruleType": 1, "details": {"name": "Incoming ICMPV6", "applictionPath": "system", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": ""}, "directlyConnected": {"enable": false}, "protocol": 4, "customProtocol": "58", "direction": 1, "ipVersion": 3}, "permission": {"home": true, "public": true, "setPermission": 1}, "type": 2, "ruleId": "4813e12a-0fc4-438c-87f3-58a1034d1d17"}, {"defaultRule": 1, "ruleType": 2, "details": {"name": "Incoming Remote Desktop Connections", "applictionPath": "", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": "3389"}, "remoteAddress": {"any": true, "portRange": ""}, "directlyConnected": {"enable": false}, "protocol": 2, "direction": 2, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 1}, "type": 3, "ruleId": "3ba3e489-176e-4baf-879d-9e81a5bfa968"}, {"defaultRule": 1, "ruleType": 2, "details": {"name": "Sending E-mails", "applictionPath": "", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": "25;143;465;587;993"}, "directlyConnected": {"enable": false}, "protocol": 2, "direction": 3, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 1}, "type": 4, "ruleId": "0ebcff1c-153c-42c3-bc74-f2ed3d6d1d39"}, {"defaultRule": 1, "ruleType": 1, "details": {"name": "Web Browsing HTTP", "applictionPath": "", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": "80;443"}, "directlyConnected": {"enable": false}, "protocol": 2, "direction": 1, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 1}, "type": 5, "ruleId": "cb02ebc1-b6ea-476f-b205-9027cb6d47d2"}, {"defaultRule": 1, "ruleType": 1, "details": {"name": "Network Printing", "applictionPath": "%system%\\spoolsv.exe", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": "20;21;35;80;92;161;162;170;515;631;1314;1392;2081;2291;3096;3396;3800;3910;3911;4088;4168;4391;4392;4393;4394;5309;6716;7228;8033;8100;8609;9100;10631;40404"}, "directlyConnected": {"enable": false}, "protocol": 1, "direction": 1, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 2}, "type": 6, "ruleId": "e9913aa9-51d4-4855-9a90-bc5223d90a9a"}, {"defaultRule": 1, "ruleType": 1, "details": {"name": "Windows Explorer Traffic on FTP", "applictionPath": "%windir%\\explorer.exe", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": "20;21"}, "directlyConnected": {"enable": false}, "protocol": 2, "direction": 1, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 2}, "type": 7, "ruleId": "968a8643-bf54-49e3-a449-ca6b4cffb0c5"}, {"defaultRule": 1, "ruleType": 1, "details": {"name": "Windows Explorer Traffic on HTTP", "applictionPath": "%windir%\\explorer.exe", "commandLine": "", "applicationMd5": ""}, "settings": {"localAddress": {"any": true, "portRange": ""}, "remoteAddress": {"any": true, "portRange": "80;443"}, "directlyConnected": {"enable": false}, "protocol": 2, "direction": 1, "ipVersion": 1}, "permission": {"home": true, "public": true, "setPermission": 2}, "type": 8, "ruleId": "a03c53fe-dc5d-4a67-b58c-dabd30c0f044"}]}, "network": {"adapters": [{"type": "Wired", "networkType": 2, "stealthMode": 2}, {"type": "Wireless", "networkType": 3, "stealthMode": 2}, {"type": "Virtual", "networkType": 1, "stealthMode": 2}], "networks": []}, "settings": {"enable": true, "blockPortScan": true, "allowInternetConnectionSharing": false, "monitorWiFiConnections": false, "logVerbosity": {"enable": true, "level": 1}, "instructionsDetectionSystem": {"enable": false, "profile": 2}}}, "general": {"advanced": {"settings": {"scanSsl": false, "browserSearchAdvisor": true, "removeEvents": {"settings": {"days": 30}}, "submitReports": true, "submitSuspicious": true, "sendTelemetry": true, "useGlobalProtectiveNetwork": true}, "passwordConfig": {"profile": 1, "value": ""}, "powerUser": {"enabled": false}}, "allowChangeByOtherUsers": false, "communication": {"ecsAssignments": [], "ecsProxy": {"profile": 1}, "cloudServicesProxy": {"profile": 1}}, "display": {"silentMode": {"enable": false, "iconNotificationArea": true, "showPopups": {"enable": false}, "displayAlertsPopups": false, "showBrowserToolbar": false, "issuesVisibility": {"profile": 1, "general": true, "antimalware": true, "firewall": true, "contentControl": false, "update": true, "installationRestartNotifications": 2, "onAccessNotifications": 3, "onDemandNotifications": 2, "dissinfectionRestartNotification": 3, "updateRestartNotifications": 3, "showAfter": 7, "cloudConnectionNotifications": 3, "enable": true}, "endpointRestartPopup": {"enable": false, "update": false, "patchManagement": false, "patchManagementAutoRestart": false, "patchManagementAutoRestartAfter": 6}}, "supportInformation": {"website": "http://enterprise.bitdefender.com/support/business.html", "email": "http://enterprise.bitdefender.com/support/contact-us.html", "phone": "1-954-776-6262"}}, "update": {"settings": {"productUpdateScheduler": {"enabled": true, "occurrence": 1, "updateInterval": 1, "weekDays": {"days": [0, 1, 2, 3, 4, 5, 6], "startHour": 0, "startMinute": 0, "endHour": 23, "endMinute": 59}, "postponeReboot": true, "rebootAfterInstalling": {"enable": false, "settings": {"day": 7, "hour": 21, "minutes": 0}}}, "signatureUpdateScheduler": {"enabled": true, "occurrence": 1, "updateInterval": 1, "weekDays": {"days": [0, 1, 2, 3, 4, 5, 6], "startHour": 0, "startMinute": 0, "endHour": 23, "endMinute": 59}}, "proxy": {"enable": false, "profile": 1, "settings": {"server": "http://proxy", "port": 12, "username": "username", "password": ""}}, "defaultLocation": true, "updateRing": 0}, "updateLocations": [{"server": "/RELAY/", "useProxy": false}, {"server": "update.cloud.2d585.cdn.bitdefender.net:80", "useProxy": false}]}, "securityTelemetry": {"enabled": false, "siem": 0, "protocol": 0, "format": 0, "url": "", "key": "", "proxy": {"profile": 3}}}, "relay": {"communication": {"cloudServicesProxy": {"profile": 1}, "applianceProxy": {"profile": 1}}, "update": {"updateInterval": {"enable": true, "hours": 1}, "downloadFolder": "", "updateLocations": {"enable": true, "locations": [{"server": "update.cloud.2d585.cdn.bitdefender.net:80", "useProxy": false}, {"server": "upgrade.bitdefender.com", "useProxy": false}]}}}, "networkSandboxing": {"enabled": false, "analysisMode": 1, "remediationActions": {"defaultAction": 3, "fallbackAction": 2}, "settings": {"isCloudSandbox": true, "ip": "", "hostname": "", "endpointId": "None"}, "proxy": {"enabled": false, "settings": {"server": "http://proxy", "port": 12, "username": "", "password": ""}}, "contentPrefiltering": {"categories": {"applications": {"enabled": true, "level": 2}, "documents": {"enabled": false, "level": 2}, "scripts": {"enabled": false, "level": 2}, "archives": {"enabled": false, "level": 2}, "emails": {"enabled": false, "level": 2}}, "excludeExtensions": [], "sizeFilter": {"enabled": false, "fileMinSizeKB": 100, "fileMaxSizeMB": 3}}}, "encryption": {"enabled": false, "mode": 0, "encryptPolicy": {"tpm": {"shouldAskForPassword": false}}}, "edrSensor": {"general": {"enabled": true}}, "patchManagement": {"enabled": false, "downloadSettings": {"cachingServers": [], "fallbackOnDirectDownload": true}, "automaticScanScheduler": {"recurrence": 2, "days": [1, 2, 3, 4, 5], "startHour": 21, "startMinute": 0, "runOnSystemChanges": true}, "installPatchesSettings": {"enabled": false, "updateType": {"securityPatchesSettings": {"enabled": true, "scheduler": {"recurrence": 1, "days": [1, 2, 3, 4, 5], "startHour": 21, "startMinute": 0}}, "nonSecurityPatchesSettings": {"enabled": true, "scheduler": {"recurrence": 3, "days": [4], "startHour": 21, "startMinute": 0}}}, "specificVendorAndProduct": {"enabled": false, "vendorProductsPairs": []}, "ifMissedRunAsSoonAsPossible": false, "postponeReboot": true}}, "storageProtection": {"icap": {"enabled": false, "serviceName": "bdicap", "listenPort": 1344, "archiveScan": {"enabled": false, "archiveMaxSize": 3, "archiveMaxDepth": 2}, "congestionControl": {"mode": 1, "maxConnections": 300}, "scanAction": {"defaultAction": 1}, "enablePort": true, "enableSslPort": false, "listenSslPort": 11344}, "exclusions": {"enabled": false, "exclusionItems": []}}, "indicatorsOfRisk": {"enabled": false, "scheduler": {"recurrenceType": 1, "runEvery": 1, "runPer": 2, "recurrentDaySun": 0, "recurrentDayMon": 0, "recurrentDayTue": 0, "recurrentDayWed": 0, "recurrentDayThu": 0, "recurrentDayFri": 0, "recurrentDaySat": 0, "recovery": {"mode": {"runImmediately": false}}}}}}}
```









