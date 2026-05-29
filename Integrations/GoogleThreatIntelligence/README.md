
# GoogleThreatIntelligence

Google Threat Intelligence (GTI) delivers comprehensive threat insights by combining Mandiant's expertise, Google's vast data resources, and VirusTotal's crowdsourced intelligence. By defending billions of users, seeing millions of phishing attacks, and spending hundreds of thousands of hours investigating incidents it has the visibility to see across the threat landscape to keep the most important organizations protected.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The API root of the Google Threat Intelligence instance.|True|String|https://www.virustotal.com|
|API Key|The Google Threat Intelligence API key.|True|Password|*****|
|ASM Project Name|The Attack Surface Management (ASM) project name to use in the Google Threat Intelligence integration. This parameter is required to execute the ASM actions.|False|String||
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to the Google Threat Intelligence server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|bcrypt-4.2.0-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|certifi-2024.8.30-py3-none-any.whl|
|paramiko-3.5.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|TIPCommon-2.2.2-py2.py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|pycryptodomex-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests-2.32.3-py3-none-any.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|httpcore-1.0.5-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|soupsieve-2.6-py3-none-any.whl|
|PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl|
|pyzipper-0.3.6-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_api_core-2.22.0-py3-none-any.whl|
|proto_plus-1.25.0-py3-none-any.whl|
|google_auth-2.35.0-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|anyio-4.4.0-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|google_api_python_client-2.151.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|


## Actions
#### Add ASM Issue Note
Use the Add ASM Issue Note action to add a note for the Attack Surface Management (ASM) issue in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The ID of the alert to update.|True|String||
|Text|Text of the analysis.|True|String||



#### Add Comment To Entity
Use the Add Comment To Entity action to add comments to the Google SecOps entities in Google Threat Intelligence. This action runs on the following Google SecOps entities: File Hash, URL, Hostname, Domain, IP Address. This action supports the MD5, SHA-1, and SHA-256 hashes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|A comment to add to all supported entities.|True|String||



##### JSON Results
```json
[{"Entity": "xxxx@xxxx.xx", "EntityResult": {"Status": "Done"}},{"Entity": "yyyy@yyyy.yy", "EntityResult": {"Status": "Not done"}}]
```



#### Add Tag To DTM Alert
Use the “Add Tag To DTM” to add tags to a Digital Threat Monitoring (DTM) alert in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The ID of the alert to update.|True|String||
|Mode|Mode for the action execution. If “Append” is selected, action will add a new tag to the alert. If “Set” is selected, action will overwrite existing tags with the provided one in “Tags” parameter.|True|List|Append|
|Tags|Comma-separated list of tags that should be added to Alert.|True|String||



#### Add Vote To Entity
Use the Add Vote To Entity action to add votes to the Google SecOps entities in Google Threat Intelligence. This action supports the following Google SecOps entities: File Hash, URL, Hostname, Domain, IP Address. This action supports the MD5, SHA-1, and SHA-256 hashes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vote|A vote to add to all supported entities.|True|List|Malicious|



##### JSON Results
```json
[{"Entity": "xxxx@xxxx.xx", "EntityResult": {"Status": "Done"}},{"Entity": "yyyy@yyyy.yy", "EntityResult": {"Status": "Not done"}}]
```



#### Download File
Use the Download File action to download a file from Google Threat Intelligence. This action runs on the Google SecOps Hash entity. This action supports the MD5, SHA-1, and SHA-256 hashes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Download Folder Path|The path to a folder to store the downloaded files, such as "/tmp/".|True|String||
|Overwrite|If selected, the action overwrites the file with the same name.|False|Boolean|true|



##### JSON Results
```json
{"absolute_file_paths": ["/tmp/9498FF82A64FF445398C8426ED63hash", "/tmp/275A021BBFB6489E54D471899F7DB9D1663FC695EC2FE2A2C453hash"]}
```



#### Enrich Entities
Use the Enrich Entities action to enrich the Google SecOps entities using information from Google Threat Intelligence. This action runs on the following Google Secops entities: IP address, URL, Hostname, Domain, Hash, Threat Actor, CVE. This action supports only MD5, SHA-1, and SHA-256 hashes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|GTI Score|GTI Score that is used to set Google SecOps entities as suspicious. This condition is validated together with GTI verdict information. If nothing is provided, action will ignore the GTI score values. This parameter only supports IP address, URL, Hostname, Domain, Hash entities.|False|String|60|
|Engine Threshold|The count of how many engines should mark the entity as malicious or suspicious, for Google SecOps to label it as suspicious. If “Engine Allowlist” contains values, action will only count results from those engines. This condition is validated together with GTI verdict information. If nothing is provided, action will ignore the Engines calculations. This parameter only supports IP address, URL, Hostname, Domain, Hash entities.|False|String|None|
|Engine Percentage Threshold|The percentage of engines should mark the entity as malicious or suspicious, for Google SecOps to label it as suspicious. If “Engine Allowlist” contains values, action will only count the percentage from those engines. If both “Engine Threshold” and “Engine Percentage Threshold” are provided, “Engine Threshold” will be used. Maximum value: 100. Minimum: 0. If nothing is provided, action will ignore the Engines calculations. This parameter only supports IP address, URL, Hostname, Domain, Hash entities.|False|String|None|
|Engine Allowlist|Comma-separated list of engines that should be used to retrieve information, whether an entity is malicious or not. Example: AlienVault,Kaspersky.If nothing is specified in this parameter, action will take results from every available engine. If the engine didn’t return any information about the entity it’s not going to be counted for the parameters “Engine Threshold” and “Engine Percentage Threshold”.|False|String||
|Resubmit Entity|If selected, the action resubmits entities for analysis instead of using the information from the previous action run. This parameter only supports the URL and Hash entities. Not selected by default.|False|Boolean|false|
|Resubmit After (Days)|The number of days for the action to wait before resubmitting the entity. To use this parameter, enable the "Resubmit Entity" parameter. The default value is 30 days. This parameter only supports the URL and Hash entities.|False|String|30|
|Sandbox|A comma-separated list of sandbox names to analyze, such as VirusTotal Jujubox, VirusTotal ZenBox, Microsoft Sysinternals, Tencent HABO. This parameter only supports the Hash entity.If you don’t set this parameter, the action uses the default sandbox, VirusTotal Jujubox.|False|String|VirusTotal Jujubox|
|Retrieve Sandbox Analysis|If selected, the action retrieves the sandbox analysis for the entity and creates a separate section for every sandbox in the JSON result. The action returns data for sandboxes that you configured in the "Sandbox" parameter. This parameter only supports the Hash entity. Not selected by default.|False|Boolean|false|
|Fetch MITRE Details|If selected, the action returns the information about the related MITRE techniques and tactics. This parameter only supports the Hash entity. Not selected by default.|False|Boolean|false|
|Lowest MITRE Technique Severity|The lowest MITRE technique severity to return. The action treats the "Unknown" severity as “Info”. This parameter only supports the Hash entity. The default value is Medium.|False|List|Medium|
|Retrieve Comments|If selected, the action retrieves comments about the entity. This parameter supports the following entities: URL, Domain, Hostname, Hash, and IP Address.|False|Boolean|true|
|Max Comments To Return|The maximum number of comments to return in every action run. The default value is 10.|False|String|10|
|Widget Theme|The theme of the augmented widget.|False|List|Chronicle|



