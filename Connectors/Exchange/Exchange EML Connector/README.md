# Exchange EML Connector



Integration: Exchange

Integration Version: 123.0

Device Product Field: device_product

Event Name Field: siemplify_event_mapping_field
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|30|
|Server IP|Server IP|True|x.x.x.x|
|Domain|Specify the domain value to use for authentication.|True|sdfgh|
|Username|Specify Username to authenticate with on mail server. Username can be provided without the domain part or in either UPN (user@fully_qualified_DNS_domain_name) or Down-Level Logon Name (domain\username) format.|True|fg|
|Password|Password|True|***************|
|Mail Address|Mail Address|True|gh|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Exchange server is valid.|False|false|
|Use Domain For Authentication|If enabled, value provided for domain parameter will be concatenated to authenticate on the mail server as username@domain. If “Username” is specified in the username@domain or domain\username formats, this parameter is ignored and values from “Domain” and “Username” parameters are not concatenated.|False|true|
|Use Delegated Access|If enabled, delegated access type will be used. Otherwise, impersonation access type is used. For details on impersonation/delegation and EWS, see the following link https://learn.microsoft.com/en-us/exchange/client-developer/exchange-web-services/impersonation-and-ews-in-exchange.|False|false|
|Folder Name|The field name used to determine the folder name. '/' separator can be used to specify a subfolder to search in, example: Inbox/Subfolder|True|Inbox|
|Environment Field Name|Environment Field Name|False||
|Environment Regex Pattern|Environment Regex Pattern|False||
|Unread Emails Only|Unread Emails Only|False|false|
|Mark Emails as Read|Mark Emails as Read|False|false|
|Max Days Backwards|Number of days before the first connector iteration to retrieve EML attachments from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Encode Data as UTF-8|Indicates whether to encode the email data with UTF-8 or not. Setting to True is recommended.|False|true|
|Attach EML or MSG File to the Case Wall|If checked, the forwarded EML or MSG file will be attached to the Case Wall.|False|true|
|Exclusion Body Regex|Exclude those emails, whose body matches this regex. For example '([N|n]ewsletter)|([O|o]ut of office)' finds all emails containing 'Newsletter' or 'Out of office' keywords.|False||
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||
|Extract urls from HTML email part?|Specify whether connector should additionally try to extract urls from html part of email. This will allow connector to extract complex urls, but urls from plain text part of email will not be extracted with this method. Extracted urls will be available in urls_from_html_part event field.|False|false|
|Event Fields to Exclude|Comma-separated list of fields to exclude from events. Example: field1,field2|False||
|Exclude Attachments|If enabled, connector will not ingest email attachments and add them to cases.|False|false|

