
# FortinetFortiSIEM

FortiSIEM brings together visibility, correlation, automated response, and remediation in a single, scalable solution. It reduces the complexity of managing network and security operations to effectively free resources, improve breach detection, and even prevent breaches.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://x.x.x.x:port|
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
|xmltodict-0.13.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities using information from Fortinet FortiSIEM CMDB. Supported entities: Hostname, IP. Note: Hostname entity should contain the "name" of the device.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Target Organization|Specify optional target organization name to look for enrichment information in this organization only.|False|String||



##### JSON Results
```json
[{"Entity": "centos-xxx", "EntityResult": {"device": {"organization": {"@id": "1xx", "@name": "Super"}, "accessIp": "172.30.xxx.xxx", "approved": "true", "components": null, "creationMethod": "LOG", "deviceType": {"accessProtocols": "TELNET,SSH", "jobWeight": "10", "model": "Unix", "vendor": "Generic", "version": "ANY"}, "discoverMethod": "LOG", "discoverTime": "1640008485000", "eventParserList": null, "interfaces": null, "ipToHostNames": null, "luns": null, "name": "centos-xxx", "naturalId": "centos%2dxxx", "processors": null, "properties": {"customproperty": [{"matched": "false", "propertyDef": {"displayInCMDB": "false", "displayName": "Importance", "groupKey": "false", "propertyName": "importance", "subValueType": "STRING", "valueType": "STRING"}, "propertyName": "importance", "propertyValue": "Normal", "updated": "false"}, {"matched": "false", "propertyDef": {"displayInCMDB": "false", "displayName": "Location Name", "groupKey": "false", "propertyName": "locationName", "subValueType": "STRING", "valueType": "STRING"}, "propertyName": "locationName", "updated": "false"}]}, "raidGroups": null, "sanControllerPorts": null, "softwarePatches": null, "softwareServices": null, "status": "2", "storageGroups": null, "storages": null, "unmanaged": "false", "updateMethod": "LOG", "version": "ANY", "winMachineGuid": null}}}, {"Entity": "172.30.xxx.xxx", "EntityResult": {"device": {"organization": {"@id": "1xx", "@name": "Super"}, "accessIp": "172.30.xxx.xxx", "applications": null, "approved": "true", "components": null, "creationMethod": "LOG", "deviceType": {"accessProtocols": "TELNET,SSH", "jobWeight": "10", "model": "Unix", "vendor": "Generic", "version": "ANY"}, "discoverMethod": "LOG", "discoverTime": "1640070721000", "eventParserList": {"eventparser": {"deviceType": {"category": "Appliance", "jobWeight": "10", "model": "Generic", "vendor": "Generic", "version": "ANY"}, "enabled": "true", "name": "SyslogNGParser", "parserXml": "<patternDefinitions><pattern>..."}}, "interfaces": null, "ipToHostNames": null, "luns": null, "name": "centos-xxx", "naturalId": "centos", "primaryContactUser": "0", "processors": null, "properties": {"customproperty": [{"matched": "false", "propertyDef": {"displayInCMDB": "false", "displayName": "Importance", "groupKey": "false", "propertyName": "importance", "subValueType": "STRING", "valueType": "STRING"}, "propertyName": "importance", "propertyValue": "Mission Critical", "updated": "false"}, {"matched": "false", "propertyDef": {"displayInCMDB": "false", "displayName": "Location Name", "groupKey": "false", "propertyName": "locationName", "subValueType": "STRING", "valueType": "STRING"}, "propertyName": "locationName", "updated": "false"}]}, "raidGroups": null, "sanControllerPorts": null, "secondaryContactUser": "0", "softwarePatches": null, "softwareServices": null, "status": "2", "storageGroups": null, "storages": null, "unmanaged": "false", "updateMethod": "MANUAL", "version": "ANY", "winMachineGuid": null}}}]
```



#### Execute Custom Query
Execute a custom query in FortiSIEM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify what fields to return. If nothing is provided, action will return all fields.|False|String||
|Sort Field|Specify what parameter should be used for sorting.|False|String||
|Sort Order|Specify the order of sorting.|False|List|DESC|
|Query|Specify a query that will be used to retrieve information about the events. Example: (relayDevIpAddr = 172.30.202.1 OR 172.30.202.2) AND (reptDevName = HOST1)|True|String||
|Max Results To Return|Specify how many results to return. Default: 50.|False|String|50|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601. Example: 2021-04-23T12:38Z|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|False|List|Last Hour|