##### JSON Results
```json
[{"Entity": "c60d529a802046e447eadbae5c6aaf9bbf746322", "EntityResult": {"id": "791d0fa941c37457973f04d12263d01ca5c480e5bfc795f025e79ac96e025af5", "type": "file", "links": {"self": "https://www.virustotal.com/api/v3/files/791d0fa941c37457973f04d12263d01ca5c480e5bfc795f025e79ac96e025af5"}, "attributes": {"detectiteasy": {"filetype": "PE64", "values": [{"version": "1.15.0-X.XX.X", "type": "Compiler", "name": "Go"}, {"info": "PKCS #7", "version": "2.0", "type": "Sign tool", "name": "Windows Authenticode"}]}, "first_submission_date": 1718412154, "names": ["C:\\\\ProgramData\\\\GooGet\\\\googet.exe", "c:\\\\users\\\\all users\\\\googet\\\\googet.exe", "c:\\\\programdata\\\\googet\\\\googet.exe", "c:\\\\google\\\\migrate\\\\googet\\\\googet.exe", "googet.exe", "/tmp/hashr-windows-cloud-windows-server-2016-dc-core-v20240612-808232598/extracted/export/ProgramData/GooGet/googet.exe"], "signature_info": {"verified": "Signed", "signing date": "11:10 PM 04/22/2024", "x509": [{"valid usage": "Code Signing", "thumbprint_sha256": "46011EDE1C147EB2BC731A539B7C047B7EE93E48B9D3C3BA710CE132BBDFAC6B", "name": "DigiCert Trusted G4 Code Signing RSA4096 SHA384 2021 CA1", "algorithm": "sha384RSA", "thumbprint_md5": "D91299E84355CD8D5A86795A0118B6E9", "valid from": "2021-04-29 00:00:00", "valid to": "2036-04-28 23:59:59", "serial number": "08 AD 40 B2 60 D2 9C 4C 9F 5E CD A9 BD 93 AE D9", "cert issuer": "DigiCert Trusted Root G4", "thumbprint": "7B0F360B775F76C94A12CA48445AA2D2A875701C"}, {"valid usage": "Code Signing", "thumbprint_sha256": "7D3D117664F121E592EF897973EF9C159150E3D736326E9CD2755F71E0FEBC0C", "name": "Google LLC", "algorithm": "sha256RSA", "thumbprint_md5": "DC429A22AA63D23DB8E84F53D05D1D48", "valid from": "2021-07-02 00:00:00", "valid to": "2024-07-10 23:59:59", "serial number": "0E 44 18 E2 DE DE 36 DD 29 74 C3 44 3A FB 5C E5", "cert issuer": "DigiCert Trusted G4 Code Signing RSA4096 SHA384 2021 CA1", "thumbprint": "2673EA6CC23BEFFDA49AC715B121544098A1284C"}, {"valid usage": "ff", "thumbprint_sha256": "D2F6E46DED7422CCD1D440576841366F828ADA559AAE3316AF4D1A9AD40C7828", "name": "DigiCert Timestamp 2023", "algorithm": "sha256RSA", "thumbprint_md5": "A6BA5FDF34F4060A647083BE314F6F24", "valid from": "2023-07-14 00:00:00", "valid to": "2034-10-13 23:59:59", "serial number": "05 44 AF F3 94 9D 08 39 A6 BF DB 3F 5F E5 61 16", "cert issuer": "DigiCert Trusted G4 RSA4096 SHA256 TimeStamping CA", "thumbprint": "66F02B32C2C2C90F825DCEAA8AC9C64F199CCF40"}, {"valid usage": "Timestamp Signing", "thumbprint_sha256": "281734D4592D1291D27190709CB510B07E22C405D5E0D6119B70E73589F98ACF", "name": "DigiCert Trusted G4 RSA4096 SHA256 TimeStamping CA", "algorithm": "sha256RSA", "thumbprint_md5": "9E3E4FA44117441DBA73C28E983FC05F", "valid from": "2022-03-23 00:00:00", "valid to": "2037-03-22 23:59:59", "serial number": "07 36 37 B7 24 54 7C D8 47 AC FD 28 66 2A 5E 5B", "cert issuer": "DigiCert Trusted Root G4", "thumbprint": "B6C8AF834D4E53B673C76872AA8C950C7C54DF5F"}, {"thumbprint_sha256": "33846B545A49C9BE4903C60E01713C1BD4E4EF31EA65CD95D69E62794F30B941", "name": "DigiCert Trusted Root G4", "algorithm": "sha384RSA", "thumbprint_md5": "8DDD0BC6D9D770EB6B2B671A862855CC", "valid from": "2022-08-01 00:00:00", "valid to": "2031-11-09 23:59:59", "serial number": "0E 9B 18 8E F9 D0 2D E7 EF DB 50 E2 08 40 18 5A", "cert issuer": "DigiCert Assured ID Root CA", "thumbprint": "A99D5B79E9F1CDA59CDAB6373169D5353F5874C6"}], "signers": "Google LLC; DigiCert Trusted G4 Code Signing RSA4096 SHA384 2021 CA1; DigiCert Trusted Root G4; DigiCert", "counter signers details": [{"status": "Valid", "valid usage": "Timestamp Signing", "name": "DigiCert Timestamp 2023", "algorithm": "sha256RSA", "valid from": "12:00 AM 07/14/2023", "valid to": "11:59 PM 10/13/2034", "serial number": "05 44 AF F3 94 9D 08 39 A6 BF DB 3F 5F E5 61 16", "cert issuer": "DigiCert Trusted G4 RSA4096 SHA256 TimeStamping CA", "thumbprint": "66F02B32C2C2C90F825DCEAA8AC9C64F199CCF40"}, {"status": "Valid", "valid usage": "Timestamp Signing", "name": "DigiCert Trusted G4 RSA4096 SHA256 TimeStamping CA", "algorithm": "sha256RSA", "valid from": "12:00 AM 03/23/2022", "valid to": "11:59 PM 03/22/2037", "serial number": "07 36 37 B7 24 54 7C D8 47 AC FD 28 66 2A 5E 5B", "cert issuer": "DigiCert Trusted Root G4", "thumbprint": "B6C8AF834D4E53B673C76872AA8C950C7C54DF5F"}, {"status": "Valid", "valid usage": "All", "name": "DigiCert Trusted Root G4", "algorithm": "sha384RSA", "valid from": "12:00 AM 08/01/2022", "valid to": "11:59 PM 11/09/2031", "serial number": "0E 9B 18 8E F9 D0 2D E7 EF DB 50 E2 08 40 18 5A", "cert issuer": "DigiCert Assured ID Root CA", "thumbprint": "A99D5B79E9F1CDA59CDAB6373169D5353F5874C6"}, {"status": "Valid", "valid usage": "Client Auth, Code Signing, Email Protection, Server Auth, Timestamp Signing", "name": "DigiCert", "algorithm": "sha1RSA", "valid from": "12:00 AM 11/10/2006", "valid to": "12:00 AM 11/10/2031", "serial number": "0C E7 E0 E5 17 D8 46 FE 8F E5 60 FC 1B F0 30 39", "cert issuer": "DigiCert Assured ID Root CA", "thumbprint": "0563B8630D62D75ABBC8AB1E4BDFB5A899B24D43"}], "counter signers": "DigiCert Timestamp 2023; DigiCert Trusted G4 RSA4096 SHA256 TimeStamping CA; DigiCert Trusted Root G4; DigiCert", "signers details": [{"status": "This certificate or one of the certificates in the certificate chain is not time valid.", "valid usage": "Code Signing", "name": "Google LLC", "algorithm": "sha256RSA", "valid from": "12:00 AM 07/02/2021", "valid to": "11:59 PM 07/10/2024", "serial number": "0E 44 18 E2 DE DE 36 DD 29 74 C3 44 3A FB 5C E5", "cert issuer": "DigiCert Trusted G4 Code Signing RSA4096 SHA384 2021 CA1", "thumbprint": "2673EA6CC23BEFFDA49AC715B121544098A1284C"}, {"status": "Valid", "valid usage": "Code Signing", "name": "DigiCert Trusted G4 Code Signing RSA4096 SHA384 2021 CA1", "algorithm": "sha384RSA", "valid from": "12:00 AM 04/29/2021", "valid to": "11:59 PM 04/28/2036", "serial number": "08 AD 40 B2 60 D2 9C 4C 9F 5E CD A9 BD 93 AE D9", "cert issuer": "DigiCert Trusted Root G4", "thumbprint": "7B0F360B775F76C94A12CA48445AA2D2A875701C"}, {"status": "Valid", "valid usage": "All", "name": "DigiCert Trusted Root G4", "algorithm": "sha384RSA", "valid from": "12:00 AM 08/01/2022", "valid to": "11:59 PM 11/09/2031", "serial number": "0E 9B 18 8E F9 D0 2D E7 EF DB 50 E2 08 40 18 5A", "cert issuer": "DigiCert Assured ID Root CA", "thumbprint": "A99D5B79E9F1CDA59CDAB6373169D5353F5874C6"}, {"status": "Valid", "valid usage": "Client Auth, Code Signing, Email Protection, Server Auth, Timestamp Signing", "name": "DigiCert", "algorithm": "sha1RSA", "valid from": "12:00 AM 11/10/2006", "valid to": "12:00 AM 11/10/2031", "serial number": "0C E7 E0 E5 17 D8 46 FE 8F E5 60 FC 1B F0 30 39", "cert issuer": "DigiCert Assured ID Root CA", "thumbprint": "0563B8630D62D75ABBC8AB1E4BDFB5A899B24D43"}]}, "last_analysis_results": {"Bkav": {"method": "blacklist", "engine_name": "Bkav", "engine_version": "2.0.0.1", "engine_update": "20250723", "category": "undetected", "result": null}, "Lionic": {"method": "blacklist", "engine_name": "Lionic", "engine_version": "8.16", "engine_update": "20250723", "category": "undetected", "result": null}, "AVG": {"method": "blacklist", "engine_name": "AVG", "engine_version": "23.9.8494.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Elastic": {"method": "blacklist", "engine_name": "Elastic", "engine_version": "4.0.216", "engine_update": "20250721", "category": "undetected", "result": null}, "MicroWorld-eScan": {"method": "blacklist", "engine_name": "MicroWorld-eScan", "engine_version": "14.0.409.0", "engine_update": "20250723", "category": "undetected", "result": null}, "CMC": {"method": "blacklist", "engine_name": "CMC", "engine_version": "2.4.2022.1", "engine_update": "20250723", "category": "undetected", "result": null}, "CAT-QuickHeal": {"method": "blacklist", "engine_name": "CAT-QuickHeal", "engine_version": "22.00", "engine_update": "20250723", "category": "undetected", "result": null}, "Skyhigh": {"method": "blacklist", "engine_name": "Skyhigh", "engine_version": "v2021.2.0+4045", "engine_update": "20250722", "category": "undetected", "result": null}, "ALYac": {"method": "blacklist", "engine_name": "ALYac", "engine_version": "2.0.0.10", "engine_update": "20250723", "category": "undetected", "result": null}, "Malwarebytes": {"method": "blacklist", "engine_name": "Malwarebytes", "engine_version": "4.5.5.54", "engine_update": "20250723", "category": "undetected", "result": null}, "VIPRE": {"method": "blacklist", "engine_name": "VIPRE", "engine_version": "6.0.0.35", "engine_update": "20250722", "category": "undetected", "result": null}, "Sangfor": {"method": "blacklist", "engine_name": "Sangfor", "engine_version": "2.22.3.0", "engine_update": "20250721", "category": "undetected", "result": null}, "K7AntiVirus": {"method": "blacklist", "engine_name": "K7AntiVirus", "engine_version": "12.249.56452", "engine_update": "20250723", "category": "undetected", "result": null}, "BitDefender": {"method": "blacklist", "engine_name": "BitDefender", "engine_version": "7.2", "engine_update": "20250723", "category": "undetected", "result": null}, "K7GW": {"method": "blacklist", "engine_name": "K7GW", "engine_version": "12.249.56453", "engine_update": "20250723", "category": "undetected", "result": null}, "CrowdStrike": {"method": "blacklist", "engine_name": "CrowdStrike", "engine_version": "1.0", "engine_update": "20231026", "category": "undetected", "result": null}, "huorong": {"method": "blacklist", "engine_name": "huorong", "engine_version": "0632fd3:0632fd3:4b2deaa:4b2deaa", "engine_update": "20250723", "category": "undetected", "result": null}, "Baidu": {"method": "blacklist", "engine_name": "Baidu", "engine_version": "1.0.0.2", "engine_update": "20190318", "category": "undetected", "result": null}, "VirIT": {"method": "blacklist", "engine_name": "VirIT", "engine_version": "9.5.1002", "engine_update": "20250722", "category": "undetected", "result": null}, "Paloalto": {"method": "blacklist", "engine_name": "Paloalto", "engine_version": "0.9.0.1003", "engine_update": "20250723", "category": "undetected", "result": null}, "Symantec": {"method": "blacklist", "engine_name": "Symantec", "engine_version": "1.22.0.0", "engine_update": "20250723", "category": "undetected", "result": null}, "tehtris": {"method": "blacklist", "engine_name": "tehtris", "engine_version": "v0.1.4", "engine_update": "20250723", "category": "undetected", "result": null}, "ESET-NOD32": {"method": "blacklist", "engine_name": "ESET-NOD32", "engine_version": "31571", "engine_update": "20250723", "category": "undetected", "result": null}, "Cynet": {"method": "blacklist", "engine_name": "Cynet", "engine_version": "4.0.3.4", "engine_update": "20250723", "category": "undetected", "result": null}, "APEX": {"method": "blacklist", "engine_name": "APEX", "engine_version": "6.678", "engine_update": "20250722", "category": "undetected", "result": null}, "Avast": {"method": "blacklist", "engine_name": "Avast", "engine_version": "23.9.8494.0", "engine_update": "20250723", "category": "undetected", "result": null}, "ClamAV": {"method": "blacklist", "engine_name": "ClamAV", "engine_version": "1.4.3.0", "engine_update": "20250722", "category": "undetected", "result": null}, "Kaspersky": {"method": "blacklist", "engine_name": "Kaspersky", "engine_version": "22.0.1.28", "engine_update": "20250723", "category": "undetected", "result": null}, "Alibaba": {"method": "blacklist", "engine_name": "Alibaba", "engine_version": "0.3.0.5", "engine_update": "20190527", "category": "undetected", "result": null}, "NANO-Antivirus": {"method": "blacklist", "engine_name": "NANO-Antivirus", "engine_version": "1.0.170.26710", "engine_update": "20250723", "category": "undetected", "result": null}, "ViRobot": {"method": "blacklist", "engine_name": "ViRobot", "engine_version": "2014.3.20.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Rising": {"method": "blacklist", "engine_name": "Rising", "engine_version": "25.0.0.28", "engine_update": "20250723", "category": "undetected", "result": null}, "Emsisoft": {"method": "blacklist", "engine_name": "Emsisoft", "engine_version": "2024.8.0.61147", "engine_update": "20250723", "category": "undetected", "result": null}, "F-Secure": {"method": "blacklist", "engine_name": "F-Secure", "engine_version": "18.10.1547.307", "engine_update": "20250723", "category": "undetected", "result": null}, "DrWeb": {"method": "blacklist", "engine_name": "DrWeb", "engine_version": "7.0.69.6040", "engine_update": "20250723", "category": "undetected", "result": null}, "Zillya": {"method": "blacklist", "engine_name": "Zillya", "engine_version": "2.0.0.5409", "engine_update": "20250722", "category": "undetected", "result": null}, "TrendMicro": {"method": "blacklist", "engine_name": "TrendMicro", "engine_version": "24.550.0.1002", "engine_update": "20250723", "category": "undetected", "result": null}, "McAfeeD": {"method": "blacklist", "engine_name": "McAfeeD", "engine_version": "1.2.0.10275", "engine_update": "20250723", "category": "undetected", "result": null}, "Trapmine": {"method": "blacklist", "engine_name": "Trapmine", "engine_version": "4.0.4.0", "engine_update": "20250721", "category": "undetected", "result": null}, "CTX": {"method": "blacklist", "engine_name": "CTX", "engine_version": "2024.8.29.1", "engine_update": "20250723", "category": "undetected", "result": null}, "Sophos": {"method": "blacklist", "engine_name": "Sophos", "engine_version": "3.0.3.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Ikarus": {"method": "blacklist", "engine_name": "Ikarus", "engine_version": "6.4.16.0", "engine_update": "20250722", "category": "undetected", "result": null}, "GData": {"method": "blacklist", "engine_name": "GData", "engine_version": "GD:27.41154AVA:64.29526", "engine_update": "20250723", "category": "undetected", "result": null}, "Jiangmin": {"method": "blacklist", "engine_name": "Jiangmin", "engine_version": "16.0.100", "engine_update": "20250722", "category": "undetected", "result": null}, "Webroot": {"method": "blacklist", "engine_name": "Webroot", "engine_version": "1.9.0.8", "engine_update": "20250227", "category": "undetected", "result": null}, "Varist": {"method": "blacklist", "engine_name": "Varist", "engine_version": "6.6.1.3", "engine_update": "20250723", "category": "undetected", "result": null}, "Avira": {"method": "blacklist", "engine_name": "Avira", "engine_version": "8.3.3.20", "engine_update": "20250723", "category": "undetected", "result": null}, "Antiy-AVL": {"method": "blacklist", "engine_name": "Antiy-AVL", "engine_version": "3.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Kingsoft": {"method": "blacklist", "engine_name": "Kingsoft", "engine_version": "None", "engine_update": "20250722", "category": "undetected", "result": null}, "Gridinsoft": {"method": "blacklist", "engine_name": "Gridinsoft", "engine_version": "1.0.221.174", "engine_update": "20250723", "category": "undetected", "result": null}, "Xcitium": {"method": "blacklist", "engine_name": "Xcitium", "engine_version": "37903", "engine_update": "20250723", "category": "undetected", "result": null}, "Arcabit": {"method": "blacklist", "engine_name": "Arcabit", "engine_version": "2025.0.0.23", "engine_update": "20250723", "category": "undetected", "result": null}, "SUPERAntiSpyware": {"method": "blacklist", "engine_name": "SUPERAntiSpyware", "engine_version": "5.6.0.1032", "engine_update": "20250721", "category": "undetected", "result": null}, "ZoneAlarm": {"method": "blacklist", "engine_name": "ZoneAlarm", "engine_version": "6.18-106782799", "engine_update": "20250723", "category": "undetected", "result": null}, "Microsoft": {"method": "blacklist", "engine_name": "Microsoft", "engine_version": "1.1.25060.6", "engine_update": "20250723", "category": "undetected", "result": null}, "Google": {"method": "blacklist", "engine_name": "Google", "engine_version": "1753254035", "engine_update": "20250723", "category": "undetected", "result": null}, "AhnLab-V3": {"method": "blacklist", "engine_name": "AhnLab-V3", "engine_version": "3.28.0.10568", "engine_update": "20250723", "category": "undetected", "result": null}, "Acronis": {"method": "blacklist", "engine_name": "Acronis", "engine_version": "1.2.0.121", "engine_update": "20240328", "category": "undetected", "result": null}, "VBA32": {"method": "blacklist", "engine_name": "VBA32", "engine_version": "5.3.2", "engine_update": "20250722", "category": "undetected", "result": null}, "TACHYON": {"method": "blacklist", "engine_name": "TACHYON", "engine_version": "2025-07-23.02", "engine_update": "20250723", "category": "undetected", "result": null}, "Cylance": {"method": "blacklist", "engine_name": "Cylance", "engine_version": "3.0.0.0", "engine_update": "20250710", "category": "undetected", "result": null}, "Panda": {"method": "blacklist", "engine_name": "Panda", "engine_version": "4.6.4.2", "engine_update": "20250722", "category": "undetected", "result": null}, "TrendMicro-HouseCall": {"method": "blacklist", "engine_name": "TrendMicro-HouseCall", "engine_version": "24.550.0.1002", "engine_update": "20250723", "category": "undetected", "result": null}, "Tencent": {"method": "blacklist", "engine_name": "Tencent", "engine_version": "1.0.0.1", "engine_update": "20250723", "category": "undetected", "result": null}, "Yandex": {"method": "blacklist", "engine_name": "Yandex", "engine_version": "5.5.2.24", "engine_update": "20250723", "category": "undetected", "result": null}, "TrellixENS": {"method": "blacklist", "engine_name": "TrellixENS", "engine_version": "6.0.6.653", "engine_update": "20250722", "category": "undetected", "result": null}, "SentinelOne": {"method": "blacklist", "engine_name": "SentinelOne", "engine_version": "25.1.1.1", "engine_update": "20250114", "category": "undetected", "result": null}, "MaxSecure": {"method": "blacklist", "engine_name": "MaxSecure", "engine_version": "1.0.0.1", "engine_update": "20250723", "category": "undetected", "result": null}, "Fortinet": {"method": "blacklist", "engine_name": "Fortinet", "engine_version": "7.0.30.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Zoner": {"method": "blacklist", "engine_name": "Zoner", "engine_version": "2.2.2.0", "engine_update": "20250723", "category": "undetected", "result": null}, "DeepInstinct": {"method": "blacklist", "engine_name": "DeepInstinct", "engine_version": "5.0.0.8", "engine_update": "20250721", "category": "undetected", "result": null}, "alibabacloud": {"method": "blacklist", "engine_name": "alibabacloud", "engine_version": "2.2.0", "engine_update": "20250321", "category": "undetected", "result": null}, "google_safebrowsing": {"method": "blacklist", "engine_name": "google_safebrowsing", "engine_version": "1.0", "engine_update": "20250723", "category": "undetected", "result": null}, "Trustlook": {"method": "blacklist", "engine_name": "Trustlook", "engine_version": "1.0", "engine_update": "20250723", "category": "type-unsupported", "result": null}, "SymantecMobileInsight": {"method": "blacklist", "engine_name": "SymantecMobileInsight", "engine_version": "2.0", "engine_update": "20250124", "category": "type-unsupported", "result": null}, "BitDefenderFalx": {"method": "blacklist", "engine_name": "BitDefenderFalx", "engine_version": "2.0.936", "engine_update": "20250416", "category": "type-unsupported", "result": null}, "Avast-Mobile": {"method": "blacklist", "engine_name": "Avast-Mobile", "engine_version": "250722-00", "engine_update": "20250722", "category": "type-unsupported", "result": null}}, "meaningful_name": "C:\\\\ProgramData\\\\GooGet\\\\googet.exe", "size": 17806624, "exiftool": {"MIMEType": "application/octet-stream", "Subsystem": "Windows command line", "MachineType": "AMD AMD64", "TimeStamp": "0000:00:00 00:00:00", "FileType": "Win64 EXE", "PEType": "PE32+", "CodeSize": "6339072", "InitializedDataSize": "424960", "ImageFileCharacteristics": "Executable, Large address aware, No debug", "FileTypeExtension": "exe", "LinkerVersion": "3.0", "SubsystemVersion": "6.1", "EntryPoint": "0x6cec0", "OSVersion": "6.1", "ImageVersion": "1.0", "UninitializedDataSize": "0"}, "last_analysis_stats": {"malicious": 0, "suspicious": 0, "undetected": 73, "harmless": 0, "timeout": 0, "confirmed-timeout": 0, "failure": 0, "type-unsupported": 4}, "type_description": "Win32 EXE", "available_tools": [], "type_tag": "peexe", "tags": ["legit", "overlay", "64bits", "peexe", "signed", "idle", "known-distributor"], "times_submitted": 2, "tlsh": "T14B078C03F8A604F6C7FEE034815252217A71B4A583357BE74FA48A7A16A6FD4773E360", "ssdeep": "196608:XZTwNHl8x+J9o2XfsM84LHgLiWuB1kQgtgax0aZdOifNC:xw7TAILoUBPottqifA", "pe_info": {"imphash": "93a138801d9601e4c36e6274c8b9d111", "machine_type": 34404, "entry_point": 446144, "overlay": {"chi2": 8007.59, "filetype": "unknown", "entropy": 7.655909061431885, "offset": 17796096, "md5": "c0fd9e3226314086487988c216bfd818", "size": 10528}, "sections": [{"name": ".text", "chi2": 75753344.0, "virtual_address": 4096, "entropy": 5.78, "raw_size": 6339072, "flags": "rx", "virtual_size": 6338661, "md5": "75d52622230ca6d3360dbef720501a48"}, {"name": ".rdata", "chi2": 206841744.0, "virtual_address": 6344704, "entropy": 5.32, "raw_size": 5762560, "flags": "r", "virtual_size": 5762528, "md5": "7685c79aa3631c10ab52723d35eb535b"}, {"name": ".data", "chi2": 23887518.0, "virtual_address": 12107776, "entropy": 4.95, "raw_size": 424960, "flags": "rw", "virtual_size": 671624, "md5": "d3e754c7bcf7b8e56179682f124e6b45"}, {"name": "/4", "chi2": 28570.0, "virtual_address": 12779520, "entropy": 4.83, "raw_size": 512, "flags": "r", "virtual_size": 281, "md5": "28a3e9c96b9bb43e6541a26c8f68899b"}, {"name": "/19", "chi2": 3853.1, "virtual_address": 12783616, "entropy": 8.0, "raw_size": 859136, "flags": "r", "virtual_size": 858951, "md5": "f7e470bdf5394285c8636ca1c660338b"}, {"name": "/32", "chi2": 17828.02, "virtual_address": 13643776, "entropy": 7.94, "raw_size": 199168, "flags": "r", "virtual_size": 198931, "md5": "568ad6fb0758e526de216f0f78f0ffa5"}, {"name": "/46", "chi2": 1222.21, "virtual_address": 13844480, "entropy": 7.98, "raw_size": 32256, "flags": "r", "virtual_size": 32076, "md5": "ce5991b862de83980fe74d159425e4f0"}, {"name": "/63", "chi2": 608.95, "virtual_address": 13877248, "entropy": 8.0, "raw_size": 101376, "flags": "r", "virtual_size": 101060, "md5": "f154d7a19d38aee5f26330529a3d829d"}, {"name": "/80", "chi2": 110463.0, "virtual_address": 13979648, "entropy": 0.74, "raw_size": 512, "flags": "r", "virtual_size": 42, "md5": "56d08c10aa9e5c0c3680f67f8992b3d4"}, {"name": "/99", "chi2": 3551.35, "virtual_address": 13983744, "entropy": 8.0, "raw_size": 1450496, "flags": "r", "virtual_size": 1450035, "md5": "7e2a9bd03b3773ec5409ac3be1cdc628"}, {"name": "/112", "chi2": 3944.84, "virtual_address": 15437824, "entropy": 8.0, "raw_size": 822272, "flags": "r", "virtual_size": 821904, "md5": "46ddd05dd78bb72c1874c966ab289047"}, {"name": "/124", "chi2": 80849.45, "virtual_address": 16261120, "entropy": 7.8, "raw_size": 266752, "flags": "r", "virtual_size": 266534, "md5": "0dc5db42e56e38eaaa9363858b6216d3"}, {"name": ".idata", "chi2": 93494.16, "virtual_address": 16531456, "entropy": 3.67, "raw_size": 1536, "flags": "rw", "virtual_size": 1184, "md5": "5a91d45f36e24b9cbd499222d267dcbf"}, {"name": ".reloc", "chi2": 1495438.62, "virtual_address": 16535552, "entropy": 5.45, "raw_size": 267776, "flags": "r", "virtual_size": 267518, "md5": "68d0fe5de42c321137eea9706e883052"}, {"name": ".symtab", "chi2": 13868011.0, "virtual_address": 16805888, "entropy": 5.41, "raw_size": 1266176, "flags": "r", "virtual_size": 1265983, "md5": "f0b070d427eefa9f03ab49a9a0670206"}], "import_list": [{"library_name": "kernel32.dll", "imported_functions": ["AddVectoredExceptionHandler", "CloseHandle", "CreateEventA", "CreateIoCompletionPort", "CreateThread", "DuplicateHandle", "ExitProcess", "FreeEnvironmentStringsW", "GetConsoleMode", "GetEnvironmentStringsW", "GetProcAddress", "GetProcessAffinityMask", "GetQueuedCompletionStatusEx", "GetStdHandle", "GetSystemDirectoryA", "GetSystemInfo", "GetThreadContext", "LoadLibraryA", "LoadLibraryW", "OpenProcess", "PostQueuedCompletionStatus", "ProcessIdToSessionId", "QueryFullProcessImageNameA", "ResumeThread", "SetConsoleCtrlHandler", "SetErrorMode", "SetEvent", "SetProcessPriorityBoost", "SetThreadContext", "SetUnhandledExceptionFilter", "SetWaitableTimer", "SuspendThread", "SwitchToThread", "VirtualAlloc", "VirtualFree", "VirtualQuery", "WaitForMultipleObjects", "WaitForSingleObject", "WriteConsoleW", "WriteFile"]}]}, "type_extension": "exe", "filecondis": {"raw_md5": "2e6c075624f9e7a4f5d7d902fef7b19e", "dhash": "707a3c3c2e374600"}, "reputation": 0, "sha1": "c60d529a802046e447eadbae5c6aaf9bbf746322", "sandbox_verdicts": {"Zenbox": {"category": "harmless", "malware_classification": ["CLEAN"], "sandbox_name": "Zenbox", "confidence": 98}}, "last_submission_date": 1741706765, "unique_sources": 2, "last_analysis_date": 1753258148, "type_tags": ["executable", "windows", "win32", "pe", "peexe"], "known_distributors": {"distributors": ["Microsoft"], "filenames": ["googet.exe"], "products": ["windows-sql-cloud-sql-2017-web-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2016-standard-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2017-standard-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2019-web-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2022-web-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2016-standard-windows-2016-dc-v20241010", "windows-cloud-windows-server-2019-dc-v20241010", "windows-sql-cloud-sql-2019-web-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2022-standard-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2019-standard-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2017-standard-windows-2016-dc-v20241010", "windows-sql-cloud-sql-2019-enterprise-windows-2019-dc-v20241010", "windows-cloud-windows-server-2022-dc-v20241010", "windows-sql-cloud-sql-2017-web-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2016-web-windows-2016-dc-v20241010", "windows-sql-cloud-sql-2022-web-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2017-express-windows-2016-dc-v20241010", "windows-cloud-windows-server-2016-dc-v20241010", "windows-sql-cloud-sql-2019-enterprise-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2019-standard-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2017-enterprise-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2017-express-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2017-enterprise-windows-2022-dc-v20241010", "windows-sql-cloud-sql-2017-standard-windows-2019-dc-v20241010", "windows-cloud-windows-server-2022-dc-core-v20241010", "windows-cloud-windows-server-2019-dc-core-v20241010", "windows-sql-cloud-sql-2017-web-windows-2016-dc-v20241010", "windows-sql-cloud-sql-2017-enterprise-windows-2016-dc-v20241010", "windows-sql-cloud-sql-2016-web-windows-2019-dc-v20241010", "windows-sql-cloud-sql-2022-standard-windows-2022-dc-v20241010"], "data_sources": ["HashDB"]}, "total_votes": {"harmless": 0, "malicious": 0}, "md5": "2a9a6165b3431295af5de41655497443", "threat_severity": {"version": 5, "threat_severity_level": "SEVERITY_NONE", "threat_severity_data": {}, "last_analysis_date": "1718412419", "level_description": "No severity score data"}, "authentihash": "9b0669effaca9634de8068abc0f36170af6166e246eee6af5652c0177df1bd48", "magic": "PE32+ executable (console) x86-64 (stripped to external PDB), for MS Windows", "vhash": "0170f7555d54547474747az28!z", "sha256": "791d0fa941c37457973f04d12263d01ca5c480e5bfc795f025e79ac96e025af5", "trid": [{"file_type": "Win64 Executable (generic)", "probability": 48.7}, {"file_type": "Win16 NE executable (generic)", "probability": 23.3}, {"file_type": "OS/2 Executable (generic)", "probability": 9.3}, {"file_type": "Generic Win/DOS Executable", "probability": 9.2}, {"file_type": "DOS Executable Generic", "probability": 9.2}], "last_modification_date": 1753265375, "downloadable": true, "magika": "PEBIN", "gti_assessment": {"threat_score": {"value": 0}, "contributing_factors": {"legitimate_software": true, "gti_confidence_score": 0}, "verdict": {"value": "VERDICT_BENIGN"}, "severity": {"value": "SEVERITY_NONE"}, "description": "This indicator is benign. It is associated with a well-known and trusted software distributor and likely poses no threat."}}, "sandboxes_data": {"VirusTotal Jujubox": null}, "related_mitre_tactics": [{"id": "TA0011", "name": "Command and Control"}, {"id": "TA0005", "name": "Defense Evasion"}, {"id": "TA0002", "name": "Execution"}, {"id": "TA0003", "name": "Persistence"}, {"id": "TA0004", "name": "Privilege Escalation"}, {"id": "TA0007", "name": "Discovery"}], "widget_link": null, "widget_html":  null, "is_risky": false, "execution_status": "success"}}]
```



