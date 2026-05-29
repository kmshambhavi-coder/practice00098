
# FireEyeHelix

To protect against advanced threats, organizations need to integrate their security and apply the right expertise and processes. FireEye Helix is a cloud-hosted security operations platform that allows organizations to take control of any incident from alert to fix.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://helix.eu.fireeye.com/helix/id/{id}/|
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|idna-3.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|netaddr-1.3.0-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|filelock-3.15.4-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Add Entities To a List
Add Siemplify entities to the FireEye Helix list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Short Name|Specify the short name of the list.|True|String||
|Risk|Specify the risk of the items.|False|List|Medium|
|Note|Specify notes that should be added to the items.|False|String||



##### JSON Results
```json
[{"Entity": "F.ATTACKER4@GMAIL.COM", "EntityResult": {"id": "4282xxxxx", "value": "f.attacker4@gmail.com", "type": "email", "risk": "Medium", "notes": "test", "list": "83xxx"}}, {"Entity": "VICKIE.B@SIEMPLIFY.CO", "EntityResult": {"id": "4282xxxxx", "value": "vickie.b@siemplify.co", "type": "email", "risk": "Medium", "notes": "test", "list": "83xxx"}}]
```



#### Add Note To Alert
Add a Note to Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify Alert ID to add note to.|True|String||
|Note|Specify note for the alert.|True|String||



#### Archive Search
Perform archive search in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query for the search, for example: srcserver=172.30.202.130|True|String||
|Time Frame|Specify the time frame for the search. Only hours and days are supported. Note: end time will be 4 hours earlier than current time and time frame will start calculation from that point. For example, if 'Time Frame' is 3h, then the start time will be the current time - 7h, while the end time will be the current time -4h. API doesn't allow archive search to be performed on events that are only 3 hours old. This is the FireEye Helix limitation. Examples of the values: 7h - 7 hours, 1d - 1 day|True|String||
|Max Results To Return|Specify how many results to return.|False|String|100|



