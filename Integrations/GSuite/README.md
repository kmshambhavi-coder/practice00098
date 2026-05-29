
# GSuite

G Suite is a brand of cloud computing, productivity and collaboration tools, software and products developed by Google.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Verify SSL|If enabled, the server-side certificate used for connection is validated.|False|Boolean||
|Service Account JSON|For the service account based authentication, specify the Service Account JSON. Parameter accepts two ways to provide the service account: First (recommended), the full JSON content of the service account can be provided. The second way (legacy, will be deprecated) is to provide the path to the stored service account JSON file on the CSOAR server.|False|Password|*****|
|Workload Identity Email|For the service account based authentication, specify the Workload Identity email.|False|String||
|Delegated Email|Specify the email that integration should use.|False|String||


#### Dependencies
| |
|-|
|certifi-2024.8.30-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|requests-2.32.3-py3-none-any.whl|
|protobuf-5.28.3-cp38-abi3-manylinux2014_x86_64.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|anyio-4.6.2.post1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_api_core-2.22.0-py3-none-any.whl|
|proto_plus-1.25.0-py3-none-any.whl|
|google_auth-2.35.0-py2.py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|google_api_python_client-2.151.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|pyparsing-3.2.0-py3-none-any.whl|
|httpx-0.27.2-py3-none-any.whl|
|TIPCommon-2.0.1-py2.py3-none-any.whl|
|httpcore-1.0.6-py3-none-any.whl|


## Actions
#### Add Members To Group
Add members to a group. Action runs on Google SecOps User entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Email Address|Email of the group to add the members to.|True|String||
|User Email Addresses|A comma-separated list of users that you want to remove from the group. Note: values from this parameter will be executed alongside User Entities.|False|String||



##### JSON Results
```json
[{"kind":"admin#directory#member","etag":"\"XXXXXXXX/XXXXX\"","id":"XXXXXXXXXXXXXXXXXXX","email":"XXXXXXXX@XXXX.XXX","role":"MEMBER","type":"USER","status":"ACTIVE"},{"kind":"admin#directory#member","etag":"\"XXXXXXXXXXXXXXXXX/XXXXXXXXXXXXXXXX\"","id":"XXXXXXXXXXXXXXXXXXXX","email":"XXXXXXX@XXXXXXXX.XX","role":"MEMBER","type":"USER","status":"ACTIVE"}]
```



#### Block Extension
Use the Block Extension action to block a specified Chrome extension in an organizational unit.
Note: A Chrome Enterprise license is required to use this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Organization Unit Name|The name of the organizational unit in which to block the extension.|True|String||
|Extension ID|The ID of the extension to block.|True|String||



##### JSON Results
```json
[{"targetKey":{"targetResource":"orgunits/03ph8a2z4jjhs0c","additionalTargetKeys":{"app_id":"chrome:aapbdbdomjkkjkaonfhkkikfgjllcleb"}},"value":{"policySchema":"chrome.users.apps.InstallType","value":{"appInstallType":"BLOCKED"}},"sourceKey":{"targetResource":"orgunits/03ph8a2z4jjhs0c"},"addedSourceKey":{"targetResource":"orgunits/03ph8a2z4jjhs0c"}}]
```



#### Create Group
Create a new group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email Address|Email address of the new group.|True|String||
|Name|Display name of the new group.|False|String||
|Description|Description of the new group.|False|String||



##### JSON Results
```json
[{"kind":"admin#directory#group","id":"XXXXXX","etag":"\"XXXXXXXXXXX\"","email":"XXXXXXXX@XXXXXXXX.com","name":"XXXXXXXXXXXXXX","description":"","adminCreated":"True"}]
```



#### Create OU
Create a new organizational unit.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Customer ID|The unique ID for the customer's G Suite account, 'my_customer' alias can also be used to represent your account's customerId.|True|String||
|Name|Display name of the new OU.|False|String||
|Description|Description of the new OU.|False|String||
|Parent OU Path|The full path to the organizational unit's parent OU.|True|String||



##### JSON Results
```json
[{"kind":"admin#directory#orgUnit","etag":"XXXXXXXXXXXX","name":"XXXXX","orgUnitPath":"/XXXXX","orgUnitId":"id:XXXXXXXXXX","parentOrgUnitPath":"/","parentOrgUnitId":"id:XXXXXXXXXX"}]
```