#### Enrich IOCs
Use the Enrich IOCs action to enrich IOCs with information from Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOC Type|The type of the IOC to enrich.|False|List|Filehash|
|IOCs|A comma-separated list of IOCs for which to ingest data.|True|String||
|Widget Theme|The theme of the augmented widget.|False|List|Chronicle|



##### JSON Results
```json
{"iocs":[{"identifier":"9498FF82A64FF445398C84xxxxxxxxxx","details":{"attributes":{"type_description":"Win32 EXE","tlsh":"T1DB44CF267660D833D0DF94316C75C3F9673BFC2123215A6B6A4417699E30xxxxxxxxxx","vhash":"025056657d755510804011z9005b9zxxxxxxxxxx","exiftool":{"SubsystemVersion":"5.1","LinkerVersion":"10.0","ImageVersion":"0.0","ProductName":"ShellExtension","FileVersionNumber":"1.0.1.6","LanguageCode":"English (U.S.)","InternalName":"ShellExtension","FileDescription":"WinMerge Shell Integration","ImageFileCharacteristics":"Executable, 32-bit","CharacterSet":"Unicode","InitializedDataSize":"199168","EntryPoint":"0x39b0","OriginalFileName":"ShellExtension","MIMEType":"application/octet-stream","Subsystem":"Windows GUI","FileVersion":"1.0.1.6","TimeStamp":"2014:09:17 10:34:37+00:00","FileType":"Win32 EXE","PEType":"PE32","FileFlagsMask":"0x003f","ProductVersion":"1.0.1.6","UninitializedDataSize":"0","OSVersion":"5.1","FileOS":"Windows NT 32-bit","LegalCopyright":"Copyright 2003-2013","MachineType":"Intel 386 or later, and compatibles","CompanyName":"MySQL, AB","CodeSize":"54784","FileSubtype":"0","ProductVersionNumber":"1.0.1.6","FileTypeExtension":"exe","ObjectFileType":"Executable application"},"trid":[{"file_type":"Win32 Executable MS Visual C++ (generic)","probability":48.8},{"file_type":"Win64 Executable (generic)","probability":16.4}],"creation_date":1410950077,"names":["ShellExtension","ZeuS_binary_9498FF82A64FF445398C84xxxxxxxxxx.exe"],"signature_info":{"product":"ShellExtension","internal name":"ShellExtension","copyright":"Copyright 2003-2013","original name":"ShellExtension","file version":"1.0.1.6","description":"WinMerge Shell Integration"},"last_modification_date":1645597878,"type_tag":"peexe","capabilities_tags":["win_token","win_files_operation"],"total_votes":{"harmless":3,"malicious":11},"size":254976,"popular_threat_classification":{"suggested_threat_label":"trojan.zbot/foreign","popular_threat_category":[{"count":31,"value":"trojan"}],"popular_threat_name":[{"count":17,"value":"zbot"}]},"authentihash":"ad56160b465f7bd1e7568640397f01fc4f8819ce6f0c1415690ecexxxxxxxxxx","times_submitted":8,"last_submission_date":1572934476,"meaningful_name":"ShellExtension","downloadable":true,"sigma_analysis_summary":{"Sigma Integrated Rule Set (GitHub)":{"high":2,"medium":0,"critical":0,"low":28}},"sandbox_verdicts":{"Zenbox":{"category":"harmless","confidence":1,"sandbox_name":"Zenbox","malware_classification":["CLEAN"]},"VirusTotal ZenBox":{"category":"harmless","confidence":1,"sandbox_name":"VirusTotal ZenBox","malware_classification":["CLEAN"]},"Tencent HABO":{"category":"malicious","sandbox_name":"Tencent HABO","malware_classification":["MALWARE"]}},"sha256":"8b2e701e91101955c73865589a4c72999aeabc11043f712e05fdb1xxxxxxxxxx","type_extension":"exe","tags":["idle","runtime-modules"],"last_analysis_date":1645581939,"unique_sources":8,"first_submission_date":1411582812,"sha1":"36f9ca40b3ce96fcee1cf1d4a72229xxxxxxxxxx","ssdeep":"61xx:Gz90qLc1zR98hUb4UdjzEwG+vqAWiR4EXePxxxxxxxxxx:Gz90qLc1lWhUbhVqxxxxxxxxxx","md5":"9498FF82A64FF445398C84xxxxxxxxxx","pe_info":{"resource_details":[{"lang":"ENGLISH US","entropy":3.271855354309082,"chi2":17094.91796875,"filetype":"Data","sha256":"851381c684c9f0c7b8cb7d0fb0cdf9837b6466b9923bebe0afdccbxxxxxxxxxx","type":"RT_DIALOG"},{"lang":"ENGLISH US","entropy":3.3894574642181396,"chi2":59740.10546875,"filetype":"Data","sha256":"a24783298e931e7949670435824fec4c4b4003f5d5d65f06fe1dcd6655df36ff","type":"RT_VERSION"}],"rich_pe_header_hash":"fa4dbca9180170710b3c24xxxxxxxxxx","imphash":"d7584447a5c5ca9b4a5594xxxxxxxxxx","compiler_product_versions":["[C++] VS2010 SP1 build 40219 count=36","[ASM] VS2010 SP1 build 40219 count=19","[ C ] VS2010 SP1 build 40219 count=110","[IMP] VS2008 SP1 build 30729 count=21","[---] Unmarked objects count=197","id: 175, version: 40219 count=1","[RES] VS2010 SP1 build 40219 count=1","[LNK] VS2010 SP1 build 40219 count=1"],"resource_langs":{"RUSSIAN":1,"ENGLISH US":6},"machine_type":332,"timestamp":1410950077,"debug":[{"codeview":{"age":127,"guid":"a996e137-27e8-4bb8-982f-4dxxxxxxxxxx","name":"H:\\\\generalise\\\\backgroun\\\\device\\\\rpt.pdb","signature":"RSDS"},"offset":145192,"type_str":"IMAGE_DEBUG_TYPE_CODEVIEW","timestamp":"Wed Sep 17 10:34:37 2014","type":2,"size":63}],"resource_types":{"RT_BITMAP":2,"RT_MENU":1,"RT_DIALOG":2,"RT_VERSION":1,"RT_MANIFEST":1},"sections":[{"name":".reloc","chi2":552797.69,"virtual_address":"270xxx","entropy":3.88,"raw_size":6656,"flags":"r","virtual_size":6200,"md5":"4be0d54241ec8f62e48c4xxxxxxxxxxx"}],"import_list":[{"library_name":"USER32.dll","imported_functions":["SetFocus","GetMessageA"]},{"library_name":"WINSPOOL.DRV","imported_functions":["EnumPrintersA","GetPrinterDriverA"]}],"entry_point":14768},"magic":"PE32 executable for MS Windows (GUI) Intel 80386 32-bit","last_analysis_stats":{"harmless":0,"type-unsupported":4,"suspicious":0,"confirmed-timeout":0,"timeout":0,"failure":1,"malicious":58,"undetected":12},"last_analysis_results":{"Bkav":{"category":"malicious","engine_name":"Bkav","engine_version":"1.3.0.9899","result":"W32.AIDetect.malware2","method":"blacklist","engine_update":"20220222"},"Lionic":{"category":"malicious","engine_name":"Lionic","engine_version":"4.2","result":"Trojan.Win32.Zbot.l!c","method":"blacklist","engine_update":"20220223"}},"reputation":-52,"sigma_analysis_stats":{"high":2,"medium":0,"critical":0,"low":28}},"type":"file","id":"8b2e701e91101955c73865589a4c72999aeabc11043f712e05fdb1xxxxxxxxxx","links":{"self":"https://www.virustotal.com/api/v3/files/8b2e701e91101955c73865589a4c72999aeabc11043f712e05fdb1xxxxxxxxxx"},"widget_url":"https://www.virustotal.com/ui/widget/html/OGIyZTcwMWU5MTEwMTk1NWM3Mzg2NTU4OWE0YzcyOTk5YWVhYmMxMTA0M2Y3MTJlMDVmZGIxYzE3YzRhYjE5YXx8ZmlsZXx8eyJiZDEiOiAiIzRkNjM4NSIsICJiZzEiOiAiIzMxM2Q1YSIsICJiZzIiOiAiIzIyMmM0MiIsICJmZzEiOiAiI2ZmZmZmZiIsICJ0eXBlIjogImRlZmF1bHQifXx8ZnVsbHx8Zm91bmR8fDE2NDYyMjI5ODd8fDZmOGFiODI3NzMzMTMxNjU2NTU2ZGE0ZmM3MmNmOThmZGY1ODRjNjNmMGU0OWFiMTlhMTBhOGZiZxxxxxxxxxx","widget_html":"<!DOCTYPE html><html><head></head><body></body></html>"}},{"identifier":"5.45.xx.xxx","details":{"attributes":{"regional_internet_registry":"RIPE NCC","jarm":"2ad2ad20d2ad2ad22c2ad2ad2ad2ad8e917db1de9d33002d7077xxxxxxxxxx","network":"5.45.64.xx/xx","last_https_certificate_date":1627256264,"tags":[],"country":"NL","as_owner":"Scalaxy B.V.","last_analysis_stats":{"harmless":72,"malicious":8,"suspicious":1,"undetected":9,"timeout":0},"asn":58061,"whois_date":1614359729,"last_analysis_results":{"0xSI_f33d":{"category":"undetected","result":"unrated","method":"blacklist","engine_name":"0xSI_f33d"},"Armis":{"category":"harmless","result":"clean","method":"blacklist","engine_name":"Armis"}},"reputation":-96,"last_modification_date":1646176786,"total_votes":{"harmless":0,"malicious":11},"last_https_certificate":{"size":1472,"public_key":{"rsa":{"key_size":2048,"modulus":"00aa8b74f0cc92a85ed4d515abef751a22fd65f2b6b0d33239040a99c65f322f3e833c77540a15ee31dabbd2889dd710ff9d8ccd3b9ea454ca87761cd9ff8a383806986461f8ff764a1202a5ebfb09995cbf40cc11eb2514529704744e6c97a872cde728e278fb140eba3c3aaf60644c8d75fd0048bb506f9b7314e33690f3514598ee45dd366c30a94d6178af91c2784872c162233c66659cea675f22f47752e0877ba5b12a3d800d2e2510d3cc1222c226cee2b85852a7e02da1de2718c746560f3ae05bc6f2d7f1cd6fcdbe37318fc7ddd19ae3486c5f3293946c068735e843fa8467199456d4725ac0b23fc4e0b7b9d3f51c0e16b27542d250xxxxxxxxxxx","exponent":"010001"},"algorithm":"RSA"},"thumbprint_sha256":"406ac0efb0ef67de743b1ab0f4e0352564a7d5ebbd71e3a883c06xxxxxxxxxxx","tags":[],"cert_signature":{"signature":"48ae0d5d0eb411e56bd328b93c7212c72fd21785070648e11d9ae2b80386711699978e650eafa233d234671b87c8134c1c38c59f702518ddebdc7849dc512e0158941507970ab3ab93788d27df728d727d7f9d28ed358abb145fb24803d0eeab04687ae07c7f1d3176374367efc000bd26d3cfc0659e54826ea2dfa2366d7bd9e8ed3bd2ff8a26898b37fadea198f93de8cf3ae3d703513bc0638f7b411d8eda9a3ac9a7510d7bfe553592792d10f8b2c255bc4a05c8c6bfbdb8def045dc754b39c9b89d2a5140818622760eb116abf6fd0a5798c1e274fe56a056ed21f419a6873d314c15238a398d8049b5ecc1ca003d0a07a989a710d137e4fxxxxxxxxxxx","signature_algorithm":"sha256RSA"},"validity":{"not_after":"2021-08-06 23:59:59","not_before":"2020-08-06 00:00:00"},"version":"V3","extensions":{"certificate_policies":["1.3.6.1.4.1.64xx.1.2.x.x","2.23.1xx.1.2.x"],"extended_key_usage":["serverAuth","clientAuth"],"authority_key_identifier":{"keyid":"8d8c5ec454ad8ae177e99bf99b05e1xxxxxxxxxx"},"subject_alternative_name":["y2y-panel.xyz","www.y2y-panel.xyz"],"tags":[],"subject_key_identifier":"4f6429eaccd761eca91d9120b004f9xxxxxxxxxx","key_usage":["ff"],"1.3.6.1.4.1.111xx.2.x.x":"0481f200f00075007d3ef2f88fff88556824c2c0ca9e5289792bcxxxxxxxxxxx","CA":true,"ca_information_access":{"CA Issuers":"http://crt.sectigo.com/SectigoRSADomainValidationSecureServerCA.crt","OCSP":"http://ocsp.sectigo.com"}},"signature_algorithm":"sha256RSA","serial_number":"248562d360bcc919bb9788xxxxxxxxxx","thumbprint":"f9aae62cc9262302e45d94fcc512dxxxxxxxxxxx","issuer":{"C":"GB","ST":"Greater Manchester","CN":"Sectigo RSA Domain Validation Secure Server CA","O":"Sectigo Limited","L":"Salford"},"subject":{"CN":"y2y-panel.xyz"}},"continent":"EU","whois":"NetRange: 5.0.0.0 - 5.255.255.255\\nCIDR: 5.0.0.0/8\\nNetName: RIPE-5\\nNetHandle: NET-5-0-0-0-1\\nParent: ()\\nNetType: Allocated to RIPE NCC\\nOriginAS: \\nOrganization: RIPE Network Coordination Centre (RIPE)\\nRegDate: 2010-11-30\\nUpdated: 2010-12-13\\nComment: These addresses have been further assigned to users in\\nComment: the RIPE NCC region. Contact information can be found in\\nComment: the RIPE database at http://www.ripe.net/whois\\nRef: https://rdap.arin.net/registry/ip/5.0.0.0\\nResourceLink: https://apps.db.ripe.net/search/query.html\\nResourceLink: whois.ripe.net\\nOrgName: RIPE Network Coordination Centre\\nOrgId: RIPE\\nAddress: P.O. Box 10096\\nCity: Amsterdam\\nStateProv: \\nPostalCode: 1001EB\\nCountry: NL\\nRegDate: \\nUpdated: 2013-07-29\\nRef: https://rdap.arin.net/registry/entity/RIPE\\nReferralServer: whois://whois.ripe.net\\nResourceLink: https://apps.db.ripe.net/search/query.html\\nOrgAbuseHandle: ABUSE3850-ARIN\\nOrgAbuseName: Abuse Contact\\nOrgAbusePhone: +31205354444 \\nOrgAbuseEmail: abuse@ripe.net\\nOrgAbuseRef: https://rdap.arin.net/registry/entity/ABUSE3850-ARIN\\nOrgTechHandle: RNO29-ARIN\\nOrgTechName: RIPE NCC Operations\\nOrgTechPhone: +31 20 535 4444 \\nOrgTechEmail: hostmaster@ripe.net\\nOrgTechRef: https://rdap.arin.net/registry/entity/RNO29-ARIN\\ninetnum: 5.45.76.0 - 5.45.79.255\\nnetname: CLOUD-NETWORK-NL\\nremarks: INFRA-AW\\ndescr: ********************************************************\\ndescr: * As ISP we provide IP transit and bandwidth services.\\ndescr: *\\ndescr: * Those services are self managed by our customers\\ndescr: * therefore, we are not using this IP space ourselves\\ndescr: * and it could be assigned to various end customers.\\ndescr: *\\ndescr: * In case of issues related with SPAM, Fraud, Phishing\\ndescr: * DDoS, port scans or others, feel free to contact us\\ndescr: * with relevant info. Abuse email: abuse@ispiria.net\\ndescr: ********************************************************\\ncountry: NL\\norg: ORG-ISPR1-RIPE\\nadmin-c: ISPR1-RIPE\\ntech-c: ISPR1-RIPE\\nstatus: ASSIGNED PA\\nmnt-by: ISPIRIA-MNT\\nmnt-routes: serverius-mnt\\nremarks: ISPIRIA Networks Ltd.\\nremarks: Technical issues: support@ispiria.net\\nremarks: Services request: sales@ispiria.net\\nremarks: Abuse departament: abuse@ispiria.net\\nremarks: Corporate web site: https://ispiria.net\\ncreated: 2013-04-24T11:28:55Z\\nlast-modified: 2019-09-26T09:25:43Z\\nsource: RIPE\\norganisation: ORG-ISPR1-RIPE\\norg-name: ISPIRIA Networks Ltd\\norg-type: OTHER\\naddress: 100 Johnny Grief Dr., Belize city, Belize\\nabuse-c: ACRO15876-RIPE\\nmnt-ref: MNT-3NT\\nmnt-by: ISPIRIA-MNT\\ncreated: 2018-05-03T08:12:15Z\\nlast-modified: 2020-05-22T20:10:44Z\\nsource: RIPE # Filtered\\nperson: James Dickins\\naddress: 100 Johnny Grief Dr., Belize city, Belize\\nphone: +1 (866) 9558855\\nnic-hdl: ISPR1-RIPE\\nmnt-by: ISPIRIA-MNT\\ncreated: 2018-05-03T08:24:33Z\\nlast-modified: 2020-05-19T10:18:30Z\\nsource: RIPE\\nroute: 5.45.76.0/22\\norigin: AS58061\\nmnt-by: ISPIRIA-MNT\\ncreated: 2020-04-24T10:37:38Z\\nlast-modified: 2020-04-24T10:37:38Z\\nsource: RIPE\\n"},"type":"ip_address","id":"5.45.xx.xxx","links":{"self":"https://www.virustotal.com/api/v3/ip_addresses/5.45.xx.xxx"},"widget_url":"https://www.virustotal.com/ui/widget/html/NS40NS43OS4xNXx8aXBfYWRkcmVzc3x8eyJiZDEiOiAiIzRkNjM4NSIsICJiZzEiOiAiIzMxM2Q1YSIsICJiZzIiOiAiIzIyMmM0MiIsICJmZzEiOiAiI2ZmZmZmZiIsICJ0eXBlIjogImRlZmF1bHQifXx8ZnVsbHx8Zm91bmR8fDE2NDYyMjMyMzd8fDhhMDM4MmE2MzQwYzk2NjEwZTM3MTc0YzI5MjIyM2M3MmNiOWJhOGZmMzMzY2Q2MjYxMGExZGE2Mxxxxxxxxxx","widget_html":"<!DOCTYPE html><html><head></head><body></body></html>"}},{"identifier":"test.com","details":{"attributes":{"last_dns_records":[{"type":"NS","value":"dns2.registrar-servers.com","ttl":3600},{"rname":"hostmaster.test.com","retry":7200,"value":"dns101.registrar-servers.com","minimum":86400,"refresh":28800,"expire":604800,"ttl":10800,"serial":1641811000,"type":"SOA"},{"type":"NS","value":"dns102.registrar-servers.com","ttl":3600}],"jarm":"2ad2ad0002ad2ad0002ad2ad2ad2ad83c2e51da709c877942c9xxxxxxxxxxx","whois":"Creation Date: 2013-12-06T02:41:09Z\\nDNSSEC: unsigned\\nDomain Name: test.COM\\nDomain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited\\nDomain Status: redemptionPeriod https://icann.org/epp#redemptionPeriod\\nName Server: DNS101.REGISTRAR-SERVERS.COM\\nName Server: DNS102.REGISTRAR-SERVERS.COM\\nRegistrar Abuse Contact Email: abuse@namecheap.com\\nRegistrar Abuse Contact Phone: +1.6613102107\\nRegistrar IANA ID: 1068\\nRegistrar URL: http://www.namecheap.com\\nRegistrar WHOIS Server: whois.namecheap.com\\nRegistrar: NameCheap, Inc.\\nRegistry Domain ID: 1838126490_DOMAIN_COM-VRSN\\nRegistry Expiry Date: 2021-12-06T02:41:09Z\\nUpdated Date: 2022-01-17T02:52:13Z","last_https_certificate_date":1638686165,"tags":[],"popularity_ranks":{"Cisco Umbrella":{"timestamp":1580139364,"rank":248453}},"last_dns_records_date":1641811567,"last_analysis_stats":{"harmless":78,"malicious":3,"suspicious":0,"undetected":9,"timeout":0},"favicon":{"raw_md5":"8613ef0ac2bc8923a85a6fxxxxxxxxxx","dhash":"1b6799xxxxxxxxxx"},"whois_date":1645002553,"reputation":0,"registrar":"NameCheap, Inc.","last_analysis_results":{"CMC Threat Intelligence":{"category":"harmless","result":"clean","method":"blacklist","engine_name":"CMC Threat Intelligence"},"Snort IP sample list":{"category":"harmless","result":"clean","method":"blacklist","engine_name":"Snort IP sample list"}},"last_update_date":1642387933,"last_modification_date":1646195427,"creation_date":1386297669,"last_https_certificate":{"public_key":{"rsa":{"key_size":2048,"modulus":"00c897b145bf71ae3b27c285283607152a23f2385635a3ca6bcede7f610cf832bebd41eb0c4afc0f0f9cc176cce3307d4dc9dfe6c56797f2ff346604a972c293f108b17711a435bc62a7a33093e2b1290e1dd579b3b14ef73c13c7148e34020b9411413f7b15db88dbec018d8556e9cfe9fa10b0966910094727f323e5fefeb60b208201af27aa114a60867b0863126d2ec36fff43d60b9af2853001c8775e98ccdc7478a5d016a7448af3f0bee097461ecefd3eba7dfc9d9ff73dda8a91e19faa075a9243286273affb8815c3bc80d515e4421a9313ad8dbefb9a0750ac73cfc82708b2a471eb33eac4b0f4ec3cec02cdb309600882d4b49d3d98adxxxxxxxxxxx","exponent":"010001"},"algorithm":"RSA"},"thumbprint_sha256":"ae10b906e8eb7a595e9bca59c88a322f1888edeee24a642a64c7c1xxxxxxxxxx","tags":[],"signature_algorithm":"sha256RSA","subject":{"CN":"raa.namecheap.com"},"validity":{"not_after":"2022-11-29 23:59:59","not_before":"2021-11-04 00:00:00"},"version":"V3","extensions":{"certificate_policies":["1.3.6.1.4.1.64xx.1.2.x.x","2.23.1xx.1.2.x"],"extended_key_usage":["serverAuth","clientAuth"],"tags":[],"subject_alternative_name":["raa.namecheap.com","www.raa.namecheap.com"],"authority_key_identifier":{"keyid":"8d8c5ec454ad8ae177e99bf99b05e1xxxxxxxxxx"},"ca_information_access":{"CA Issuers":"http://crt.sectigo.com/SectigoRSADomainValidationSecureServerCA.crt","OCSP":"http://ocsp.sectigo.com"},"subject_key_identifier":"604abb11b7ef0b58a5a444c1cf0814xxxxxxxxxx","key_usage":["ff"],"1.3.6.1.4.1.111xx.2.x.x":"0482016c016a00770046a555eb75fa912030b5a28969f4f37d11xxxxxxxxxxxx","CA":true},"cert_signature":{"signature_algorithm":"sha256RSA","signature":"06275db636f55c3d11f38ed2fe869cfc0d194533f2fa4ee48b790208f87db73bc92ede5f1629db743afc16341ee43f0ac0e44e16f86d70bd383c8f0cee927d4a53baea044996202a556efcef465ac718f448b7f90529976c536dddbfa37ea72b6fd2fd19701adc0503e24c58d01fee07a997fa419e9aebd85a720ac3a2be02de1ebb9d0fbfed3742f446eb2518305714b532b6fe3368ff05b28feeb10405c643239e1be57c69087b40c92736b06859e43d8963a1b53f0850b40417064ecdcf497ca71aba87047a7d137bea244d3fdf66cac1f0815b85ee010ae7c92d701dc04ead1c81fb3767dd09492e38d71556fc8e2faf4866a8d40e61297d7dxxxxxxxxxx"},"serial_number":"31d763c4fdab90f2875bd1xxxxxxxxxx","thumbprint":"004a44ff4929e5fd91538276fe45fbxxxxxxxxxx","issuer":{"C":"GB","L":"Salford","CN":"Sectigo RSA Domain Validation Secure Server CA","O":"Sectigo Limited","ST":"Greater Manchester"},"size":1608},"categories":{"Webroot":"Phishing and Other Frauds","Comodo Valkyrie Verdict":"media sharing","Forcepoint ThreatSeeker":"bot networks"},"total_votes":{"harmless":0,"malicious":0}},"type":"domain","id":"test.com","links":{"self":"https://www.virustotal.com/api/v3/domains/test.com"},"widget_url":"https://www.virustotal.com/ui/widget/html/bWFya29zc29sb21vbi5jb218fGRvbWFpbnx8eyJiZDEiOiAiIzRkNjM4NSIsICJiZzEiOiAiIzMxM2Q1YSIsICJiZzIiOiAiIzIyMmM0MiIsICJmZzEiOiAiI2ZmZmZmZiIsICJ0eXBlIjogImRlZmF1bHQifXx8ZnVsbHx8Zm91bmR8fDE2NDYyMjM0NDJ8fDI0OWZmZGZmNmE3N2JiNDg0ZWQ4MDlmNjk0ZjFhZmRhY2ZhYmVhMWJkOWVjMGNiMjJlZWRkOGM4xxxxxxxxxxx","widget_html":"<!DOCTYPE html><html><head></head><body></body></html>"}},{"identifier":"https://jsonlint.com/","details":{"attributes":{"favicon":{"raw_md5":"8edf857a9d7fec7adc627xxxxxxxxxxx","dhash":"000000xxxxxxxxxx"},"last_modification_date":1646031287,"times_submitted":196,"total_votes":{"harmless":0,"malicious":0},"threat_names":[],"last_submission_date":1646030550,"last_http_response_content_length":16063,"last_http_response_headers":{"transfer-encoding":"chunked","cf-cache-status":"HIT","vary":"Accept-Encoding","last-modified":"Tue, 01 Feb 2022 22:07:06 GMT","link":"</css/style-1.css>; rel=preload; as=style","report-to":{"endpoints":[{"url":"https:\\\\/\\\\/a.nel.cloudflare.com\\\\/report\\\\/v3?s=KOr5NdjXWyZnJBiC%2BUQgHNyK44r7irlJW8%2Fv3iQ7pEnLt4jQ9AWKR%2BNNdZhgxvQE0fibELaKi0SVhhyDZHGeNUAdiQSI%2BkOc5447gvdUdYH7fT8y2A%2FPANRd9nE60Q%3D%3D"}],"group":"cf-nel","max_age":604800},"date":"Mon, 28 Feb 2022 06:49:10 GMT","cf-ray":"6e47b620ab7a62fa-ORD","access-control-allow-origin":"*","expect-ct":"max-age=604800","report-uri":"https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct","nel":{"success_fraction":0,"report_to":"cf-nel","max_age":604800},"content-encoding":"br","strict-transport-security":"max-age=15768000","server":"cloudflare","connection":"keep-alive","cache-control":"max-age=14400","content-type":"text/html"},"reputation":0,"tags":[],"last_analysis_date":1646030550,"has_content":false,"first_submission_date":1494403073,"categories":{"Forcepoint ThreatSeeker":"information technology","Sophos":"information technology","alphaMountain.ai":"Information Technology","Comodo Valkyrie Verdict":"mobile communications","BitDefender":"computersandsoftware"},"last_http_response_content_sha256":"fb73ff6938ef4095b0be1b6e922b636bf612b67edd58a44d8d47c1xxxxxxxxxx","last_http_response_code":200,"last_final_url":"https://jsonlint.com/","trackers":{"Google Analytics":[{"url":"https://www.google-analytics.com/analytics.js","timestamp":1646030550,"id":"UA-69209117-1"}]},"url":"https://jsonlint.com/","title":"JSON Online Validator and Formatter - JSON Lint","last_analysis_stats":{"harmless":84,"malicious":0,"suspicious":0,"undetected":9,"timeout":0},"last_analysis_results":{"CMC Threat Intelligence":{"category":"harmless","result":"clean","method":"blacklist","engine_name":"CMC Threat Intelligence"},"Snort IP sample list":{"category":"harmless","result":"clean","method":"blacklist","engine_name":"Snort IP sample list"}},"html_meta":{"google-site-verification":["T1nWWoSoh2qccuR4z4J2MH9AuFVnl7vQHxxxxxxxxxx"],"description":["JSONLint is the free online validator and reformatter tool for JSON, a lightweight data-interchange format."],"viewport":["width=device-width,initial-scale=1"],"robots":["index"]},"outgoing_links":["https://jsonlint.memberful.com/checkout?plan=21158","https://dns-lookup.com/","http://www.crockford.com/","https://jsoncompare.com/","https://github.com/zaach/jsonlint","https://www.json.org/","https://www.github.com/circlecell/jsonlintdotcom","https://www.buysellads.com/buy/detail/266667/zone/1303970","https://randomkeygen.com/","https://jscompress.com/","https://validatejavascript.com/","http://zaa.ch/"]},"type":"url","id":"91ea0979b401289efe3c586df3275aebdd12dcdaf4c7c10b68b1cxxxxxxxxxxx","links":{"self":"https://www.virustotal.com/api/v3/urls/91ea0979b401289efe3c586df3275aebdd12dcdaf4c7c10b68b1cxxxxxxxxxxx"},"widget_url":null,"widget_html":null}}]}
```



