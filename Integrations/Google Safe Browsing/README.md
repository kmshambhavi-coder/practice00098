
# Google Safe Browsing

Safe Browsing is a Google service that lets client applications check URLs against Google's constantly updated lists of unsafe web resources. Examples of unsafe web resources are social engineering sites (phishing and deceptive sites) and sites that host malware or unwanted software. Any URL found on a Safe Browsing list is considered unsafe.

Getting start - https://developers.google.com/safe-browsing/v4/get-started

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key|Api Key|True|Password|*****|


#### Dependencies
| |
|-|
|requests-2.32.4-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|configparser-7.2.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|pysafebrowsing-0.1.3-py3-none-any.whl|


## Actions
#### Lookup
Check if a specific URL is safe for browsing
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Url|The URL you would like to check in Google Safe Browsing.|True|String|http://malware.testing.google.test/testing/malware/|



##### JSON Results
```json
{"http://malware.testing.google.test/testing/malware/": {"malicious": true, "platforms": ["ANY_PLATFORM"], "threats": ["MALWARE"], "cache": "300s"}}
```



#### Ping
Testing connectivity with Google Safe Browsing
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









