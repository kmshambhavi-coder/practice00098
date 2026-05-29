
# NozomiNetworks

Nozomi Networks Guardianâ„¢ unlocks visibility across OT, IoT, and IT for accelerated security and digital transformation. Its physical or virtual appliances monitor network communications and device behavior, delivering instant awareness of your OT/IoT network and its activity patterns. You see the highest priority vulnerabilities as well as threats and anomalous behavior, enabling you to respond faster, ensuring high reliability and security.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API URL||True|String|https://x.x.x.x:port|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|False|
|CA Certificate File||False|String||


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
|EnvironmentCommon-1.0.0-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich Siemplify Host or IP entities based on the information from the Nozomi Networks device.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional fields to add to enrichment|Comma separated list of fields that should be additionally taken from Nodes query to add to fields that are used for enrichment by default.|False|String||



##### JSON Results
```json
[{"Entity": "172.30.xxx.xxx", "EntityResult": {"appliance_host": "nozomi-n2os.local", "label": "DESKTOP-8P0TH6Q.local", "id": "172.30.xxx.xxx", "_asset_kb_id": null, "ip": "172.30.xxx.xxx", "mac_address": "00:50:56:xx:xx:xx", "mac_address:info": {"source": "", "likelihood": 0, "likelihood_level": "unconfirmed"}, "mac_vendor": "VMware, Inc.", "_private_status": "no", "subnet": "172.30.xxx.xxx", "vlan_id": null, "vlan_id:info": {"source": "passive"}, "zone": "Internal", "level": "5", "type": "computer", "type:info": {"source": "passive"}, "os": "Windows 10 / Server 2016", "vendor": null, "vendor:info": {"source": "passive"}, "product_name": null, "product_name:info": {"source": "passive"}, "firmware_version": null, "firmware_version:info": {"source": "passive"}, "serial_number": null, "serial_number:info": {"source": "passive"}, "is_broadcast": false, "is_public": false, "reputation": null, "is_confirmed": true, "is_learned": true, "is_fully_learned": true, "is_disabled": false, "_is_licensed": true, "roles": ["other"], "links": [{"id": "224.0.xxx.xxx", "protos": [{"name": "llmnr", "last_activity": "1602495882225"}]}, {"id": "172.30.xxx.xxx", "protos": [{"name": "browser", "last_activity": "1605052230602"}, {"name": "netbios-ns", "last_activity": "1604654773056"}]}, {"id": "224.0.xxx.xxx", "protos": [{"name": "mdns", "last_activity": "1602636321803"}]}, {"id": "239.255.xxx.xxx", "protos": [{"name": "ssdp", "last_activity": "1600331209918"}]}], "links_count": "5", "protocols": ["browser", "llmnr", "mdns", "netbios-ns", "ssdp"], "created_at": "1595315728295", "first_activity_time": "1595315728295", "last_activity_time": "1605052230602", "received.packets": "0", "received.bytes": "0", "received.last_5m_bytes": "0", "received.last_15m_bytes": "0", "received.last_30m_bytes": "0", "sent.packets": "5088", "sent.bytes": "1031179", "sent.last_5m_bytes": "0", "sent.last_15m_bytes": "0", "sent.last_30m_bytes": "0", "tcp_retransmission.percent": 0, "tcp_retransmission.packets": "0", "tcp_retransmission.bytes": "0", "tcp_retransmission.last_5m_bytes": "0", "tcp_retransmission.last_15m_bytes": "0", "tcp_retransmission.last_30m_bytes": "0", "variables_count": null, "device_id": "TIP-HW-HOST-033", "properties": {}, "custom_fields": {}, "bpf_filter": "ip host 172.30.xxx.xxx", "device_modules": {}, "capture_device": "em1"}}, {"Entity": "FIREEYE-DOMAIN", "EntityResult": {"appliance_host": "nozomi-n2os.local", "label": "FIREEYE-DOMAIN", "id": "172.30.xxx.xxx", "_asset_kb_id": null, "ip": "172.30.xxx.xxx", "mac_address": "00:50:56:xx:xx:xx", "mac_address:info": {"source": "", "likelihood": 0, "likelihood_level": "unconfirmed"}, "mac_vendor": "VMware, Inc.", "_private_status": "no", "subnet": "172.30.xxx.xxx", "vlan_id": null, "vlan_id:info": {"source": "passive"}, "zone": "Internal", "level": "5", "type": "computer", "type:info": {"source": "passive"}, "os": "Windows Server 2016", "vendor": null, "vendor:info": {"source": "passive"}, "product_name": null, "product_name:info": {"source": "passive"}, "firmware_version": null, "firmware_version:info": {"source": "passive"}, "serial_number": null, "serial_number:info": {"source": "passive"}, "is_broadcast": false, "is_public": false, "reputation": null, "is_confirmed": true, "is_learned": true, "is_fully_learned": true, "is_disabled": false, "_is_licensed": true, "roles": ["other"], "links": [{"id": "224.0.xxx.xxx", "protos": [{"name": "other", "last_activity": "1602636289985"}]}, {"id": "172.30.xxx.xxx", "protos": [{"name": "browser", "last_activity": "1603365034756"}, {"name": "netbios-ns", "last_activity": "1603363386900"}]}, {"id": "224.0.xxx.xxx", "protos": [{"name": "llmnr", "last_activity": "1603363385754"}]}], "links_count": "4", "protocols": ["browser", "llmnr", "netbios-ns", "other"], "created_at": "1589544466017", "first_activity_time": "1589544466017", "last_activity_time": "1603365034756", "received.packets": "0", "received.bytes": "0", "received.last_5m_bytes": "0", "received.last_15m_bytes": "0", "received.last_30m_bytes": "0", "sent.packets": "39621", "sent.bytes": "6309729", "sent.last_5m_bytes": "0", "sent.last_15m_bytes": "0", "sent.last_30m_bytes": "0", "tcp_retransmission.percent": 0, "tcp_retransmission.packets": "0", "tcp_retransmission.bytes": "0", "tcp_retransmission.last_5m_bytes": "0", "tcp_retransmission.last_15m_bytes": "0", "tcp_retransmission.last_30m_bytes": "0", "variables_count": null, "device_id": "FIREEYE-DOMAIN", "properties": {}, "custom_fields": {}, "bpf_filter": "ip host 172.30.xxx.xxx", "device_modules": {}, "capture_device": "em1"}}]
```



