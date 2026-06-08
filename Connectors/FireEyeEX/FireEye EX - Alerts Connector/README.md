# FireEye EX - Alerts Connector
FireEye EX - Alerts Connector.


Integration: FireEyeEX

Integration Version: 15.0

Device Product Field: Product Name

Event Name Field: name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored.
If the environment field isn't found, the environment is the default environment.
|False||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.
Default is .* to catch all and return the value unchanged.
Used to allow the user to manipulate the environment field via regex logic.
If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.
|False|.*|
|Script Timeout (Seconds)|Timeout limit for the python process running the current script.|True|180|
|API Root|API root of FireEye EX server.|True|https://x.x.x.x:x|
|Username|Username of the FireEye EX account.|True|hgfds|
|Password|Password of the FireEye EX account.|True|***************|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FireEye EX server is valid.|False|true|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Max supported value is 48. This is the FireEye EX limitation.|True|1|
|Proxy Server Address|The address of the proxy server to use|False||
|Proxy Username|The proxy username to authenticate with|False||
|Proxy Password|The proxy password to authenticate with|False||

