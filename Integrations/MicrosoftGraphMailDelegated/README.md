
# MicrosoftGraphMailDelegated

This integration version uses Delegated Authentication in Microsoft 365 and requires interactive login of the user on behalf of which integration should communicate with Microsoft 365. To configure this integration, provide all parameters except for Refresh Token, and save the integration configuration, then run “Get Authorization” and “Generate Token” actions to get the token and then provide it in integration configuration to finish the process. Microsoft 365 and Office 365 deliver the power of cloud productivity to businesses of all sizes, helping save time, money, and free up valued resources. The Microsoft 365 and Office 365 plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet. This integration uses Microsoft Graph Mail API to communicate with Microsoft 365 and Office 365 services.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Microsoft Entra ID Endpoint|The Microsoft Entra ID endpoint to connect to (formerly known as Azure AD). The value can be different for different tenant types.|True|String|https://login.microsoftonline.com|
|Microsoft Graph Endpoint|The Microsoft Graph Endpoint to connect to. The value can be different for different tenant types.|True|String|https://graph.microsoft.com|
|Client ID|The client (application) ID of the Microsoft Entra application to use in the integration.|True|String||
|Client Secret Value|The client secret value of the Microsoft Entra app to use in the integration.|True|Password|*****|
|Microsoft Entra ID Directory ID|The Microsoft Entra ID (tenant ID) value.|True|String||
|User Mailbox|The mailbox to use in the integration.|True|String||
|Refresh Token|The refresh token that is used to authenticate.|True|Password|*****|
|Verify SSL|If selected, the integration verifies that the SSL certificate for the connection to the Microsoft Graph server is valid. Selected by default.|False|Boolean|true|
|Mail Field Source|If selected, the integration retrieves the mailbox address from the user details "mail" attribute. If not selected, the integration retrieves the mailbox address from the "userPrincipalName" field. Selected by default|False|Boolean|true|
|Base64 Encoded Private Key|Specify a base64 encoded private key that will be used to decrypt the email.|False|Password|*****|
|Base64 Encoded Certificate|Specify a base64 encoded certificate that will be used to decrypt the email.|False|Password|*****|
|Base64 Encoded CA certificate|Specify a base64 encoded trusted CA certificate for signature verification.|False|Password|*****|
|Redirect URL|The Redirect URL that you configured when you created your Microsoft Entra ID application.|False|String|http://localhost|


#### Dependencies
| |
|-|
|icalendar-6.0.1-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|tzlocal-5.2-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|IMAPClient-3.0.1-py2.py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux_2_34_x86_64.whl|
|PyJWT-2.9.0-py3-none-any.whl|
|extract_msg-0.52.0-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|httplib2-0.32.0-py3-none-any.whl|
|red-black-tree-mod-1.20.tar.gz|
|emaildata-0.3.4-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|pyth3-0.7-py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|anyio-4.14.1-py3-none-any.whl|
|TIPCommon-2.4.3-py3-none-any.whl|
|siemplify_html2text-2020.1.16-py3-none-any.whl|
|python_smail-0.9.0-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|asn1crypto-1.5.1-py2.py3-none-any.whl|
|pytz-2024.2-py2.py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|exceptiongroup-1.2.2-py3-none-any.whl|
|RTFDE-0.1.2-py3-none-any.whl|
|typing_extensions-4.16.0-py3-none-any.whl|
|compressed_rtf-1.0.6.tar.gz|
|google_api_python_client-2.188.0-py3-none-any.whl|
|lark-1.1.9-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|pcodedmp-1.2.6-py2.py3-none-any.whl|
|olefile-0.47-py2.py3-none-any.whl|
|oletools-0.60.2-py2.py3-none-any.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|protobuf-7.35.1-cp310-abi3-manylinux2014_x86_64.whl|
|ebcdic-1.1.1-py2.py3-none-any.whl|
|oscrypto-1.3.0-py3-none-any.whl|
|certifi-2026.6.17-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|tzdata-2024.2-py2.py3-none-any.whl|
|colorclass-2.2.2-py2.py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|easygui-0.98.3-py2.py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|msoffcrypto_tool-5.4.2-py3-none-any.whl|
|idna-3.18-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|


