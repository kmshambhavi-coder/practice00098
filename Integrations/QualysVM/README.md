
# QualysVM

Qualys VM (Vulnerability Management) is a cloud-based service that gives you immediate, global visibility into where your IT systems might be vulnerable to the latest Internet threats and how to protect them. It helps you to continuously identify threats and monitor unexpected changes in your network before they turn into breaches.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String||
|Username||True|String||
|Password||True|Password|*****|
|X-Requested-With Header|On behalf of whom, the API requests need to be executed in the integration|True|String|Google SecOps SOAR|
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
|xmltodict-0.13.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Download Vm Scan Results
Fetch vulnerability scan results by scan id.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan ID|Scan ID value. Scan ID format: scan/{integer}.{integer}|True|String||



##### JSON Results
```json
[{"username": "username", "city": "New York", "zip": "10024", "name": "user name", "add1": "Broadway", "country": "United States of America", "company": "X", "state": "New York", "scan_report_template_title": "Scan Results", "result_date": "01/28/2019 12:16:42", "role": "Manager", "add2": "Suite"}, {"status": "Finished", "scanner_appliance": "1.1.1.1 (Scanner 10.10.10-1, Vulnerability Signatures 10.10.10-2)", "network": "Global Default Network", "reference": "scan/1533110666.07264", "ips": "1.1.1.1", "launch_date": "08/01/2018 08:04:26", "option_profile": "Initial Options", "total_hosts": "1", "scan_title": "My first scan", "duration": "00:06:20", "excluded_ips": "", "asset_groups": null, "type": "API", "active_hosts": "1"}, {"protocol": "tcp", "qid": 86000, "results": "Server Version\tServer Banner\ncloudflare-nginx\tcloudflare-nginx", "solution": "N/A", "ip_status": "host scanned, found vuln", "port": "80", "category": "Web server", "severity": "1", "title": "Web Server Version", "instance": null, "dns": "1dot1dot1dot1.cloudflare-dns.com", "ip": "1.1.1.1", "type": "Ig", "vendor_reference": null, "cve_id": null, "ssl": "no", "netbios": null, "associated_malware": null, "pci_vuln": "no", "impact": "N/A", "fqdn": "", "bugtraq_id": null, "threat": "N/A", "os": "Linux 3.13", "exploitability": null}, {"target_distribution_across_scanner_appliances": "External : 1.1.1.1"}]
```