#### Create User
Create a new user.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Given Name|The user's first name|True|String||
|Family Name|The user's last name|True|String||
|Password|The password of the new user.|True|Password|*****|
|Email Address|The user's primary email address|True|String||
|Phone|The phone number of the user.|False|String||
|Gender|The gender of the user. Valid values: female, male, other, unknown.|False|String||
|Department|The name of the department of the user.|False|String||
|Organization|The name of the organization of the user.|False|String||
|Change Password At Next Login|Whether to force the user to change his password on next login.|False|Boolean|false|



##### JSON Results
```json
[{"kind":"admin#directory#user","id":"XXXXXXXXXXX","etag":"XXXXXX","primaryEmail":"first@XXX.com","name":{"givenName":"XXXXXX","familyName":"XXXXXXX"},"isAdmin":"False","isDelegatedAdmin":"False","creationTime":"2020-12-22T13:44:29.000Z","organizations":[{"name":"MyOrg"}],"phones":[{"value":"XXXXXXXX"}],"gender":{"type":"male"},"customerId":"XXXXXX","orgUnitPath":"/","isMailboxSetup":"False"}]
```



#### Delete Extension
Preview. Use the Delete Extension action to delete a specified Chrome extension from an organizational unit blocklist. 
Note: A Chrome Enterprise license is required to use this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Organization Unit Name|The name of the organizational unit from which to delete the extension.|True|String||
|Extension ID|The ID of the extension to delete.|True|String||



##### JSON Results
```json
[{"deleted_extensions": ["xxxx"]}]
```



#### Delete Group
Delete a Google Workspace Directory Group.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Email Address|Email of the group to delete.|True|String||



#### Delete OU
Delete an organizational unit.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Customer ID|The unique ID for the customer's G Suite account, 'my_customer' alias can also be used to represent your account's customerId.|True|String||
|OU Path|The full path to the organizational unit. If organizational unit is located under root (/) path, provide just organizational unit name, without path.|True|String||



#### Delete User
Delete a user.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email Address|The email address of the user to delete.|True|String||



