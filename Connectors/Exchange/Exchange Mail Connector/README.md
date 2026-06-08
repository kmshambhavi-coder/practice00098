# Exchange Mail Connector
Exchange Mail Connector


Integration: Exchange

Integration Version: 123.0

Device Product Field: device_product

Event Name Field: siemplify_event_mapping_field
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|60|
|Server Ip|x.x.x.x|True|dfgh|
|Domain|Specify the domain value to use for authentication.|True|dfg|
|Username|Specify Username to authenticate with on mail server. Username can be provided without the domain part or in either UPN (user@fully_qualified_DNS_domain_name) or Down-Level Logon Name (domain\username) format.|False|vb|
|Password|Password|True|***************|
|Mail Address|Mail address to pull emails from. e.g. user@domain.com|True|hg|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Exchange server is valid.|False|false|
|Use Domain For Authentication|If enabled, value provided for domain parameter will be concatenated to authenticate on the mail server as username@domain. If “Username” is specified in the username@domain or domain\username formats, this parameter is ignored and values from “Domain” and “Username” parameters are not concatenated.|False|true|
|Use Delegated Access|If enabled, delegated access type will be used. Otherwise, impersonation access type is used. For details on impersonation/delegation and EWS, see the following link https://learn.microsoft.com/en-us/exchange/client-developer/exchange-web-services/impersonation-and-ews-in-exchange.|False|false|
|Unread Emails Only|If checked, pull only unread mails|False|true|
|Mark Emails as Read|If checked, mark mails as read after pulling them|False|false|
|Attach Original EML|If checked, attach the original message as eml file.|False|false|
|Folder Name|The field name used to determine the folder name. '/' separator can be used to specify a subfolder to search in, example: Inbox/Subfolder|True|Inbox|
|Environment Field Name|If defined - connector will extract the environment from the specified event field. You can manipulate the field data using the Regex pattern field to extract specific string. In case the the extracted environment field and Siemplify environment name are not equal - you can map them in the map.json that is auto-generated on the first run, inside the <run-folder>.<run-folder> = C:\Siemplify_Server\Scripting\SiemplifyConnectorExecution<Connector_Folder>|False||
|Environment Regex Pattern|If defined - the connector will implement the specific RegEx pattern on the data from "envirnment field" to extract specific string. For example - extract domain from sender's address: "(?<=@)(\S+$)"|False||
|Max Days Backwards|Number of days before the first connector iteration to retrieve mails from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. e.g. 3|True|5|
|Exclusion Subject Regex|Exclude those emails, whose subject matches this regex. For example '([N|n]ewsletter)|([O|o]ut of office)' finds all emails containing 'Newsletter' or 'Out of office' keywords.|False||
|Exclusion Body Regex|Exclude those emails, whose body matches this regex. For example '([N|n]ewsletter)|([O|o]ut of office)' finds all emails containing 'Newsletter' or 'Out of office' keywords.|False||
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||
|Event Fields to Exclude|Comma-separated list of fields to exclude from events. Example: field1,field2|False||
|Exclude Attachments|If enabled, connector will not ingest email attachments and add them to cases.|False|false|