##### JSON Results
```json
{"dsl":{"from":0,"aggs":{"groupby:class":{"meta":{"field":"class","type":"groupby"},"terms":{"field":"class","order":{"_count":"desc"},"min_doc_count":1,"size":50}}},"terminate_after":-1,"directives":{"scroll_id":"","page_size":2,"start":"2020-09-15T14:00:00.000Z","highlight_terms":[],"limit":-1,"timeout":120000,"offset":0,"indices":["events","alerts","appliance_health"],"end":"2020-09-16T14:45:54.307Z","search_customer_ids":null,"customer_id":"","scroll":false},"timeout":"120000ms","query":{"bool":{"filter":[{"range":{"meta_ts":{"gte":"2020-09-15T14:00:00.000Z","lte":"2020-09-16T14:45:54.307Z"}}},{"exists":{"field":"class"}}]}},"size":2},"mql":"has(class) | groupby class sep=`|%$,$%|`","results":{"hits":{"stored":"xx","hits":[{"_type":"event","_id":"b13xxxxx-xxxx-xxxx-a726-ac4198dxxxxx#x","_source":{"_eventid":"b13xxxxx-xxxx-xxxx-a726-ac4198dxxxxx#x","product":"hx","edition":"classic","meta_ts":"2020-09-16T14:45:01.444Z","serial":"vmware-xx xx xx xx xx 91 c5 8c-b7 94 d4 xx xx xx xx xx","statuscode":10,"category":"healthupdate","meta_rule":"appliance_health-ss-0.0.2","service_health":[{"timestamp":"2020-09-16T14:43:00.000Z","servicecount":{"healthy":2,"total":2}},{"timestamp":"2020-09-16T14:38:00.000Z","servicecount":{"healthy":2,"total":2}},{"timestamp":"2020-09-16T14:33:00.000Z","servicecount":{"healthy":2,"total":2}}],"version":"1.0","metaclass":"health","mode":"2way","status":"ok","eventtime":"2020-09-16T14:45:00.000Z","devicename":"fireeyehx","meta_deviceid":"86B7F11xxxxx","devicetype":"fireeyehx2502v","deployment":"onpremise","class":"appliance_health","__metadata__":{"received":"2020-09-16T14:45:01.000Z","raw_batch_id":"b13xxxxx-xxxx-xxxx-a726-ac4198dxxxxx","data_type":"passthrough","disable_index":false,"dynamic_taxonomy":true,"num_events":1,"source_type":"json","target_index":"appliance_health","batch_id":"b13xxxxx-xxxx-xxxx-a726-ac4198dxxxxx","customer_id":"hexqxxxxx","id":"b13xxxxx-xxxx-xxxx-a726-ac4198dxxxxx#x","sequence_number":0},"appliance":{"domainName":"fireeye-lab.local","systemType":"virtual","compositeVersion":"hx hx (hx) 5.0.1.917137 #917137 2020-07-07 22:45:00 x86_64 build@vta414:fireeye/hx-5.0.x","dtiEnabled":"true","components":{"upTime":{"status":"ok","upTimeDuration":"30d 4h 50m 54s","upTimeMilliSeconds":"2609454848","name":"uptime"},"dbDisk":{"status":"ok","deviceName":"/dev/sda9","bytesTotal":"316932882432","name":"dbdisk","bytesUsed":"273215488","fsType":"ext4","bytesAvail":"300536766464","bytesFree":"316659666944","percentFree":"99"},"raid":{"status":"ok","name":"raid"},"usb":{"status":"ok","mounted":"false","name":"usb"},"cmsConnection":{"status":"ok","name":"cmsconnection","lastFormedAt":"unknown","connected":"unknown","lastAttemptedAt":"2020/08/17 09:56:12","lastBrokenAt":"unknown","failureReason":"none","brokenReason":"have not connected yet"},"location":{"status":"ok","timezone":"etc/utc","utc_offset":"0","name":"location","geoLocation":"unknown"},"service_health":{"status":"ok","health_metrics":[{"timestamp":"2020-09-16T14:43:00.000Z","services_status":[{"status":"healthy","service_id":"diskio","category":"system","name":"disk storage","details":{"text":"healthy"}},{"status":"healthy","service_id":"interface_health","category":"system","name":"ethernet interfaces","details":{"text":"healthy"}}]},{"timestamp":"2020-09-16T14:38:00.000Z","services_status":[{"status":"healthy","service_id":"diskio","category":"system","name":"disk storage","details":{"text":"healthy"}},{"status":"healthy","service_id":"interface_health","category":"system","name":"ethernet interfaces","details":{"text":"healthy"}}]},{"timestamp":"2020-09-16T14:33:00.000Z","services_status":[{"status":"healthy","service_id":"diskio","category":"system","name":"disk storage","details":{"text":"healthy"}},{"status":"healthy","service_id":"interface_health","category":"system","name":"ethernet interfaces","details":{"text":"healthy"}}]}],"name":"services health"},"physicalDisksda":{"status":"ok","name":"physicaldisksda","desc":"virtual machine, status may not be applicable"},"fireeyeSupportLicense":{"status":"ok","expiresInSeconds":"16967700","name":"fireeyesupportlicense","license":"fireeye_support","perpetual":"no","expDate":"2021/04/01 00:00:00","expInDays":"196"},"securityContent":{"status":"ok","lastUploadFailed":"false","name":"securitycontent","lastUpdateTime":"2020/09/15 10:38:35","timestamp":"2020-09-15T05:46:36.000Z","version":"426.101"},"configDisk":{"status":"ok","deviceName":"/dev/sda7","bytesTotal":"511461376","name":"configdisk","bytesUsed":"4665344","fsType":"ext4","bytesAvail":"475761664","bytesFree":"506796032","percentFree":"99"},"eula":{"status":"ok","accepted":"true","acceptedTime":"2020/05/28 05:35:54","name":"eula"},"systemSoftware":{"status":"ok","currentVersion":"5.0.1","name":"systemsoftware"},"fireeyeApplianceLicense":{"status":"ok","perpetual":"yes","name":"fireeyeappliancelicense","license":"fireeye_appliance"},"address":{"status":"ok","ipv4":"172.xx.xxx.xxx","hostName":"fireeyehx","ipv6Enabled":"false","domainName":["fireeye-lab.local"]},"contentUpdatesLicense":{"status":"ok","expiresInSeconds":"16967700","name":"contentupdateslicense","license":"content_updates","perpetual":"no","expDate":"2021/04/01 00:00:00","expInDays":"196"},"dataDisk":{"status":"ok","deviceName":"/dev/sda11","bytesTotal":"795835797504","name":"datadisk","bytesUsed":"4354248704","fsType":"ext4","bytesAvail":"751031685120","bytesFree":"791481548800","percentFree":"99"},"varDisk":{"status":"ok","deviceName":"/dev/sda8","bytesTotal":"101327228928","name":"vardisk","bytesUsed":"1358991360","fsType":"ext4","bytesAvail":"94797504512","bytesFree":"99968237568","percentFree":"98"},"hxRole":{"status":"ok","role":"master"},"hxAdvancedLicense":{"status":"ok","expiresInSeconds":"16967700","name":"hxadvancedlicense","license":"hx_advanced","perpetual":"no","expDate":"2021/04/01 00:00:00","expInDays":"196"},"rootDisk":{"status":"ok","deviceName":"/dev/sda5","bytesTotal":"4160356352","name":"rootdisk","bytesUsed":"2905587712","fsType":"ext4","bytesAvail":"1023246336","bytesFree":"1254768640","percentFree":"30"}},"timezone":"etc/utc","customerId":"4xxxxx"},"reason":"periodic","client":"hx (hx) 5.x.1.9xxxxx","deviceid":"86b7f11xxxxx"},"_index":"archive"},{"_type":"event","_id":"e50xxxxx-xxxx-xxxx-814b-287a3adxxxxx#x","_source":{"_eventid":"e50xxxxx-xxxx-xxxx-814b-287a3adxxxxx#x","product":"cms","edition":"classic","meta_ts":"2020-09-16T14:45:01.803Z","serial":"vmware-xx xx xx xx xx 88 21 72-65 8d f9 xx xx xx xx xx","statuscode":10,"category":"healthupdate","meta_rule":"appliance_health-ss-0.0.2","service_health":[{"timestamp":"2020-09-16T14:44:00.000Z","servicecount":{"healthy":7,"disabled":1,"total":8}}],"version":"1.0","metaclass":"health","mode":"2way","status":"ok","eventtime":"2020-09-16T14:45:00.000Z","devicename":"fireeye-cm","meta_deviceid":"86F781Dxxxxx","devicetype":"fireeyecm2500v","class":"appliance_health","__metadata__":{"received":"2020-09-16T14:45:01.000Z","raw_batch_id":"e50xxxxx-xxxx-xxxx-814b-287a3adxxxxx","data_type":"passthrough","disable_index":false,"dynamic_taxonomy":true,"num_events":1,"source_type":"json","target_index":"appliance_health","batch_id":"e50xxxxx-xxxx-xxxx-814b-287a3adxxxxx","customer_id":"hexqxxxxx","id":"e50xxxxx-xxxx-xxxx-814b-287a3adxxxxx#x","sequence_number":0},"appliance":{"domainName":"siemplifylab.local","systemType":"virtual","compositeVersion":"cms cms (cms) 9.0.0.916210 #916210 2020-06-19 09:23:22 x86_64 build@vta467:fireeye/9.0.x-denali","dtiEnabled":"true","components":{"upTime":{"status":"ok","upTimeDuration":"42d 2h 30m 16s","upTimeMilliSeconds":"3637816576","name":"uptime"},"dbDisk":{"status":"ok","deviceName":"/dev/sda9","bytesTotal":"257893908480","name":"dbdisk","bytesUsed":"2475343872","fsType":"ext4","bytesAvail":"242294591488","bytesFree":"255418564608","percentFree":"99"},"raid":{"status":"ok","name":"raid"},"usb":{"status":"ok","mounted":"false","name":"usb"},"service_health":{"status":"ok","health_metrics":[{"timestamp":"2020-09-16T14:44:00.000Z","services_status":[{"status":"healthy","service_id":"wsapi","category":"system","name":"wsapi service","details":{"text":"healthy"}},{"status":"disabled","service_id":"ips_sync","category":"system","name":"ips policy sync engine","details":{"text":"state information not ready yet"}},{"status":"healthy","service_id":"system_load_health","category":"system","name":"system load","details":{"text":"healthy"}},{"status":"healthy","service_id":"perfmon_health","category":"system","name":"system performance monitor","details":{"text":"healthy"}},{"status":"healthy","service_id":"fedb_external","category":"system","name":"database service","details":{"text":"healthy"}},{"status":"healthy","service_id":"fe_licenses","category":"system","name":"licenses monitoring","details":{"text":"healthy"}},{"status":"healthy","service_id":"diskio","category":"system","name":"disk storage","details":{"text":"healthy"}},{"status":"healthy","service_id":"interface_health","category":"system","name":"ethernet interfaces","details":{"text":"healthy"}}]}],"name":"services health"},"physicalDisksda":{"status":"ok","name":"physicaldisksda","desc":"virtual machine, status may not be applicable"},"fireeyeSupportLicense":{"status":"ok","expiresInSeconds":"16967699","name":"fireeyesupportlicense","license":"fireeye_support","perpetual":"no","expDate":"2021/04/01 00:00:00","expInDays":"196"},"systemSoftware":{"status":"ok","currentVersion":"9.0.0","name":"systemsoftware"},"configDisk":{"status":"ok","deviceName":"/dev/sda7","bytesTotal":"511461376","name":"configdisk","bytesUsed":"4674560","fsType":"ext4","bytesAvail":"475752448","bytesFree":"506786816","percentFree":"99"},"eula":{"status":"ok","accepted":"true","acceptedTime":"2020/05/19 18:09:45","name":"eula"},"location":{"status":"ok","timezone":"etc/utc","utc_offset":"0","name":"location","geoLocation":"unknown"},"fireeyeApplianceLicense":{"status":"ok","perpetual":"yes","name":"fireeyeappliancelicense","license":"fireeye_appliance"},"address":{"status":"ok","ipv4":"172.xx.xxx.xxx","hostName":"fireeye-cm","ipv6Enabled":"false","domainName":["siemplifylab.local"]},"contentUpdatesLicense":{"status":"ok","expiresInSeconds":"16967699","name":"contentupdateslicense","license":"content_updates","perpetual":"no","expDate":"2021/04/01 00:00:00","expInDays":"196"},"dataDisk":{"status":"ok","deviceName":"/dev/sda11","bytesTotal":"216511635456","name":"datadisk","bytesUsed":"19627397120","fsType":"ext4","bytesAvail":"185862451200","bytesFree":"196884238336","percentFree":"90"},"varDisk":{"status":"ok","deviceName":"/dev/sda8","bytesTotal":"21003517952","name":"vardisk","bytesUsed":"2675654656","fsType":"ext4","bytesAvail":"17237348352","bytesFree":"18327863296","percentFree":"87"},"rootDisk":{"status":"ok","deviceName":"/dev/sda5","bytesTotal":"4160356352","name":"rootdisk","bytesUsed":"1791291392","fsType":"ext4","bytesAvail":"2137542656","bytesFree":"2369064960","percentFree":"56"}},"timezone":"etc/utc","customerId":"4xxxxx"},"reason":"periodic","client":"cms (cms) 9.0.x.9xxxxx","deviceid":"86f781dxxxxx"},"_index":"archive"}],"total":34},"aggregations":{"groupby:class":{"limited":false,"buckets":[{"key":"appliance_health","doc_count":34}],"doc_count_error_upper_bound":0,"sum_other_doc_count":0}},"took":1518}}
```