## Actions
#### 1PCopy of Forward Email
Use the Forward Email action to forward emails that include previous threads. With the appropriate permissions, this action can send emails from a mailbox different than the one specified in the integration configuration. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Folder Name|A mailbox folder in which to search for an email. To specify a subfolder, use the “/” forward slash, such as {Inbox/Subfolder}.|False|String|Inbox|
|Subject|The email subject.|True|String||
|Send to|A comma-separated list of email addresses for the email recipients, such as user1@example.com, user2@example.com.|True|String||
|CC|A comma-separated list of email addresses for the email CC field, such as user1@example.com, user2@example.com.|False|String||
|BCC|A comma-separated list of email addresses for the email BCC field, such as user1@example.com, user2@example.com.|False|String||
|Attachments Paths|A comma-separated list of paths for file attachments stored on the server, for example, /{FILE_DIRECTORY}/file.pdf, /{FILE_DIRECTORY}/image.jpg.|False|String||
|Mail Content|The email body.|True|String||
|Attachment Location|A location where the attachments are stored. By default, the action attempts to upload attachments from the Cloud Storage bucket. The possible values are GCP Bucket or Local File System. The default value is GCP Bucket.|True|List|GCP Bucket|
|Send From|An optional email address from which to send an email if permissions allow it. By default, the email is sent from the default mailbox that is specified in the integration configuration.|True|String|Default Mailbox|
|Mail ID|The email ID or the internetMessageId value of the email to forward.|True|String||



##### JSON Results
```json
{"id": "xxxxx", "createdDateTime": "2024-02-02T09:49:53Z", "lastModifiedDateTime": "2024-02-02T09:51:19Z", "changeKey": "ieiohjdskj", "categories": [], "receivedDateTime": "2024-02-02T09:49:54Z", "sentDateTime": "2024-02-02T09:49:54Z", "hasAttachments": true, "internetMessageId": "<xyz>", "subject": "xxxx", "bodyPreview": "Mail Action body", "importance": "normal", "parentFolderId": "ddd==", "conversationId": "dagazz=", "conversationIndex": "daf+UJo/clVcxTQ==", "isDeliveryReceiptRequested": false, "isReadReceiptRequested": false, "isRead": true, "isDraft": false, "webLink": "https://www.example.com/about", "inferenceClassification": "focused", "body": {"contentType": "text", "content": "Send Mail Action body"}, "sender": {"emailAddress": {"name": "wdzd", "address": "sample@s.com"}}, "from": {"emailAddress": {"name": "safd", "address": "xxx"}}, "toRecipients": [{"emailAddress": {"name": "xx", "address": "aef"}}], "ccRecipients": [{"emailAddress": {"name": "as", "address": "kdaw"}}], "bccRecipients": [{"emailAddress": {"name": "xxsf", "address": "wf"}}], "replyTo": [], "uniqueBody": {"contentType": "html", "content": "Mail Action body"}, "flag": {"flagStatus": "notFlagged"}}
```






## Jobs

#### 1PCopy of Refresh Token Renewal Job
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Integration Environments|False|String||
|Connector Names|False|String||



