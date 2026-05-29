
# F5BIGIPiControlAPI

F5's BIG-IP is a family of products covering software and hardware designed around application availability, access control, and security solutions.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https:/{{ip address}}|
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
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Add IP To Address List
Add IP to the address list in F5 BIG-IP. Supported entities: IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address List Name|Specify the name of the address list to which you want to add IP addresses.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:address-list:address-liststate", "name": "internal_ips", "partition": "Common", "fullPath": "/Common/internal_ips", "generation": 713, "selfLink": "https://localhost/mgmt/tm/security/firewall/address-list/~Common~internal_ips?ver=16.0.1.1", "addresses": [{"name": "192.168.0.0"}, {"name": "192.168.0.0"}, {"name": "192.168.0.0"}]}
```



#### Add IP To Data Group
Add IP to the data group in F5 BIG-IP. Supported entities: IP address. Note: action only supports internal data groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Data Group Name|Specify the name of the data group to which you want to add IP addresses.|True|String||



##### JSON Results
```json
{"kind": "tm:ltm:data-group:internal:internalstate", "name": "aol", "fullPath": "aol", "generation": 739, "selfLink": "https://localhost/mgmt/tm/ltm/data-group/internal/aol?ver=16.0.1.1", "type": "ip", "records": [{"name": "1.1.1.1/32", "data": "1.1.1.1/32"}, {"name": "2.2.2.2/32", "data": "2.2.2.2"}, {"name": "64.12.96.0/19", "data": ""}, {"name": "195.93.16.0/20", "data": ""}, {"name": "195.93.48.0/22", "data": ""}, {"name": "195.93.64.0/19", "data": ""}]}
```



#### Add Port To Port List
Add port to the port list in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Port List Name|Specify the name of the port list to which you want to add ports.|True|String||
|Ports|Specify a comma-separated list of ports that need to be added.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:port-list:port-liststate", "name": "koko", "fullPath": "koko", "generation": 895, "selfLink": "https://localhost/mgmt/tm/security/firewall/port-list/koko?ver=16.0.1.1", "ports": [{"name": "22"}, {"name": "53"}]}
```



#### Create Address List
Create an address list in F5 BIG-IP. Supported entities: IP address. Note: address list requires 1 IP address to be available during creation.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the address list that needs to be created.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:address-list:address-liststate", "name": "internal_ips", "partition": "Common", "fullPath": "/Common/internal_ips", "generation": 713, "selfLink": "https://localhost/mgmt/tm/security/firewall/address-list/~Common~internal_ips?ver=16.0.1.1", "addresses": [{"name": "192.168.0.0"}, {"name": "192.168.0.0"}, {"name": "192.168.0.0"}]}
```



#### Create Data Group
Create a data group in F5 BIG-IP. Note: action only supports internal data groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Type|Specify the type for the data group.|True|List|IP Address|
|Name|Specify the name of the data group that needs to be created.|True|String||



##### JSON Results
```json
{"kind": "tm:ltm:data-group:internal:internalstate", "name": "test", "partition": "Common", "fullPath": "/Common/test", "generation": 912, "selfLink": "https://localhost/mgmt/tm/ltm/data-group/internal/~Common~test?ver=16.0.1.1", "type": "ip"}
```



#### Create Port List
Create a port list in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the port list that needs to be created. Note: name shouldn't contain whitespace. This is F5 BIG-IP limitation.|True|String||
|Ports|Specify a comma-separated list of ports that will be a part of the new port list.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:port-list:port-liststate", "name": "koko", "fullPath": "koko", "generation": 895, "selfLink": "https://localhost/mgmt/tm/security/firewall/port-list/koko?ver=16.0.1.1", "ports": [{"name": "22"}, {"name": "53"}]}
```



#### Create iRule
Create an iRule in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the iRule that needs to be created.|True|String||
|Rule|Specify the rule that needs to be executed.|True|String||



##### JSON Results
```json
{"kind": "tm:ltm:rule:rulestate", "name": "test", "partition": "Common", "fullPath": "/Common/test", "generation": "9xx", "selfLink": "https://localhost/mgmt/tm/ltm/rule/~Common~test?ver=16.0.x.x", "apiAnonymous": "when CLIENT_ACCEPTED { if { [IP::addr [IP::client_addr] equals 10.10.xx.xx] } { pool my_pool } }"}
```



#### Delete Address List
Delete an address list in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the address list that needs to be deleted.|True|String||



#### Delete Data Group
Delete a data group in F5 BIG-IP. Note: action only supports internal data groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the data group that needs to be deleted.|True|String||



#### Delete Port List
Delete a port list in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the port list that needs to be deleted.|True|String||



#### Delete iRule
Delete an iRule in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the iRule that needs to be deleted.|True|String||