#### Execute IOC Search
Use the Execute IOC Search action to run the IOC search in Google Threat Intelligence.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Query|A search query to execute, such as "crowdsourced_yara_rule:*apt* and p:3+ and fs:2d+".|True|String||
|Max Results To Return|The maximum number of results to return for every action run. The default value is 50. The maximum value is 200.|False|String|50|



##### JSON Results
```json
[{"id": "9c5xxxxxxxxxx", "type": "file", "links": {"self": "https://www.virustotal.com/api/v3/files/9c5xxxxxxxxxx"}, "attributes": {"trid": [{"file_type": "Android Package", "probability": 49}], "sha256": "9c5xxxxxxxxxx", "times_submitted": 59750, "type_extension": "apk", "reputation": 0, "sha1": "f7dxxxxxxxxxx", "meaningful_name": "Ludio_Player.apk", "last_analysis_date": 1740481863, "magika": "APK", "names": ["Ludio_Player.apk", "base.apk"], "type_tag": "android", "ssdeep": "19xxxx:mx3xxxxxxxxxx", "type_tags": ["executable", "mobile"], "vhash": "577xxxxxxxxxx", "last_analysis_results": {"Bkav": {"method": "blacklist", "engine_name": "Bkav", "engine_version": "2.0.0.1", "engine_update": "202xxxxx", "category": "undetected", "result": null}, "Lionic": {"method": "blacklist", "engine_name": "Lionic", "engine_version": "8.16", "engine_update": "202xxxxx", "category": "undetected", "result": null}}, "exiftool": {"ZipRequiredVersion": "20", "MIMEType": "application/zip", "ZipCRC": "0xaxxxxxxx", "FileType": "ZIP", "ZipCompression": "Deflated", "ZipUncompressedSize": "14208", "ZipCompressedSize": "3434", "FileTypeExtension": "zip", "ZipFileName": "AndroidManifest.xml", "ZipBitFlag": "0x0808", "ZipModifyDate": "2016:01:10 17:03:08"}, "permhash": "a0bxxxxxxxxxx", "threat_severity": {"version": 5, "threat_severity_level": "SEVERITY_NONE", "threat_severity_data": {"num_av_detections": 2}, "last_analysis_date": "1728081112", "level_description": "Severity NONE because the file has no Google antivirus detections and no bad network activity"}, "bundle_info": {"highest_datetime": "2016-01-10 17:03:08", "lowest_datetime": "2016-01-10 17:03:08", "num_children": 2100, "extensions": {"xml": 232, "dex": 1}, "file_types": {"XML": 232, "DEX": 1}, "type": "APK", "uncompressed_size": 28102995}, "tlsh": "T1Cxxxxxxxxxx", "downloadable": true, "md5": "544xxxxxxxxxx", "type_description": "Android", "unique_sources": 76, "last_modification_date": 1740482034, "filecondis": {"dhash": "000xxxxxxxxxx", "raw_md5": "e45xxxxxxxxxx"}, "size": 14267767, "total_votes": {"harmless": 0, "malicious": 0}, "first_submission_date": 1615438126, "available_tools": [], "main_icon": {"raw_md5": "470xxxxxxxxxx", "dhash": "c4dxxxxxxxxxx"}, "last_analysis_stats": {"malicious": 2, "suspicious": 0, "undetected": 66, "harmless": 0, "timeout": 1, "confirmed-timeout": 0, "failure": 0, "type-unsupported": 8}, "magic": "Java archive data (JAR)", "androguard": {"VTAndroidInfo": 2, "AndroidApplicationError": false, "MinSdkVersion": "21", "AndroguardVersion": "4.1.2", "Activities": ["com.mr.ludiop.activity.PlayerSplashActivity", "com.google.android.gms.common.api.GoogleApiActivity"], "certificate": {"Subject": {"DN": "CN:editor", "CN": "editor"}, "validto": "2115-12-17 08:03:09", "serialnumber": "231xxxxx", "thumbprint": "927xxxxxxxxxx", "validfrom": "2016-01-10 08:03:09", "Issuer": {"DN": "CN:editor", "CN": "editor"}}, "AndroidApplication": 1, "RiskIndicator": {"APK": {"DEX": 1, "SHARED LIBRARIES": 20}, "PERM": {"DANGEROUS": 2, "INTERNET": 1, "INSTANT": 2, "NORMAL": 4}}, "Services": ["com.google.android.gms.cast.framework.ReconnectionService", "com.google.android.gms.cast.framework.media.MediaNotificationService"], "AndroidVersionCode": "130xxxxx", "Package": "com.mr.ludiop", "AndroidVersionName": "2.0.0", "TargetSdkVersion": "30", "AndroidApplicationInfo": "APK", "Providers": ["androidx.core.content.FileProvider", "androidx.lifecycle.ProcessLifecycleOwnerInitializer"], "Receivers": ["com.google.android.gms.cast.framework.media.MediaIntentReceiver"], "StringsInformation": ["http://cablegratishd.com/"], "main_activity": "com.mr.ludiop.activity.PlayerSplashActivity", "intent_filters": {"Activities": {"com.mr.ludiop.iptvReader.MainIptvActivity": {"action": ["android.intent.action.VIEW"]}}, "Receivers": {"com.google.firebase.iid.FirebaseInstanceIdReceiver": {"action": ["com.google.android.c2dm.intent.RECEIVE"]}}}, "permission_details": {"android.permission.READ_EXTERNAL_STORAGE": {"permission_type": "dangerous"}}}, "last_submission_date": 1740481863, "tags": ["runtime-modules", "mysql-communication"], "gti_assessment": {"verdict": {"value": "VERDICT_UNDETECTED"}, "threat_score": {"value": 1}, "severity": {"value": "SEVERITY_NONE"}, "description": "This indicator did not match our detection criteria and there is currently no evidence of malicious activity."}}}]
```



