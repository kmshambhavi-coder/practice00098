
# InfobloxThreatDefenseWithDDI

Infoblox is a leading provider of secure cloud-managed network services that provide visibility and control over who and what connects to your network. The platform combines DNS, DHCP, and IP Address Management (DDI) with advanced security and threat defense capabilities. In case of any queries, please reach out to support@infoblox.com

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|http://csp.infoblox.com|
|API Key|A unique identifier used to authenticate and authorize access to the API.|True|Password|*****|
|Verify SSL|Verify SSL.|False|Boolean|true|


#### Dependencies
| |
|-|
|anyio-4.9.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|typing_extensions-4.14.1-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|protobuf-6.31.1-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|TIPCommon-1.1.9.2-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|google_api_python_client-2.177.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|certifi-2025.7.14-py3-none-any.whl|


## Actions
#### Create Custom List
Creates a new custom list for use in security policies.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the Custom List to create.|True|String| |
|Type|Specify the type of Custom List to create.|True|String|custom_list|
|Items|Specify comma-separated items to include in the Custom List.|False|String|None|
|Description|Description of Custom List.|False|String|None|
|Confidence Level|Specify the confidence level for this list.|False|List|High|
|Threat Level|Specify the threat level for this list.|False|List|Low|
|Tags|Add tags to categorize and organize the Custom List|False|String|None|



##### JSON Results
```json
{"confidence_level": "MEDIUM", "created_time": "2025-07-07T09:01:38Z", "description": "Test action", "id": 831832, "item_count": 1, "items": ["example1.somedomain.com"], "items_described": [], "name": "test-89", "policies": [], "tags": {"Test2": "SS2"}, "threat_level": "INFO", "type": "custom_list", "updated_time": "2025-07-07T09:01:38Z"}
```



#### Create Network List
Creates a new network list to define where security policies should be applied.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the network list.|True|String| |
|Items|Specify the comma-separated items to include in the network list (e.g., IP addresses)|True|String| |
|Description|Specify a description for the network list|False|String|None|



##### JSON Results
```json
{"created_time": "2025-07-02T06:03:25Z", "description": "Test Network List 1 Description", "id": 1858966, "item_approvals": [], "items": ["192.0.2.0/24", "192.0.3.0/24"], "name": "tesst-1", "policy_id": 204970, "updated_time": "2025-07-02T06:03:25Z"}
```



#### Create Security Policy
Creates a new security policy.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Specify the name of the security policy to create.|True|String| |
|Description|Specify description for this security policy.|False|String|None|
|Rules|Specify security rules as a list of JSON objects, each with action, type, data, policy_name and redirect_name.|False|String|None|
|Network Lists|Specify the comma-separated network lists to associate with this policy (e.g 522436, 522438).|False|String|None|
|DFPS|Specify the comma-separated DNS Forwarding Proxies to associate with this policy (e.g 12456, 12458).|False|String|None|
|Roaming Device Groups|Specify the comma-separated Roaming Device Groups to associate with this policy (e.g 56312, 56316).|False|String|None|
|Block DNS Rebinding|Specify whether to block DNS rebinding attacks.|False|Boolean|false|
|Safe Search|Specify whether to enable safe search filtering.|False|Boolean|false|
|Tags|Add tags used to categorize and organize the Security Policy.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to update (precedence, access_codes, doh_enabled, doh_fqdn, ecs, onprem_resolve, dfp_services, etc).|False|String|None|



