
# ExabeamAdvancedAnalytics

Exabeam Advanced Analytics is the world's most deployed behavioral analytics platform. Advanced Analytics automatically links and analyzes user and entity activity to better inform security analysts about threats and corresponding remediation.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{api root}|
|API Token|None|True|Password|*****|
|Verify SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|idna-3.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|


## Actions
#### Add Comments To Entity
Add comments to entities in Exabeam Advanced Analytics. Supported entities: Hostname, IP and User.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Comment|Specify the comment that needs to be added to the entity.|True|String||



##### JSON Results
```json
[{"newComment":{"commentId":"XXXXXXXXX","commentType":"asset","commentObjectId":"XXXXXXXXX","text":"my comment","exaUser":"admin", "createTime":"XXXXXXXXX","updateTime":"XXXXXXXXX","edited":"false"}}]
```



#### Add Entity To Watchlist
Add entities to the watchlist in Exabeam Advanced Analytics. Note: Watchlists with category 'AssetLabels' and 'UserLabels' are not supported in this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Title|Specify the title of the watchlist of which you want to add entities.|True|String||



#### Create Watchlist
Create a watchlist in Exabeam Advanced Analytics.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Title|Specify the title of the watchlist.|True|String||
|Category|Specify the category for the watchlist.|True|List|User|
|Access Control|Specify the access control for the watchlist.|True|List|Private|
|Description|Specify description for the watchlist.|False|String||



##### JSON Results
```json
[{"watchlistId":"XXXXXXXXXXXXXX","title":"My Watchlist","category":"Users"}]
```



#### Delete Watchlist
Delete a watchlist in Exabeam Advanced Analytics.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Title|Specify the title of the watchlist that needs to be deleted.|True|String||



#### Enrich Entities
Enrich entities using the information from Exabeam Advanced Analytics. Supported entities: Hostname, IP and User. Event time frame parameter works with hours.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Return Entity Timeline|If enabled, action will return the timeline for the entity.|False|Boolean|True|
|Event Time Frame|Specify the frame for the events that you want to see in hours.|False|String|24|
|Only Anomaly Events|If enabled, action will only return events that are considered to be anomalies.|False|Boolean|True|
|Lowest Event Risk Score To Fetch|Specify what should be the lowest risk score of the event in order to ingest it. If nothing is specified, action will not do any filtering.|False|String||
|Return Comments|If enabled, action will return comments related to the entity.|False|Boolean|True|
|Create Insight|If enabled, action will create an insight per entity.|False|Boolean|True|
|Max Events To Return|Specify how many events should be returned. If nothing is specified, action will return all of the events.|False|String||
|Max Comments To Return|Specify how many comments to return.|False|String|10|



