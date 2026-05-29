
# McAfeeTIEDXL

McAfee Threat Intelligence Exchange optimizes threat detection and response by closing the gap from malware encounter to containment from days, weeks, and months down to milliseconds.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|None|ssl://{IP}:{PORT}|
|Broker CA Bundle Path||True|String||
|Client Cert File Path||True|String||
|Client Key File Path||True|String||


#### Dependencies
| |
|-|
|dxlclient-5.6.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|PySocks-1.7.1-py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|configobj-5.0.9-py2.py3-none-any.whl|
|dxlbootstrap-0.2.2-py2.py3-none-any.whl|
|asn1crypto-1.5.1-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|dxltieclient-0.3.0-py2.py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|oscrypto-1.3.0-py2.py3-none-any.whl|
|msgpack-1.1.2-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|


## Actions
#### Get File References
Get references for a file (the agent on which the file was used)
Timeout - 600 Seconds



#### Get File Reputation
Get file reputation
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Enrich with all services|If checked, enrich with all results from all returned services. Else, store only the worst reputation as enrichment.|False|Boolean|False|



##### JSON Results
```json
[{"EntityResult": [{"Verbose Trust level": "KNOWN_MALICIOUS", "First Contact": "2020-04-07 08:35:22 +00:00", "Verbose Provider": "Global Threat Intelligence (GTI)", "Provider ID": 1, "Trust Level": "1"}, {"Verbose Trust level": "NOT_SET", "First Contact": "2020-04-07 08:35:22 +00:00", "Verbose Provider": "McAfee Threat Intelligence Exchange", "Provider ID": 3, "Trust Level": "0"}, {"Verbose Trust level": "UNKNOWN", "First Contact": "2020-05-26 10:17:58 +00:00", "Verbose Provider": "Advanced Threat Defense (ATD)", "Provider ID": 5, "Trust Level": "50"}], "Entity": "275A021BBFB6489E54D471899F7DB9D1663FC695EC2FE2A2C4538AABF651FD0F"}]
```



#### Ping
Test connectivity
Timeout - 600 Seconds



#### Set File Reputation
Set a file's enterprise reputation
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Trust Level|The trust level to set to the file's reputation|True|String||
|File Name|The name of the file|False|String|None|
|Comment|The comment to add to the file's reputation|False|String|None|