#### Enrich Host
Enrich host with information from Qualys VM. Note: AssetView module is required. Supported entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"LAST_VM_SCANNED_DATE": "2019-01-06T12: 39: 00Z", "LAST_VM_SCANNED_DURATION": "490", "NETWORK_ID": "0", "IP": "1.1.1.1", "LAST_VULN_SCAN_DATETIME": "2019-01-06T12: 39: 00Z", "COMMENTS": "AddedbyX", "TRACKING_METHOD": "IP", "DNS": "one.one.one.one", "OS": "Linux3.13", "ID": "54664176"}, "Entity": "1.1.1.1"}]
```



#### Download Report
Fetch report by ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report ID|Report ID value.|True|String||



##### JSON Results
```json
{"STATUS": {"STATE": "Finished"}, "EXPIRATION_DATETIME": "2019-02-04T13:11:15Z", "TITLE": "Scan scan/1533110666.07264 Report", "USER_LOGIN": "sempf3mh", "OUTPUT_FORMAT": "PDF", "LAUNCH_DATETIME": "2019-01-28T13:11:14Z", "TYPE": "Scan", "ID": "775111", "SIZE": "22.17 KB"}
```



#### Launch Compliance Report
Launch a compliance report
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Title|A user-defined report title. The title may have a maximum of 128 characters. For a PCI compliance report, the report title is provided by Qualys and cannot be changed.|True|String||
|Report Type|Template name. For example: Qualys Top 20 Report, Payment Card Industry (PCI).|True|String||
|Output Format|One output format may be specified. When output_format=pdf is specified, the Secure PDF Distribution may be used. e.g: pdf, mht and html.|True|String||
|IPs/Ranges|Specify IPs/ranges to change (override) the report target, as defined in the patch report template. Multiple IPs/ranges are comma separated.|False|String||
|Asset Groups|Asset groups.if more than one has to be comma separated.|False|String||
|Scan Reference|Show only a scan with a certain scan reference code.|False|String||



#### Launch Patch Report
Launch a patch report
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Title|A user-defined report title. The title may have a maximum of 128 characters. For a PCI compliance report, the report title is provided by Qualys and cannot be changed.|True|String||
|Report Type|Template name. For example: Qualys Patch Report.|True|String||
|Output Format|One output format may be specified. When output_format=pdf is specified, the Secure PDF Distribution may be used. e.g: pdf, online, xml or csv.|True|String||
|IPs/Ranges|Specify IPs/ranges to change (override) the report target, as defined in the patch report template. Multiple IPs/ranges are comma separated.|False|String||
|Asset Groups|Asset groups.if more than one has to be comma separated.|False|String||



#### Launch Remediation Report
Launch a remediation report
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Title|A user-defined report title. The title may have a maximum of 128 characters. For a PCI compliance report, the report title is provided by Qualys and cannot be changed.|True|String||
|Report Type|Template name. For example: Tickets per Asset Group, Tickets per Vulnerability.|True|String||
|Output Format|One output format may be specified. When output_format=pdf is specified, the Secure PDF Distribution may be used. e.g: pdf, mht and html.|True|String||
|IPs/Ranges|Specify IPs/ranges to change (override) the report target, as defined in the patch report template. Multiple IPs/ranges are comma separated.|False|String||
|Asset Groups|Asset groups.if more than one has to be comma separated.|False|String||
|Display Results For All tickets|Specifies whether the report will include tickets assigned to the current user (User is set by default), or all tickets in the user account. By default tickets assigned to the current user are included.|False|Boolean|false|



#### Launch Scan Report
Launch a scan report
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Title|A user-defined report title. The title may have a maximum of 128 characters. For a PCI compliance report, the report title is provided by Qualys and cannot be changed.|True|String||
|Report Type|Template name. For example: Technical Report.|True|String||
|Output Format|One output format may be specified. When output_format=pdf is specified, the Secure PDF Distribution may be used. e.g: pdf, mht and html.|True|String||
|IPs/Ranges|Specify IPs/ranges to change (override) the report target, as defined in the patch report template. Multiple IPs/ranges are comma separated.|False|String||
|Asset Groups|Asset groups.if more than one has to be comma separated.|False|String||
|Scan Reference|For a PCI compliance report, either the technical or executive report, this parameter specifies the scan reference to include. A scan reference starts with the string "scan/" followed by a reference ID number. The scan reference must be for a scan that was run using the PCI Options profile. Only one scan reference may be specified.|False|String||



#### List Endpoint Detections
List endpoint detections in Qualys VM. Supported entities: IP Address, Hostname.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status Filter|Specify a comma-separated list of statuses that should be used during ingestion. If nothing is provided, the action will ingest detections with New, Active, Re-Opened statuses. Possible values: New, Active, Re-Opened, Fixed|False|String|New, Active, Re-Opened|
|Lowest Severity To Fetch|Specify the lowest severity that will be used to fetch detections.|False|List|Medium|
|Max Detections To Return|Specify how many detections to return per entity. Default: 50. Maximum: 200.|False|String|50|
|Ingest Ignored Detections|If enabled, action will also return ignored detections.|False|Boolean|false|
|Ingest Disabled Detections|If enabled, action will also return disabled detections.|False|Boolean|false|
|Create Insight|If enabled, action will create an insight containing information about vulnerabilities found on the entity.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "EX01", "EntityResult": [{"QID": "xxxx", "VULN_TYPE": "Vulnerability", "SEVERITY_LEVEL": "5", "TITLE": "Microsoft Exchange Server Multiple Vulnerabilities (ProxyShell) (unauthenticated)", "CATEGORY": "Mail services", "LAST_SERVICE_MODIFICATION_DATETIME": "2021-09-07T17:53:26Z", "PUBLISHED_DATETIME": "2021-08-10T01:47:23Z", "PATCHABLE": "1", "SOFTWARE_LIST": {"SOFTWARE": {"PRODUCT": "exchange_server", "VENDOR": "microsoft"}}, "VENDOR_REFERENCE_LIST": {"VENDOR_REFERENCE": [{"ID": "CVE-2021-34473", "URL": "https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-34473"}, {"ID": "CVE-2021-26855", "URL": "https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-31207"}, {"ID": "CVE-2021-34523", "URL": "https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-31207"}]}, "CVE_LIST": {"CVE": [{"ID": "CVE-2021-34473", "URL": "http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-34473"}, {"ID": "CVE-2021-34523", "URL": "http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-34523"}, {"ID": "CVE-2021-31207", "URL": "http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-31207"}]}, "DIAGNOSIS": "Microsoft Exchange Server is prone to multiple vulnerabilities including remote code and privilege escalation.<P>\nMicrosoft released the following details and the security updates.<BR>\n\nAffected Versions:<BR>\nMicrosoft Exchange Server 2013 Cumulative Update 23<BR>\nMicrosoft Exchange Server 2019 Cumulative Update 9<BR>\nMicrosoft Exchange Server 2019 Cumulative Update 10<BR>\nMicrosoft Exchange Server 2016 Cumulative Update 20<BR>\nMicrosoft Exchange Server 2016 Cumulative Update 21<P>\n\nQID Detection Logic (unauthenticated):<BR>\nThe QID checks for vulnerable versions of exchange which is retrieved via a GET request to URI &quot;autodiscover/autodiscover.json?@test.com/ecp/?&#38;Email=autodiscover/autodiscover.json%3F@test.com&quot;. <BR>\nThe QID also checks for vulnerable instances via GET request &quot;autodiscover/autodiscover.json?@test.com/mapi/nspi/?&#38;Email=autodiscover/autodiscover.json%3F@test.com&quot;. Vulnerable instance will return &quot;NT AUTHORIT SYSTEM&quot; in the response.<P>", "CONSEQUENCE": "Successful exploitation allows attackers to execute remote code.<BR>", "SOLUTION": "Customers are advised to refer to <A HREF=https://support.microsoft.com/help/5004780 TARGET=_blank>KB5004780</A>, <A HREF=https://support.microsoft.com/help/5004779 TARGET=_blank>KB5004779</A>, <A HREF=https://support.microsoft.com/help/5004778 TARGET=_blank>KB5004778</A> for information pertaining to this vulnerability.<BR>\n<P>Patch:<BR>\nFollowing are links for downloading patches to fix the vulnerabilities:\n<P> <A HREF=http://www.microsoft.com/download/details.aspx?familyid=cae731a5-0d00-4f76-b2c6-84bd511e529f TARGET=_blank>KB5004778</A><P> <A HREF=http://www.microsoft.com/download/details.aspx?familyid=ccf40c19-2653-4b5c-b922-d6d09bbf1c3e TARGET=_blank>KB5004779</A><P> <A HREF=http://www.microsoft.com/download/details.aspx?familyid=07683b40-1608-437d-a90a-xxx TARGET=_blank>xxx</A>", "PCI_FLAG": "1", "DISCOVERY": {"REMOTE": "1", "ADDITIONAL_INFO": "Patch Available"}}]}]
```



