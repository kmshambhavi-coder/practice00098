
# IBoss

The iboss cloud provides fast and secure Internet access on any device, from any location, in the cloud. Shift the focus from following perimeters to following users so that consistent cloud security is applied while users are in the office or on the road.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cloud API Root||True|String|https://cloud.iboss.com/|
|Account API Root||True|String|https://accounts.iboss.com/|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|true|


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


## Actions
#### Add IP to Policy Block List
Add IP to iBoss Block List.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category ID|Specify to which policy category you want to add the IP.|True|String|1001|
|Priority|Specify priority of the IP that needs to be blocked.|True|String|50|
|Direction|Specify what is the direction of the IP.|True|List|Destination|
|Start Port|Specify the start port related to the IP that needs to be blocked. Note: if only "Start Port" or "End Port" is specified, the value will be added to both action parameters.|False|String||
|End Port|Specify the end port related to the IP that needs to be blocked. Note: if only "Start Port" or "End Port" is specified, the value will be added to both action parameters.|False|String||
|Note|Add a note related to the IP that needs to be blocked.|False|String||
|Is Regular Expression|If enabled, IP will be considered as a regular expression.|False|Boolean|false|



#### Add URL to Policy Block List
Add URL to iBoss Block List.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category ID|Specify to which policy category you want to add the URL.|True|String|1001|
|Priority|Specify priority of the URL that needs to be blocked.|True|String|50|
|Direction|Specify what is the direction of the URL.|True|List|Destination|
|Start Port|Specify the start port related to the URL that needs to be blocked. Note: if only "Start Port" or "End Port" is specified, the value will be added to both action parameters.|False|String||
|End Port|Specify the end port related to the URL that needs to be blocked. Note: if only "Start Port" or "End Port" is specified, the value will be added to both action parameters.|False|String||
|Note|Add a note related to the URL that needs to be blocked.|False|String||
|Is Regular Expression|If enabled, URL will be considered as a regular expression.|False|Boolean|false|
|Strip Scheme|If enabled, action will strip the scheme related to the URL.|False|Boolean|false|



#### List Policy Block List Entries
Return iBoss Block List entries in a specific group.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category ID|Specify in which policy category do you want to list Block List entries.|True|String|1001|
|Max Entries to Return|Specify how many entries to return.|False|String|50|



##### JSON Results
```json
[{"applyKeywordAndSafeSearch": 0, "direction": 0, "endPort": 13, "isRegex": 1, "isTimedUrl": 0, "note": "testing", "priority": 20, "startPort": 12, "timedUrlExpiresInMinutes": 0, "type": 1, "url": "https://stackoverflow.com/", "weight": 10504}, {"applyKeywordAndSafeSearch": 0, "direction": 1, "endPort": 66, "isRegex": 1, "isTimedUrl": 0, "note": "testing note", "priority": 50, "startPort": 5, "timedUrlExpiresInMinutes": 0, "type": 1, "url": "222.22.22.22", "weight": 25600}, {"applyKeywordAndSafeSearch": 0, "direction": 1, "endPort": 66, "isRegex": 1, "isTimedUrl": 0, "note": "testnig note", "priority": 50, "startPort": 5, "timedUrlExpiresInMinutes": 0, "type": 1, "url": "222.222.222.222", "weight": 25600}, {"applyKeywordAndSafeSearch": 0, "direction": 1, "endPort": 66, "isRegex": 1, "isTimedUrl": 0, "note": "testing note", "priority": 50, "startPort": 5, "timedUrlExpiresInMinutes": 0, "type": 1, "url": "222.222.222.222", "weight": 25600}]
```



#### Ping
Test connectivity to the iBoss with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Remove IP from Policy Block List
Remove IP from iBoss Block List.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category ID|Specify from which policy category do you want to remove IP.|True|String|1001|
|Start Port|Specify start port related to the IP that needs to be deleted. This parameter is mandatory, if the desired URL has a defined start port. This is an IBoss limitation.|False|String||
|End Port|Specify end port related to the IP that needs to be deleted. This parameter is mandatory, if the desired IP has a defined end port. This is an IBoss limitation.|False|String||



#### Remove URL from Policy Block List
Remove URL from iBoss Block List.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Category ID|Specify from which policy category do you want to remove the URL.|True|String|1001|
|Start Port|Specify start port related to the URL that needs to be deleted. This parameter is mandatory, if the desired URL has a defined start port. This is an IBoss limitation.|False|String||
|End Port|Specify end port related to the URL that needs to be deleted. This parameter is mandatory, if the desired URL has a defined end port. This is an IBoss limitation.|False|String||
|Strip Scheme|If enabled, action will strip the scheme related to the URL.|False|Boolean|false|



#### URL Lookup
Perform URL Lookup.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group ID|Specify for which group to perform  a URL Lookup. If nothing is specified, “Default” group will be used.|False|String||



##### JSON Results
```json
[{"Entity": "HTTP://S.DB1.IN/RIVWT", "EntityResult": {"activeMalwareSubscription": 1, "categories": "0000000000000000000000100000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000", "categorized": "true", "googleSafeBrowsingSupport": 0, "isSafeUrl": 0, "malwareEngineAnalysisDescription": "Clean - Allowed 200", "malwareEngineAnalysisEnabled": 1, "malwareEngineAnalysisSuccess": 1, "malwareEngineIsSafeUrl": 1, "malwareEngineResultCode": 1, "message": "Status: Url Known. Please see categories below.", "realtimeCloudLookupEnabled": 0, "reputationDatabaseBotnetDetection": 0, "reputationDatabaseEnabled": 1, "reputationDatabaseIsSafeUrl": 0, "reputationDatabaseLookupSuccess": 1, "reputationDatabaseMalwareDetection": 1, "url": "HTTP://S.DB1.IN/RIVWT", "webRequestHeuristicSupport": 0}}]
```



#### URL Recategorization
Submit URL for recategorization.
Timeout - 600 Seconds