#### List Vulnerabilities
List vulnerabilities discovered by Nozomi device based on the provided action input parameters.  Note: Action is not working with Siemplify entities, only with action input parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IP Address|List vulnerabilities for the provided ip address. Parameter accepts multiple values as a comma separated string.|False|String||
|CVE Score|Minimum CVE score vulnerability should have to be listed, score can be a number from 0 to 10.|False|String||
|Vulnerability Name Contains|Specify a string that vulnerability name should contain to be listed.|False|String||
|CVE ID|If you know specific CVE to look for, provide the related id in this field, for example, CVE-2020-1207. Parameter accepts multiple values as a comma separated string.|False|String||
|Record Limit|Can be used to specify how many records can be returned by the action.|True|String|25|
|Include vulnerabilities that marked as resolved?|Specify whether action should also return vulnerabilities that are marked as resolved.|False|Boolean|false|



##### JSON Results
```json
[{"id": "e1c0edf3-8447-4558-ac5c-9df7dd0xxxxx", "node_id": "172.30.xxx.xxx", "cve": "CVE-2020-xxxx", "cve_summary": "An elevation of privilege vulnerability exists when the Windows CSC Service improperly handles memory.To exploit this vulnerability, an attacker would first have to gain execution on the victim system, aka Windows CSC Service Elevation of Privilege Vulnerability. This CVE ID is unique from CVE-2020-xxxx.", "cve_score": 4.6, "cve_creation_time": 1584015300000, "cve_update_time": 1584432720000, "time": 1598981272597, "cwe_id": "269", "cwe_name": "Improper Privilege Management", "matching_cpes": ["cpe:/o:microsoft:windows_server_2016:-:-:-"], "cve_references": [{"name": "https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2020-xxxx", "reference_type": "VENDOR_ADVISORY", "source": "MISC", "url": "https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2020-xxxx"}], "likelihood": 0.4, "resolved": false, "resolved_reason": "", "resolved_source": null, "installed_on": null, "appliance_id": "", "appliance_ip": "", "appliance_host": "", "zone": "Internal"}, {"id": "a9f77ae2-2434-4e06-874b-3558554xxxxx", "node_id": "172.30.xxx.xxx", "cve": "CVE-2020-xxxx", "cve_summary": "An information disclosure vulnerability exists in the way that the Windows Graphics Device Interface (GDI) handles objects in memory, allowing an attacker to retrieve information from a targeted system, aka Windows GDI Information Disclosure Vulnerability. This CVE ID is unique from CVE-2020-xxxx, CVE-2020-xxxx, CVE-2020-xxxx.", "cve_score": 2.1, "cve_creation_time": 1590088500000, "cve_update_time": 1590489180000, "time": 1602573657354, "cwe_id": "200", "cwe_name": "Information Exposure", "matching_cpes": ["cpe:/o:microsoft:windows_server_2016:-:-:-"], "cve_references": [{"name": "https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2020-xxxx", "reference_type": "VENDOR_ADVISORY", "source": "MISC", "url": "https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2020-xxxx"}], "likelihood": 0.4, "resolved": false, "resolved_reason": "", "resolved_source": null, "installed_on": null, "appliance_id": "", "appliance_ip": "", "appliance_host": "", "zone": "Internal"}]
```