#### List Address Lists
List available address lists in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. |False|String||
|Max Address Lists To Return|Specify how many address lists to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"kind": "tm:security:firewall:address-list:address-liststate", "name": "internal_ips", "partition": "Common", "fullPath": "/Common/internal_ips", "generation": 713, "selfLink": "https://localhost/mgmt/tm/security/firewall/address-list/~Common~internal_ips?ver=16.0.1.1", "addresses": [{"name": "192.168.0.0"}, {"name": "192.168.0.0"}, {"name": "192.168.0.0"}]}]
```



#### List Data Groups
List available data groups in F5 BIG-IP. Note: action only supports internal data groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Data Groups To Return|Specify how many data groups to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"kind": "tm:ltm:data-group:internal:internalstate", "name": "images", "partition": "Common", "fullPath": "/Common/images", "generation": 1, "selfLink": "https://localhost/mgmt/tm/ltm/data-group/internal/~Common~images?ver=16.0.1.1", "type": "string", "records": [{"name": ".bmp", "data": ""}, {"name": ".gif", "data": ""}, {"name": ".jpg", "data": ""}]}, {"kind": "tm:ltm:data-group:internal:internalstate", "name": "private_net", "partition": "Common", "fullPath": "/Common/private_net", "generation": 1, "selfLink": "https://localhost/mgmt/tm/ltm/data-group/internal/~Common~private_net?ver=16.0.1.1", "type": "ip", "records": [{"name": "10.0.0.0/8", "data": ""}, {"name": "172.16.0.0/12", "data": ""}, {"name": "192.168.0.0/16", "data": ""}]}]
```



#### List Port Lists
List available port lists in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Port Lists To Return|Specify how many port lists to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"kind": "tm:security:firewall:port-list:port-liststate", "name": "_sys_self_allow_udp_defaults", "partition": "Common", "fullPath": "/Common/_sys_self_allow_udp_defaults", "generation": 1, "selfLink": "https://localhost/mgmt/tm/security/firewall/port-list/~Common~_sys_self_allow_udp_defaults?ver=16.0.1.1", "ports": [{"name": "53"}, {"name": "161"}, {"name": "520"}, {"name": "1026"}, {"name": "4353"}]}, {"kind": "tm:security:firewall:port-list:port-liststate", "name": "koko", "partition": "Common", "fullPath": "/Common/koko", "generation": 811, "selfLink": "https://localhost/mgmt/tm/security/firewall/port-list/~Common~koko?ver=16.0.1.1", "ports": [{"name": "123"}]}]
```



#### List iRules
List available iRules in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. |False|String||
|Max iRules To Return|Specify how many iRules to return. Default: 50.|False|String|50|



##### JSON Results
```json
[{"kind": "tm:ltm:rule:rulestate", "name": "_sys_APM_ExchangeSupport_OA_BasicAuth", "partition": "Common", "fullPath": "/Common/_sys_APM_ExchangeSupport_OA_BasicAuth", "generation": 1, "selfLink": "https://localhost/mgmt/tm/ltm/rule/~Common~_sys_APM_ExchangeSupport_OA_BasicAuth?ver=16.0.1.1", "apiAnonymous": "rule", "apiRawValues": {"verificationStatus": "signature-verified"}}]
```



#### Ping
Test connectivity to the F5 BIG-IP with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Remove IP From Address List
Remove IP from the address list in F5 BIG-IP. Supported entities: IP address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address List Name|Specify the name of the address list from which you want to remove IP addresses.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:address-list:address-liststate", "name": "internal_ips", "partition": "Common", "fullPath": "/Common/internal_ips", "generation": 713, "selfLink": "https://localhost/mgmt/tm/security/firewall/address-list/~Common~internal_ips?ver=16.0.1.1", "addresses": [{"name": "192.168.0.0"}, {"name": "192.168.0.0"}, {"name": "192.168.0.0"}]}
```



#### Remove IP From Data Group
Remove IP from the data group in F5 BIG-IP. Supported entities: IP address. Note: action only supports internal data groups.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Data Group Name|Specify the name of the data group from which you want to remove IP addresses.|True|String||



##### JSON Results
```json
{"kind": "tm:ltm:data-group:internal:internalstate", "name": "test", "fullPath": "test", "generation": "10xx", "selfLink": "https://localhost/mgmt/tm/ltm/data-group/internal/test?ver=16.0.x.x", "type": "ip", "records": [{"name": "128.3.x.x/32", "data": "128.3.x.x"}, {"name": "192.1.x.x/32", "data": "192.1.x.x"}]}
```



#### Remove Port From Port List
Remove port from the port list in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Port List Name|Specify the name of the port list from which you want to remove ports.|True|String||
|Ports|Specify a comma-separated list of ports that need to be removed.|True|String||



##### JSON Results
```json
{"kind": "tm:security:firewall:port-list:port-liststate", "name": "koko", "fullPath": "koko", "generation": 895, "selfLink": "https://localhost/mgmt/tm/security/firewall/port-list/koko?ver=16.0.1.1", "ports": [{"name": "22"}, {"name": "53"}]}
```



#### Update iRule
Update an iRule in F5 BIG-IP.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Specify the name of the iRule that needs to be updated.|True|String||
|Rule|Specify the new rule that needs to be executed.|True|String||



##### JSON Results
```json
{"kind": "tm:ltm:rule:rulestate", "name": "test", "fullPath": "test", "generation": "9xx", "selfLink": "https://localhost/mgmt/tm/ltm/rule/test?ver=16.0.x.x", "apiAnonymous": "when CLIENTSSL_HANDSHAKE { set tmm_auth_ssl_ocsp_done 1 }"}
```