#### Get ASM Entity Details
Use the Get ASM Entity Details action to obtain information about an Attack Surface Management (ASM) entity in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity ID|A comma-separated list of entity IDs for which to obtain details.|True|String||



##### JSON Results
```json
[{"Entity":"a52f8d9b78206d7eae64d0c8aa8e000000000x0x00000000xx00000x0xx0x0","EntityResult":{"uuid":"140e8ca8-XXXX-XXXX-XXXX-f40e3c32117e","dynamic_id":"Intrigue::Entity::Uri#http://name.name.com:1111","collection_name":"collection_name","alias_group":11111111,"aliases":["http://downloads.asd.com:2095"],"allow_list":false,"ancestors":[{"type":"Intrigue::Entity::Domain","name":"name.com"}],"category":"None","collection_naics":"None","confidence":"None","deleted":false,"deny_list":false,"details":{"asn":"None","ssl":false,"uri":"http://name.name.com:1111","code":"200","port":2095,"forms":false,"title":"UnauthorizedAccess","verbs":"None","cookies":[],"headers":["Connection:Keep-Alive","Keep-Alive:timeout=5,max=100","content-type:text/html;charset=UTF-8","content-length:1512","date:Wed,15Jan202503:54:20GMT","server:CaptchaServer"],"host_id":4907844,"net_geo":"US","scripts":["scripts"],"service":"http","auth.2fa":true,"auth.any":false,"dom_sha1":"XXXXXXXX95639b554051XXXXXXXX1dd931786e4","net_name":"NAMECHEAP-NET,US","protocol":"tcp","alt_names":[],"auth.ntlm":false,"generator":"None","auth.basic":false,"auth.forms":true,"ip_address":"111.11.111.11","favicon_md5":"None","fingerprint":[{"cpe":"cpe:2.3:a:roundcube:roundcube::","hide":false,"tags":["Email","COTS"],"type":"fingerprint","issues":[],"method":"godent","update":"","vendor":"vendor","product":"product","version":"","inference":false,"description":"RoundcubeRoundcube-CookiesMatch","match_logic":"any","unique_path":"http://name.name.com:1111/","positive_matches":[{"type":"content_cookies","regex":["(?i)roundcube_sessauth="],"condition":""},{"type":"content_cookies","regex":["(?i)roundcube_cookies="],"condition":""}]}],"geolocation":{"asn":{"asn":22612,"isp":"Namecheap,Inc.","name":"Namecheap,Inc.","organization":"Namecheap,Inc.","connection_type":"Corporate"},"city":"NewYork","postal":"10123","country":"UnitedStates","latitude":40.7128,"continent":"NorthAmerica","longitude":-74.006,"time_zone":"America/New_York","country_code":"US","continent_code":"NA"},"vuln_checks":["broken_link"],"api_endpoint":false,"cloud_hosted":false,"favicon_sha1":"None","domain_cookies":"None","redirect_chain":[{"to":"https://name.name.com:11111/","from":"http://name.name.com:11111/","step":1,"http_code":301}],"redirect_count":2,"cloud_providers":[],"hidden_original":"http://name.name.com:1111","extended_ciphers":[],"net_country_code":"None","protocol_detected":"http","screenshot_exists":true,"cloud_fingerprints":[],"response_data_hash":"csElooQm56RZAbbS4Edn8SOjDMkJxEau9Dwsy5gudZs=","extended_favicon_data":"None","extended_path_to_seed":[{"id":4908127,"_id":344062,"name":"http://name.name.com:1111","seed":false,"type":"Intrigue::Entity::Uri","_type":"Entity","hidden":false,"creates":[{"id":4907844,"_id":343779,"name":"111.11.111.11","seed":false,"type":"Intrigue::Entity::IpAddress","_type":"Entity","hidden":false,"creates":[{"id":4907799,"_id":343744,"name":"name.name.com","seed":false,"type":"Intrigue::Entity::DnsRecord","_type":"Entity","hidden":false,"creates":[{"id":1111111,"_id":11111,"name":"name.com","seed":true,"type":"Intrigue::Entity::Domain","_type":"Entity","hidden":false,"creates.verb":"queried","hidden_reason":"","creates.hidden":"false","creates.source_name":"source_name","creates.source_type":"source_type"}],"creates.verb":"enriched","hidden_reason":"","creates.hidden":"false","creates.source_name":"enrich/dns_record","creates.source_type":"self"}],"creates.verb":"queried","hidden_reason":"","creates.hidden":"false","creates.source_name":"source_name","creates.source_type":"source_type"}],"hidden_reason":""}],"extended_configuration":[{"hide":false,"name":"Authentication-Forms","task":[],"type":"content","issue":[],"result":{"bool_value":true,"list_value":"None","null_value":"NULL_VALUE","number_value":0,"string_value":"","struct_value":"None"}}],"extended_response_body":"extended_response_body","extended_screenshot_contents":"string","extended_browser_request_urls":["string"]},"details_file":"details_file","description":"None","first_seen":"2025-01-14T10:32:32.000Z","hidden":false,"last_seen":"2025-01-15T04:05:21.000Z","name":"http://name.name.com:1111","scoped":true,"scoped_reason":"allowlistmatch","seed":false,"source":"None","status":"None","task_results":[{"id":1111111,"name":"search_shodan_ranger_on_111.11.111.11","base_entity_name":"111.11.111.11","base_entity_type":"base_entity_type"}],"type":"type","uid":"a52f8d9b78206d7eae64d0c8aa8e000000000x0x00000000xx00000x0xx0x0","created_at":"2025-01-14T12:55:54.085Z","updated_at":"2025-01-14T00:00:00.000Z","collection_id":1111111,"elasticsearch_mappings_hash":"None","collection":"collection","collection_uuid":"XXXXXXXXX-60da-XXXX-a678-XXXXXXXXXXXXX","organization_uuid":"XXXXXXXXX-7202-XXXX-808b-XXXXXXXXXXXXX","collection_type":"collection_type","fingerprint":[{"cpe":"cpe:2.3:a:cpe:cpe::","hide":false,"tags":["Email"],"type":"type","issues":[],"method":"godent","update":"","vendor":"vendor","product":"product","version":"","inference":false,"description":"description","match_logic":"all","unique_path":"http://path.path.com:11111/","positive_matches":[{"type":"content_cookies","regex":["(?i)id="],"condition":""}],"local_icon_path":"/path/path/path.png"}],"summary":{"scoped":true,"issues":{"current_with_cve":0,"current_by_severity":{"0":0,"1":0,"2":0,"3":1,"4":0,"5":0},"all_time_by_severity":{"0":0,"1":0,"2":0,"3":1,"4":0,"5":0},"current_count":1,"all_time_count":1,"critical_or_high":false,"current_issue_cves":[]},"task_results":["search_shodan_ranger"],"screenshot_exists":true,"geolocation":{"city":"NewYork","country_code":"US","country_name":"None","latitude":40.7128,"longitude":-74.006,"asn":"None"},"http":{"code":200,"title":"UnauthorizedAccess","content":{"favicon_hash":"None","hash":"None","forms":false},"auth":{"any":false,"basic":false,"ntlm":false,"forms":true,"2fa":true}},"ports":{"tcp":[2095],"udp":[],"count":1},"network":{"name":"Namecheap,Inc.","asn":22612,"route":"None","type":"None"},"technology":{"cloud":false,"cloud_providers":[],"cpes":[{"cpe":"cpe:2.3:a:bootstrap:bootstrap::","detection_method":"boostrapcss"}],"technologies":["Bootstrap"],"technology_labels":["JavaScript"]},"vulns":{"current_count":0,"vulns":[]}},"tags":[],"id":1111111111,"enriched":true,"scoped_at":"2025-01-1503:54:19+0000","detail_string":"Fingerprint:GenericWebPanel;Roundcube;cPanelWebmail|Title:UnauthorizedAccess","enrichment_tasks":["enrich/uri","uri_browser_analysis_ferrum"],"generated_at":"2025-01-15T04:05:33Z"}}]
```



