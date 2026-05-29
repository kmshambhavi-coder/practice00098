
# ANYRUN-TI-Feeds

ANY.RUN Threat Intelligence Feeds (TI Feeds) is a service that delivers data on indicators of compromise derived from real-time analyses in the ANY.RUN Sandbox. With fresh and accurate IOCs, including malicious IPs, URLs, and domains, you can seamlessly integrate it with Google SecOps. This expands your existing threat coverage and boosts detection rates for more effective security operations.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Google service account|Google service account info in raw json representation.|True|Password|*****|
|Project ID|Google SecOps - project.|True|String||
|Project location|Google SecOps - location.|True|String||
|Instance ID|Google SecOps - instance.|True|String||
|ANYRUN TI Feeds API key|Example [WmNfqnpo...2Sjon7mtvm8e ]|True|Password|*****|
|Verify SSL|Enable to validate SSL certificates for API connections.|False|Boolean|true|
|Enable proxy|Enable/disable proxy using.|False|Boolean|false|
|Proxy host|Specify proxy host.|False|String||
|Proxy port|Specify proxy port.|False|String||


#### Dependencies
| |
|-|
|aiofiles-24.1.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|google_auth-2.41.1-py2.py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|charset_normalizer-3.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|frozenlist-1.8.0-cp311-cp311-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|httplib2-0.31.0-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|certifi-2025.10.5-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|TIPCommon-2.2.11-py2.py3-none-any.whl|
|yarl-1.22.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|google_api_python_client-2.184.0-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|aiohttp-3.12.14-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|anyrun_sdk-1.12.11-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|google_api_core-2.26.0-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|multidict-6.7.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|aiosignal-1.4.0-py3-none-any.whl|
|aiohappyeyeballs-2.6.1-py3-none-any.whl|
|pyparsing-3.2.5-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|propcache-0.4.1-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|cachetools-6.2.1-py3-none-any.whl|
|protobuf-6.32.1-py3-none-any.whl|
|anyio-4.11.0-py3-none-any.whl|
|attrs-25.4.0-py3-none-any.whl|


## Actions
#### Ping
Test connectivity with ANYRUN TI Feeds
Timeout - 600 Seconds



##### JSON Results
```json
{}
```






## Jobs

#### ANYRUN TI Feeds
Perform threat intelligence using specified Entity.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Feed Fetch Depth|True|String|90|



