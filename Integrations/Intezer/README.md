
# Intezer

Intezer Integration for Google SecOps SOAR enables security teams to automate the analysis, detection, and response of threats by integrating Intezer's technology into their Google SecOps workflows

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Intezer service.|True|String|https://analyze.intezer.com/api/v2-0/|
|API key|Intezer API key|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Intezer service is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2024.8.30-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_auth-2.35.0-py2.py3-none-any.whl|
|TIPCommon-1.1.3.2-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Detonate File
Analyze a file from Splunk vault with Intezer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|Path to file for analyzing. Multiple values can be provided as a comma-separated string.|True|String||
|Related Alert ID|The alert id related to the file.|False|String||



##### JSON Results
```json
[{"analysis_id": "xxxx-xxxxx-xxxxxx-xxxxxxxx", "analysis_status": "xxxx", "analysis_type": "file", "identifier": "/tmp/abc.exe"}]
```



#### Detonate Hash
Analyze a file hash (SHA1, SHA256, or MD5) on Intezer Analyze.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Hash|Hash of the desired report. Multiple values can be provided as a comma-separated string.|False|String||



##### JSON Results
```json
[{"analysis_id": "xxxxx-xxxxxx-xxxxxxx-xxxxxxxx", "analysis_status": "xxxx", "analysis_type": "file", "identifier": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"}]
```



#### Detonate URL
Analyze a suspicious URL with Intezer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Url|URL to analyze. Multiple values can be provided as a comma-separated string.|False|String||



##### JSON Results
```json
[{"analysis_id": "xxxxx-xxxxxxx-xxxxxx-xxxxxxx", "analysis_status": "xxxx", "analysis_type": "url", "identifier": "https://www.dummy.com/"}]
```



#### Get Alert
Get an ingested alert triage and response information using alert ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The alert id to query.|True|String||
|Wait For Completion|Whether to wait for the analysis to finish.|False|Boolean|false|



##### JSON Results
```json
{"result": {"alert_id": "ldt:xxxxxx","source": "cs","sender": "cs","raw_alert": {"cid": "xxxxxx","created_timestamp": "xxxx","detection_id": "ldt:xxxxxx","device": {"device_id": "xxxxxx","cid": "xxxxxx","agent_load_flags": "0","agent_local_time": "xxx","agent_version": "xxx","bios_manufacturer": "xxxx","bios_version": "xx","config_id_base": "xxxx","config_id_build": "xxxx","config_id_platform": "x","external_ip": "xx.xx.xx.xx","hostname": "xxxxxx","first_seen": "xxxx","last_seen": "xxxx","local_ip": "xx.xx.xx.xx","mac_address": "xx-xx-xx-xx-xx-xx","major_version": "xx","minor_version": "xx","os_version": "xx","platform_id": "xx","platform_name": "Linux","product_type_desc": "Server","status": "normal","system_manufacturer": "VMware, Inc.","system_product_name": "VMware Virtual Platform","groups": ["xxxxxx"],"modified_timestamp": "xx"},"behaviors": [{"device_id": "xxxxxx","timestamp": "xxx","template_instance_id": "xx","behavior_id": "xx","filename": "bash","filepath": "/xx/xx/xxx","alleged_filetype": "","cmdline": "bash crowdstrike_test_high","scenario": "suspicious_activity","objective": "Falcon Detection Method","tactic": "Falcon Overwatch","tactic_id": "xx","technique": "Malicious Activity","technique_id": "xx","display_name": "TestTriggerHigh","description": "A high level detection was triggered on this process for testing purposes.","severity": 1,"confidence": 1,"ioc_type": "","ioc_value": "","ioc_source": "","ioc_description": "","user_name": "root","user_id": "0","control_graph_id": "xx:xxxxxx:xxx","triggering_process_graph_id": "xx:xxxxxx:xxx","sha256": "xxxxxx","md5": "xxxxxx","parent_details": {"parent_sha256": "xxxxxx","parent_md5": "xxxxxx","parent_cmdline": "/bin/sh -c ./xxx.sh","parent_process_graph_id": "pid:xxxxxx:xxxx"},"pattern_disposition": 0,"pattern_disposition_details": {"indicator": false,"detect": false,"inddet_mask": false,"sensor_only": false,"rooting": false,"kill_process": false,"kill_subprocess": false,"quarantine_machine": false,"quarantine_file": false,"policy_disabled": false,"kill_parent": false,"operation_blocked": false,"process_blocked": false,"registry_operation_blocked": false,"critical_process_disabled": false,"bootup_safeguard_enabled": false,"fs_operation_blocked": false,"handle_operation_downgraded": false,"kill_action_failed": false,"blocking_unsupported_or_disabled": false,"suspend_process": false,"suspend_parent": false}}],"email_sent": false,"first_behavior": "2023-11-09T00:03:02Z","last_behavior": "2023-11-09T00:03:02Z","max_confidence": 100,"max_severity": 70,"max_severity_displayname": "High","show_in_ui": true,"status": "new","hostinfo": {"domain": ""},"seconds_to_triaged": 0,"seconds_to_resolved": 0,"behaviors_processed": ["pid:xxxx:xxx:xxx"],"date_updated": "2023-11-09T00:06:14Z"},"alert_sub_types": [],"alert": {"alert_id": "ldt:xxxxxx","alert_url": null,"creation_time": "2023-11-09T00:06:14","alert_title": "ldt:xxxxxx","device": {},"creation_time_display": "xx"},"triage_result": {"alert_verdict": "audited","risk_category": "audited","risk_level": "informational","risk_score": 60,"risk_level_display": "Informational","risk_category_display": "Audited","alert_verdict_display": "Audited"},"response": {"status": "no_action_needed","automated_response_actions": [],"user_recommended_actions": [],"user_recommended_actions_display": "","status_display": "No Action Needed"},"note": "xxx","source_display": "CrowdStrike","source_type": "edr","intezer_alert_url": "https://analyze.intezer.com/alerts/ldt:xxxxxx"},"status": "succeeded"}
```



