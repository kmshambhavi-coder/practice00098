
# AnomaliStaxx

Anomali STAXX provides bi-directional sharing of threat intelligence from STIX/TAXII sources that are in the cloud (such as Anomali Limo, http://hailataxii.com, an ISAC, or Anomali ThreatStream) or on premise. With Anomali STAXX, you can connect to STIX/TAXII servers, discover and configure their threat feeds, and poll (download) threat intelligence from those feeds. You can also import threat intelligence into Anomali STAXX and push (upload) selected observables to other STIX/TAXII servers.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|String|https://<ip>:<port>|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|python_dateutil-2.8.2-py2.py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the Anomali Staxx with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Anomali Staxx - Indicators Connector
Pull indicators from Anomali Staxx

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|itype|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|Server Address|Server address of the Anomali Staxx instance.|True|String|https://<ip>:<port>|
|Username|Username of the Anomali Staxx account.|True|String||
|Password|Password of the Anomali Staxx account.|True|Password|*****|
|Server Timezone|Specify which timezone is set on the Anomali Staxx server in regards to UTC. For example, +1, -1, etc. If nothing is specified, the connector will use UTC as a default timezone.|False|String||
|Lowest Severity To Fetch|Lowest severity that will be used to fetch incidents. Possible values: Low, Medium, High, Critical.|True|String|Medium|
|Lowest Confidence To Fetch|Lowest confidence that will be used to fetch indicators.|False|Integer|0|
|Fetch Max Hours Backwards|Amount of hours from where to fetch indicators.|False|Integer|1|
|Max Indicators To Fetch|How many indicators to process per one connector iteration.|False|Integer|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Anomali Staxx server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