## Connectors
#### Copy of Microsoft Graph Mail Delegated Connector
Connector can be used to fetch emails from the Microsoft Graph Mail service. Connector dynamic list can be used to filter specific values from the email body and subject parts using regexes. By default, regex is used to filter out the urls from the email. This connector uses Delegated Authentication in Microsoft 365 and requires interactive login of the user on behalf of which integration should communicate with Microsoft 365. To configure the connector, make sure that the integration configuration is already finished, and the refresh token needed to communicate with Office 365 is generated.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment. The default value is ""|False|String||
|Environment Regex Pattern|A regular expression pattern to run on the value found in the Environment Field Name field. This parameter lets you manipulate the environment field using the regular expression logic. Use the default value .* to retrieve the required raw Environment Field Name value. If the regular expression pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Email Exclude Pattern|A regular expression to exclude specific emails from ingestion, such as spam or news. This parameter works with both the subject and body of the email.|False|String||
|Microsoft Entra ID Endpoint|The Microsoft Entra endpoint to connect to. The default value is https://login.microsoftonline.com.|True|String|https://login.microsoftonline.com|
|Microsoft Graph Endpoint|The Microsoft Graph endpoint to connect to. The default value is https://graph.microsoft.com.|True|String|https://graph.microsoft.com|
|Mail Address|An email address for the connector to use.|True|String|b|
|Refresh Token|The refresh token that you obtained after you generated a token.|True|Password|*****|
|Client ID|For Microsoft 365 OAuth 2.0 authentication, the application (client) ID of the Microsoft Entra application that is used in the integration.|True|String|n|
|Client Secret Value|For Microsoft 365 OAuth 2.0 authentication, the client secret value that is provided for the authentication flow.|True|Password|*****|
|Microsoft Entra ID Directory ID|For Microsoft 365 OAuth authentication, the tenant (directory) ID of the Microsoft Entra ID application that you used in the integration.|True|String|n|
|Folder To Check For Emails|An email folder to search for the emails. This parameter accepts a comma-separated list of folders to check the user response in multiple folders. To specify a subfolder, use the “/” forward slash, such as {Inbox/Subfolder}. This parameter is case-sensitive. The default value is Inbox.|True|String|Inbox|
|Offset Time In Hours|The number of hours before the first connector iteration to retrieve the incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time. The connector can use this parameter as a fallback value when the timestamp from the latest connector iteration expires.|True|Int|24|
|Max Emails Per Cycle|The maximum number of emails to fetch for every connector iteration.|True|Int|10|
|Unread Emails Only|If selected, the connector creates cases only for unread emails.|False|Boolean|false|
|Mark Emails as Read|If selected, the connector marks ingested emails as read.|False|Boolean|false|
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism.|False|Boolean|false|
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to the Microsoft Graph server is valid.|False|Boolean|true|
|Base64 Encoded Private Key|Specify a base64 encoded private key that will be used to decrypt the email.|False|Password|*****|
|Base64 Encoded Certificate|Specify a base64 encoded certificate that will be used to decrypt the email.|False|Password|*****|
|Base64 Encoded CA certificate|Specify a base64 encoded trusted CA certificate for signature verification.|False|Password|*****|
|Mail Field Source|If selected, the connector retrieves the mailbox address from the user details “mail” attribute. If not selected, the integration retrieves the mailbox address from the “userPrincipalName” field. Selected by default.|False|Boolean|true|
|Original Received Mail Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the original email received in the monitored mailbox. The default value is orig.|False|String|orig|
|Attached Mail File Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the attached email file received in the monitored mailbox. The default value is attach.|False|String|attach|
|Create a Separate Google SecOps Alert Per Attached Mail File|If selected, the connector creates multiple alerts, with one alert for every attached email file. This behavior is useful when you process emails with multiple email files attached and set the Google SecOps event mapping to create entities from attached email files.|False|Boolean|false|
|Attach Original EML|If selected, the connector attaches the original email to the case info as an EML file.|False|Boolean|false|
|Headers to add to events|A comma-separated string of email headers to add to Google SecOps events, such as “DKIM-Siganture”, “Received”, “From”. You can provide an exact match for headers or set this parameter value as a regular expression. The connector filters the configured values from the “internetMessageHeaders” list and adds them to the Google SecOps event. By default, the connector adds all available headers. To prevent the connector from adding headers to the event, set the parameter value as follows: None.|False|String||
|Case Name Template|A custom case name. When you configure this parameter, the connector adds a new key called custom_case_name to the Google SecOps event. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys that contain the string value.|False|String||
|Alert Name Template|A custom alert name. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys that contain the string value. If you configure an invalid template or don't set a value, the connector uses the default alert name.|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy server username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Extract URLs from HTML Email Part|If enabled, connector will try to extract URLs from HTML part of email. This will allow connector to extract complex URLs, but URLs from plain text part of email will not be extracted with this method. Extracted URLs will be available in urls_from_html_part event field.|False|Boolean|true|
|Event Fields to Exclude|Comma-separated list of event fields to exclude from events. Example: field1, field2.|False|String||
|Exclude Attachments|If enabled, connector will not ingest email attachments and add them to cases.|False|Boolean|false|
|Bypass S/MIME Signature Verification|If enabled, the connector will ingest S/MIME signed emails without requiring a Base64 Encoded CA certificate for signature verification. The message body, headers, and attachments will be extracted directly.|False|Boolean|false|





InthiswehaveaddedonlytheDUPE