##### JSON Results
```json
{"access_codes": ["7TYWLZ"], "block_dns_rebind_attack": false, "created_time": "2025-07-10T09:15:56Z", "default_action": "action_allow", "default_redirect_name": "", "description": "", "dfp_services": [], "dfps": [], "doh_enabled": false, "doh_fqdn": "", "ecs": false, "id": 226393, "is_default": false, "migration_status": {"uses_legacy_feeds": true}, "name": "Policy09", "net_address_dfps": [], "network_lists": [], "onprem_resolve": false, "precedence": 28, "roaming_device_groups": [], "rules": [{"action": "action_block", "data": "suspicious", "description": "Suspicious destinations: Enables protection against hostnames that have not been directly linked to malicious behavior but behave in a manner that suggests malicious behavior may be imminent.", "type": "named_feed"}, {"action": "action_allow", "data": "Default Allow", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_block", "data": "Default Block", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_block", "data": "suspicious-lookalikes", "description": "These are domains that appear to impersonate other trusted domains, but have demonstrated enough abnormal behavior to warrant concern.", "type": "named_feed"}, {"action": "action_block", "data": "base", "description": "Suspicious/malicious as destinations: Enables protection against known hostnames such as APT, Bot, Compromised Host/Domains, Exploit Kits, Malicious Name Servers, and Sinkholes.", "type": "named_feed"}, {"action": "action_log", "data": "antimalware", "description": "Suspicious/malicious as destinations: Enables protection against known malicious hostname threats that can take action on or control of your systems, such as Malware Command & Control, Malware Download, and active Phishing sites.", "type": "named_feed"}, {"action": "action_block", "data": "malware-dga", "description": "Suspicious/malicious as destinations: Domain generation algorithm (DGA) are algorithms seen in various families of malware that are used to periodically generate a large number of domain names that can be used as rendezvous points with their command and control servers. Examples include Ramnit, Conficker, and Banjori.", "type": "named_feed"}, {"action": "action_block", "data": "ransomware", "description": "Suspicious/malicious as destinations: Enables protection against ransomware taking over your system. Ransomware will encrypt files on your system and require you to pay in order to get them decrypted. This feed prevents ransomware to contact the servers which it needs to encrypt your files.", "type": "named_feed"}, {"action": "action_block", "data": "public-doh-ip", "description": "The Public DOH IP feed provides a list of known public DNS services that tunnel their traffic over HTTP. This may be from a browser (such as Mozilla Firefox), a piece of malware, or a user attempting to bypass your organization's DNS policies. This feed contains \u201ccanary\u201d addresses. We recommend all organizations enable this blocking rule.", "type": "named_feed"}, {"action": "action_block", "data": "suspicious-noed", "description": "These are High Risk, New Domains. These domains have only recently become active, and share one or more characteristics with other known malicious domains to warrant concern.", "type": "named_feed"}, {"action": "action_log", "data": "tor-exit-node-ip", "description": "Not necessarily malicious, but may be blocked based on company policy. Tor Exit Nodes are the gateways where encrypted Tor traffic hits the Internet. This means an exit node can be used to monitor Tor traffic (after it leaves the onion network). It is in the design of the Tor network that locating the source of that traffic through the network should be difficult to determine.", "type": "named_feed"}, {"action": "action_block", "data": "public-doh", "description": "The Public DOH feed provides a list of known public DNS services that tunnel their traffic over HTTP. This may be from a browser (such as Mozilla Firefox), a piece of malware, or a user attempting to bypass your organization's DNS policies. This feed contains \u201ccanary\u201d domains. We recommend all organizations enable this blocking rule.", "type": "named_feed"}, {"action": "action_log", "data": "noed", "description": "These are recently created and newly active domain names. These are not necessarily suspicious but some may wish to log traffic going to these domains as there is a low likelihood that these domains would be visited normally.", "type": "named_feed"}, {"action": "action_log", "data": "Threat Insight - DGA", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_log", "data": "Threat Insight - Data Exfiltration", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_log", "data": "Threat Insight - DNS Messenger", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_log", "data": "antimalware-ip", "description": "Suspicious/malicious as destinations: Enables protection against known malicious or compromised IP addresses. These are known to host threats that can take action on or control of your systems, such as Malware Command & Control, Malware Download, and active Phishing sites.", "type": "named_feed"}, {"action": "action_log", "data": "dhs-ais-domain", "description": "Suspicious/malicious as destinations: The Department of Homeland Security's (DHS) Automated Indicator Sharing (AIS) program enables the exchange of cyber threat indicators between the Federal Government and the private sector. AIS is a part of the Department of Homeland Security's effort to create an ecosystem where as soon as a company or federal agency observes an attempted compromise, the indicator is shared with AIS program partners, including Infoblox. Hostname Indicators contained in this feed are not validated by DHS as the emphasis is on velocity and volume. Infoblox does not modify or verify the indicators. However, indicators from the AIS program are classified and normalized by Infoblox to ease consumption. Data included in this feed includes AIS data subject to the U.S. Department of Homeland Security Automated Indicator Sharing Terms of Use available at https://www.us-cert.gov/ais and must be handled in accordance with the Terms of Use. Prior to further distributing the AIS data, you may be required to sign and submit the Terms of Use. Please email ncciccustomerservice@hq.dhs.gov for additional information.", "type": "named_feed"}, {"action": "action_log", "data": "Threat Insight - Notional Data Exfiltration", "description": "Auto-generated", "type": "custom_list"}, {"action": "action_log", "data": "ext-base-antimalware", "description": "Suspicious/malicious as destinations: An extension of the Base and AntiMalware feed that contains recently expired hostname indicators with an extended time-to-live (TTL) applied. The extended time-to-live (TTL) provides an extended reach of protection for the DNS FW, but may also increase the risk of false positives as some of these Base and Antimalware feed related domains and hosts may no longer be active.", "type": "named_feed"}, {"action": "action_log", "data": "ext-ransomware", "description": "Suspicious/malicious as destinations: An extension of the Ransomware feed that contains recently expired Ransomware with an extended time-to-live (TTL) applied. The extended time-to-live (TTL) provides an extended reach of protection for the DNS FW, but may also increase the risk of false positives as some of the Ransomware related domains and hosts may no longer be active.", "type": "named_feed"}, {"action": "action_log", "data": "ext-antimalware-ip", "description": "Suspicious/malicious as destinations: An extension of the AntiMalware IP feed that contains recently expired Malware IP's with an extended time-to-live (TTL) applied. The extended time-to-live (TTL) provides an extended reach of protection for the DNS FW, but may also increase the risk of false positives as some of these Malware IP's may no longer be active.", "type": "named_feed"}, {"action": "action_log", "data": "cryptocurrency", "description": "The use and mining of cryptocurrency is not inherently benign or malicious, or used exclusively by threat actors or general users. However, over the last several years, it has been increasingly used for illegal and/or fraudulent activities such as human trafficking, black market sales/purchases, and ransomware payments, and others. Cryptocurrency mining can impair system performance and risk end users and businesses to information theft, hijacking, and a plethora of other malware. This feed features threats that allow malicious actors to perform illegal and/or fraudulent activities, coinhives that allows site owners to embed cryptocurrency mining software into their webpages as a replacement to normal advertising, Cryptojacking  that allows site owners  to mine for cryptocurrency without the owner's consent, and cryptocurrency mining pools working together to mine cryptocurrency. This feed features indicators of activity which may indicate malicious or unauthorized use of resources including: coinhive which can be embed into a site owners web pages to lie cryptocurrency with the visitors permission as an alternative to web banner advertising; cryptojacking where malicious actors use in-browser mining without the victim's consent; and cryptocurrency mining pools working together to mine cryptocurrency.", "type": "named_feed"}], "safe_search": false, "scope_expr": "", "scope_tags": [], "tags": null, "updated_time": "2025-07-10T09:15:56Z", "user_groups": []}
```