#### Close Alert
Close Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be closed in FireEye Helix.|True|String||
|Revision Note|Specify revision note for the alert.|False|String||



#### Enrich Endpoint
Fetch endpoint's system information by its hostname.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "fireeye-domain", "EntityResult": {"risk_score": 0, "last_event_at": null, "asset_job_title": null, "severity": "Low", "cidr_range": null, "asset_status": "active", "source": "detection", "created_at": "2020-08-25T20:26:18.491515+00:00", "events_count": 0, "is_vip_asset": false, "asset_type": "Host", "asset_name": "fireeye-domain", "last_activity": "2020-08-25T20:26:18.491515+00:00", "detections": 0, "asset_uuid": "961d38e6-11c1-4c0b-b205-19f0adf00000", "location": null, "properties": {"os": "windows server 2016 standard evaluation"}, "org": "hexqsxxxx", "id": 0000000, "asset_department": null}}]
```



#### Enrich User
Fetch information about users from FireEye Helix.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "fireeye-domain", "EntityResult": {"risk_score": 0, "last_event_at": null, "asset_job_title": null, "severity": "Low", "cidr_range": null, "asset_status": "active", "source": "detection", "created_at": "2020-08-25T20:26:18.491515+00:00", "events_count": 0, "is_vip_asset": false, "asset_type": "Host", "asset_name": "fireeye-domain", "last_activity": "2020-08-25T20:26:18.491515+00:00", "detections": 0, "asset_uuid": "961d38e6-11c1-4c0b-b205-19f0adf00000", "location": null, "properties": {"os": "windows server 2016 standard evaluation"}, "org": "hexqsxxxx", "id": 0000000, "asset_department": null}}]
```



