
# FortiManager

FortiManager provides one console to manage your network, giving you full control of your Fortinet devices with enterprise-class management.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://x.x.x.x/jsonrpc|
|Username|None|True|String||
|Password|None|True|Password|*****|
|Verify SSL|None|False|Boolean||
|Workflow Mode|If enabled, integration will use workflow sessions to execute API requests. This mandatory if FortiManager is configured in workflow mode.|False|Boolean|false|



## Actions
#### Add IP To Group
Create a firewall address object and add it to a suitable address group. 
Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ADOM Name|The name of the ADOM. Default: root.|True|String|root|
|Address Group Name|The name of the address group to add to address object to.|True|String|None|



#### Add URL To Url Filter
Add a new block record to a url filter by it's name. 
Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ADOM Name|The name of the ADOM. Default: root.|True|String|root|
|Url Filter Name|The name of the URL filter to add record to.|True|String|None|



#### Execute Script
Execute existing script.Can be executed on device group and on a single device if VDOM provided.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ADOM Name|The name of the ADOM. Default: root.|True|String|None|
|Policy Package Name|The full name of the package, including package name and any parent folders.|True|String|None|
|Script Name|The name of the script to execute.|True|String|None|
|Device Name|The name of the device to execute the script on.|True|String|None|
|VDOM|The virtual domain of the device.|False|String|None|



#### Get Task Information
Get task information by ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Task ID|The ID of the task to get information about.|True|String|None|



#### Ping
Test integration connectivity.
Timeout - 600 Seconds



#### Remove IP From Group
Remove a firewall address object from a suitable address group and delete the firewall address object. 
Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ADOM Name|The name of the ADOM. Default: root.|True|String||
|Address Group Name|The name of the address group to remove the address from.|True|String|None|



#### Remove URL From Url Filter
Remove a block record from a url filter by it's name. 
Action is running as async, please adjust script timeout value in Chronicle SOAR IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ADOM Name|The name of the ADOM. Default: root.|True|String|None|
|Url Filter Name|The name of the URL filter to remove the record from.|True|String|None|