#### DNS Record Lookup
Performs a DNS record query to retrieve associated IPs or domains.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DNS Record Filter|Filter DNS records by specific criteria (e.g., type==”PTR” and absolute_zone_name == “Test”).|False|String|None|
|Tag Filter|Filter DNS records by specific tags (e.g., 'nios/federation_enabled'==true).|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|
|Order By|Comma-separated JSON fields to sort the results. Use asc or desc for sort direction. Defaults to ascending. Supports dot notation for nested fields.|False|String|None|



##### JSON Results
```json
{"results": [{"absolute_name_spec": "crest.", "absolute_zone_name": "crest.", "comment": "Auto-created by Add Zone", "compartment_id": "", "created_at": "2025-05-07T09:51:55.056896Z", "delegation": null, "disabled": false, "dns_absolute_name_spec": "crest.", "dns_absolute_zone_name": "crest.", "dns_name_in_zone": "", "dns_rdata": "infoblox.localdomain.", "id": "dns/record/9fa2075a-5ec7-40af-8498-6e5d5a50dbce", "inheritance_sources": null, "ipam_host": null, "last_queried": null, "name_in_zone": "", "nios_metadata": {"federation": true, "gridId": "92b54f9e010e44c68cede2f69206b6f1", "niosKey": [".com.infoblox.dns.bind_ns$._default.crest..infoblox.localdomain"], "objType": "record_ns"}, "options": null, "provider_metadata": null, "rdata": {"dname": "infoblox.localdomain."}, "source": ["SYSTEM"], "subtype": "", "tags": {"nios/federation_enabled": "true", "nios/grid_name": "crest_Infoblox_ise", "nios/import_timestamp": "2025-05-07T09:51:42Z", "nios/imported": "true"}, "ttl": 28800, "type": "NS", "updated_at": "2025-05-07T09:51:55.056896Z", "view": "dns/view/157bbb3c-2643-4e65-a671-fb3140def66b", "view_name": "default-crest_Infoblox_ise", "zone": "dns/auth_zone/45bfdc4b-dcb5-4013-9dcc-8825d2cbd391"}, {"absolute_name_spec": "crest.", "absolute_zone_name": "crest.", "comment": "Auto-created by Add Zone", "compartment_id": "", "created_at": "2025-05-07T09:51:40.371930Z", "delegation": null, "disabled": false, "dns_absolute_name_spec": "crest.", "dns_absolute_zone_name": "crest.", "dns_name_in_zone": "", "dns_rdata": "ns.b1ddi.crest. hostmaster.crest. 1 10800 3600 2419200 900", "id": "dns/record/e58593cc-3ff6-4dd8-817c-8d02d9fd7b9f", "inheritance_sources": null, "ipam_host": null, "last_queried": null, "name_in_zone": "", "nios_metadata": {"federation": true, "gridId": "92b54f9e010e44c68cede2f69206b6f1", "niosKey": [".com.infoblox.dns.bind_soa$._default.crest"], "objType": "record_soa"}, "options": null, "provider_metadata": null, "rdata": {"expire": 2419200, "mname": "ns.b1ddi.crest.", "negative_ttl": 900, "refresh": 10800, "retry": 3600, "rname": "hostmaster@crest", "serial": 1}, "source": ["SYSTEM"], "subtype": "", "tags": {"nios/federation_enabled": "true", "nios/grid_name": "crest_Infoblox_ise", "nios/import_timestamp": "2025-05-07T09:51:42Z", "nios/imported": "true"}, "ttl": 28800, "type": "SOA", "updated_at": "2025-05-07T09:51:55.075214Z", "view": "dns/view/157bbb3c-2643-4e65-a671-fb3140def66b", "view_name": "default-crest_Infoblox_ise", "zone": "dns/auth_zone/45bfdc4b-dcb5-4013-9dcc-8825d2cbd391"}]}
```



#### Get Custom List
Retrieves the contents of a custom list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Custom List ID|Specify the ID of the Custom List to retrieve.|False|String||
|Name|The name of the custom list.|False|String|None|
|Type|The type of the custom list.|False|String|custom_list|
|Tag Filter|Filter security policy by specific tags format: '<tag_name>'='<tag_value>'.|False|String|None|
|Tag Sort Filter|Sort Custom List by Tags (e.g.: Test1).|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|



##### JSON Results
```json
{"results": [{"confidence_level": "LOW", "created_time": "2025-06-26T12:36:15Z", "description": "Named List A Description", "id": 831056, "item_count": 2, "name": "block_unblock_IP_TEST1", "policies": ["test-policy"], "tags": {}, "threat_level": "INFO", "type": "custom_list", "updated_time": "2025-07-04T12:02:36Z"}, {"confidence_level": "LOW", "created_time": "2025-04-24T12:46:56Z", "description": "Named List A Description", "id": 827783, "item_count": 3, "name": "block_unblock_IP_TEST1_UPDATED", "policies": ["New Network Policy"], "tags": {}, "threat_level": "INFO", "type": "custom_list", "updated_time": "2025-07-04T12:02:01Z"}, {"confidence_level": "HIGH", "created_time": "2024-07-03T17:36:56Z", "description": "", "id": 808094, "item_count": 19, "name": "ConfigError", "policies": ["Config Error"], "tags": null, "threat_level": "LOW", "type": "custom_list", "updated_time": "2025-05-14T09:10:19Z"}]}
```



#### Get Indicator Intel Lookup Result
Retrieves the result of a previously initiated Dossier lookup for an indicator (IP/URL/Host/Email/Hash).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Specify the Job ID of the Dossier lookup job to retrieve the results for|True|String| |