#### Enrich Entities
Enrich Google SecOps User entities with information from Google Workspace.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity":"XXXXXX@XXXXXX.XXX","EntityResult":{"kind":"admin#directory#user","id":"105122240427909920723","etag":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX","primaryEmail":"XXXXXX@XXXXXX.XXX","name":{"givenName":"XXXXX","familyName":"XXXXX","fullName":"XXXXXXXXX"},"isAdmin":"False","isDelegatedAdmin":"False","lastLoginTime":"1970-01-01T00:00:00.000Z","creationTime":"2020-12-22T13:18:36.000Z","agreedToTerms":"False","suspended":"False","archived":"False","changePasswordAtNextLogin":"True","ipWhitelisted":"False","emails":[{"address":"XXXXXX@XXXXXX.XXX","primary":"True"},{"address":"XXXXX@XXXXXX.XXXX.test-google-a.com"}],"nonEditableAliases":["XXXXX@XXXXXXXX.com.test-google-a.com"],"customerId":"XXXXXXXX","orgUnitPath":"XXXXXXXX","isMailboxSetup":"True","isEnrolledIn2Sv":"False","isEnforcedIn2Sv":"False","includeInGlobalAddressList":"True"}}]
```



#### Get Group Details
Retrieve information about a group using Google Workspace.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Email Addresses|A comma-separated list of group emails that you want to examine.|True|String||



##### JSON Results
```json
[{"Entity": "mytest@smplylab.com", "EntityResult": {"kind": "groupsSettings#groups", "email": "mytest@smplylab.com", "name": "000", "description": "testdesc", "whoCanJoin": "CAN_REQUEST_TO_JOIN", "whoCanViewMembership": "ALL_MEMBERS_CAN_VIEW", "whoCanViewGroup": "ALL_MEMBERS_CAN_VIEW", "whoCanInvite": "ALL_MANAGERS_CAN_INVITE", "whoCanAdd": "ALL_MANAGERS_CAN_ADD", "allowExternalMembers": "false", "whoCanPostMessage": "ANYONE_CAN_POST", "allowWebPosting": "true", "primaryLanguage": "en_US", "maxMessageBytes": 26214400, "isArchived": "false", "archiveOnly": "false", "messageModerationLevel": "MODERATE_NONE", "spamModerationLevel": "MODERATE", "replyTo": "REPLY_TO_IGNORE", "includeCustomFooter": "false", "customFooterText": "", "sendMessageDenyNotification": "false", "defaultMessageDenyNotificationText": "", "showInGroupDirectory": "true", "allowGoogleCommunication": "false", "membersCanPostAsTheGroup": "false", "messageDisplayFont": "DEFAULT_FONT", "includeInGlobalAddressList": "true", "whoCanLeaveGroup": "ALL_MEMBERS_CAN_LEAVE", "whoCanContactOwner": "ANYONE_CAN_CONTACT", "whoCanAddReferences": "NONE", "whoCanAssignTopics": "NONE", "whoCanUnassignTopic": "NONE", "whoCanTakeTopics": "NONE", "whoCanMarkDuplicate": "NONE", "whoCanMarkNoResponseNeeded": "NONE", "whoCanMarkFavoriteReplyOnAnyTopic": "NONE", "whoCanMarkFavoriteReplyOnOwnTopic": "NONE", "whoCanUnmarkFavoriteReplyOnAnyTopic": "NONE", "whoCanEnterFreeFormTags": "NONE", "whoCanModifyTagsAndCategories": "NONE", "favoriteRepliesOnTop": "true", "whoCanApproveMembers": "ALL_MANAGERS_CAN_APPROVE", "whoCanBanUsers": "OWNERS_AND_MANAGERS", "whoCanModifyMembers": "OWNERS_AND_MANAGERS", "whoCanApproveMessages": "OWNERS_AND_MANAGERS", "whoCanDeleteAnyPost": "OWNERS_AND_MANAGERS", "whoCanDeleteTopics": "OWNERS_AND_MANAGERS", "whoCanLockTopics": "OWNERS_AND_MANAGERS", "whoCanMoveTopicsIn": "OWNERS_AND_MANAGERS", "whoCanMoveTopicsOut": "OWNERS_AND_MANAGERS", "whoCanPostAnnouncements": "OWNERS_AND_MANAGERS", "whoCanHideAbuse": "NONE", "whoCanMakeTopicsSticky": "NONE", "whoCanModerateMembers": "OWNERS_AND_MANAGERS", "whoCanModerateContent": "OWNERS_AND_MANAGERS", "whoCanAssistContent": "NONE", "customRolesEnabledForSettingsToBeMerged": "false", "enableCollaborativeInbox": "false", "whoCanDiscoverGroup": "ALL_IN_DOMAIN_CAN_DISCOVER", "defaultSender": "DEFAULT_SELF"}}]
```



#### Get Host Browser Details
Use the Get Host Browser Details action to retrieve information about browsers associated with a specified Google SecOps Hostname entity.
Note: This action requires a Chrome Enterprise license.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity":"xxxx","EntityResult":{"deviceId":"xxxx","kind":"xxxx","lastPolicyFetchTime":"xxxx","osPlatform":"xxxx","osArchitecture":"xxxx","osVersion":"xxxx","machineName":"xxxx","lastRegistrationTime":"xxxx","extensionCount":"xxxx","policyCount":"xxxx","lastDeviceUser":"xxxx","lastActivityTime":"xxxx","osPlatformVersion":"xxxx","browserVersions":["xxxx"],"lastStatusReportTime":"xxxx","lastDeviceUsers":[{"userName":"xxxx","lastStatusReportTime":"xxxx"}],"machinePolicies":[{"source":"xxxx","name":"xxxx","value":"xxxx","error":"xxxx"}],"browsers":[{"browserVersion":"xxxx","channel":"xxxx","lastStatusReportTime":"xxxx","executablePath":"xxxx","profiles":[{"name":"xxxx","id":"xxxx","lastStatusReportTime":"xxxx","lastPolicyFetchTime":"xxxx","chromeSignedInUserEmail":"xxxx","extensions":[{"extensionId":"xxxx","version":"xxxx","permissions":["xxxx"],"name":"xxxx","description":"xxxx","appType":"xxxx","homepageUrl":"xxxx","installType":"xxxx","disabled":"xxxx","manifestVersion":"xxxx"}],"userPolicies":[{"source":"xxxx","name":"xxxx","value":"xxxx"}]}],"pendingInstallVersion":"xxxx"}],"virtualDeviceId":"xxxx","orgUnitPath":"xxxx","deviceIdentifiersHistory":{"records":[{"identifiers":{"machineName":"xxxx"},"firstRecordTime":"xxxx","lastActivityTime":"xxxx"}]}}}]
```