##### JSON Results
```json
[{"Entity":"XX-XXXXX-XXX","EntityResult":{"info":{"hostName":"XX-XXXXX-XXX","ipAddress":"XX.XX.XXX.XX","assetType":"Windows","firstSeen":"XXXXXXXXXXXXXXXXX","lastSeen":"XXXXXXXXXXXXXXXXX","riskScore":"150.0","latestSequenceId":"asset@XX-XXXXX-XXX-XXXXXXXX"},"labels":[],"commentCount":"1","hasDisabledModel":"False","hasDisabledEventType":"False","comments":[{"commentId":"XXXXXXXXXXXXXXX","commentType":"asset","commentObjectId":"XXXXXXXX","text":"MyComment","exaUser":"siemplify","exaUserFullname":"","createTime":"XXXXXXXXXXXXXXXXX","updateTime":"XXXXXXXXXXXXXXXXX","edited":"False"}],"events":[{"process_name":"example.exe","alert_severity":"HIGH","event_category":["user-events","asset-events","security-alerts"],"source":"PaloAltoNetworksWildFire","malware_url":"http://221.194.44.219/upload.php","alert_id":"XXXXXXXX","session_id":"XXXXXXX-XXXXXXX","rawlog_time":"XXXXXXXXXX","process":"XXXXX.exe","src_host":"XX-XXXXX-XXX","host":"XX-XXXXXX-XXX","additional_info":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","alert_name":"Malwarefoundonhost","f_ast":"XXXXXX","src_port":"XXX","alert_type":"View-Contact","sensor_id":"XXXXXXXX","src_ip":"XX.X.XX.XXX","session_order":"XXXX","dest_ip":"XXX.XXX.XX.XXX","dest_host":"XXXXXXXXXX","hash":"XXXXXXXXXX","md5":"XXXXXXXXXXXXXXXXXXXXX","dest_port":"XXXXX","event_type":"security-alert","f_usr":"XXXXXX","src_dest_alert":"Malwarefoundonhost:XX-XXXXXX-XXX:XXXXXXXX","account":"XXXXXX","time":"XXXXXXXX","local_asset":"XXX-XXXXXX-XXX","vendor":"PaloAltoNetworksWildFire","event_id":"XXXXXX@m","f_org":"XXXXX","user":"XXXXX","entity_asset_id":"asset@XX-XXXXXX-XXX-XXXXXXXX","risk_score":"10.0"}]}},{"Entity":"slee","EntityResult":{"username":"slee","userInfo":{"username":"slee","riskScore":"457","averageRiskScore":"217","pastScores":["57.19","0.0","0.0","0.0","0.0","0.0","0.0"],"lastSessionId":"XXXXXXX-XXXXXXXXXXXX","firstSeen":"XXXXXXXXXXXX","lastSeen":"XXXXXXXXXXXX","lastActivityType":"Accountisactive","lastActivityTime":"XXXXXXXXXXXX","info":{"location":"XXXXXXXXXXXXXX","photo":"XXXXXX","phoneCell":"(XXXXXXX)XXXXXXX-XXXXXXX","email":"XXXXXXX.lee@XXXXXXX.com","employeeType":"XXXXXXX","fullName":"XXXXXXXXXXXXXX","departmentNumber":"XXXXXXX","dn":"cn=XXXXXXXlee,ou=XXXXXXX,ou=XXXXXXX,XXXXXXX=XXXXXXX,XXXXXXX=XXXXXXX","country":"XXXXXXX","division":"XXXXXXX","department":"XXXXXXX","manager":"cn,XXXXXXX=XXXXXXX,XXXXXXX=XXXXXXX,XXXXXXX=XXXXXXX","phoneOffice":"XXXXXXX-XXXXXXX-XXXXXXX","employeeNumber":"XXXXXXX-XXXXXXX","title":"salesrepresentative","group":"salesforce:sap:jobvite"},"labels":[],"pendingRiskTransfers":[]},"isExecutive":"XXXXXX","accountNames":[],"managerInfo":{"username":"XXXXXX","riskScore":"0.0","averageRiskScore":"","pastScores":[],"firstSeen":"","lastSeen":"","lastActivityType":"","lastActivityTime":"0","info":{"location":"XXXXXXXXXXXXXXXXXXXXXX","photo":"ZZZZZZZ","phoneCell":"(343)ZZZ-ZZZZZ","email":"XXXXXX.ZZZZZZZ@XXXXXX.com","employeeType":"ZZZZZZ","fullName":"XXXXXXXXXXXX","departmentNumber":"ZZZ","dn":"","country":"XXXXXXXXXXX","manager":"","phoneOffice":"XXXXXXXXXXXX-XXXXXXXXXXXX-XXXXXXXXXXXX","employeeNumber":"21D-XXXXXXXXXXXX","title":"XXXXXXXXXXXXXXXXXXXXXXXX","group":"XXXXXXXXXXX:XXXXXXXXXXX:XXXXXXXXXXX"},"labels":[],"pendingRiskTransfers":[]},"peerGroupFieldName":"XXXXXXXXXXXXXXXXXXXXXXX","peerGroupFieldValue":"XXXXXXXXXXXX","peerGroupDisplayName":"XXXXXXXXXXXX","peerGroupCount":"21","peerGroupType":"XXXXXXXXXXXXXXXXXXXXXX","peerCount":"3","isMultiPeerGroup":"true","commentCount":"0","isOnWatchlist":"true","hasDisabledModel":"False","hasDisabledEventType":"false","events":[{"source":"Windows","session_id":"XXXXXXXXXXX-XXXXXXXXXX","rawlog_time":"XXXXXXXX","src_host":"lt-XXX-XXXXXXXXXXX","domain":"kt","host":"XXXXXX","auth_process":"XXXXXXXXXXX","asset_feature":"XXXXXXXXXXX:lt-XXXXXXXXXXX-888","src_ip":"XX.X.XX.XXXX","session_order":"X","dest_ip":"XX.XX.XX.21X","getvalue('zone_info',src)":"XXXXXXXXXXXXXXXXXXXXXXoffice","dest_host":"XXXXXXXXXXX","hash":"XXXXXXXXXXX","auth_package":"ntlm","event_type":"XXXXXXXXXXX-XXXXXXXXXXX","src_host_windows":"lt-XXXXXXXXXXX-888","user_sid":"XXXXXXXXXX","account":"slee","time":"XXXXXXXXXXX","logon_type_text":"3-XXXXXXXXXXX","event_id":"XXXXXXXXXXX@m","ntlm_host":"XXXXXXXXXXX-XXXXXXXXXXX-888","user":"XXXXXXXXXXX","event_code":"XXXXXXXXXXX","entity_asset_id":["asset@lt-XXXXXXXXXXX-XXXXXXXXXXX-XXXXXXXXXXX","asset@XXXXXXXXXXX-XXXXXXXXXXX","asset@10.4.XXXXXXXXXXX.XXXXXXXXXXX-XXXXXXXXXXX","asset@10.XXXXXXXXXXX.XXXXXXXXXXX.XXXXXXXXXXX-XXXXXXXXXXX"],"risk_score":"XXXXXXXXXXX"}]}}]
```