##### JSON Results
```json
{"state": "completed", "status": "success", "job_id": "72fa20c0-b846-4d35-83e9-d265971621a7", "results": [{"task_id": "f7532c64-231b-47b1-ab5d-24fe2f529e8c", "params": {"type": "host", "target": "one.one.one.one", "source": "atp"}, "status": "success", "time": 20511, "v": "3.0.0", "data": {"record_count": 1695, "threat": [{"batch_id": "206bdd2c-4913-11ee-80ef-17047141876a", "class": "InternetInfrastructure", "confidence": 100, "confidence_score": 8.1, "confidence_score_rating": "High", "confidence_score_vector": "COSIS:1.0/SR:H/POP:N/TLD:N/CP:T", "detected": "2023-09-01T22:00:15.97Z", "dga": "false", "domain": "one.one", "expiration": "2023-09-08T22:00:15.97Z", "extended": {"cyberint_guid": "c91ec6a21efa0f94347bc22b7c823bdd", "no_whitelist": "true", "notes": "Associated with DoHService Operated by Cloudflare"}, "full_profile": "IID:IID_IRD", "host": "one.one.one.one", "id": "2071d0b7-4913-11ee-80ef-17047141876a", "imported": "2023-09-01T22:01:39.245Z", "profile": "IID", "property": "InternetInfrastructure_DoHService", "received": "2023-09-01T22:01:39.245Z", "risk_score": 0, "risk_score_rating": "None", "risk_score_vector": "RSIS:1.0/TSS:L/TLD:N/CVSS:N/EX:N/MOD:N/AVL:N/T:L/DT:L", "threat_level": 0, "threat_score": 3.9, "threat_score_rating": "Low", "threat_score_vector": "TSIS:1.0/AV:N/AC:L/PR:N/UI:N/EX:N/MOD:N/AVL:N/CI:N/ASN:N/TLD:N/DOP:N/P:F", "tld": "one", "type": "HOST"}]}}]}
```



#### Get Network List
Retrieves the contents of a network list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Network Filter|Filter network lists by a logical expression string (e.g., name == 'net_list1').|False|String||
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|
|Network List ID|Specify the ID of the network list.|False|String|None|



##### JSON Results
```json
{"results": [{"created_time": "2024-04-01T18:27:37Z", "description": "Network List Description", "id": 1527535, "item_approvals": [{"account_id": 2007292, "address": "42.42.42.3/32", "approval_status": "AUTO_VERIFIED", "comments": "", "company_name": "Technology Alliances|Crest Data Systems - 1", "requested_at": "2024-04-29T14:38:35Z", "updated_time": "0001-01-01T00:00:00Z", "username": ""}], "items": ["42.42.42.3/32"], "name": "DoH-1", "policy_id": 207665, "updated_time": "2025-06-30T05:12:50Z"}, {"created_time": "2024-07-04T08:06:07Z", "description": "Test Network List 1 Description", "id": 1744522, "item_approvals": [{"account_id": 2007292, "address": "122.170.106.85/32", "approval_status": "AUTO_VERIFIED", "comments": "", "company_name": "Technology Alliances|Crest Data Systems - 1", "requested_at": "2025-07-01T08:59:54Z", "updated_time": "0001-01-01T00:00:00Z", "username": ""}, {"account_id": 2007292, "address": "122.170.105.85/32", "approval_status": "AUTO_VERIFIED", "comments": "", "company_name": "Technology Alliances|Crest Data Systems - 1", "requested_at": "2025-07-01T09:02:06Z", "updated_time": "0001-01-01T00:00:00Z", "username": ""}], "items": ["122.170.106.85/32", "122.170.105.85/32"], "name": "test-1", "policy_id": 218916, "updated_time": "2025-07-01T09:02:06Z"}]}
```



#### Get Security Policies
Retrieves all configured security policies and their metadata.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Policy Filter|A logical expression string to filter security policies (e.g., name== 'sec_policy_a').|False|String|None|
|Tag Filter|Filter security policy by specific tags format: '<tag_name>'='<tag_value>'.|False|String|None|
|Tag Sort Filter|Sort security policy list by Tags.|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|



##### JSON Results
```json
{"results": [{"access_codes": [], "block_dns_rebind_attack": false, "created_time": "2024-04-26T13:44:41Z", "default_action": "action_allow", "default_redirect_name": "", "description": "", "dfp_services": [], "dfps": [], "doh_enabled": false, "doh_fqdn": "", "ecs": true, "id": 207665, "is_default": false, "migration_status": {"uses_legacy_feeds": false}, "name": "CDS_Block", "net_address_dfps": [{"addr_net": "", "dfp_ids": [], "dfp_service_ids": [], "end": "10.50.7.90", "external_scope_id": "c391412b-fcad-11ee-9624-4a0e9455f8d2", "host_id": "", "ip_space_id": "29b07f2d-fca7-11ee-952b-26d521eb7155", "scope_type": "RANGE", "start": "10.50.7.83"}], "network_lists": [1527535], "onprem_resolve": true, "precedence": 8, "roaming_device_groups": [], "rules": [{"action": "action_block", "data": "Default Block", "description": "Auto-generated", "type": "custom_list"}], "safe_search": true, "scope_expr": "", "scope_tags": [], "tags": {}, "updated_time": "2025-06-26T12:28:08Z", "user_groups": []}]}
```



#### Get SOC Insights Assets
Retrieve the list of associated assets for a given Insight ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|Specify the ID of the insight to retrieve assets from.|True|String| |
|Asset IP|Filter assets by IP address.|False|String|None|
|MAC Address|Filter assets by MAC address.|False|String|None|
|OS Version|Filter assets by operating system version|False|String|None|
|User|Filter assets by associated user|False|String|None|
|Limit|Specify the maximum number of results to return|False|String|100|
|From|Filter by assets changed after this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|
|To|Filter by assets changed before this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|



