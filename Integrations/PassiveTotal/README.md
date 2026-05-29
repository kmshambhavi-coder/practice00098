
# PassiveTotal

RiskIQ Community. Automated Intelligence,Faster Decisions. RiskIQ Community brings petabytes of internet intelligence directly to your fingertips. Investigate threats by pivoting through attacker infrastructure data. Understand your digital assets that are internet-exposed, and map and monitor your external attack surface.


Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User name||True|String||
|Api Key||True|Password|*****|


#### Dependencies
| |
|-|
|tldextract-5.3.1-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|passivetotal-2.5.9-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|requests_file-3.0.1-py2.py3-none-any.whl|
|packaging-26.2-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|pluggy-1.6.0-py3-none-any.whl|
|iniconfig-2.3.0-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|pytest-9.0.3-py3-none-any.whl|
|future-1.0.0-py3-none-any.whl|
|pygments-2.20.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|filelock-3.29.0-py3-none-any.whl|
|pytest_mock-3.15.1-py3-none-any.whl|


## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### WhoIs Address Reputation
Request address reputation from RiskIQ
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"results": [{"recordHash": "1cb21131ee1c1be14c862d446d149d43296fa8bfa9678374f25ea9ab3c38b777", "resolve": "com-abhut.cricket", "recordType": "A", "resolveType": "domain", "value": "1.1.1.1", "source": ["virustotal"], "lastSeen": "2015-11-09 00:00:00", "collected": "2015-11-09 00:00:00", "firstSeen": "2015-11-09 00:00:00"}], "totalRecords": 6912, "queryValue": "1.1.1.1", "pager": "None", "queryType": "ip", "firstSeen": "1970-01-01 00:00:00", "lastSeen": "2019-01-24 09:43:20"}, "Entity": "1.1.1.1"}]
```



#### WhoIs Scan Address
RiskIQ address WHOIS query
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"contactEmail": "john_doe@example.com", "domain": "1.1.1.1", "name": "N/A", "billing": {}, "admin": {"organization": "Abuse", "email": "john_doe@example.com", "telephone": "1-650-253-0000"}, "text": "IANA WHOIS server for more information on IANA.", "registered": "2014-03-14T00:00:00.000-0700", "lastLoadedAt": "2018-06-22T10:35:52.694-0700", "whoisServer": "whois.arin.net", "telephone": "N/A", "registryUpdatedAt": "1991-11-02T00:00:00.000-0800", "nameServers": [], "tech": {"organization": "test LLC", "email": "john_doe@example.com", "telephone": "1-650-253-0000"}, "organization": "test LLC", "registrar": "Administered by ARIN", "zone": {}, "registrant": {"city": "Mountain View", "country": "US", "state": "CA", "street": "1600 Amphitheatre Parkway", "postalCode": "94043", "organization": "test LLC"}}, "Entity": "1.1.1.1"}]
```



#### WhoIs Scan Domain
RiskIQ domain WHOIS query
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"domain": "test.com", "name": "N/A", "billing": {}, "admin": {}, "text": "Domain Name: test.COM   Registry Domain ID: 2138514_DOMAIN_COM-VRSN.", "registered": "1997-09-14T21:00:00.000-0700", "lastLoadedAt": "2018-10-01T15:38:19.795-0700", "whoisServer": "whois.markmonitor.com", "telephone": "N/A", "registryUpdatedAt": "2018-02-21T10:36:40.000-0800", "nameServers": ["ns1.test.com", "ns2.test.com", "ns3.test.com"], "expiresAt": "2020-09-13T21:00:00.000-0700", "tech": {}, "organization": "N/A", "registrar": "MarkMonitor Inc.", "zone": {}, "registrant": {}}, "Entity": "test.com"}]
```



#### Whois Host Reputation
Request host reputation from RiskIQ 
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"results": [{"recordHash": "0aad10e23953813834d28098db21c0902f01190c3eba7e38869f798ca56abda7", "resolve": "1.1.1.1", "recordType": "A", "resolveType": "ip", "value": "test.com", "source": ["riskiq"], "lastSeen": "2013-09-12 13:08:07", "collected": "2019-01-24 12:36:12", "firstSeen": "2013-09-12 13:08:07"}], "totalRecords": 5099, "queryValue": "test.com", "pager": "None", "queryType": "domain", "firstSeen": "2009-09-01 19:59:32", "lastSeen": "2019-01-24 12:36:11"}, "Entity": "test.com"}]
```