#### Get Alert Details
Retrieve information about Alert from FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be enriched in FireEye Helix.|True|String||
|Max Notes To Return|Specify how many associated notes to return.|False|String|50|



##### JSON Results
```json
{"_assignedAt": null, "_assignedTo": null, "_createdBy": {"id": "abd5feae-84fc-41e9-be61-336ec358xxxx", "avatar": "https://secure.gravatar.com/avatar/8267ad472cbc450380f270ee60d729b5", "name": "System User", "username": "system_user", "primary_email": "no.reply@fireeye.com"}, "_updatedBy": {"id": "0b48dde7-5c81-4899-978d-79354086xxxx", "avatar": "https://secure.gravatar.com/avatar/0feb076e8da5a3dff2b62cf8e53525cd", "name": "MilenIvanov", "username": "tip.labops@siemplify.co", "primary_email": "tip.labops@siemplify.co"}, "alertThreat": "Unknown", "alertType": "customer_rule", "alertTypeDetails": {"detail": {"eventid": "7256xxx", "username": "fireeye-lab\\administrator", "domain": "fedeploycheck.fireeye.com", "process": "microsoftedge.exe", "result": "alert", "msg": "normal", "metaclass": "ids", "class": "fireeye_hx_alert"}, "summary": {"metaclass": "ids", "class": "fireeye_hx_alert"}}, "classification": 0, "closedState": "Unknown", "confidence": "Low", "context": null, "createDate": "2020-09-03T14:07:25.742459Z", "customer_id": "hexqsxxxx", "description": "", "displayId": 1210972, "distinguisherKey": "", "distinguishers": {}, "emailedAt": 737671, "eventCount": 34, "eventsThreshold": 1, "firstEventAt": "2020-09-03T14:07:09.850000Z", "lastEventAt": "2020-09-03T14:20:12.495000Z", "external": [], "externalCount": 0, "externalId": "", "id": "5f50f892d746121afa03xxxx", "infoLinks": [], "internal": [], "internalCount": 0, "isThreat": false, "isTuned": false, "killChain": [], "lastSyncMs": 1599142815150, "message": "test", "notes": [{"_author": {"id": "0b48dde7-5c81-4899-978d-79354086xxxx", "avatar": "https://secure.gravatar.com/avatar/0feb076e8da5a3dff2b62cf8e53525cd", "name": "MilenIvanov", "username": "tip.labops@siemplify.co", "primary_email": "tip.labops@siemplify.co"}, "createDate": "2020-09-11T09:55:35.694905Z", "customer_id": "hexqsxxxx", "id": 50371, "updateDate": "2020-09-11T09:55:35.694905Z", "note": "עליחךלחי"}, {"_author": {"id": "0b48dde7-5c81-4899-978d-79354086xxxx", "avatar": "https://secure.gravatar.com/avatar/0feb076e8da5a3dff2b62cf8e53525cd", "name": "MilenIvanov", "username": "tip.labops@siemplify.co", "primary_email": "tip.labops@siemplify.co"}, "createDate": "2020-09-11T09:55:17.345442Z", "customer_id": "hexqsxxxx", "id": 50370, "updateDate": "2020-09-11T09:55:17.345442Z", "note": "jhgfdfd"}], "revisionNotes": "note h1", "risk": "Low", "riskOrder": 1, "search": "class=fireeye_hx_alert", "secondsThreshold": 3600, "severity": "Low", "sourceRevision": 0, "sourceUrl": "https://helix.eu.fireeye.com/helix/id/hexqsxxxx/alerts/5f50f892d746121afa03xxxx", "state": "Reopened", "suppressed": true, "tags": [], "threatChangedAt": null, "threatType": 0, "triggerId": "9999.0.3", "triggerRevision": 0, "tuningSearch": "", "updateDate": "2020-09-13T07:19:42.316049Z"}
```



