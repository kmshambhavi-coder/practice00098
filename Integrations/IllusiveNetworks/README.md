
# IllusiveNetworks

Shrink your organization’s attack surface. Find and eliminate the vulnerable credentials and connections that attackers use to escalate privileges and move laterally. Agentless, undetectable deception technology that creates a hostile environment for attackers, stopping lateral movement and access to your critical assets. Get actionable, real-time or on-demand forensic attack insight to accelerate blocking and remediation.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|http://x.x.x.x|
|API Key||True|Password|*****|
|CA Certificate File||False|String||
|Verify SSL||False|Boolean|false|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|


## Actions
#### Add Deceptive Server
Add deceptive servers in Illusive Networks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Name|Specify what kind of deceptive items should be returned.|True|String||
|Service Types|Specify a comma-separated list of service types for new deceptive server.|True|String|DB|
|Policy Names|Specify a comma-separated list of policies that need to be applied to the new deceptive server. If nothing is provided action will use by default all policies.|False|String||



#### Add Deceptive User
Add deceptive users in Illusive Networks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Username|Specify the username for the new deceptive user.|True|String||
|Password|Specify the password for the new deceptive user.|True|Password|*****|
|DNS Domain|Specify the domain name for the new deceptive user.|False|String||
|Policy Names|Specify a comma-separated list of policies that need to be applied to the new deceptive user. If nothing is provided action will use by default all policies.|False|String||