#### Get File Report
Get a file analysis report based on an analysis ID or a file hash.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Analysis ID|Specify a comma-separated list of File Analysis IDs to run the action on. Analysis ID is case sensitive. Note: if both "Analysis ID" and "File Hash" are provided, then "File Hash" value will have priority. Multiple values can be provided as a comma-separated string.|False|String|None|
|File Hash|Specify a comma-separated list of file hashes to run the action on. File Hash is case sensitive. Note: if both "Analysis ID" and "File Hash" are provided, then "File Hash" value will have priority. Multiple values can be provided as a comma-separated string.|False|String|None|
|Private Only|Whether to show only private reports (relevant only for hashes).|False|Boolean|false|
|Wait For Completion|Whether to wait for the analysis to complete before returning the report.|False|Boolean|false|



##### JSON Results
```json
[{"analysis_id": "fxxxx", "analysis_type": "file", "analysis_status": "succeeded", "analysis_content": {"analysis": {"analysis_id": "fxxxx", "analysis_time": "xxxx", "analysis_url": "https://analyze.intezer.com/analyses/fxxxx", "file_name": "file_name", "is_private": true, "sha256": "xxxx", "sub_verdict": "xxx", "verdict": "unknown"}, "iocs": {"files": [{"analysis_id": "fxxxx", "family": null, "path": "file_name", "sha256": "xxxx", "type": "main_file", "verdict": "unknown"}], "network": [{"classification": "suspicious", "ioc": "x.x.x.x", "source": ["Network communication"], "type": "ip"}]}, "ttps": [{"data": [{"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}, {"cid": 1, "pid": 1, "type": "xx"}], "description": "xxxxx.", "name": "xxx", "severity": 2, "ttps": [{"name": "xxx", "ttp": "xxx"}]}], "metadata": {"file_type": "xxx", "indicators": [{"classification": "informative", "name": "non_executable"}], "md5": "xxxx", "sha1": "xxx", "sha256": "xxxx", "size_in_bytes": 21, "ssdeep": "xxx"}, "root-code-reuse": null}}]
```



#### Get URL Report
Get a URL analysis report based on a URL analysis ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Analysis ID|Specify a comma-separated list of URL Analysis IDs to run the action on. Analysis ID is case sensitive. The analysis ID is returned when submitting a URL for analysis. Multiple values can be provided as a comma-separated string.|True|String||
|Wait For Completion|Whether to wait for the analysis to finish.|False|Boolean|false|