#### Get List Items
Return information about FireEye Helix lists items.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Short Name|Specify the short name of the list.|True|String||
|Value|Specify value filter for the items.|False|String||
|Type|Specify type filter for the items.|False|List|ALL|
|Sort By|Specify which parameter should be used for sorting results.|False|List|Value|
|Sort Order|Specify the sorting order for the results.|False|List|Ascending|
|Max Items To Return|Specify how many items to return.|False|String|100|



##### JSON Results
```json
[{"id": "420xxxxxx", "value": "99.xx.x.x/16", "type": "misc", "risk": "Low", "notes": "", "list": "84xxx"}, {"id": "420xxxxxx", "value": "2600:xxxx:81xx::/48", "type": "misc", "risk": "Low", "notes": "", "list": "84xxx"}]
```



#### Ping
Test connectivity to the FireEye Helix with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Suppress Alert
Suppress Alert in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify ID of the Alert that needs to be suppressed in FireEye Helix.|True|String||
|Duration|Specify for how long the Alert should be suppressed in minutes.|True|String||



#### Index Search
Perform index search in FireEye Helix.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query for the search, for example: srcserver=172.30.202.130|True|String||
|Time Frame|Specify the time frame for the search. Only hours and days are supported. This is the FireEye Helix limitation. Examples of the values: 7h - 7 hours 1d - 1 day|False|String||
|Max Results To Return|Specify how many results to return.|False|String|100|