#### List Group Members
List the members of a group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Email Address|Email address of the group.|True|String||
|Include Derived Membership|Whether to list indirect memberships.|False|Boolean|true|



##### JSON Results
```json
[{"status": "ACTIVE", "kind": "admin#directory#member", "email": "XXXX_XXX@example.com", "etag": "\"XXXXXXXXXXXXXXXXXXX\"", "role": "MEMBER", "type": "USER", "id": "XXX"}]
```



#### List Group Privileges
List roles and privileges related to the group using Google Workspace.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Expand Privileges|If enabled, action will return information about all of the unique privileges related to the group.|False|Boolean||
|Max Roles To Return|Specify how many roles related to the group to return.|True|String|100|
|Group Email Addresses|A comma-separated list of groups that you want to examine|True|String||
|Check Roles|Specify a comma-separated list of roles that you want to check in relation to the group.|False|String||
|Check Privileges|Specify a comma-separated list of permission that you want to check in relation to the group. Note: "Expand Privileges" needs to be enabled for this parameter to work. If there are values inside the "Check Roles" parameter, action will check the privileges only among those roles.|False|String||
|Max Privileges To Return|Specify how many privileges related to the group to return.|True|String|100|



##### JSON Results
```json
[{"Entity": "fakeuser@smplylab.com", "EntityResult": {"roles": ["GSuiteTests", "_GROUPS_EDITOR_ROLE", "ray-test2-role"], "unique_privileges": ["VIEW_SITE_DETAILS", "ACCESS_EMAIL_LOG_SEARCH", "ACCESS_ADMIN_QUARANTINE", "ACCESS_RESTRICTED_QUARANTINE", "ADMIN_QUALITY_DASHBOARD_ACCESS", "MANAGE_DLP_RULE", "DASHBOARD_ACCESS", "MANAGE_GSC_RULE", "VIEW_GSC_RULE", "SECURITY_HEALTH_DASHBOARD_ACCESS", "SIT_CALENDAR_VIEW_METADATA", "SIT_CHAT_VIEW_METADATA", "SIT_CHROME_VIEW_METADATA", "SIT_DEVICE_UPDATE_DELETE", "SIT_DEVICE_VIEW_METADATA", "SIT_DRIVE_UPDATE_DELETE"]}}]
```



#### List OU Of Account
List the organizational units of an account
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Customer ID|The unique ID for the customer's G Suite account, 'my_customer' alias can also be used to represent your account's customerId.|True|String|my_customer|
|Organization Unit Path|The path of the organizational unit that needs to be returned.|False|String|/|
|Max Organization Units|Number of organizational units to return. Maximum is 100.|True|String|50|



##### JSON Results
```json
[{"kind": "admin#directory#orgUnit", "parentOrgUnitPath": "/", "name": "XXXXX", "etag": "\"XXXXXXXXXXXXXXXXXXXXXXXXXX\"", "orgUnitPath": "/OU-1", "parentOrgUnitId": "id:XXXX", "blockInheritance": false, "orgUnitId": "id:XXX", "description": ""}]
```



#### List Users
List users present in account.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Customer ID|The unique ID for the customer's G Suite account, 'my_customer' alias can also be used to represent your account's customerId.|False|String||
|Domain|Specify a domain to search for users in.|False|String||
|Manager Email|The email address of a user's direct manager|False|String||
|Return only Admin Accounts?|Specify whether to return only admin accounts.|False|Boolean|false|
|Return only Delegated Admin Accounts?|Specify whether to return only delegated admin accounts.|False|Boolean|false|
|Return only Suspended Users?|Specify whether to return only suspended accounts.|False|Boolean|false|
|Org Unit Path|The full path of an org unit to retrieve users from. This matches all org unit chains under the target.|False|String||
|Department|The department within the organization to retrieve users from.|False|String||
|Record Limit|Specify how many records can be returned by the action.|False|String|20|
|Custom Query Parameter|Optional. Specify custom query parameter you want to add to the list users search call. For example, orgName='Human Resources' For reference on which fields can be used see https://developers.google.com/admin-sdk/directory/v1/guides/search-users#fields. Note: when providing the 'Custom Query Parameter', make sure that you are not providing 'email' field alongside 'Email Addresses' parameter as the generated query will not work.|False|String||
|Return only users without 2fa?|If enabled, action will only return users that don't have 2fa enabled.|False|Boolean|false|
|Email Addresses|Specify a comma-separated list of email addresses that need to be searched for. Note: if 'Email Addresses' parameter is used, then 'Record Limit' parameter is ignored.|False|String||



