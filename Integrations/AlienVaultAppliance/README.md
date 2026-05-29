
# AlienVaultAppliance

USM Appliance includes the essential security capabilities and continuously delivered threat intelligence needed to quickly and easily identify and respond to threats in your physical and virtual infrastructure.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|None|https://<instance>.alienvault.com|
|Username|None|True|String||
|Password|None|True|Password|*****|


#### Dependencies
| |
|-|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|dateparser-1.2.0-py2.py3-none-any.whl|
|soupsieve-2.5-py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|regex-2024.4.16-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pytz-2024.1-py2.py3-none-any.whl|
|simplejson-3.19.2-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|tzlocal-5.2-py3-none-any.whl|


## Actions
#### Enrich Assets
Retrieve information about assets from AlienVault USM Appliance
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"model": null, "descr": "", "hostname": "Lanthanum", "asset_type": "Internal", "fqdn": "", "devices": [], "asset_value": "2", "ips": {"3.3.3.3": {"ip": "1.1.1.1", "mac": "11:DE:B0:DD:54:54"}}, "id": "123D37D595B800734550B9D9D6A958C6", "sensors": {"C221234962EA11E697DE0AF71A09DF3B": {"ip": "1.1.1.1", "ctxs": {"C228355962EA11E697DE0AF71A09DF3B": "AlienVault"}, "name": "DA"}}, "os": "Linux", "networks": {"7E4B12EEFD06A21F898345C2AB46EB10": {"ips": "1.1.1.1/16", "ctx": "C228355962EA11E697DE0AF71A09DF3B", "name": "Pvt_000"}}, "icon": ""}, "Entity": "domain.com"}]
```



#### Enrich Vulnerabilities
Retrieve information about vulnerabilities from AlienVault USM Appliance
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": [{"Severity": "High", "Service": "general (0/tcp))", "Vulnerability": "TCP Sequence Number Approximation Reset Denial of Service Vulnerability", "Scan Time": "2014-02-26 02:08:59", "Asset": "Lanthanum (1.1.1.1)", "Id": "123456"}, {"Severity": "High", "Service": "https (443/tcp)", "Vulnerability": "robot(s).txt exists on the Web Server", "Scan Time": "2014-02-26 02:08:59", "Asset": "Lanthanum (1.1.1.1)", "Id": "123457"}, {"Severity": "Medium", "Service": "general (0/tcp))", "Vulnerability": "TCP timestamps", "Scan Time": "2014-02-26 02:08:59", "Asset": "Lanthanum (1.1.1.1)", "Id": "123458"}], "Entity": "test"}]
```



#### Fetch Last PCAP Files
Fetch last PCAP files from AlienVault
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Number Of Files To Fetch|e.g. 10|True|String||



##### JSON Results
```json
[{"scan_name": "pcap_file_1545041396_10_1.1.1.1.pcap", "creation_time": "2018-12-17 10:09:56                                        ", "user": null, "download_link": "https://www.alienvault.com/ossim/pcap/download.php?scan_name=0000000_10_1.1.1.1.pcap&sensor_ip=1.1.1.1", "sensor_ip": "1.1.1.1", "duration": "10"}, {"scan_name": "pcap_file_1545041397_10_1.1.1.1.pcap", "creation_time": "2018-12-17 10:09:56                                        ", "user": null, "download_link": "https://www.alienvault.com/ossim/pcap/download.php?scan_name=0000000_10_1.1.1.1.pcap&sensor_ip=1.1.1.1", "sensor_ip": "1.1.1.1", "duration": "10"}, {"scan_name": "pcap_file_1545041398_10_1.1.1.1.pcap", "creation_time": "2018-12-17 10:09:56                                        ", "user": null, "download_link": "https://www.alienvault.com/ossim/pcap/download.php?scan_name=0000000_10_1.1.1.1.pcap&sensor_ip=1.1.1.1", "sensor_ip": "1.1.1.1", "duration": "10"}]
```



#### Get PCAP Files For Events
Get PCAP files for events in an alert
Timeout - 600 Seconds



##### JSON Results
```json
{"#0-1B09DN3B0D2011E985730AS799BFE5BC": "obLD1AACAAQAAAAAAAAAAAAABdwAAAABV+kUZQAHyFMAAAXqAAAF6gr3GgnfOwobLz7Y6wgARQAF3Dd3QABnBvvXVduqw6wfLg8MmgG7xmc2dMr3EdxQEAD+OgAAABcDAwdVAAAAAAAAAASEw70Ys0kQbz8wdaj1lsHAAA=="}
```



#### Get Vulnerability Reports
Get environment vulnerability report files
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Number Of Files To Fetch|e.g. 10|True|String||



##### JSON Results
```json
[{"creation_time": "2014-02-26 02:08:59", "download_link": "https://www.alienvault.com/ossim/vulnmeter/lr_rescsv.php?treport=latest&ipl=1.1.1.1&ctx=C22835597DE0AF71A09DF3B&scantype=M", "Address": "Helium (1.1.1.1)"}, {"creation_time": "2014-02-26 02:08:59", "download_link": "https://www.alienvault.com/ossim/vulnmeter/lr_rescsv.php?treport=latest&ipl=1.1.1.1&ctx=C228351E697DE071A09DF3B&scantype=M", "Address": "Holmium (1.1.1.1)"}, {"creation_time": "2014-02-26 02:08:59", "download_link": "https://www.alienvault.com/ossim/vulnmeter/lr_rescsv.php?treport=latest&ipl=1.1.1.1&ctx=C22835597DE0AF71A09DF3B&scantype=M", "Address": "Indium (1.1.1.1)"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









## Connectors
#### AlienVault USM Appliance Connector


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The field name used to determine the device product|True|String|device_product|
|EventClassId|The field name used to determine the event name (sub-type)|False|String|name|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|60|
|Api Root|e.g. https://<instance>.alienvault.com|True|String||
|Username|Username|True|String||
|Password|Password|True|Password|*****|
|Max Events Per Alert|Limit the number of events per alert. e.g. 10|True|Integer|10|
|Max Days Backwards|This field is used in the connector first running cycle and determine the connector start time. e.g. 3|True|Integer|1|
|Max Alerts Per Cycle|Limit the number of alerts in every cycle. e.g. 10|True|Integer|10|
|Server Timezone|The timezone configured in the AlienVault's, ex. UTC, Asia/Jerusalem etc.|True|String|UTC|
|Environment Field Name|The name of the environment's field. e.g. AlienVault Sensor|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