##### JSON Results
```json
[{"custId": "1", "attributes": {"eventType": "Unknown_EventType", "eventSeverity": "3", "eventAction": "0 (Permit)", "phRecvTime": "Wed Dec 29 00:36:55 IST 2021", "relayDevIpAddr": "172.30.20xxx", "reptDevIpAddr": "172.30.20xxx", "destIpAddr": "172.30.20xxx", "destName": "HOST-172.30.20xxx", "reptDevName": "centos-xxx", "reptVendor": "Unknown", "customer": "Super", "reptModel": "Unknown", "rawEventMsg": "<27>Dec 29 00:36:47 centos-xxx aella_flow[5074]: 1902195|aos_afix_json|ERR|Failed to send message: Couldn't connect to server/7", "collectorId": "1", "eventId": "4242813061460978xxx", "phEventCategory": "0 (External)", "count": "1", "eventName": "Unknown event type", "eventParsedOk": "0", "parserName": "SyslogNGParser"}, "dataStr": null, "eventType": "Unknown_EventType", "id": "4242813061460978xxx", "index": "0", "nid": "4242813061460978xxx", "receiveTime": "2021-12-29T00:36:55+02:00"}]
```



#### Execute Simple Query
Execute FortiSIEM events query based on the provided parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Fields To Return|Specify what fields to return. If nothing is provided, action will return all fields.|False|String||
|Sort Field|Specify what parameter should be used for sorting.|False|String||
|Sort Order|Specify the order of sorting.|False|List|DESC|
|Minimum Severity to Fetch|Specify minimum event severity to fetch to Siemplify in numbers, for example 5 or 7.|False|String||
|Event Types|Specify event types query should fetch. Parameter accepts multiple values as a comma separated string.|False|String||
|Event Category|Specify event category query should fetch. Parameter accepts multiple values as a comma separated string.|False|String||
|Event IDs|Specify optionally exact event ids query should fetch. Parameter accepts multiple values as a comma separated string.|False|String||
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601. Example: 2021-04-23T12:38Z|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Max Results To Return|Specify how many results to return. Default: 50.|False|String|50|
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|False|List|Last Hour|



##### JSON Results
```json
[{"custId": "1", "attributes": {"eventType": "Unknown_EventType", "eventSeverity": "3", "eventAction": "0 (Permit)", "phRecvTime": "Wed Dec 29 00:36:55 IST 2021", "relayDevIpAddr": "172.30.20xxx", "reptDevIpAddr": "172.30.20xxx", "destIpAddr": "172.30.20xxx", "destName": "HOST-172.30.20xxx", "reptDevName": "centos-xxx", "reptVendor": "Unknown", "customer": "Super", "reptModel": "Unknown", "rawEventMsg": "<27>Dec 29 00:36:47 centos-xxx aella_flow[5074]: 1902195|aos_afix_json|ERR|Failed to send message: Couldn't connect to server/7", "collectorId": "1", "eventId": "4242813061460978xxx", "phEventCategory": "0 (External)", "count": "1", "eventName": "Unknown event type", "eventParsedOk": "0", "parserName": "SyslogNGParser"}, "dataStr": null, "eventType": "Unknown_EventType", "id": "4242813061460978xxx", "index": "0", "nid": "4242813061460978xxx", "receiveTime": "2021-12-29T00:36:55+02:00"}]
```



#### Ping
Test connectivity to the FortiSIEM installation with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### FortiSIEM Incidents Connector
Connector can be used to fetch FortiSIEM incidents. Connector whitelist can be used to ingest only specific types of incidents based on incident’s “eventType” attribute value. SourceGroupIdentifier of the connector can be used to group Siemplify alerts based on incident id.  Connector requires FortiSIEM version 6.3 or newer.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|deviceProduct|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|eventType|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Specify the timeout for connector to run.|True|Integer|300|
|API Root|Specify the API root for the target FortiSIEM installation.|True|String|https://x.x.x.x:port|
|Username|Specify the username to use for the target FortiSIEM installation.|True|String||
|Password|Specify the password to use for the target FortiSIEM installation.|True|Password|*****|
|Verify SSL|If enabled, Siemplify server will check the certificate configured for API root.|False|Boolean|true|
|Target Organization|Specify organizations connector should fetch incidents for.|False|String||
|Max hours backwards|Specify the time frame to fetch incidents from X hours backwards.|True|Integer|24|
|Max Incidents Per Cycle|Specify how many incidents should be processed during one connector run.|True|Integer|10|
|Max Events Per Incidents|Specify the maximum number of events the connector should track for the incident. Once the limit will be reached, new events will not be added to Siemplify.|True|Integer|100|
|Incident Statuses to Fetch|Specify incident' statuses to fetch to Siemplify. Parameter accepts multiple values as a comma separated string. 0 stands for incidents in open status.|False|String|0|
|Minimum Severity to Fetch|Specify minimum incident’s event severity to fetch to Siemplify in numbers, for example 5 or 7.|False|Integer||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Track New Events Added to Already Ingested Incidents|If enabled, if new events are added to already ingested FortiSIEM incident, additional new alert will be created in Siemplify that will have those new events.|False|Boolean|true|
|Track New Events Threshold (hours)|If "Track New Events Added to Already Ingested Incidents" checkbox is checked, specify the maximum number of hours connector should track already ingested incidents for new events. Once the limit will be reached, new events will not be added to Siemplify.|True|Integer|24|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