##### JSON Results
```json
[{"kind": "admin#directory#user","id": "XXXXXXXXXXXXXXXXXXXXXXXXX","etag": "\"XXXXXXXXXXXXXXXXXXXXXXXXXX\"","primaryEmail": "XXXXXXXX@XXXXXXX.XXX","name": {"givenName": "XXXXXXXX","familyName": "XXXXXX","fullName": "XXXXXXXXX"},"isAdmin":"True","isDelegatedAdmin":"False","lastLoginTime": "2020-12-22T09:45:34.000Z","creationTime": "2020-07-22T09:23:28.000Z","agreedToTerms":"True","suspended":"False","archived":"False","changePasswordAtNextLogin":"False","ipWhitelisted":"False","emails": [{"address": "XXXXXXXX@XXXXXXX.XXX","primary":"True"},{"address": "XXXXXXXXXX@XXXXXXXX.com.test-google-a.com"}],"relations": [{"value": "XXXXXXXX@smplylab.com","type": "manager"}],"organizations": [{"primary":"True","customType": "","department": "XXXXXXXX"}],"nonEditableAliases": ["XXXXXXXX@XXXXXXXX.com.test-google-a.com"],"customerId": "XXXXXXXXX","orgUnitPath": "/Management","isMailboxSetup":"True","isEnrolledIn2Sv":"False","isEnforcedIn2Sv":"False","includeInGlobalAddressList":"True","recoveryEmail": "XXXXXXX@XXXXXXXXX.XX"},{"kind": "admin#directory#user","id": "XXXXXXXXXXXXXXXXXX","etag": "\"XXXXXXXXXXXXXXXXXXXXX\"","primaryEmail": "XXXXXXX@XXXXXXXX.com","name": {"givenName": "XXXXXXXX","familyName": "XXXXXXXXXX","fullName": "Siemplify LAB Siemplify LAB"},"isAdmin":"True","isDelegatedAdmin":"False","lastLoginTime": "2020-12-25T13:02:42.000Z","creationTime": "2020-05-14T14:00:52.000Z","agreedToTerms":"True","suspended":"False","archived":"False","changePasswordAtNextLogin":"False","ipWhitelisted":"False","emails": [{"address": "XXXXXXX-XXXX@XXXXXXXXX.com","primary":"True"},{"address": "XXXXXXXX-XXXX@XXXXXXXX.com.test-google-a.com"}],"nonEditableAliases": ["XXXXXXXX-XXXX@XXXXXXXX.com.test-google-a.com"],"customerId": "XXXXXXXX","orgUnitPath": "/Management","isMailboxSetup":"True","isEnrolledIn2Sv":"False","isEnforcedIn2Sv":"False","includeInGlobalAddressList":"True","recoveryEmail": "XXXXXXX@XXXXXXX.co"}]
```



#### Ping
Test connectivity to Google Workspace
Timeout - 600 Seconds



#### Remove Extension
Use the Remove Extension action to remove a specified Chrome extension from an organizational unit registered Chrome browsers.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Organization Unit Name|The name of the organizational unit from which to remove the extension.|True|String||
|Extension ID|The ID of the extension to remove.|True|String||



##### JSON Results
```json
[{"removed_extensions": ["xxxx"]}]
```



#### Remove Members From Group
Remove members from a group. Action runs on Google SecOps User entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Email Address|Email of the group to remove the members from.|True|String||
|User Email Addresses|A comma-separated list of users that you want to remove from the group. Note: values from this parameter will be executed alongside User Entities.|False|String||



#### Revoke User Session
Use the Revoke User Sessions action to revoke the user web and device sessions and reset their sign-in cookies using Google Workspace. This action runs on the Google SecOps User entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Email Addresses|A comma-separated list of users to sign out. The action runs the values from this parameter with User entities.|False|String||