#### Ping
Test connectivity to the Nozomi Networks instance with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Run a CLI Command
Run a CLI command on Nozomi Networks device. Note: Nozomi API doesnt provide a validation for executed CLI commands, its up to the User to make sure that the provided CLI command is correct. Note2: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|CLI Command|Specify a CLI Command to execute on Nozomi Networks device.  Note: Nozomi API doesnt provide a validation for executed CLI commands, its up to the User to make sure that the provided CLI command is correct.|True|String||



#### Run a Query
Run a query on Nozomi Networks device. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify a query to execute on Nozomi Networks device, for example: alerts | head 10|True|String||
|Record Limit|Can be used to specify how many records can be returned by the action. If default value of 10 is set, parameter adds “| head 10” to the final query to limit the number of returned records. If nothing is provided for the parameter - all query results are returned. Negative values are ignored.|False|String|10|



##### JSON Results
```json
[{"id": "4c6f3727-ffc1-40a8-a879-2eab19fxxxxx", "type_id": "VI:NEW-ARP", "name": "New ARP", "description": "New ARP packet from node with MAC address 00:50:56:a2:xx:xx and IP address 172.30.xxx.xxx", "severity": 10, "mac_src": "00:50:56:a2:xxx:xx", "mac_dst": "ff:ff:ff:ff:ff:ff", "ip_src": "172.30.xxx.xxx", "ip_dst": null, "risk": "6.0", "protocol": "arp", "src_roles": "other", "dst_roles": "other", "time": 1596675527674, "ack": false, "id_src": "00:50:56:a2:xx:xxx", "id_dst": "ff:ff:ff:ff:ff:ff", "synchronized": false, "appliance_id": "", "port_src": null, "port_dst": null, "label_src": null, "label_dst": null, "trigger_id": null, "trigger_type": null, "appliance_host": "nozomi-n2os.local", "appliance_ip": "172.30.xxx.xxx", "transport_protocol": "ethernet", "is_security": true, "note": null, "appliance_site": null, "parents": ["2a9530ed-75fd-4bf7-8eb2-d58dd01xxxxx", "9638651c-8035-4cad-b131-d4c9d91xxxxx"], "is_incident": false, "properties": {"base_risk": 4, "from_id": "00:50:56:a2:xxx:xx", "is_dst_node_learned": true, "is_dst_reputation_bad": false, "is_src_node_learned": false, "is_src_reputation_bad": false, "to_id": "ff:ff:ff:ff:ff:ff"}, "created_time": 1596675527674, "incident_keys": [], "bpf_filter": "ether host 00:50:56:a2:xx:xx and ether host ff:ff:ff:ff:ff:ff and ether proto 0x0806", "closed_time": 0, "status": "open", "session_id": "154400:50:56:a2:xx:xxxff:ff:ff:ff:ff:ff0000173002xxxxx", "replicated": false, "capture_device": "em1", "threat_name": "", "type_name": "New ARP", "sec_profile_visible": true, "zone_src": "Layer2", "zone_dst": "Layer2"}, {"id": "7715c90a-60e6-4180-bf01-f08ad69xxxxx", "type_id": "VI:NEW-ARP", "name": "New ARP", "description": "New ARP packet from node with MAC address 00:50:56:a2:xxx:xx and IP address 172.30.xxx.xxx", "severity": 10, "mac_src": "00:50:56:a2:xx:xx", "mac_dst": "ff:ff:ff:ff:ff:ff", "ip_src": "172.30.xxx.xxx", "ip_dst": null, "risk": "6.0", "protocol": "arp", "src_roles": "other", "dst_roles": "other", "time": 1601690812945, "ack": false, "id_src": "00:50:56:a2:xxx:xxx", "id_dst": "ff:ff:ff:ff:ff:ff", "synchronized": false, "appliance_id": "", "port_src": null, "port_dst": null, "label_src": null, "label_dst": null, "trigger_id": null, "trigger_type": null, "appliance_host": "nozomi-n2os.local", "appliance_ip": "172.30.xxx.xx", "transport_protocol": "ethernet", "is_security": true, "note": null, "appliance_site": null, "parents": ["6d1b009a-489b-455d-9461-8c7bce7xxxxx", "f36c3de4-d3f0-4d5d-8d6a-8d17019xxxx"], "is_incident": false, "properties": {"base_risk": 4, "from_id": "00:50:56:a2:xx:xx", "is_dst_node_learned": true, "is_dst_reputation_bad": false, "is_src_node_learned": false, "is_src_reputation_bad": false, "to_id": "ff:ff:ff:ff:ff:ff"}, "created_time": 1601690812945, "incident_keys": [], "bpf_filter": "ether host 00:50:56:a2:xxx:xx and ether host ff:ff:ff:ff:ff:ff and ether proto 0x0806", "closed_time": 0, "status": "open", "session_id": "154400:50:56:xxx:xxx:abff:ff:ff:ff:ff:ff0000174ecxxxxxx", "replicated": false, "capture_device": "em1", "threat_name": "", "type_name": "New ARP", "sec_profile_visible": true, "zone_src": "Layer2", "zone_dst": "Layer2"}]
```









