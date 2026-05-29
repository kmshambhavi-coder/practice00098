
# JoeSandbox

Deep Malware Analysis. Joe Sandbox combines the best parts of multiple techniques. This enables deep analysis, excellent detection and big evasion resistance.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://jbxcloud.joesecurity.org|
|Api Key|None|True|Password|*****|
|Use SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|urllib3-2.2.1-py3-none-any.whl|


## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Search Hash
Search for a hash in sandbox records
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"status": "finished", "runs": [{"detection": "clean", "yara": false, "system": "w7_1", "error": null}, {"detection": "clean", "yara": false, "system": "w7x64", "error": null}], "sha1": "e96a0e74ed5cfbcaa65c764939b29945e988be9b", "tags": [], "webid": "773601", "comments": "testing", "filename": "mocks.txt", "scriptname": "default.jbs", "time": "2019-01-21T11:21:20+01:00", "duration": 530, "sha256": "6087f230c0d6ea362f23ca2abb4baf82a9058cb0143af3e82584005f56626000", "md5": "502cddb08849eb191386017dfca05000", "analysisid": "765760"}, "Entity": "502cddb08849eb191386017dfca05000"}]
```



#### Search Url
Search for a URL in sandbox records
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"status": "finished", "runs": [{"detection": "clean", "yara": false, "system": "w7_1", "error": null}, {"detection": "clean", "yara": false, "system": "w7x64", "error": null}], "sha1": "e96a0e74ed5cfbcaa65c764939b29945e988b000", "tags": [], "webid": "773601", "comments": "testing", "filename": "mocks.txt", "scriptname": "default.jbs", "time": "2019-01-21T11:21:20+01:00", "duration": 530, "sha256": "6087f230c0d6ea362f23ca2abb4baf82a9058cb0143af3e82584005f56626000", "md5": "502cddb08849eb191386017dfca05000", "analysisid": "765760"}, "Entity": "https://sampleweb.com"}]
```



#### Detonate File
Scan file and fetch its reputation. Note : This action requires Pro level account.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Paths|The paths of the files to scan comma separated.|True|String|None|
|Comment|The comment to add to the entry|False|String|None|
|Report Format|The format of the report|False|String|None|



##### JSON Results
```json
{"path\\mocks.txt": {"status": "finished", "runs": [{"detection": "clean", "yara": false, "system": "w7_1", "error": null}, {"detection": "clean", "yara": false, "system": "w7x64", "error": null}], "sha1": "e96a0e74ed5cfbcaa65c764939b29945e988be9b", "tags": [], "webid": "773601", "comments": "testing", "filename": "mocks.txt", "scriptname": "default.jbs", "time": "2019-01-21T11:21:20+01:00", "duration": 530, "sha256": "6087f230c0d6ea362f23ca2abb4baf82a9058cb0143af3e82584005f56626000", "md5": "502cddb08849eb191386017dfca05000", "analysisid": "765760"}}
```









