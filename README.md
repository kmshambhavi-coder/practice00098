# GitSync

## Integrations
|Name|Description|
|----|-----------|
|Google Chronicle|Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.|
|Microsoft Graph Mail|Microsoft 365 and Office 365 deliver the power of cloud productivity to businesses of all sizes, helping save time, money, and free up valued resources. The Microsoft 365 and Office 365 plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet. This integration uses Microsoft Graph Mail API to communicate with Microsoft 365 and Office 365 services.|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Crowdstrike - Detections Connector|Deprecated. Pull detections from Crowdstrike. Whitelist works with filters that are supported by the API of Crowdstrike. For the details, please refer to the documentation portal.|False|
|changedCrowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|False|
|Exchange EML Connector||False|
|Exchange Mail Connector|Exchange Mail Connector|False|
|Exchange Mail Connector v2|Exchange Mail Connector v2|False|
|FireEye EX - Alerts Connector|FireEye EX - Alerts Connector.|False|
|Google Chronicle - Chronicle Alerts Connector|Pull information about Rule based alerts from Google Chronicle. Note: dynamic list is used for filtering purposes. For all of the details please visit the documentation portal.|False|


## Jobs
|Name|Description|
|----|-----------|
|Google Chronicle Sync Job|This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM. Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.|

