
# IronPort

Cisco IronPort Email Security Appliance is an email security gateway product. It is designed to detect and block a wide variety of email-borne threats, such as malware, spam and phishing attempts. 

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IronPort Server Address||True|String|x.x.x.x|
|IronPort AsyncOS API Port||True|String|6443|
|Username||True|String||
|Passphrase (password)||True|Password|*****|
|CA Certificate File - parsed into Base64 String||False|String||
|Use SSL||False|Boolean|true|
|Verify SSL||False|Boolean|false|


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
#### Get All Recipients By Sender
Get a list of recipients who received emails from a given sender. Note: for action to work, please make sure that message tracking is enabled in IronPort, along with AsyncOS API.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sender|The sender email address to filter by|True|String||
|Search Emails for Last X|Specify a time frame for which to search for emails. Note that this value should be set accordingly to the amount of emails processed by Ironport, if big enough value will be provided action can time out.|True|String|7|
|Set Search Email Period in|Specify if search emails should be done with the period of days or hours.|True|List|Days|
|Max Recipients to Return|Specify how many recipients action should return.|False|String|20|
|Page Size|Specify the page size for the action to use when searching for emails.|False|String|100|



##### JSON Results
```json
{"email0@dworld.co.uk": ["email1@dworld.co.uk", "email2@dworld.co.uk"]}
```



#### Get All Recipients By Subject
Get a list of all recipients that received an email with the same subject. Note: for action to work, please make sure that message tracking is enabled in IronPort, along with AsyncOS API.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|The subject to filter by|True|String||
|Search Emails for Last X|Specify a time frame for which to search for emails. Note that this value should be set accordingly to the amount of emails processed by Ironport, if big enough value will be provided action can time out.|True|String|7|
|Set Search Email Period in|Specify if search emails should be done with the period of days or hours.|True|List|Days|
|Max Recipients to Return|Specify how many recipients action should return.|False|String|20|
|Page Size|Specify the page size for the action to use when searching for emails.|False|String|100|



##### JSON Results
```json
{"Survive in bed (men only)": ["email1@dworld.co.uk", "email2@dworld.co.uk"]}
```



#### Get Report
Fetch specific Ironport report information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Report Type|The type of the report to fetch. Note: mail_sender_ip_hostname_detail and mail_incoming_ip_hostname_detail reports work based on Siemplify IP or Host entities;  mail_users_detail works on Siemplify User entity (with email address). Other reports are working without Siemplify entities.|True|List||
|Search Reports Data for Last X Days|Specify a time frame in days for which to search for reports data. By default is set to last 7 days.|True|String|7|
|Max Records to Return|Specify a time frame in days for which to search for reports data. By default is set to last 7 days.|True|String|20|



##### JSON Results
```json
{"email@dworld.co.uk": {"incoming_social_mail": 0, "incoming_detected_amp": 0, "outgoing_detected_content_filter": 0, "incoming_marketing_mail": 0, "outgoing_detected_spam": 0, "incoming_detected_virus": 0, "incoming_bulk_mail": 0, "incoming_total_clean_recipients": 1, "incoming_detected_spam": 0, "incoming_detected_content_filter": 0, "incoming_threat_content_filter": 0, "outgoing_detected_virus": 0, "incoming_detected_ims_spam_increment_over_case": 0, "outgoing_total_clean_recipients": 0, "outgoing_threat_content_filter": 0, "outgoing_detected_ims_spam_increment_over_case": 0, "incoming_graymail": 0}}
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