#### Get Graph Details
Use the Get Graph Details action to obtain detailed information about graphs in Google Threat Intelligence. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Graph ID|A comma-separated list of graph IDs for which to retrieve information.|True|String||
|Max Links To Return|The maximum number of links to return. The default value is 50.|True|String|50|



##### JSON Results
```json
[{"Entity": "g0cxxxxxxxxxx", "EntityResult": {"data": {"id": "g0cxxxxxxxxxx", "type": "graph", "links": {"self": "https://www.virustotal.com/api/v3/graphs/g0cxxxxxxxxxx"}, "attributes": {"position": {"y": 100, "x": 100, "scale": "2.5xxxxxxxxxx"}, "comments_count": 0, "private": false, "creation_date": 1541669403, "last_modified_date": 1541669403, "links": [{"connection_type": "itw_urls", "source": "f3bxxxxxxxxxx", "target": "relationships_itw_urls_f3bxxxxxxxxxx"}, {"connection_type": "itw_urls", "source": "relationships_itw_urls_f3bxxxxxxxxxx", "target": "2f6xxxxxxxxxx"}], "views_count": 17, "nodes": [{"index": 0, "entity_id": "f3bxxxxxxxxxx", "fx": 100, "fy": -100, "entity_attributes": {"type_tag": "peexe", "has_detections": true}, "text": "test.exe", "y": -100, "x": 100, "type": "file"}], "graph_data": {"version": "3.0.7"}}, "context_attributes": {"shared_with_me": false, "role": "viewer"}}}}]
```



#### Get Related Associations
Use the Get Related Associations action to get information about associations (reports, campaigns, IOC collections, malware families, software toolkits, vulnerabilities, threat actors) related to the provided entities in Google Threat Intelligence. Supported entities: IP, URL, Filehash, Hostname, Domain. Note: only MD5, SHA-1 and SHA-256 hashes are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Association Types|A comma-separated list of associations to return. Possible values: Report, Campaign, Collections, Malware Family, Vulnerability, Threat Actor. If no value is provided, the action returns all associations. Note: Reports are processed after all other associations are complete.|False|String|Report, Campaign, Collection, Malware Family, Vulnerability, Threat Actor|
|Create Entity|If selected, the action creates an entity for related Threat Actors, CVEs and Campaigns, linking it to the original entity. Note: Only CVE, Threat Actor and Campaign entities are created.|False|Boolean|false|
|Max Associations To Return|The maximum number of IOCs to return for every entity. Max: 1000.|False|String|50|



##### JSON Results
```json
[{"Entity":"8.8.8.8","EntityResult":{"malware-family":[{"id":"malware--f1a2b3c4-d5e6-7f8a-9b0c-d1e2f3a4b5c6","type":"collection","links":{"self":"https://www.virustotal.com/api/v3/collections/malware--f1a2b3c4-d5e6-7f8a-9b0c-d1e2f3a4b5c6"},"context_attributes":{"shared_with_me":false,"role":"observer"},"attributes":{"targeted_industries_tree":[{"industry_group":"Industrial & Chemical Sector","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Building & Development","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Academic Sector","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Power & Public Services","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Public Administration","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Medical Services","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Lodging & Tourism","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Law & Consulting Firms","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Production & Assembly","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Publishing & Broadcasting","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Petroleum Industry","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Consumer Goods Sales","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Information Technology","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Logistics & Transit","industry":null,"confidence":"verified","first_seen":null,"last_seen":null,"description":null,"source":null}],"exploitation_vectors":[],"summary_stats":{"first_submission_date":{"min":1747282975.0,"max":1754037707.0,"avg":1751290096.0},"last_submission_date":{"min":1756794484.0,"max":1758368897.0,"avg":1757770092.0},"files_detections":{"min":22.0,"max":41.0,"avg":30.545454545454547}},"threat_scape":[],"targeted_regions_hierarchy":[],"targeted_informations":[],"merged_actors":[],"is_content_translated":false,"source_regions_hierarchy":[],"workarounds":[],"alt_names_details":[{"value":"MalSentry (ThreatWatch)","description":null,"first_seen":null,"confidence":"provisional","last_seen":null},{"value":"AlteredCook (CyberSecure)","description":null,"first_seen":null,"confidence":"provisional","last_seen":null}],"risk_factors":[],"recent_activity_summary":[ 92,481,397,378,291,527,120,99,414,373,291,241,221,72 ],"version_history":[],"description":"COIN_DROP is a JavaScript-based backdoor that uses HTTP for command and control. Its capabilities include file transfers, filesystem management, registry editing, process listing,and extracting information from web browsers. The trojan can also execute arbitrary commands and files, triggered by hard-coded command-line arguments that map to its specific functions.","private":true,"tags":[],"origin":"Global Cybersecurity Analysts","affected_systems":[],"operating_systems":[{"value":"Microsoft OS","description":null,"first_seen":null,"confidence":"provisional","last_seen":null}],"motivations":[],"last_modification_date":1758240000,"top_icon_md5":[ "7e01d0c3c9f5e7af77fc63cc50e1c70e","938ce3e8c96440c117cfcaaf278378db","11bed8401bdab09f8bbe8ee1daef23b5" ],"ip_addresses_count":0,"domains_count":4,"tags_details":[],"last_seen_details":[{"value":"2025-09-16T10:29:00Z","description":null,"first_seen":null,"confidence":"provisional","last_seen":null}],"name":"COIN_DROP","collection_links":[],"available_mitigation":[],"recent_activity_relative_change":-0.6648218029350105,"detection_names":[],"last_seen":1758018540,"files_count":11,"creation_date":1758143476,"collection_type":"malware-family","mitigations":[],"references_count":0,"urls_count":0,"autogenerated_tags":[ "nsis" ],"malware_roles":[{"value":"Remote Access Trojan","description":null,"first_seen":null,"confidence":"provisional","last_seen":null}],"targeted_regions":[],"technologies":[],"alt_names":[ "AlteredCook (CyberSecure)","MalSentry (ThreatWatch)" ],"targeted_industries":[],"intended_effects":[],"capabilities":[{"value":"Utilizes network sockets for communication","description":"Is able to communicate via network sockets.","first_seen":null,"confidence":"provisional","last_seen":null},{"value":"Locates files on the system","description":"Can search for or identify specific files, or utilizes APIs for resource location.","first_seen":null,"confidence":"provisional","last_seen":null},{"value":"Opens a listening port for connections","description":"Can listen on a network port to establish TCP or UDP server functions, or uses APIs for this purpose.","first_seen":null,"confidence":"provisional","last_seen":null},{"value":"Injects code into other running processes","description":"Is capable of injecting code into another process or uses APIs associated with this technique.","first_seen":null,"confidence":"provisional","last_seen":null}],"status":"PROCESSED","field_sources":[],"subscribers_count":0,"first_seen_details":[],"vendor_fix_references":[],"counters":{"files":11,"domains":4,"ip_addresses":0,"urls":0,"iocs":15,"subscribers":0,"attack_techniques":1}}}],"report":[{"id":"report--ob-10000001","type":"collection","links":{"self":"https://www.virustotal.com/api/v3/collections/report--ob-10000001"},"attributes":{"version_history":[],"attacking_ease":"","report_type":"Malware Profile","is_content_translated":false,"name":"Ransomware Profile [P-Variant]","collection_links":[],"risk_factors":[],"report_id":"ob-10000001","subscribers_count":0,"last_seen_details":[],"report_confidence":"","ip_addresses_count":0,"targeted_regions":[],"top_icon_md5":[ "e5a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5" ],"intended_effects":[],"targeted_regions_hierarchy":[],"risk_rating":"","targeted_industries_tree":[{"industry_group":"Retail","industry":null,"confidence":"possible","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Hospitality","industry":null,"confidence":"possible","first_seen":null,"last_seen":null,"description":null,"source":null},{"industry_group":"Financial Services","industry":null,"confidence":"possible","first_seen":null,"last_seen":null,"description":null,"source":null}],"affected_systems":[ "Users / Workstation","Users / Application and Software / Operating System (OS)","Users/Application and Software" ],"summary_stats":{"first_submission_date":{"min":1458773633.0,"max":1458773633.0,"avg":1458773633.0},"last_submission_date":{"min":1762607579.0,"max":1762607579.0,"avg":1762607579.0},"files_detections":{"min":68.0,"max":68.0,"avg":68.0}},"tmh_accuracy_ranking":"","capabilities":[],"domains_count":0,"analyst_comment":"","workarounds":[],"author":"","mitigations":[],"detection_names":[],"alt_names_details":[],"status":"COMPUTED","autogenerated_tags":[],"private":true,"recent_activity_summary":[ 10,4,8 ],"creation_date":1460130953,"exploitation_vectors":[],"counters":{"files":2,"domains":0,"ip_addresses":0,"urls":0,"iocs":2,"subscribers":0,"attack_techniques":0},"tags_details":[],"operating_systems":[],"targeted_industries":[],"threat_scape":[ "Cyber Crime" ],"executive_summary":"Brief summary of the threat actor and malware behavior.","merged_actors":[],"motivations":[],"files_count":2,"references_count":2,"malware_roles":[],"targeted_informations":[],"field_sources":[],"collection_type":"report","autogenerated_summary":"Short technical summary of the ransomware's TTPs.","date_of_disclosure":0,"alt_names":[],"exploitation_consequence":"","origin":"Google Threat Intelligence","first_seen_details":[],"technologies":[],"vulnerable_products":"","version":4,"available_mitigation":[],"last_modification_date":1466528312,"tags":[],"source_regions_hierarchy":[],"urls_count":0,"recent_activity_relative_change":0.02898550724637672,"vendor_fix_references":[],"content":"Full detailed technical analysis, including static/dynamic analysis and IoCs.","aggregations":{}},"context_attributes":{"shared_with_me":false,"role":"viewer"}}]}}]
```