#### List Groups
List asset groups in the user's account.
Timeout - 600 Seconds



##### JSON Results
```json
[{"TITLE": "All", "IP_SET": {"IP": ["1.1.1.1"]}, "DOMAIN_LIST": {"DOMAIN": [{"@network_id": "0", "#text": "google.com"}, {"@network_id": "0", "#text": "none", "@netblock": "1.1.1.1-1.1.1.1"}]}, "LAST_UPDATE": "2018-07-25T14:56:05Z", "NETWORK_ID": "0", "OWNER_USER_NAME": "Global User", "BUSINESS_IMPACT": "High", "ID": "1111"}, {"TITLE": "G", "NETWORK_ID": "0", "LAST_UPDATE": "2018-08-13T08:14:55Z", "OWNER_USER_NAME": "user (Manager)", "OWNER_USER_ID": "11111", "BUSINESS_IMPACT": "High", "ID": "11111"}]
```



#### List Ips
List IP addresses in the user's account. By default, all hosts in the user's account are included.
Timeout - 600 Seconds



##### JSON Results
```json
["1.1.1.1", "1.1.100.100", "10.10.10.10"]
```



#### List Reports
List of reports in the user's account when Report Share feature is enabled. The report list output includes all report types, including scorecard reports. 
Timeout - 600 Seconds



##### JSON Results
```json
[{"STATUS": {"STATE": "Finished"}, "EXPIRATION_DATETIME": "2019-02-04T13:11:15Z", "TITLE": "Scan scan/1533110666.07264 Report", "USER_LOGIN": "sempf3mh", "OUTPUT_FORMAT": "PDF", "LAUNCH_DATETIME": "2019-01-28T13:11:14Z", "TYPE": "Scan", "ID": "775111", "SIZE": "22.17 KB"}]
```



