
# CheckPointThreatReputation

Leverage the Check Pointâ€™s threat intelligence to enrich your SIEM and SOAR solutions and to secure your business applications and websites by using simple RESTful APIs.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://rep.checkpoint.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean||


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
#### Get File Hash Reputation
Enrich Siemplify File hash entity based on the information from the CheckPoint Threat Reputation service. Action accepts file hashes in md5, sha1 and sha256 formats.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



##### JSON Results
```json
[{"EntityResult": {"resource": "36F9CA40B3CE96FCEE1CF1D4A7222935536FD25B", "reputation": {"classification": "Malware", "severity": "High", "confidence": "High"}, "risk": 100, "context": {"malware_family": "Zbot", "protection_name": "Trojan.Win32.Generic.TC.ernzl", "malware_types": ["Bot", "Trojan"], "metadata": {"company_name": "MySQL, AB", "product_name": "ShellExtension", "copyright": "Copyright 2003-2013", "original_name": "ShellExtension"}}}, "Entity": "36F9CA40B3CE96FCEE1CF1D4A7222935536FD25B"}]
```



#### Get Host Reputation
Enrich the Siemplify Host entity based on the information from the CheckPoint Threat Reputation service.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



##### JSON Results
```json
[{"EntityResult": {"resource": "google.com", "reputation": {"classification": "Benign", "severity": "N/A", "confidence": "High"}, "risk": 0, "context": {"categories": [{"id": 52000132, "name": "Search Engines / Portals"}], "indications": ["The domain is known benign by Check Point's Threat Cloud", "The domain\u2019s Alexa rank is 1", "The domain has good reputation", "The URL is known benign by Check Point's Threat Cloud", "The domain is popular in Hungary", "The domain's registrant is connected to domains with good reputation", "The domain is popular among websites with good reputation", "VirusTotal vendors detected benign URLs of the domain", "The domain is hosted on an IP address that belongs to benign ASN: Google LLC"], "vt_positives": 0, "alexa_rank": 1, "registrant": "dns-admin@google.com", "safe": true, "creation_date": "2017:01:30 00:00:00", "related_ips": [{"ip": "172.217.18.206", "classification": "Benign", "confidence": "Low"}, {"ip": "216.58.209.36", "classification": "Benign", "confidence": "Low"}]}}, "Entity": "google.com"}]
```



#### Get IP Reputation
Enrich Siemplify IP entity based on the information from the CheckPoint Threat Reputation service.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



##### JSON Results
```json
[{"EntityResult": {"resource": "8.8.8.8", "reputation": {"classification": "Benign", "severity": "N/A", "confidence": "High"}, "risk": 0, "context": {"location": {"countryCode": "US", "countryName": "United States", "region": null, "city": null, "postalCode": null, "latitude": 37.751007, "longitude": -97.822, "dma_code": 0, "area_code": 0, "metro_code": 0}, "asn": 15169, "as_owner": "Google LLC"}}, "Entity": "8.8.8.8"}]
```



#### Ping
Test connectivity to the CheckPoint Threat Reputation service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