#### Get Related IOCs
Use the Get Related IOCs action to obtain information about IOCs that are related to Google SecOps entities using information from Google Threat Intelligence. This action runs on the following Google SecOps entities: IP address, URL, Hostname, Domain, Hash, Threat Actor. This action only supports the MD5, SHA-1, and SHA-256.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOC Types|A comma-separated list of IOCs to extract. The possible values are as follows: IP, Hash, URL, Domain, Threat Actors, Malware, Campaigns.|True|String|IP, Hash, URL, Domain|
|Max IOCs To Return|The maximum number of IOCs to return for selected IOC types  for every entity. The default value is 40.|True|String|40|



##### JSON Results
```json
[  
  {  
    "Entity": "example.com",  
    "EntityResult": {  
      "IP": [  
        "8.8.8.8"  
      ],  
      "Hash": [  
        "ee29a990fb0f37XXXXXXXXXXXXXXXXXXXXXXXXf3f68e01691773b2e1"  
      ],  
      "URL": [  
        "http://example.com/"  
      ],  
      "Domain": [  
        "example.ru"  
      ]  
    }  
  }  
]
```



#### Ping
Use the Ping action to test the connectivity to Google Threat Intelligence. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds



#### Private Submit URL
Use the Private Submit URL action to submit a URL for private scan in Google Threat Intelligence. For regular scan and enrichment use the action “Enrich Entities”. Supported Entities: URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL|Comma-separated list of URLs that need to be scanned. Values from this parameter and entities will be processed together.|False|String||
|Check Existing Submissions First|If enabled, action will first check if there is any available information about the URL in public or private submissions. If it’s available, it will return the information without the submission flow.|False|Boolean|false|
|Resubmit After (Days)|The number of days that must elapse from the last public analysis for the URL to be eligible for resubmission.To use this parameter, “Check Existing Submissions First” must be enabled.|False|String|30|



##### JSON Results
```json
[{"Entity": "string", "EntityResult": {"data": {"id": "string", "type": "private_url", "links": {"self": "string"}, "attributes": {"redirection_chain": [], "url": "string", "expiration": 123456, "last_final_url": "string", "outgoing_links": [], "title": "string", "html_meta": {}, "tags": [], "tld": "string"}}}}, {"Entity": "string", "EntityResult": {"data": {"id": "string", "type": "url", "links": {"self": "string"}, "attributes": {"title": "string", "first_submission_date": 123456, "threat_names": ["string", "string"], "last_modification_date": 123456, "total_votes": {"harmless": 123456, "malicious": 123456}, "times_submitted": 123456, "tld": "string", "last_final_url": "string", "categories": {"alphaMountain.ai": "string", "Sophos": "string", "Webroot": "string"}, "last_analysis_results": {"string": {"method": "string", "engine_name": "string", "category": "string", "result": "string"}}, "last_analysis_date": 123456, "reputation": 123456, "url": "string", "favicon": {"raw_md5": "string", "dhash": "string"}, "last_submission_date": 123456, "has_content": 123456, "threat_severity": {"version": "string", "threat_severity_level": "string", "threat_severity_data": {"num_detections": 123456}, "last_analysis_date": "string", "level_description": "string"}, "last_analysis_stats": {"malicious": 123456, "suspicious": 123456, "undetected": 123456, "harmless": 123456, "timeout": 123456}, "tags": [], "gti_assessment": {"severity": {"value": "string"}, "threat_score": {"value": 123456}, "verdict": {"value": "string"}, "contributing_factors": {"gti_confidence_score": 123456, "malicious_sandbox_verdict": 123456, "safebrowsing_verdict": "string"}, "description": "string"}}}}}]
```



#### Search ASM Entities
Use the Search ASM Entities action to search for Attack Surface Management (ASM) entities in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project Name|The name of the ASM project. If you don’t set a value, the action uses the value that you configured for the "ASM Project Name" integration parameter.|False|String||
|Entity Name|A comma-separated list of entity names for which to find related entities. The action treats entity names that contain forward slashes (/) as invalid names.|False|String||
|Minimum Vulnerabilities Count|The minimum number of vulnerabilities that the entity has for the action to return the entity.|False|String||
|Minimum Issues Count|The minimum number of issues that are related to the entity for the action to return the entity.|False|String||
|Tags|A comma-separated list of tag names to use when searching for entities.|False|String||
|Max Entities To Return|The maximum number of entities to return for every action run. The default value is 50. The maximum value is 200.|True|String|50|
|Critical or High Issue|If selected, the action only returns issues with High and Critical severity.|False|Boolean|false|



##### JSON Results
```json
[{  
      "id": "e947ffd19081586e8e2aafef0db2fdafd7b4d764ff5203cedb8ac2bae8c9b14f",  
      "uid": "e947ffd19081586e8e2aafef0db2fdafd7b4d764ff5203cedb8ac2bae8c9b14f",  
      "uuid": "5241cc42-XXXX-XXXX-XXXX-d89febf8bf48",  
      "dynamic_id": "Intrigue::Entity::ApiEndpoint#entity_name",  
      "alias_group": "11111111",  
      "name": "entity_name",  
      "type": "Intrigue::Entity::ApiEndpoint",  
      "first_seen": "2021-09-03T17:03:38Z",  
      "last_seen": "2021-09-03T17:03:38Z",  
      "collection": "mandiant",  
      "collection_type": "Intrigue::Collections::PreCollection",  
      "collection_naics": ["111111", "1111111"],  
      "collection_uuid": "a8de4539-XXXX-XXXX-XXXX-0ee1770e871f",  
      "organization_uuid": null,  
      "hidden": false,  
      "seed": false,  
      "tags": [],  
      "issues": [],  
      "exfil_lookup_identifier": null,  
      "summary": {  
        "scoped": true,  
        "issues": {  
          "current_by_severity": {},  
          "current_with_cve": 0,  
          "all_time_by_severity": {},  
          "current_count": 0,  
          "all_time_count": 0,  
          "critical_or_high": false  
        },  
        "task_results": ["uri_check_api_endpoint"],  
        "screenshot_exists": false,  
        "http": {  
          "code": 403,  
          "title": null,  
          "content": { "favicon_hash": null, "hash": null, "forms": null },  
          "auth": {  
            "any": null,  
            "basic": null,  
            "ntlm": null,  
            "forms": null,  
            "2fa": null  
          }  
        },  
        "ports": { "count": 0, "tcp": null, "udp": null },  
        "technology": { "cloud": false, "cloud_providers": [] },  
        "network": { "name": null, "asn": null, "route": null, "type": null }  
      }  
    },  
   {  
      "id": "20f65f6175a73d9aee82b4dbcbcd245c94ac5b9e1aae25c2ad3c322284c9a8b8",  
      "uid": "20f65f6175a73d9aee82b4dbcbcd245c94ac5b9e1aae25c2ad3c322284c9a8b8",  
      "uuid": "5412df85-XXXX-XXXX-XXXX-f65enfd0bf11",  
      "dynamic_id": "Intrigue::Entity::Uri#entity_name2",  
      "alias_group": "cbeb42a84fb7c6e48e88",  
      "name": "entity_name2",  
      "type": "Intrigue::Entity::Uri",  
      "first_seen": "2021-09-03T17:03:38Z",  
      "last_seen": "2021-09-03T17:03:38Z",  
      "collection": "mandiant",  
      "collection_type": "Intrigue::Collections::PreCollection",  
      "collection_naics": ["111111", "111111"],  
      "collection_uuid": "a8de3539-XXXX-XXXX-XXXX-0ee1770e982f",  
      "organization_uuid": null,  
      "hidden": false,  
      "seed": false,  
      "tags": [],  
      "issues": [],  
      "exfil_lookup_identifier": null,  
      "summary": {  
        "scoped": true,  
        "issues": {  
          "current_by_severity": {},  
          "current_with_cve": 0,  
          "all_time_by_severity": {},  
          "current_count": 0,  
          "all_time_count": 0,  
          "critical_or_high": false  
        },  
        "task_results": ["search_shodan"],  
        "screenshot_exists": false,  
        "geolocation": {  
          "city": null,  
          "country_code": "US",  
          "country_name": null,  
          "latitude": null,  
          "asn": null  
        },  
        "http": {  
          "code": 200,  
          "title": "FireEye Threat Intelligence",  
          "content": { "favicon_hash": null, "hash": null, "forms": false },  
          "auth": {  
            "any": false,  
            "basic": false,  
            "ntlm": false,  
            "forms": true,  
            "2fa": false  
          }  
        },  
        "ports": { "count": 1, "tcp": ["80"], "udp": null },  
        "network": { "name": "DATE", "asn": null, "route": null, "type": null },  
        "technology": {  
          "cloud": true,  
          "cloud_providers": ["threat intelligence"]  
        },  
        "vulns": { "current_count": 0, "vulns": [] }  
      }  
    }  
    
]
```



#### Search Graphs
Use the Search Graphs action to search for graphs that are based on custom filters in Google Threat Intelligence.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|A query filter for the graph. For example, to search for graphs in the selected period, format the query as follows: "creation_date:2018-11-1+creation_date:2018-11-12"|True|String||
|Sort Field|The value to sort the results. By default, the action sorts the results by last modified date.|False|List|Last Modified Date|
|Max Graphs To Return|The maximum number of graphs to return for a specified query. The default value is 10.|True|String|10|



##### JSON Results
```json
[{"attributes": {"graph_data": {"description": "mhb concluding exercise", "version": "api-5.0.0"}}, "id": "g18xxxxxxxxxx"}, {"attributes": {"graph_data": {"description": "NL", "version": "5.0.0"}}, "id": "g44xxxxxxxxxx"}]
```



#### Set DTM Alert Analysis
Use the Set DTM Alert Analysis action to set an analysis for a Digital Threat Monitoring (DTM) alert in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The ID of the alert to update.|True|String||
|Text|Text of the analysis.|True|String||
|Attachment File Paths|Comma-separated list of attachment file paths. Note: only 10 files can be attached to the alert.|False|String||



##### JSON Results
```json

```



#### Submit File
Use the Submit File action to submit a file and return results from Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|External URLs|A comma-separated list of public URLs for the files to submit. If both “External URL” and “File Paths” are provided, action will collect files from both inputs.|False|String||
|File Paths|A comma-separated list of absolute file paths. If you configure the “Linux Server Address” parameter, the action attempts to retrieve the file from a remote server. If both “External URL” and “File Paths” are provided, action will collect files from both inputs.|False|String||
|Check Hash First|If enabled, action will first calculate the hashes for the files and search, if there is any available information for it. If it’s available, it will return the information without the submission flow.|False|Boolean|false|
|GTI Score|GTI Score that is used to set is_risky property in JSON result to true. This condition is validated together with GTI verdict information. If nothing is provided, action will ignore the GTI score values.|False|String|60|
|Engine Threshold|The count of how many engines should mark the file as malicious or suspicious, for is_risky property in JSON result to be set to true. If “Engine Allowlist” contains values, action will only count results from those engines. This condition is validated together with GTI verdict information. If nothing is provided, action will ignore the Engines calculations.|False|String|None|
|Engine Percentage Threshold|The percentage of engines should mark the entity as malicious or suspicious, for is_risky property in JSON result to be set to true. If “Engine Allowlist” contains values, action will only count the percentage from those engines. If both “Engine Threshold” and “Engine Percentage Threshold” are provided, “Engine Threshold” will be used. Maximum value: 100. Minimum: 0. If nothing is provided, action will ignore the Engines calculations.|False|String|None|
|Engine Allowlist|Comma-separated list of engines that should be used to retrieve information, whether a file is malicious or not. Example: AlienVault,Kaspersky.If nothing is specified in this parameter, action will take results from every available engine. If the engine didn’t return any information about the file it’s not going to be counted for the parameters “Engine Threshold” and “Engine Percentage Threshold”.|False|String||
|Resubmit After (Days)|The number of days for the action to wait before resubmitting the file even if the hash is available for the file in the GTI database. To use this parameter, enable the “Check Hash First” parameter. The default value is 30 days.|False|String|30|
|Fetch MITRE Details|If selected, the action returns the information about the related MITRE techniques and tactics. This parameter only supports the Hash entity. Not selected by default.|False|Boolean|false|
|Lowest MITRE Technique Severity|The lowest MITRE technique severity to return. The action treats the "Unknown" severity as “Info”. This parameter only supports the Hash entity. The default value is Medium.|False|List|Medium|
|Private Submission|If selected, the action submits the file in a private mode.|False|Boolean|false|
|Retrieve Comments|If selected, the action retrieves comments about the entity. This parameter supports the following entities: URL, Domain, Hostname, Hash, and IP Address.|False|Boolean|true|
|Max Comments To Return|The maximum number of comments to return in every action run. The default value is 10.|False|String|10|
|Linux Server Address|Specify the IP address of the remote linux server, where the file is located.|False|String||
|Linux Username|Specify the username of the remote linux server, where the file is located.|False|String||
|Linux Password|Specify the password of the remote linux server, where the file is located.|False|Password|*****|
|ZIP Password|A password for the zipped folder that contains the files to submit.|False|Password|*****|