##### JSON Results
```json
{"assets": [{"cmac": "00:0c:29:09:38:65", "count": 21, "qip": "10.196.217.80", "threatLevelMax": "3", "threatIndicatorDistinctCount": "20", "timeMax": "2025-06-11T04:00:00.000", "timeMin": "2025-06-11T04:00:00.000"}]}
```



#### Get SOC Insights Comments
Retrieve the list of comments available in the specified SOC insight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|ID of the insight to retrieve comments from.|True|String| |
|From|Filter by comments changed after this time in this format: YYYY-MM-DDTHH:mm:ss.SSS. |False|String|None|
|To|Filter by comments changed before this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|



##### JSON Results
```json
{"comments": [{"commentsChanger": "user.service@infoblox.invalid", "newComment": "ServiceNow incident", "dateChanged": "2025-07-07T01:08:34.082", "status": "Active"}]}
```



#### Get SOC Insights Events
Retrieve the list of events available in the specified SOC insight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|ID of the insight to retrieve events from.|True|String| |
|Device IP|Filter assets by Device IP.|False|String|None|
|Query|Filter by query string.|False|String|None|
|Query Type|Filter events by DNS query type (e.g., TXT, A, MX).|False|String|None|
|Source|Filter events by the threat intelligence source or feed (e.g., DFP (DFP)).|False|String|None|
|Indicator|Filter events by a specific threat indicator such as a domain, IP, or hash (e.g., hmdns.top).|False|String|None|
|Threat Level|Filter by threat level.|False|List|All|
|Confidence Level|Filter by confidence level.|False|List|All|
|Limit|Specify the maximum number of results to return.|False|String|100|
|From|Filter by events detected after this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|
|To|Filter by events detected before this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String||



##### JSON Results
```json
{"events": [{"confidenceLevel": "High", "source": "unknown", "action": "Allow - No Log", "policy": "DoH", "deviceIp": "34.96.34.26", "query": "soc-botnet.xhexriya.ru", "queryType": "ANY", "class": "TI-BOTNET", "threatFamily": "QTYPEANY", "detected": "2025-07-09 11:42:30 +0000 UTC", "property": "soc-botnet.xhexriya.ru", "user": "unknown", "threatLevel": "Medium"}]}
```



#### Get SOC Insights Indicators
Retrieve the list of indicators available in the specified SOC insight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Insight ID|ID of the insight to retrieve indicators from.|True|String| |
|Confidence|Filter by confidence score.|False|String|None|
|Indicator|Filter by specific indicator value.|False|String|None|
|Actor|Filter by threat actor|False|String|None|
|From|Filter by indicators seen after this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|
|To|Filter by indicators seen before this time in this format: YYYY-MM-DDTHH:mm:ss.SSS|False|String|None|
|Action|Filter by action taken.|False|String|None|
|Limit|Specify the maximum number of results to return|False|String|100|



##### JSON Results
```json
{"indicators": [{"action": "Blocked", "confidence": "3", "count": 78, "feedName": "suspicious-noed", "threatLevelMax": "3", "indicator": "hmdns.top", "timeMax": "2025-07-03T05:00:00.000", "timeMin": "2025-06-09T16:00:00.000", "actor": "abc"}]}
```



#### Host Lookup
Retrieve host information from the Infoblox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tag Filter|Filter IP addresses by specific tags (e.g. 'Tenable_scan'=='true').|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|
|Host Filter|Filter IPAM hosts by specific criteria (e.g., name=="webserver01" or ip_address=="192.168.1.100").|False|String|None|
|Order By|Comma-separated JSON fields to sort the results. Use asc or desc for sort direction. Defaults to ascending. Supports dot notation for nested fields.|False|String|None|



##### JSON Results
```json
{"page": null, "results": [{"addresses": [{"address": "10.50.1.255", "ref": "ipam/address/384ce8ac-5355-11f0-a48b-f6ee09972954", "space": "ipam/ip_space/29b07f2d-fca7-11ee-952b-26d521eb7155"}], "auto_generate_records": false, "comment": "comment-123", "created_at": "2025-06-27T13:21:04.708027Z", "host_names": [], "id": "ipam/host/93e5d665-5359-11f0-b6d1-3e4a9b62b555", "name": "temp-name", "tags": {"temptag": "true", "temptas3": "nos/de"}, "updated_at": "2025-06-27T13:21:04.708027Z"}]}
```



#### Indicator Threat Lookup With TIDE
Looks up threat intelligence details for an indicator (IP/URL/Host/Email/Hash) using Infoblox TIDE.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator Type|Specify the type of indicator to search for (Host, IP, URL, Email, Hash, All).|False|List|All|
|Indicator Value|Specify the indicator value(s) based on the indicator type you want to search for.|False|String|None|
|Domain|Specify the comma-separated domain(s) to search for.|False|String|None|
|Top-Level Domain|Specify the comma-separated top-level domain(s) to search for.|False|String|None|
|Threat Class|Specify the comma-separated threat class(es) to search for.|False|String|None|
|Target|Specify the comma-separated target(s) to search for.|False|String|None|
|Expiration|Period of time after which data is no longer considered active.|False|String|None|
|Limit|Specify the maximum number of results to return.|False|String|1000|