##### JSON Results
```json
{"hits": {"hits": [{"_score": 0.0, "_type": "_doc", "_id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "_source": {"srccountry": "sg", "rawmsg": {"dstip": "217.xxx.xxx.xxx", "dst_location": "Koeln", "app": "careerpassport", "object_type": "Employee", "device": "Windows PC", "id": "1xxx", "app_session_id": "20657xxxxx", "dst_region": "Nordrhein-Westfalen", "dst_country": "DE", "src_zipcode": "10010", "type": "nspolicy", "object": "James Taggart", "srcip": "8.12.xxx.x", "timestamp": 1600182083, "src_region": "Singapore", "alert": "no", "user": "Clelia.Potts@kkrlogistics.com", "from_user": "bloomberg@bloomberg.com", "src_location": "Singapore", "org": "kkrlogistics.com", "src_country": "SG", "count": 2, "dst_zipcode": null, "url": "https://www.careerpassport.eu/solutions?s=ga", "sv": "unknown", "activity": "Invite", "userip": "127.0.0.1", "os": "Windows 7", "browser": "Chrome", "organization_unit": "", "src_geoip_src": 1, "dst_geoip_src": 1, "userkey": "Clelia.Potts@kkrlogistics.com", "ur_normalized": "clelia.potts@kkrlogistics.com", "site": "careerpassport", "traffic_type": "CloudApp", "ccl": "unknown", "category": "HR", "_insertion_epoch_timestamp": 1600182298, "dst_longitude": 6.95, "dst_latitude": 50.933331, "src_longitude": 103.850067, "src_latitude": 1.28967, "_id": "1afcbbdabc3ca2xxxxxxxxxx", "cci": null, "page_id": "26331xxxxx", "appcategory": "HR"}, "site": "careerpassport", "meta_cbname": "helix-netskope", "dstregion": "nordrhein-westfalen", "meta_ts": "2020-09-15T15:10:38.801Z", "meta_cbid": "15917007xxxxx", "srclongitude": 103.850067, "srcregion": "singapore", "category": "hr", "detectedtime": "2020-09-15T15:01:23.000Z", "logonid": "clelia.potts@kkrlogistics.com", "srczipcode": "10010", "dstcountry": "de", "_errors": [{"field": "dstlocation", "message": "Invalid type: geolocation", "value": "Koeln"}, {"field": "device_type", "message": "Invalid field", "value": "Windows PC"}, {"field": "type", "message": "Unable to convert field to integer", "value": "nspolicy"}, {"field": "alerted", "message": "Unable to convert field to boolean", "value": "no"}, {"field": "srclocation", "message": "Invalid type: geolocation", "value": "Singapore"}], "dstlatitude": 50.933331, "srclatitude": 1.28967, "metaclass": "http_proxy", "eventtime": "2020-09-15T15:04:58.000Z", "dstlongitude": 6.95, "object": "james taggart", "meta_oml": "12xx", "mailbox": "clelia.potts@kkrlogistics.com", "accountname": "clelia.potts@kkrlogistics.com", "class": "netskope", "appcategory": "hr", "count": 2, "rawmsghostname": "helix-netskope-partners.goskope.com", "__metadata__": {"received": "2020-09-15T15:10:40.000Z", "raw_batch_id": "595xxxxx-3913-xxxx-80c0-dad88cbxxxxx", "data_type": "passthrough", "disable_index": false, "dynamic_taxonomy": false, "num_events": 502, "source_type": "json", "target_index": "", "batch_id": "595xxxxx-3913-xxxx-80c0-dad88cbxxxxx", "customer_id": "hexqxxxxx", "id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "sequence_number": 35}, "url": "https://www.careerpassport.eu/solutions?s=ga", "activity": "invite", "meta_rts": "2020-09-15T15:10:38.000Z", "os": "windows 7", "_eventid": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "objecttype": "employee"}, "_index": "2020-09-15t12:15:00.000z"}, {"_score": 0.0, "_type": "_doc", "_id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "_source": {"srccountry": "pr", "rawmsg": {"dstip": "69.xx.xxx.xx", "dst_location": "Markham", "app": "AA Tools for Dynamics GP Analytical Accounting", "object_type": "Dashboard", "device": "iPad", "id": "2xxx", "app_session_id": "20657xxxxx", "dst_region": "Ontario", "dst_country": "CA", "src_zipcode": "00926", "type": "nspolicy", "object": "Account Manager", "srcip": "24.xx.xx.1", "timestamp": 1600182058, "src_region": "00", "alert": "no", "user": "Aaron.Etheridge@kkrlogistics.com", "from_user": "bloomberg@bloomberg.com", "src_location": "San Juan", "org": "kkrlogistics.com", "src_country": "PR", "count": 2, "dst_zipcode": "L3P", "url": "http://www.crgroup.com/aatools", "sv": "unknown", "activity": "Delete", "userip": "127.0.0.1", "os": "iOS 7", "browser": "Safari", "organization_unit": "", "src_geoip_src": 2, "dst_geoip_src": 2, "userkey": "Aaron.Etheridge@kkrlogistics.com", "ur_normalized": "aaron.etheridge@kkrlogistics.com", "site": "AA Tools for Dynamics GP Analytical Accounting", "traffic_type": "CloudApp", "ccl": "unknown", "category": "Business Intelligence and Data Analytics", "_insertion_epoch_timestamp": 1600182298, "dst_longitude": -79.2638, "dst_latitude": 43.879, "src_longitude": -66.1057, "src_latitude": 18.4686, "_id": "59e268096e4039xxxxxxxxxx", "cci": null, "page_id": "26331xxxxx", "appcategory": "Business Intelligence and Data Analytics"}, "site": "aa tools for dynamics gp analytical accounting", "meta_cbname": "helix-netskope", "dstregion": "ontario", "meta_ts": "2020-09-15T15:10:38.801Z", "meta_cbid": "15917007xxxxx", "srclongitude": -66.1057, "srcregion": "00", "category": "business intelligence and data analytics", "detectedtime": "2020-09-15T15:00:58.000Z", "logonid": "aaron.etheridge@kkrlogistics.com", "srczipcode": "00926", "dstcountry": "ca", "_errors": [{"field": "dstlocation", "message": "Invalid type: geolocation", "value": "Markham"}, {"field": "device_type", "message": "Invalid field", "value": "iPad"}, {"field": "type", "message": "Unable to convert field to integer", "value": "nspolicy"}, {"field": "alerted", "message": "Unable to convert field to boolean", "value": "no"}, {"field": "srclocation", "message": "Invalid type: geolocation", "value": "San Juan"}], "dstlatitude": 43.879, "srclatitude": 18.4686, "metaclass": "http_proxy", "eventtime": "2020-09-15T15:04:58.000Z", "dstlongitude": -79.2638, "object": "account manager", "meta_oml": "13xx", "mailbox": "aaron.etheridge@kkrlogistics.com", "accountname": "aaron.etheridge@kkrlogistics.com", "class": "netskope", "appcategory": "business intelligence and data analytics", "count": 2, "rawmsghostname": "helix-netskope-partners.goskope.com", "__metadata__": {"received": "2020-09-15T15:10:40.000Z", "raw_batch_id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx", "data_type": "passthrough", "disable_index": false, "dynamic_taxonomy": false, "num_events": 502, "source_type": "json", "target_index": "", "batch_id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx", "customer_id": "hexqxxxxx", "id": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "sequence_number": 37}, "url": "http://www.crgroup.com/aatools", "activity": "delete", "dstzipcode": "l3p", "meta_rts": "2020-09-15T15:10:38.000Z", "os": "ios 7", "_eventid": "595xxxxx-3913-xxxx-xxxx-dad88cbxxxxx#xx", "objecttype": "dashboard"}, "_index": "2020-09-15t12:15:00.000z"}], "total": 624, "max_score": 0.0}, "_shards": {"successful": 11, "failed": 0, "skipped": 0, "total": 11}, "took": 3, "timed_out": false, "metrics": {"load": 5.283333333333334, "regex": false, "list": false, "aggregation": false, "subsearch": false}, "failures": []}
```