#### Launch VM Scan And Fetch Results
Launch vulnerability scan on a host in your network and fetch results. NOTICE! This action will automatically new hosts to Qualys as assets. Please note that your license limit number of hosts depends on your subscription. Supported entities: IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scanner Appliance|The friendly names of the scanner appliances to be used or "External" for external scanners. Multiple entries are comma separated.|False|String||
|Network|The ID of a network used to filter the IPs/ranges specified in the "ip" parameter. Set to a custom network ID (note this does not filter IPs/ranges specified in "asset_groups" or "asset_group_ids"). Or set to "0" (the default) for the Global Default Network - this is used to scan hosts outside of your custom networks.|False|String||
|Title|The scan title. This can be a maximum of 2000 characters (ascii)|False|String||
|Processing Priority|Specify a value of 0 - 9 to set a processing priority level for the scan. When not specified, a value of 0 (no priority) is used. Valid values are: 0 for No Priority (the default), 1 for Emergency, 2 for Ultimate,3 for Critical, 4 for Major, 5 for High, 6 for Standard 7 for Medium, 8 for Minor and 9 for Low|True|String||
|Scan Profile|The title of the compliance option profile to be used. One of these parameters must be specified in a request: option_title or option_id. For example: Qualys Top 20 Options.|True|String||



##### JSON Results
```json
[{"username": "username", "city": "New York", "zip": "10024", "name": "user name", "add1": "Broadway", "country": "United States of America", "company": "X", "state": "New York", "scan_report_template_title": "Scan Results", "result_date": "01/28/2019 12:16:42", "role": "Manager", "add2": "Suite"}, {"status": "Finished", "scanner_appliance": "1.1.1.1 (Scanner 10.10.10-1, Vulnerability Signatures 10.10.10-2)", "network": "Global Default Network", "reference": "scan/1533110666.07264", "ips": "1.1.1.1", "launch_date": "08/01/2018 08:04:26", "option_profile": "Initial Options", "total_hosts": "1", "scan_title": "My first scan", "duration": "00:06:20", "excluded_ips": "", "asset_groups": null, "type": "API", "active_hosts": "1"}, {"protocol": "tcp", "qid": 86000, "results": "Server Version\tServer Banner\ncloudflare-nginx\tcloudflare-nginx", "solution": "N/A", "ip_status": "host scanned, found vuln", "port": "80", "category": "Web server", "severity": "1", "title": "Web Server Version", "instance": null, "dns": "1dot1dot1dot1.cloudflare-dns.com", "ip": "1.1.1.1", "type": "Ig", "vendor_reference": null, "cve_id": null, "ssl": "no", "netbios": null, "associated_malware": null, "pci_vuln": "no", "impact": "N/A", "fqdn": "", "bugtraq_id": null, "threat": "N/A", "os": "Linux 3.13", "exploitability": null}, {"target_distribution_across_scanner_appliances": "External : 1.1.1.1"}]
```



#### List Scans
List of scans launched within the past 30 days.
Timeout - 600 Seconds



##### JSON Results
```json
[{"STATUS": {"STATE": "Finished"}, "TARGET": "1.1.1.1", "TITLE": "Test Scan", "USER_LOGIN": "*****", "LAUNCH_DATETIME": "2019-01-06T12:29:52Z", "PROCESSED": "1", "REF": "scan/1546777792.44756", "PROCESSING_PRIORITY": "0 - No Priority", "DURATION": "00:08:24", "TYPE": "On-Demand"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### Qualys VM - Detections Connector
Pull detections from Qualys VM. Note: whitelist works with "Type" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|event_type|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API Root of the Qualis VM instance.|True|String||
|Username|Username of the Qualis VMDR instance.|True|String||
|Password|Password of the Qualis VMDR instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Qualys VM server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|Lowest severity that will be used to fetch detections. If nothing is provided, the connector will fetch all detections. Maximum: 5.|False|Integer|1|
|Status Filter|Status filter for the connector. If nothing is provided, the connector will ingest detections with "New, Active, Re-Opened" statuses. Possible values: NEW, ACTIVE, FIXED, RE-OPENED.|False|String|NEW, ACTIVE, RE-OPENED|
|Ingest Ignored Detections|If enabled, the connector will ingest ignored detections.|False|Boolean|false|
|Ingest Disabled Detections|If enabled, the connector will ingest disabled detections.|False|Boolean|false|
|Grouping Mechanism|Grouping mechanism that will be used to create Siemplify Alerts. Possible values: Host, Detection, None. If Host is provided, the connector will create 1 Siemplify alert containing all of the detection related to the host. If Detection is provided, the connector will create 1 Siemplify Alert containing information about all of the hosts that have that detection. If None or invalid value is provided, the connector will create a new Siemplify alert for each separate detection per host.|True|String|Detection|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|X-Requested-With Header|On behalf of whom, the API requests need to be executed in the integration|True|String|Google SecOps SOAR|