##### JSON Results
```json
{"threat": [{"id": "b099a146-8731-11ef-911d-47e265fc2653", "type": "IP", "ip": "1.1.1.1", "profile": "IID", "property": "InternetInfrastructure_DoHService", "class": "InternetInfrastructure", "threat_level": 0, "expiration": "2025-10-10T17:58:08.847Z", "detected": "2024-10-10T17:58:08.847Z", "received": "2024-10-10T18:01:35.775Z", "imported": "2024-10-10T18:01:35.775Z", "confidence": 100, "batch_id": "b098ddca-8731-11ef-911d-47e265fc2653", "extended": {"cyberint_guid": "de44eb0308f0f0cfc35206f96e6a7896", "no_whitelist": "true", "notes": "IP is hosting a DNS over HTTPS (DoH) domain."}}], "record_count": 1}
```



#### Initiate Indicator Intel Lookup With Dossier
Initiates an indicator (IP/URL/Host/Email/Hash) investigation using Infoblox Dossier.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator Type|Specify the type of indicator to search for (Host, IP, URL, Email, Hash).|True|List|Host|
|Indicator Value|Specify the indicator value(s) based on the indicator type you want to search for.|True|String| |
|Source|Specify the comma-separated sources to query|False|String|None|
|Wait for Results|If set to true, the call will wait for results to complete else return the jobID|False|Boolean|false|



##### JSON Results
```json
[{"status": "pending", "job_id": "72fa20c0-b846-4d35-83e9-d265971621a7", "job": {"id": "72fa20c0-b846-4d35-83e9-d265971621a7", "state": "created", "status": "pending", "create_ts": 1751285949589, "create_time": "2025-06-30T12:19:09.589260341Z", "start_ts": 1751285949589, "start_time": "2025-06-30T12:19:09.589260341Z", "request_ttl": 0, "result_ttl": 3600, "pending_tasks": ["f7532c64-231b-47b1-ab5d-24fe2f529e8c", "977a5630-72a5-4c97-9955-584931d924f0"], "org": "001SAND30ab5807046", "user": "test.user@example.com", "tasks_tbc": 0}, "tasks": {"977a5630-72a5-4c97-9955-584931d924f0": {"id": "977a5630-72a5-4c97-9955-584931d924f0", "state": "created", "status": "pending", "create_ts": 1751285949589, "create_time": "2025-06-30T12:19:09.589260341Z", "params": {"type": "host", "target": "one.one.one.one", "source": "atp"}, "results": null, "rl": false}, "f7532c64-231b-47b1-ab5d-24fe2f529e8c": {"id": "f7532c64-231b-47b1-ab5d-24fe2f529e8c", "state": "created", "status": "pending", "create_ts": 1751285949589, "create_time": "2025-06-30T12:19:09.589260341Z", "params": {"type": "host", "target": "one.one.one.one", "source": "atp"}, "results": null, "rl": false}}}, {"status": "success", "job_id": "34f53069-391e-4b4d-89fa-2372a06286e2", "job": {"id": "34f53069-391e-4b4d-89fa-2372a06286e2", "state": "completed", "status": "success", "create_ts": 1751450789352, "create_time": "2025-07-02T10:06:29.352Z", "request_ttl": 0, "result_ttl": 3600, "completed_tasks": ["9380a4e7-524c-4a60-a65d-39416b826b66"], "org": "001SAND30ab5807046", "user": "john.deo@example.com", "tasks_tbc": 0}, "tasks": {"9380a4e7-524c-4a60-a65d-39416b826b66": {"id": "9380a4e7-524c-4a60-a65d-39416b826b66", "state": "completed", "status": "success", "create_ts": 1751450789352, "create_time": "2025-07-02T10:06:29.352Z", "start_ts": 1751450790794, "start_time": "2025-07-02T10:06:30.794Z", "end_ts": 1751450791125, "end_time": "2025-07-02T10:06:31.125Z", "params": {"type": "host", "target": "one.one.one.one", "source": "geo"}, "options": {}, "results": null, "rl": false}}, "results": [{"task_id": "9380a4e7-524c-4a60-a65d-39416b826b66", "params": {"type": "host", "target": "one.one.one.one", "source": "geo"}, "status": "success", "time": 6, "v": "3.0.0", "data": {"asn_num": "13335", "city": "Sydney", "country_code": "AU", "country_name": "Australia", "isp": "Cloudflare, Inc.", "latitude": -33.8688, "longitude": 151.209, "org": "", "postal_code": "1001", "region": "New South Wales"}}]}]
```



#### IP Lookup
Retrieves IP address information from Infoblox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IP Filter|Filter IP addresses by specific criteria (e.g., address=="192.168.1.100" or state=="USED").|False|String|None|
|Address State|Filter by IP address state (e.g., ''free'', ''used'', ''any'').|False|List|Used|
|Scope|Specify the scope for IP address lookup.|False|String|None|
|Tag Filter|Filter IP addresses by specific tags (e.g. 'Tenable_scan'=='true').|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|
|Order By|Comma-separated JSON fields to sort the results. Use asc or desc for sort direction. Defaults to ascending. Supports dot notation for nested fields.|False|String|None|