#### Get Lists
Return information about FireEye Helix lists.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify name filter.|False|String||
|Short Name|Specify short name filter.|False|String||
|Active|Specify, whether action should only return active lists.|False|Boolean|false|
|Internal|Specify, whether action should only return internal lists.|False|Boolean|false|
|Protected|Specify, whether action should only return protected lists.|False|Boolean|false|
|Sort By|Specify which parameter should be used for sorting results.|False|List|Name|
|Sort Order|Specify the sorting order for the results.|False|List|Ascending|
|Max Lists To Return|Specify how many lists to return.|False|String|100|



##### JSON Results
```json
[{"id": "83xxx", "short_name": "home_domain", "item_count": 1, "types": ["misc"], "created_by": {"id": "b6682a18-xxxx-48a6-xxxx-ef9axxxxxxxx", "avatar": "https://secure.gravatar.com/avatar/abb3c72c8a308e547e37a430a6f01c0d", "name": "Helix Detection", "username": "helix.detection@fireeye.com", "primary_email": "helix.detection@fireeye.com"}, "updated_by": {"id": "b6682a18-xxxx-48a6-xxxx-ef9axxxxxxxx", "avatar": "https://secure.gravatar.com/avatar/abb3c72c8a308e547e37a430a6f01c0d", "name": "Helix Detection", "username": "helix.detection@fireeye.com", "primary_email": "helix.detection@fireeye.com"}, "created_at": "2020-06-05T14:31:53.389886Z", "updated_at": "2020-09-10T21:13:19.415214Z", "name": "home_domain", "type": "default", "description": "Dynamic (FEYE managed) list. Domains of seen home domain(s). Modifications will be overwritten.", "usage": [], "is_internal": false, "is_protected": false, "is_active": true, "hash": "364d83730052f3b351108261xxxxxxxxxxxxxxxx"}, {"id": "83xxx", "short_name": "home_domain_permutation", "item_count": 3790, "types": ["misc"], "created_by": {"id": "b6682a18-xxxx-48a6-xxxx-ef9axxxxxxxx", "avatar": "https://secure.gravatar.com/avatar/abb3c72c8a308e547e37a430a6f01c0d", "name": "Helix Detection", "username": "helix.detection@fireeye.com", "primary_email": "helix.detection@fireeye.com"}, "updated_by": {"id": "b6682a18-xxxx-48a6-xxxx-ef9axxxxxxxx", "avatar": "https://secure.gravatar.com/avatar/abb3c72c8a308e547e37a430a6f01c0d", "name": "Helix Detection", "username": "helix.detection@fireeye.com", "primary_email": "helix.detection@fireeye.com"}, "created_at": "2020-06-06T14:32:06.637410Z", "updated_at": "2020-09-10T23:16:26.442002Z", "name": "home_domain_permutation", "type": "default", "description": "Dynamic (FEYE managed) list. This list contains similar-looking domain names with respect to home domain name. Modifications will be overwritten.", "usage": [], "is_internal": false, "is_protected": false, "is_active": true, "hash": "61ea8e74fea8436a3b6446c3xxxxxxxxxxxxxxxx"}]
```









## Connectors
#### FireEye Helix - Alerts Connector
Pull alerts from FireEye Helix.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|class|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API Root of the FireEye Helix instance. Example: https://helix.eu.fireeye.com/helix/id/aaaqsj477/|True|String|https://helix.eu.fireeye.com/helix/id/{id}/|
|API Token|API Token of the FireEye Helix account.|True|Password|*****|
|Server Timezone|Specify which timezone is set on the FireEye Helix server in regards to UTC. For example, +1, -1, etc. If nothing is specified, the connector will use UTC as a default timezone.|False|String||
|Lowest Risk To Fetch|Lowest risk that will be used to fetch Alert. Possible values: Low, Medium, High, Critical.|True|String|Medium|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|False|Integer|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye Helix server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