#### Enrich Entities
Enrich entities using information from Illusive Networks. Supported entities: Hostname.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "MSSQL-XXX", "EntityResult": {"content": [{"machineId": "32de351a-755c-40c7-806b-8xxx", "machineName": "MSSQL-XXX", "isHealthy": "false", "lastDeploymentMethodType": "WMI", "distinguishedName": "CN=MSSQL-XXX,CN=Computers,dc=lab,dc=local", "groupName": null, "sourceDiscoveryName": "lab.local", "collectData": true, "policyName": null, "assignmentStatus": "ANALYSIS", "operatingSystemType": "Windows", "operatingSystemName": "Windows Server 2016 Standard Evaluation", "operatingSystemVersion": "10.0 (14393)", "agentVersion": null, "bitness": null, "loggedInUserName": null, "lastLogonTime": 1610487457236, "succeededDeceptionFamilies": 0, "shouldBeUninstalledDeceptionFamilies": 0, "desiredDeceptionFamilies": 0, "deceptionFamiliesPercentages": null, "lastExecutionType": "AGENT", "machineLastExecutionPhaseType": "CONNECTION", "machineLastExecutionPhaseStatus": "FAILURE", "machineLastExecutionPhaseErrorMessage": "Unreachable - no ping", "mitigationStatusType": null, "machineExecutionUnifiedStatus": "FAILURE_CONNECTION", "machineLastExecutionPhaseFinishDate": "2021-03-02T21:13:04.636Z", "endpointTrapHealthCheckHostStatus": "NotTested", "endpointTrapHealthCheckHostStatusLastUpdated": null, "failedDeceptionFamilies": 0, "inProgressDeceptionFamilies": 0, "notDeployedDeceptionFamilies": 0, "policyId": null, "ghost": false}], "totalQueryResults": 1}}]
```



#### List Deceptive Items
List available deceptive items in Illusive Networks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Deceptive Type|Specify what kind of deceptive items should be returned.|True|List|All|
|Deceptive State|Specify what kind of deceptive items should be returned based on state.|True|List|All|
|Max Items To Return|Specify how many items to return. Default: 50. If nothing is specified, action will return all items.|False|String|50|



##### JSON Results
```json
{"users": [{"username": "Administrator", "password": "xxxxx", "domainName": "siemplifylab.xxxx", "policyNames": ["Full Protection"], "adUser": true, "activeUser": true, "deceptiveState": "APPROVED"}, {"username": "accountpriv", "password": "xxxxxx", "domainName": "siemplifylab.xxxx", "policyNames": [], "adUser": false, "activeUser": false, "deceptiveState": "SUGGESTED"}], "servers": [{"host": "ex001.xxxx.local", "serviceTypes": ["WEB", "SSH", "SHARE", "DB"], "policyNames": ["Full Protection"], "adHost": true, "deceptiveState": "APPROVED"}]}
```



#### Ping
Test connectivity to the Illusive Networks with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Remove Deceptive Server
Remove deceptive server from Illusive Networks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Name|Specify the name of the deceptive server that needs to be removed.|True|String||



#### Remove Deceptive User
Remove deceptive user from Illusive Networks.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Username|Specify the username of the deceptive user that needs to be removed.|True|String||



#### Run Forensic Scan
Run forensic scan on the endpoint in the Illusive Networks. Works with IP and Hostname entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Include System Information|If enabled, action will return system information.|False|Boolean|true|
|Include Prefetch Files Information|If enabled, action will return information about prefetch files.|False|Boolean|true|
|Include Add-Remove Programs Information|If enabled, action will return information about add-remove programs.|False|Boolean|false|
|Include Startup Processes Information|If enabled, action will return information about startup processes.|False|Boolean|false|
|Include Running Processes Information|If enabled, action will return information about running processes.|False|Boolean|false|
|Include User-Assist Programs Information|If enabled, action will return information about user-assist programs.|False|Boolean|false|
|Include Powershell History Information|If enabled, action will return information about powershell history.|False|Boolean|false|
|Max Items To Return|Specify how many items to return. If nothing is provided, action will return everything.|False|String|50|



##### JSON Results
```json
[{"Entity": "some_entity", "EntityResult": {"host_info": {"osName": "Windows 10", "machineType": "Workstation", "host": "xxx.yyy.local", "loggedInUser": "No User is Logged-in", "userProfiles": ["admin", "Administrator"], "operatingSystemType": "Windows", "timeDeviationInHours": -8.0, "daylightSavingDeviationInHours": 0.0}, "prefetch_info": [{"details": {"MD5": "N/A", "SHA256": "N/A", "dataSource": "Prefetch", "isFileExists": "No", "lastExecutionTime": "2021-03-08T02:32:07.123-08:00", "lastRunTimes": ["2021-03-01T02:25:26.533-08:00", "2021-02-18T18:23:10.450-08:00", "2021-02-18T17:09:42.157-08:00", "2021-02-17T18:23:58.376-08:00"], "prefetchFileName": "C:\\Windows\\Prefetch\\AM_DELTA.EXE-3A6EE7FD.pf", "relatedModules": ["\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\MPSIGSTUB.EXE", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\NTDLL.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SOFTWAREDISTRIBUTION\\DOWNLOAD\\INSTALL\\AM_DELTA.EXE", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\KERNEL32.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\KERNELBASE.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\LOCALE.NLS", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\ADVAPI32.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\MSVCRT.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\SECHOST.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\RPCRT4.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\VERSION.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\BCRYPTPRIMITIVES.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\$MFT"], "runCount": 0, "version": 30}, "fileName": "C:\\WINDOWS\\SOFTWAREDISTRIBUTION\\DOWNLOAD\\INSTALL\\AM_DELTA.EXE"}, {"details": {"MD5": "N/A", "SHA256": "N/A", "dataSource": "Prefetch", "isFileExists": "No", "lastExecutionTime": "2021-02-15T18:23:20.701-08:00", "lastRunTimes": [], "prefetchFileName": "C:\\Windows\\Prefetch\\AM_DELTA_PATCH_1.331.1067.0.E-C66E0B1B.pf", "relatedModules": ["\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\NTDLL.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SOFTWAREDISTRIBUTION\\DOWNLOAD\\INSTALL\\AM_DELTA_PATCH_1.331.1067.0.EXE", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\KERNEL32.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\KERNELBASE.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\LOCALE.NLS", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\ADVAPI32.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\MSVCRT.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\SECHOST.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\RPCRT4.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\VERSION.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\BCRYPTPRIMITIVES.DLL", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\SYSTEM32\\MPSIGSTUB.EXE", "\\VOLUME{01d7035e6f98cb77-266fcfdc}\\WINDOWS\\APPPATCH\\SYSMAIN.SDB"], "runCount": 0, "version": 30}, "fileName": "C:\\WINDOWS\\SOFTWAREDISTRIBUTION\\DOWNLOAD\\INSTALL\\AM_DELTA_PATCH_1.331.1067.0.EXE"}], "installed_programs_info": [{"details": {"MD5": "N/A", "SHA256": "N/A", "dataSource": "Add Remove Programs", "displayName": "Microsoft Update Health Tools", "isFileExists": "No", "lastWriteTime": "2021-02-20T14:18:49.409-08:00", "version": "2.75.0.0"}, "fileName": "MsiExec.exe /X{BAB9FCC5-1506-4B4F-BFCA-EDE0BDB86C21}"}], "startup_processes": [{"Caption": "OneDriveSetup", "Command": "C:\\Windows\\SysWOW64\\OneDriveSetup.exe /thfirstsetup", "Description": "OneDriveSetup", "Location": "HKU\\S-1-5-19\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run", "Name": "OneDriveSetup", "SettingID": "", "User": "NT AUTHORITY\\LOCAL SERVICE", "UserSID": "S-1-5-19"}, {"Caption": "OneDriveSetup", "Command": "C:\\Windows\\SysWOW64\\OneDriveSetup.exe /thfirstsetup", "Description": "OneDriveSetup", "Location": "HKU\\S-1-5-20\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run", "Name": "OneDriveSetup", "SettingID": "", "User": "NT AUTHORITY\\NETWORK SERVICE", "UserSID": "S-1-5-20"}], "running_processes": [{"MD5": "N/A", "SHA256": "N/A", "administratorPrivilleges": "True", "commandline": "", "processID": 4, "processName": "N/A", "processParent": "N/A", "processPath": "N/A", "session": "RDP-Tcp (0)", "sessionId": 0, "startTime": "2021-02-22T02:04:29.428-08:00", "user": "NT AUTHORITY\\SYSTEM", "userSid": "S-1-5-18"}, {"MD5": "N/A", "SHA256": "5BE0DE7F915BA819D4BA048DB7A2A87F6F3253FDD4865DC418181A0D6A031CAA", "administratorPrivilleges": "True", "commandline": "C:\\Windows\\system32\\svchost.exe -k DcomLaunch -p -s LSM", "processID": 8, "processName": "svchost.exe", "processParent": "N/A", "processPath": "C:\\Windows\\System32\\svchost.exe", "session": "RDP-Tcp (0)", "sessionId": 0, "startTime": "2021-02-22T02:06:35.629-08:00", "user": "NT AUTHORITY\\SYSTEM", "userSid": "S-1-5-18"}]}}]
```









## Connectors
#### Illusive Networks - Incidents Connector
Pull incidents with related forensic timeline from Illusive Networks. Note: This connector requires changes to the rate limiting on the Illusive Networks server. Default rate limit is too small. All of the steps are available in the documentation. Whitelisting and Blacklisting is done via type of the incident

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|details_serviceType|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Illusive Networks instance.|True|String|http://x.x.x.x|
|API Key|API Key of the Illusive Networks. Note: string "Basic" shouldn't be a part of the value.|True|Password|*****|
|CA Certificate File|Base 64 encoded CA certificate file.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Illusive Networks server is valid.|False|Boolean|false|
|Alert Severity|Severity of the Siemplify alert that will be created based on the incidents from Illusive Networks. Possible values: Informational Low Medium High Critical|True|String|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 1000.|False|Integer|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


##### Allowlist
| |
|-|
|EXTERNAL|