##### JSON Results
```json
{"results": [{"address": "10.50.8.13", "comment": "", "compartment_id": "", "created_at": "2024-09-04T12:20:38.326472Z", "dhcp_info": null, "disable_dhcp": false, "discovery_attrs": null, "discovery_metadata": null, "external_keys": null, "host": null, "hwaddr": "", "id": "ipam/address/182225cf-6ab8-11ef-8d2e-669fd47b53f9", "interface": "", "names": [{"name": "gigavue-fm-6501", "type": "lease"}], "parent": "ipam/subnet/8abe72ce-fcad-11ee-9624-4a0e9455f8d2", "protocol": "ip4", "range": "ipam/range/fb7bfaf8-24d1-11ef-9e44-e26969575d2b", "space": "ipam/ip_space/29b07f2d-fca7-11ee-952b-26d521eb7155", "state": "used", "tags": {"Snow_cmdb_table_name": "cmdb_ci_ip_device", "Snow_sys_id": "1d9b1bde9316121027d9369d1dba1091"}, "updated_at": "2024-12-08T12:45:50.421331Z", "usage": ["DHCP LEASED", "DHCP RANGE"]}, {"address": "10.50.7.89", "comment": "", "compartment_id": "", "created_at": "2024-09-25T06:33:34.317431Z", "dhcp_info": null, "disable_dhcp": false, "discovery_attrs": null, "discovery_metadata": null, "external_keys": null, "host": null, "hwaddr": "", "id": "ipam/address/16bb0923-7b08-11ef-8e4b-861b01ad009b", "interface": "", "names": [{"name": "ce", "type": "lease"}], "parent": "ipam/subnet/8abe72ce-fcad-11ee-9624-4a0e9455f8d2", "protocol": "ip4", "range": "ipam/range/c391412b-fcad-11ee-9624-4a0e9455f8d2", "space": "ipam/ip_space/29b07f2d-fca7-11ee-952b-26d521eb7155", "state": "used", "tags": {"Snow_cmdb_table_name": "cmdb_ci_ip_device", "Snow_sys_id": "0f8b5756479212106f74bc8f016d43ed"}, "updated_at": "2024-12-08T12:45:41.024987Z", "usage": ["DHCP LEASED", "DHCP RANGE"]}]}
```



#### DHCP Lease Lookup
Looks up DHCP lease information based on specified DHCP filter criteria (such as IP address or MAC address). 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DHCP Lease Filter|Filter DHCP leases by specific criteria (e.g., address == “127.0.0.1” and hostname == “ubuntu”).|False|String|None|
|Offset|Specify the offset from where to start pagination.|False|String|0|
|Limit|Specify the maximum number of results to return.|False|String|100|
|Order By|Comma-separated JSON fields to sort the results. Use asc or desc for sort direction. Defaults to ascending. Supports dot notation for nested fields.|False|String|None|



##### JSON Results
```json
{"results": [{"address": "10.196.217.80", "client_id": "ff:29:1e:55:ab:00:01:00:01:2f:e2:5b:40:00:0c:29:1e:55:ab", "ends": "2025-06-16T05:59:11Z", "fingerprint": "VMware::Windows:", "fingerprint_processed": "processed", "ha_group": null, "hardware": "00:0c:29:1e:55:ab", "host": "dhcp/host/1516583", "hostname": "infoblox", "iaid": 0, "last_updated": "2025-06-16T04:59:11.372Z", "options": "{\"Options\":[{\"Code\":\"61\",\"Value\":\"/ykeVasAAQABL+JbQAAMKR5Vqw==\"},{\"Code\":\"12\",\"Value\":\"YmxveG9uZS1pbmZvYmxveA==\"},{\"Code\":\"50\",\"Value\":\"CsTZUA==\"},{\"Code\":\"53\",\"Value\":\"Aw==\"},{\"Code\":\"54\",\"Value\":\"CsTZtQ==\"},{\"Code\":\"55\",\"Value\":\"ARwCAw8GdwwsLxp5Kg==\"}]}", "preferred_lifetime": "2025-06-16T04:59:11Z", "protocol": "", "space": "ipam/ip_space/1f99d3a6-2982-11f0-b65e-fe20d626f7e6", "starts": "2025-06-16T04:59:11Z", "state": "used", "type": "DHCPv4"}]}
```



#### Remove Network List
Remove an existing network list from the environment
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Network List ID|Specify the ID of the network list to remove.|True|String|0|



##### JSON Results
```json
{}
```



#### Remove Security Policy
Deletes a specified security policy from the system to unblock an indicator.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Policy ID|Specify the ID of the security policy to delete.|True|String|0|



##### JSON Results
```json
{}
```



#### Update Custom List
Modifies entries in an existing custom list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the custom list to update.|False|String|None|
|Custom List ID|Specify the ID of the custom list to update.|True|String|0|
|Description|Specify description of custom list. Use keyword `empty` to remove the description|False|String|None|
|Confidence Level|Specify the confidence level for the custom list.|False|List||
|Threat Level|Specify the threat level for the custom list.|False|List||
|Tags|Add tags to categorize and organize the custom list. Use keyword `empty` to remove the tags|False|String|None|



##### JSON Results
```json
{"confidence_level": "HIGH", "created_time": "2025-07-09T10:08:24Z", "description": "Test Desc", "id": 832273, "item_count": 0, "items": [], "items_described": [], "name": "Test-1", "policies": [], "tags": {"Test1": "S2"}, "threat_level": "INFO", "type": "custom_list", "updated_time": "2025-07-09T10:33:46Z"}
```



#### Update Custom List Items
Updates the items in an existing custom list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Custom List ID|Specify the ID of the Custom List to update.|True|String|0|
|Action|Add or Remove Custom List item. (e.g Add, Remove).|True|List|Add|
|Items|Specify comma-separated items to insert or delete from the Custom List.|True|String| |



##### JSON Results
```json
{"deleted_items": [], "inserted_items": [{"description": "", "item": "193.56.2.11/32", "status": -1, "status_details": ""}, {"description": "", "item": "2001:db8:ffff:ffff:ffff:ffff:ffff:fff1/128", "status": -1, "status_details": ""}], "updated_items": []}
```



#### Update Network List
Updates an existing network list with new name, items or description. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Network List ID|Specify the ID of the network list to update.|True|String|0|
|Name|Specify the name of the network list.|False|String|None|
|Items|Specify the comma-separated items to include in the network list (e.g., IP addresses).|False|String|None|
|Description|Specify a description for the network list. Use keyword `empty` to remove the description.|False|String|None|