#### List Watchlist Items
List available items in watchlists from Exabeam Advanced Analytics.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Titles|Specify a comma-separated list of watchlist titles for which you want to return items.|True|String||
|Max Items To Return|Specify how many watchlist items should be returned.|False|String|100|
|Max Days Backwards|Specify how many days backwards to list watchlists. Default: 1|False|String|1|



##### JSON Results
```json
[{"title": "XXXXXX","creator": "admin","accessControl": "public","category": "Assets","description": "","isOutOfBox": "false","items": [{"asset": {"hostName": "centos","assetType": "UNIX","firstSeen": "XXXXXXXXXXX","lastSeen": "XXXXXXXXXXX","compromisedTime": "0"},"latestAssetComment": {"commentId": "XXXXXXXXXXX","commentType": "asset","commentObjectId": "XXXXXXXXXXX","text": "text","exaUser": "admin","createTime": "XXXXXXXXXXX","updateTime": "XXXXXXXXXXX","edited": "false"},"highestRiskScore": "0.0","labels": ["TopTalker","Server","EducatedGuess"],"incidentIds": []},{"asset": {"ipAddress": "XXX.XX.XXX.XXX","assetType": "UNIX","firstSeen": "XXXXXXXXXXXX","lastSeen": "XXXXXXXXXXXX","compromisedTime": 0},"latestAssetComment": {"commentId": "XXXXXXXXXXXXX","commentType": "asset","commentObjectId": "XXX.XX.XXX.XXX","text": "asd","exaUser": "admin","createTime": "XXXXXXXXXXXXX","updateTime": "XXXXXXXXXXXXX","edited": "false"},"highestRiskScore": "0.0","labels": [],"incidentIds": [],"zone": "XXXXXXX"}],"criteria": [],"accessControlRoles": [],"numberOfNotableItems": "0"},{"title": "XXXXXXXX","creator": "admin","accessControl": "public","category": "Users","description": "","isOutOfBox": "false","items": [{"username": "administrator", "user": {"username": "administrator","riskScore": "0.0","averageRiskScore": "0.0","pastScores": [],"lastSessionId": "NA","firstSeen": "0","lastSeen": "0","lastActivityType": "Account deleted","lastActivityTime": "0","info": {},"labels": [],"pendingRiskTransfers": []},"isExecutive": "true","latestUserComment": {"commentId": "XXXXXXXXX","commentType": "user", "commentObjectId": "administrator","text": "text","exaUser": "admin", "createTime": "XXXXXXXXXXX","updateTime": "XXXXXXXXXXX","edited": "false"},"highestRiskScore": "0.0","incidentIds": [],"initials": "AD"}],"criteria": [],"accessControlRoles": [],"numberOfNotableItems": "0"}]
```



#### List Watchlists
List available watchlists in Exabeam Advanced Analytics.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Watchlists To Return|Specify how many watchlists should be returned.|False|String|100|



##### JSON Results
```json
[{"watchlistId":"XXXXXXXXXXX","title":"Service Accounts","category":"UserLabels"},{"watchlistId":"XXXXXXXXXXX","title":"Executive Users","category":"UserLabels"}]
```



#### Ping
Test connectivity to the Exabeam Advanced Analytics with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Remove Entity From Watchlist
Remove entities from the watchlist in Exabeam Advanced Analytics. Note: Watchlists with categori 'AssetLabels' and 'UserLabels' are not supported in this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Title|Specify the title of the watchlist from which you want to remove entities.|True|String||