## Connectors
#### Nozomi Networks Alerts Connector
Connector to fetch Nozomi Networks Alerts to Siemplify.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|Operation|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API URL|Nozomi API URL to connect to.|True|String|https://x.x.x.x:port|
|Username|Nozomi account username to use for connection.|True|String||
|Password|Nozomi account password to use for connection.|True|Password|*****|
|Verify SSL|Specify whether API URL certificate should be validated before connection.|False|Boolean|false|
|CA Certificate File|CA Certificate File - parsed into Base64 String.|False|String||
|Minimum severity to fetch|Minimum severity alert should have to be ingested, severity can be a number from 0 to 10.|False|Integer||
|Ingest only alerts that have “is_security” attribute set to True?|Specify if only alerts that have “is_security” attribute set to True should be ingested.|False|Boolean|false|
|Ingest only alerts that have “is_incident” attribute set to True?|Specify if only alerts that have “is_incident” attribute set to True should be ingested.|False|Boolean|false|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Integer|8|
|Fetch Backwards Time Interval (minutes)|Time interval connector should use to fetch alerts from max hours backwards. If Nozomi Device is deployed in a large network, the number of generated alerts can be substantial. Because of this, this parameter in minutes can be used to split max hours backwards on smaller segments and process them individually. Time interval cant be bigger than max hours backwards value.|True|Integer|60|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