##### JSON Results
```json
[{"analysis_id": "xxxx", "analysis_type": "xxx", "analysis_status": "xxx", "analysis_content": {"analysis": {"analysis_id": "xxxx", "analysis_time": "xxx", "analysis_url": "https://analyze.intezer.com/url/xxxx", "api_void_risk_score": 0, "certificate": {"issuer": "Go Daddy Secure Certificate Authority - G2", "protocol": "xxx", "subject_name": "analyze.intezer.com", "valid_from": "xxxx", "valid_to": "xxxx"}, "domain_info": {"creation_date": "xxxx", "domain_name": "intezer.com", "registrar": "xxx"}, "indicators": [{"classification": "informative", "indicator_info": "text/html", "indicator_type": "content_type", "text": "Content type: text/html"}, {"classification": "informative", "indicator_type": "valid_https", "text": "Valid https"}, {"classification": "informative", "indicator_type": "url_accessible", "text": "URL is accessible"}, {"classification": "xx", "indicator_type": "empty_page_title", "text": "Has empty page title"}, {"classification": "informative", "indicator_type": "domain_ipv4_assigned", "text": "Assigned IPv4 domain"}, {"classification": "informative", "indicator_type": "domain_ipv4_valid", "text": "xx IPv4 domain"}, {"classification": "informative", "indicator_type": "xxx", "text": "Uses xxx"}], "ip": "xx.xx.xx.xx", "redirect_chain": [{"response_status": 200, "url": "https://analyze.intezer.com/"}], "scanned_url": "https://analyze.intezer.com/", "submitted_url": "https://analyze.intezer.com", "summary": {"description": "No suspicious activity was detected for this URL", "main_connection_gene_count": 0, "main_connection_gene_percentage": 0.0, "title": "No Threats", "verdict_name": "no_threats", "verdict_type": "no_threats"}}}}]
```



#### Index File
Index the file's genes into the organizational database.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index As|Index as trusted or malicious|True|List|trusted|
|SHA256|Sha256 to index. Multiple values can be provided as a comma-separated string.|False|String||
|Family Name|Family name to index as|False|String||



##### JSON Results
```json
[{"index_id": "xxxx", "status": "succeeded"}]
```



#### Ping
Test connectivity to the Intezer with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Submit Alert
Submit a new alert including the raw alert information to Intezer for processing.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source|The source of the alert|True|String|alert source|
|Raw Alert|Alert raw data in JSON format|True|String|JSON format|
|Alert Mapping|Mapping to use for the alert in JSON format|True|String|JSON format|



##### JSON Results
```json
{"alert_id": "ldt:xxxxxxxxxxxxxxxxxxxx:xxxxxxxxxxxxxx"}
```



#### Submit File
Submit a file for analysis.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|The paths of the file to analyze.|True|String|None|



##### JSON Results
```json
{"/tmp/abc.txt": {"analysis_id": "xxxx", "file_name": "xxxx", "sub_verdict": "xxxx", "analysis_url": "https://analyze.intezer.com/analyses/xxxxx", "verdict": "trusted", "sha256": "xxxxx", "is_private": true, "analysis_time": "Xxx, xx Xxx xxxx xx:xx:xx GMT"}}
```



#### Submit Hash
Submit a hash for analysis.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"family_name": "Turla", "analysis_id": "548e6b8b-20b1-445c-9922-af6b52a8abc3", "sub_verdict": "known_malicious", "analysis_url": "https://analyze.intezer.com/#/analyses/548e6b8b-20b1-445c-9922-af6b52a8abc3", "verdict": "malicious", "sha256": "4e553bce90f0b39cd71ba633da5990259e185979c2859ec2e04dd8efcdafe356", "is_private": true, "analysis_time": "Thu, 14 Feb 2019 08:58:27 GMT"}, "Entity": "4e553bce90f0b39cd71ba633da5990259e185979c2859ec2e04dd8efcdafe356"}]
```



#### Submit Suspicious Email
Submit a suspicious phishing email in a raw format (.MSG or .EML) to Intezer for processing
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email File Path|Path to the email file|True|String|None|



##### JSON Results
```json
{"alert_id": "xxxxxx59d5xxxxxx34350xxxxxx"}
```



#### Unset Index File
Unset file's indexing.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SHA256|SHA256 file to unset the indexing. Multiple values can be provided as a comma-separated string.|False|String||



##### JSON Results
```json
{}
```