##### JSON Results
```json
[{"Entity": "test@domain.com", "EntityResult": {"Status": "done"}}]
```



#### Update OU
Update an organizational unit.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Customer ID|The unique ID for the customer's G Suite account, 'my_customer' alias can also be used to represent your account's customerId.|True|String||
|Name|Display name of the OU.|False|String||
|Description|Description of the OU.|False|String||
|OU Path|The full path to the organizational unit. If organizational unit is located under root (/) path, provide just organizational unit name, without path.|True|String||



##### JSON Results
```json
[{"kind":"admin#directory#orgUnit","etag":"XXXXXXXXXXXX","name":"XXXXX","orgUnitPath":"/XXXXX","orgUnitId":"id:XXXXXXXXXX","parentOrgUnitPath":"/","parentOrgUnitId":"id:XXXXXXXXXX"}]
```



#### Update User
Update a Google Workspace Directory user. Note: action is not working on Google SecOps entities
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email Address|A comma-separated list of primary email addresses that will be used to identify users that need to be updated.|True|String||
|Given Name|The user's first name|False|String||
|Family Name|The user's last name|False|String||
|Password|The password of the user.|False|Password|*****|
|Phone|The phone number of the user.|False|String||
|Gender|The gender of the user. Valid values: female, male, other, unknown.|False|String||
|Department|The name of the department of the user.|False|String||
|Organization|The name of the organization of the user.|False|String||
|Change Password At Next Login|Whether to force the user to change his password on next login.|False|Boolean|false|
|User Status|Specify if user status should be updated to blocked or unblocked. By default action is no changing the user status.|False|List|Not Changed|



##### JSON Results
```json
[{"kind":"admin#directory#user","id":"XXXXXXXX","etag":"\"XXXXXXXXXXXXXXXXXX\"","primaryEmail":"XXXXXX@XXXXXX.com","name":{"givenName":"XXXXXXX","familyName":"XXXXXXXX"},"isAdmin":"False","isDelegatedAdmin":"False","lastLoginTime":"2020-12-22T15:07:44.000Z","creationTime":"2020-12-22T14:38:52.000Z","agreedToTerms":"True","suspended":"False","archived":"False","changePasswordAtNextLogin":"False","ipWhitelisted":"False","emails":[{"address":"XXXXXX@XXXXXX.com","primary":"True"},{"address":"XXXXX@XXXXXX.com.test-google-a.com"}],"organizations":[{"name":"update_org","customType":"","department":""}],"phones":[{"value":"XXXXXXX","type":"custom","customType":""}],"nonEditableAliases":["XXXXXX@XXXXXX.com.test-google-a.com"],"gender":{"type":"female"}, "customerId":"XXXXXXX","orgUnitPath":"/","isMailboxSetup":"True","includeInGlobalAddressList":"True","recoveryEmail":""}]
```



#### Get Extension Details
Use the Get Extension Details action to retrieve information about a specified Chrome Extension. 
Note: A Chrome Enterprise license is required to use this action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Extension ID|A comma-separated list of extension IDs to enrich.|True|String||
|Max Requesting Users To Return|The maximum number of users to return who requested the extension installation.The maximum value is `1000`.|True|String|100|
|Max Requesting Devices To Return|The maximum number of devices to return where the extension installation was requested.The maximum value is `1000`.|True|String|100|



##### JSON Results
```json
[{"Entity":"xxxx","EntityResult":{"name":"xxxx","displayName":"xxxx","description":"xxxx","appId":"xxxx","revisionId":"xxxx","type":"xxxx","iconUri":"xxxx","detailUri":"xxxx","firstPublishTime":"xxxx","latestPublishTime":"xxxx","publisher":"xxxx","reviewNumber":"xxxx","reviewRating":4,"chromeAppInfo":{"supportEnabled":true,"minUserCount":1000,"permissions":[{"type":"xxxx"},{"type":"xxxx","documentationUri":"xxxx","accessUserData":false},{"type":"xxxx","documentationUri":"xxxx","accessUserData":false},{"type":"xxxx","documentationUri":"xxxx","accessUserData":true}],"siteAccess":[{"hostMatch":"xxxx"},{"hostMatch":"xxxx"}],"isTheme":false,"googleOwned":true,"isCwsHosted":true,"kioskEnabled":false,"isKioskOnly":false,"type":"xxxx","isExtensionPolicySupported":false,"manifestVersion":"xxxx","requestingUserDetails":[{"email":"xxxx","justification":"xxxx"}],"requestingDeviceDetails":[{"device":"xxxx","justification":"xxxx"}]}}}]
```