##### JSON Results
```json
{"created_time": "2025-07-02T06:03:25Z", "description": "Test Network List 1 Description", "id": 1858966, "item_approvals": [], "items": ["192.0.2.0/24", "192.0.3.0/24"], "name": "tesst-1", "policy_id": 204970, "updated_time": "2025-07-02T06:03:25Z"}
```



#### Ping

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Update Security Policy
Modifies an existing security policy’s configurations or linked lists.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Policy ID|Specify the ID of the security policy to update.|True|String|0|
|Policy Name|Specify the name of the security policy to update.|False|String|None|
|Description|Specify an updated description for this security policy. Use keyword `empty` to remove the description.|False|String|None|
|Network Lists|Specify the comma-separated network lists to associate with this policy (e.g 522436, 522438). Use keyword `empty` to remove the network lists.|False|String|None|
|DFPS|Specify the comma-separated Default Forwarding Policies to update. Use keyword `empty` to remove the DFPS.|False|String|None|
|Roaming Device Groups|Specify the comma-separated Roaming Device Groups to associate with this policy (e.g 56312, 56316). Use keyword `empty` to remove the devices.|False|String|None|
|Rules|Specify updated security rules as a list of JSON objects, each with action, type, data, policy_name, redirect_name. Use keyword`empty `to remove rule.|False|String|None|
|Safe Search|Specify whether to enable safe search filtering.|False|List||
|Block DNS Rebinding|Specify whether to block DNS rebinding attacks (true/false).|False|List||
|Tags|Update tags used to categorize and organize the Security Policy.|False|String|None|
|Additional Parameters|JSON object containing additional parameters to update (precedence, access_codes, doh_enabled, doh_fqdn etc).|False|String|None|



##### JSON Results
```json
{"access_codes": [], "block_dns_rebind_attack": false, "created_time": "2025-07-10T05:55:54Z", "default_action": "action_allow", "default_redirect_name": "", "description": "Desc", "dfp_services": [], "dfps": [], "doh_enabled": false, "doh_fqdn": "", "ecs": false, "id": 226360, "is_default": false, "migration_status": {"uses_legacy_feeds": true}, "name": "Test-1l", "net_address_dfps": [], "network_lists": [], "onprem_resolve": false, "precedence": 28, "roaming_device_groups": [], "rules": [{"action": "action_allow", "data": "ip_blocking_plicy.ff", "type": "named_feed"}, {"action": "action_log", "data": "ext-antimalware-ip", "description": "Suspicious/malicious as destinations: An extension of the AntiMalware IP feed that contains recently expired Malware IP's with an extended time-to-live (TTL) applied. The extended time-to-live (TTL) provides an extended reach of protection for the DNS FW, but may also increase the risk of false positives as some of these Malware IP's may no longer be active.", "type": "named_feed"}], "safe_search": false, "scope_expr": "", "scope_tags": [], "tags": {"test": "11"}, "updated_time": "2025-07-10T11:10:17Z", "user_groups": []}
```



#### Remove Custom List
Deletes a specified custom list from the system.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Custom List ID|Specify the ID of the custom list to remove.|True|String|0|



##### JSON Results
```json
{}
```









## Connectors
#### Infoblox - DNS Security Events Connector
Retrieve DNS security events from the Infoblox platform by applying various filters for investigation, enrichment, or automated response.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|300|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|tclass|
|DeviceProductField|The field name used to determine the device product|True|String|Infoblox Threat Defense with DDI|
|API Key|A unique identifier used to authenticate and authorize access to the API.|True|Password|*****|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|https://csp.infoblox.com/|
|Feed Name|Filter by comma-separated threat feed or custom list name.|False|String|None|
|Limit|Specify the maximum number of alerts to create.|False|String|100|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from for the first time.|False|String|24|
|Network|Filter by comma-separated network name, on-premises host, endpoint, or DFP name.|False|String|None|
|Policy Action|Filter by comma-separated action performed (Log, Block, Default, Redirect).|False|String|None|
|Policy Name|Filter by comma-separated security policy names.|False|String|None|
|Queried name|Filter by comma-separated queried domain names.|False|String|None|
|Threat Class|Filter by comma-separated threat category (e.g.,”Malware”, “MalwareDownload”).|False|String|None|
|Threat Family|Filter by comma-separated threat family (e.g., Log4Shell, OPENRESOLVER).|False|String|None|
|Threat Indicator|Filter by comma-separated threat indicators (domains, IPs).|False|String|None|
|Threat Level|Filter by threat severity level (LOW, MEDIUM, HIGH).|False|String|None|
|Verify SSL|Verify SSL|False|Boolean|true|


#### Infoblox - SOC Insights Connector
Retrieve all SOC Insights (Security Operations Center insights) from the Infoblox platform for investigation, enrichment, or further automated response.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|300|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|tclass|
|DeviceProductField|The field name used to determine the device product|True|String|Infoblox Threat Defense with DDI|
|API Root|The base URL of the API, used as the entry point for all API requests.|True|String|https://csp.infoblox.com/|
|API Key|A unique identifier used to authenticate and authorize access to the API.|True|Password|*****|
|Verify SSL|Enable/disable SSL certificate verification for API requests.|False|Boolean|true|
|Status|Filter Insights by their current status (ACTIVE, CLOSED).|False|String|None|
|Threat Type|Filter Insights by the type of threat detected.|False|String|None|
|Priority|Filter Insights by priority level (INFO, LOW, MEDIUM, HIGH, CRITICAL).|False|String|None|