##### JSON Results
```json
[{"Entity": "/opt/siemplify/test_file_car.txt","EntityResult": {"id": "xxxxx","type": "file","links": {"self": "https://www.virustotal.com/api/v3/files/xxxxx"}, "attributes": {"available_tools": [ ], "sandbox_verdicts": {"Xxxxx1": {"category": "harmless", "malware_classification": [ "XXXX" ], "sandbox_name": "Xxxxx1", "confidence": 100}, "Xxxxx2": {"category": "harmless", "malware_classification": [ "XXXX" ], "sandbox_name": "Xxxxx2", "confidence": 100}}, "ssdeep": "x:xxx:xxx", "magic": "EICAR virus test files", "tags": [], "total_votes": {}, "crowdsourced_yara_results": [ ], "exiftool": {"MIMEType": "text/plain", "FileType": "TXT", "WordCount": "1", "LineCount": "1", "MIMEEncoding": "us-ascii", "FileTypeExtension": "txt", "Newlines": "(none)"}, "known_distributors": {"distributors": [ "Offensive Security" ], "filenames": [ "eicar.com" ], "products": ["Kali Linux Nethunter", "BlackArch Linux" ], "data_sources": [ "National Software Reference Library (NSRL)" ]}, "popular_threat_classification": {"popular_threat_category": [ {"value": "virus", "count": 15}, {"value": "trojan", "count": 2} ], "suggested_threat_label": "virus.eicar/test", "popular_threat_name": [ {"value": "eicar", "count": 59}, {"value": "test", "count": 49}, {"value": "file", "count": 34} ]}, "threat_severity": {"threat_severity_level": "XXXXX", "threat_severity_data": {"belongs_to_bad_collection": true, "num_gav_detections": 4, "popular_threat_category": "xxx", "has_references": true}, "last_analysis_date": "1705419337", "version": 5, "level_description": "Severity HIGH because it was considered virus. Other contributing factor was that it could not be run in sandboxes."}, "type_tag": "powershell", "last_seen_itw_date": 1713844800, "type_extension": "ps1", "unique_sources": 3557, "tlsh": "XXXXXXXX", "reputation": 3669, "filecondis": {"dhash": "0000000", "raw_md5": "xxxxx"}, "first_submission_date": 1148301722, "last_analysis_results": {"Xxx": {"method": "xxx", "engine_name": "Xxx", "engine_version": "2.0.0.1", "engine_update": "20250415", "category": "malicious", "result": "W32.EicarTest.Trojan"}}, "size": 68, "mandiant_ic_score": 0, "times_submitted": 1075275, "last_analysis_date": 1744757172, "autostart_locations": [ ], "sigma_analysis_stats": {"high": 0, "medium": 0, "critical": 0, "low": 1}, "sigma_analysis_summary": {"Sigma Integrated Rule Set (GitHub)": {"high": 0, "medium": 0, "critical": 0, "low": 1}}, "last_submission_date": 1744757172, "names": [ ], "downloadable": true, "antiy_info": "Trojan/Generic.ASBOL.2A", "sha256": "xxxx", "type_description": "Powershell", "type_tags": [ "source", "powershell", "ps", "ps1" ], "trid": [ {"file_type": "EICAR antivirus test file", "probability": 100.0} ], "last_analysis_stats": {}, "md5": "xxxxx", "meaningful_name": "eicar.com-18190", "first_seen_itw_date": 1582585760, "magika": "POWERSHELL", "sha1": "xxxx", "last_modification_date": 1744757227, "sigma_analysis_results": [ ], "crowdsourced_ai_results": [ ], "gti_assessment": {"verdict": {"value": "XXXXX"}, "severity": {"value": "XXXX"}, "threat_score": {"value": 0}, "contributing_factors": {"legitimate_software": true}, "description": "This indicator is benign. It is associated with a well-known and trusted software distributor and likely poses no threat."}}, "sandboxes_data": {}, "widget_link": null, "widget_html": null, "is_risky": false, "execution_status": "success"}}]
```



#### Update ASM Issue
Use the Update ASM Issue to update an Attack Surface Management (ASM) issue in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Issue ID|The ID of the issue to update.|True|String||
|Status|The new status to set for the issue. The default value is Select One. If you use the default value, the action fails.|True|List|Select One|



##### JSON Results
```json
{"success":true,"message":"Successfully reported status as open_new","result":"open_new"}
```



#### Update DTM Alert
Use the Update DTM Alert to update a Digital Threat Monitoring (DTM) alert in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The ID of the alert to update.|True|String||
|Status|The new status to set for the alert. The default value is Select One. If you use the default value, the action fails.|False|List||



##### JSON Results
```json
{"id":"cpcs4x","monitor_id":"cnipx","topic_matches":[{"topic_id":"4a6ffb0x","value":"scram2.private","term":"lwd","offsets":[26,29]},{"topic_id":"doc_type:domain","value":"domain"}],"label_matches":[],"doc_matches":[],"tags":[],"created_at":"2024-05-31T12:27:43.475Z","updated_at":"2024-05-31T12:43:20.399Z","labels_url":"https://api.intelligence.mandiant.com/v4/dtm/docs/domain_discovery/78190f53-818f-4e57-8218-b3060d14fcc2/labels","topics_url":"https://api.intelligence.mandiant.com/v4/dtm/docs/domain_discovery/78190f53-818f-4e57-8218-b3060d14fcc2/topics","doc_url":"https://api.intelligence.mandiant.com/v4/dtm/docs/domain_discovery/78190f53-818f-4e57-8218-b3060d14fcc2","status":"closed","alert_type":"Domain Discovery","alert_summary":"See alert content for details","title":"Suspicious domain \"scram2.privatelinkcanary.hlwded.c4.kafka.ap-southeast-1.amazonaws.com\" similar to \"lwd\"","email_sent_at":"","severity":"medium","confidence":0.5,"has_analysis":false,"monitor_version":2}
```



#### Search Entity Graphs
Use the Search Entity Graphs action to search graphs that are based on Google SecOps entities in Google Threat Intelligence. This action runs on the following Google SecOps entities: IP, URL, Filehash, Hostname, Domain, Threat Actor, User. This action only supports the MD5, SHA-1, and SHA-256 hashes.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sort Field|The value to sort the results. By default, the action sorts the results by owner.|False|List|Owner|
|Max Graphs To Return|The maximum number of graphs to return for a specified query. The default value is 10.|True|String|10|



##### JSON Results
```json
[{"attributes": {"graph_data": {"version": "3.0.7"}, "links": [{"connection_type": "itw_urls", "source": "f3bxxxxxxxxxx", "target": "relationships_itw_urls_f3bxxxxxxxxxx"}, {"connection_type": "itw_urls", "source": "relationships_itw_urls_f3bxxxxxxxxxx", "target": "2f6xxxxxxxxxx"}], "views_count": 15, "position": {"y": 100, "x": 100, "scale": "2.5xxxxxxxxxx"}, "comments_count": 0, "creation_date": 1541669403, "last_modified_date": 1541669403, "private": false, "nodes": [{"index": 0, "entity_id": "f3bxxxxxxxxxx", "fx": 100, "fy": -100, "entity_attributes": {"type_tag": "peexe", "has_detections": true}, "text": "test.exe", "y": -100, "x": 100, "type": "file"}, {"index": 1, "entity_id": "relationships_itw_urls_f3bxxxxxxxxxx", "fx": -100, "fy": -100, "y": -100, "x": -100, "type": "relationship"}]}, "id": "g0cxxxxxxxxxx"}, {"attributes": {"graph_data": {"version": "3.1.1", "description": ""}, "links": [{"connection_type": "urls", "source": "10.x.x.x", "target": "relationships_urls_10zxxxxxxxxxx"}], "views_count": 26, "position": {"y": -100, "x": 100, "scale": "0.9xxxxxxxxxx"}, "comments_count": 0, "creation_date": 1547344218, "last_modified_date": 1547344218, "private": false, "nodes": [{"index": 0, "entity_id": "10.x.x.x", "text": "10.x.x.x", "entity_attributes": {"country": "ZZ"}, "y": 100, "x": 100, "type": "ip_address"}, {"y": 100, "x": 100, "entity_id": "relationships_urls_10zxxxxxxxxxx", "type": "relationship", "index": 1}]}, "id": "gbdxxxxxxxxxx"}]
```



#### Search ASM Issues
Use the Search ASM Issues action to search for Attack Surface Management (ASM) issues in Google Threat Intelligence. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project Name|The name of the ASM project. If you don’t set a value, the action uses the value that you configured for the "ASM Project Name" integration parameter.|False|String||
|Issue ID|A comma-separated list of issue IDs for which to obtain details.|False|String||
|Entity ID|A comma-separated list of entity IDs for which to find related issues.|False|String||
|Entity Name|A comma-separated list of entity names for which to find related issues. The action treats entity names that contain forward slashes (/) as invalid names.|False|String||
|Time Parameter|The time parameter to filter the results.|False|List|First Seen|
|Time Frame|A period to search for issues. If you select the "Custom" value, set the "Start Time" parameter. The default value is Last Hour.|False|List|Last Hour|
|Start Time|The start time to search for results. If you select "Custom" for the "Time Frame" parameter,  this parameter is required. To configure this parameter, set the start time in the ISO 8601 format.|False|String||
|End Time|The end time to search for results. If you don’t set a value and select "Custom" for the "Time Frame" parameter, this parameter uses the current time as end time value. To configure this parameter, set the end time in the ISO 8601 format.|False|String||
|Lowest Severity To Return|The lowest severity of the issues to return. The default value is Select One. If you use the default parameter value, this filter doesn’t apply to search.|False|List|Select One|
|Status|The status of the issues to return. The default value is Select One. If you use the default parameter value, this filter doesn’t apply to search.|False|List|Select One|
|Tags|A comma-separated list of tag names to use when searching for issues.|False|String||
|Max Issues To Return|The maximum number of issues to return for every action run. The default value is 50. The maximum value is 200.|True|String|50|



##### JSON Results
```json
[{"id": "xxxxxxxx", "uuid": "89d68a35-ba7b-47b7-825c-e7febe611f4b", "dynamic_id": 2867262, "name": "self_signed_certificate", "upstream": "intrigue", "last_seen": "2022-03-03T21:00:04.000Z", "first_seen": "2022-03-03T21:00:04.000Z", "entity_uid": "e1f175c3c7568570caa0c7855801c08bb30cdb0de7756746905617893f086559", "entity_type": "Intrigue::Entity::Uri", "entity_name": "https://3.214.213.33:443", "alias_group": "13372361", "collection": "mandiant", "collection_uuid": "a8de4539-f269-447b-81fb-0ee1770e982f", "collection_type": "pre_collection", "organization_uuid": null, "summary": {"pretty_name": "Self Signed Certificate Detected", "severity": 5, "scoped": true, "confidence": "confirmed", "status": null, "category": "misconfiguration", "identifiers": null, "status_new": "closed", "status_new_detailed": null, "ticket_list": null}, "tags": []}]
```









## Connectors
#### Google Threat Intelligence - ASM Issues Connector
Use the Google Threat Intelligence - ASM Issues Connector to retrieve information about the Attack Surface Management (ASM) issues from Google Threat Intelligence. The dynamic list filter works with the "category" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Use dynamic list as a blocklist|If selected, the connector uses th dynamic list as a blocklist. Not selected by default.|False|Boolean|false|
|DeviceProductField|The name of the field where the product name is stored.|True|String|Product Name|
|EventClassId|The name of the field where the event name (subtype) is stored.|True|String|entity_type|
|PythonProcessTimeout|The timeout limit in seconds for the Python process running the current script. The default value is 180 seconds.|True|Integer|180|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment. The default value is "".|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the "Environment Field Name" field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value ".*" to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|The API root of the Google Threat Intelligence instance.|True|String|https://www.virustotal.com|
|API Key|The Google Threat Intelligence API key.|True|Password|*****|
|Project Name|The name of the ASM project.|False|String||
|Verify SSL|If selected, the connector verifies that the SSL certificate for connecting to Google Threat Intelligence is valid.|False|Boolean|true|
|Lowest Severity To Fetch|The lowest severity of the alerts to fetch. If you don’t set a value, the connector ingests alerts with all severity levels. The possible values are as follows: Informational, Low, Medium, High, Critical.|False|String||
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation. Selected by default.|False|Boolean|true|
|Issue Name Filter|Comma-separated list of names of issues that need to be ingested. If the input is provided as “!issue_name”, connector will ingest everything except for the provided issue. If nothing is provided, the connector will not apply this filter. Input is case sensitive.|False|String||
|Status Filter|Comma-separated list of issue statuses that need to be ingested. If nothing is provided, the connector will process only opened issues. Possible Values: Open, Closed.|False|String|Open|
|Max Hours Backwards|The number of hours before the first connector iteration to retrieve issues from. This parameter applies either to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp. The default value is 1 hour.|True|Integer|1|
|Max Issues To Fetch|The maximum number of issues to process for every connector iteration. The default value is 10. The maximum value is 100.|True|Integer|10|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Google Threat Intelligence - DTM Alerts Connector
Use the Google Threat Intelligence - DTM Alerts Connector to retrieve alerts from Google Threat Intelligence. The dynamic listworks with the "alert_type" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The name of the field where the product name is stored|True|String|Product Name|
|EventClassId|The name of the field where the event name (subtype) is stored.|True|String|event_type|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment. The default value is "".|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the "Environment Field Name" field. This parameter lets you manipulate the environment field using the regular expression logic.Use the default value ".*" to retrieve the|False|String|.*|
|API Root|The API root of the Google Threat Intelligence instance.|True|String|https://www.virustotal.com|
|API Key|The Google Threat Intelligence API key.|True|Password|*****|
|Verify SSL|If selected, the connector verifies that the SSL certificate for connecting to Google Threat Intelligence is valid.|False|Boolean|true|
|Lowest Severity To Fetch|The lowest severity of the alerts to fetch. If you don’t set a value, the connector ingests alerts with all severity levels. The possible values are as follows: Low, Medium, High.|False|String||
|Monitor ID Filter|A comma-separated list of monitor IDs from which to retrieve alerts. This parameter is applied alongside side Monitor Name values as OR filter.|False|String||
|Monitor Name Filter|A comma-separated list of monitor names from which to retrieve alerts. Note: if there are several monitors with the same name, connector will ingest from all of them. This parameter is applied alongside side Monitor ID values as OR filter.|False|String||
|Event Type Filter|A comma-separated list of event types that needs to be returned. If input is provided in format “!event_type”, then action will return all events except for the provided one. If nothing is provided, the connector will process all event types. Input is case sensitive.|False|String||
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation. Selected by default.|False|Boolean|true|
|Max Hours Backwards|The number of hours before the first connector iteration to retrieve responses from. This parameter applies either to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp. The default value is 1 hour.|True|Integer|1|
|Max Alerts To Fetch|The maximum number of alerts to process for every connector iteration. The default value is 25. The maximum value is 25.|True|Integer|25|
|Use dynamic list as a blocklist|If selected, the connector uses th dynamic list as a blocklist. Not selected by default.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Google Threat Intelligence - Livehunt Connector
Use the Google Threat Intelligence - Livehunt Connector to retrieve information about the Livehunt notifications and their related files from Google Threat Intelligence. The dynamic list works with the "rule_name" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The name of the field where the product name is stored.|True|String|Product Name|
|EventClassId|The name of the field where the event name (subtype) is stored.|True|String|type|
|PythonProcessTimeout|The timeout limit in seconds for the Python process running the current script. The default value is 180 seconds.|True|Integer|180|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is set to the default environment. The default value is "".|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the "Environment Field Name" field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value ".*" to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|The API root of the Google Threat Intelligence instance.|True|String|https://www.virustotal.com|
|API Key|The Google Threat Intelligence API key.|True|Password|*****|
|Verify SSL|If selected, the connector verifies that the SSL certificate for connecting to Google Threat Intelligence is valid.|False|Boolean|true|
|Max Hours Backwards|The number of hours before the first connector iteration to retrieve notifications from. This parameter applies either to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp. The default value is 1 hour.|False|Integer|1|
|Max Notifications To Fetch|The maximum number of notifications to process for every connector iteration. The default value is 40.|False|Integer|40|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation. Selected by default.|False|Boolean|true|
|Use dynamic list as a blocklist|If selected, the connector uses th dynamic list as a blocklist. Not selected by default.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