#### List User Privileges
List roles and privileges related to the user using Google Workspace. Supported entities: User.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Email Addresses|A comma-separated list of users that you want to remove from the group. Note: values from this parameter will be executed alongside User Entities.|False|String||
|Check Roles|Specify a comma-separated list of roles that you want to check in relation to the user.|False|String||
|Check Privileges|Specify a comma-separated list of permission that you want to check in relation to the user. Note: "Expand Privileges" needs to be enabled for this parameter to work. If there are values inside the "Check Roles" parameter, action will check the privileges only among those roles.|False|String||
|Include Inherited Roles|If enabled, action will additionally return user roles that were inherited from groups.|False|Boolean||
|Expand Privileges|If enabled, action will return information about all of the unique privileges related to the user.|False|Boolean||
|Max Roles To Return|Specify how many roles related to the user to return.|True|String|100|
|Max Privileges To Return|Specify how many privileges related to the user to return.|True|String|100|



##### JSON Results
```json
[{"Entity": "fakeuser@smplylab.com", "EntityResult": {"roles": ["GSuiteTests", "_GROUPS_EDITOR_ROLE", "ray-test2-role"], "unique_privileges": ["VIEW_SITE_DETAILS", "ACCESS_EMAIL_LOG_SEARCH", "ACCESS_ADMIN_QUARANTINE", "ACCESS_RESTRICTED_QUARANTINE", "ADMIN_QUALITY_DASHBOARD_ACCESS", "MANAGE_DLP_RULE", "DASHBOARD_ACCESS", "MANAGE_GSC_RULE", "VIEW_GSC_RULE", "SECURITY_HEALTH_DASHBOARD_ACCESS", "SIT_CALENDAR_VIEW_METADATA", "SIT_CHAT_VIEW_METADATA", "SIT_CHROME_VIEW_METADATA", "SIT_DEVICE_UPDATE_DELETE", "SIT_DEVICE_VIEW_METADATA", "SIT_DRIVE_UPDATE_DELETE"]}}]
```



#### Search User Activity Events
Use the User Activity Events action to retrieve activity events from an application for a specified Google SecOps User entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|User Email Addresses|A comma-separated list of additional user email addresses to process.The action processes all users in this list in addition to a User entity (if one is provided).|False|String||
|Application Names|A list of applications to query for activity events.For a full list of supported applications, see the [ApplicationName documentation](https://developers.google.com/workspace/admin/reports/reference/rest/v1/activities/list#applicationname).|True|None|ALL|
|Event Type Filter|A comma-separated list of event types to retrieve.|False|String||
|Time Frame|The time frame for the activity search. If Custom is selected, the Start Time parameter is required.The possible values are as follows:     • Last Hour    • Last 6 Hours    • Last 24 Hours    • Last Week    • Last Month    • Custom|False|List|Last Hour|
|Start Time|The start of the time range for the activity search.This parameter is required if Custom is selected for the Time Frame parameter.Configure the value in ISO 8601 format.|False|String||
|End Time|The end of the time range for the activity search.This parameter is optional when Custom is selected for the Time Frame parameter and defaults to the current time if not provided.Configure the value in ISO 8601 format.|False|String||
|Max Events To Return|The maximum number of events to return per user. The default value is 200.The maximum value is 1000.The action processes a maximum of 1000 events per user, per application.|False|String|200|



##### JSON Results
```json
[{"Entity": "xxxx", "EntityResult": [{"applicationName": "xxxx", "type": "xxxx", "name": "xxxx", "parameters": [{"name": "xxxx", "value": "xxxx"}, {"name": "xxxx", "multiMessageValue": [{"parameter": [{"name": "xxxx", "value": "xxxx"}, {"name": "xxxx", "multiValue": ["xxxx"]}]}]}, {"name": "xxxx", "multiValue": ["xxxx"]}, {"name": "xxxx", "boolValue": "xxxx"}]}]}]
```









