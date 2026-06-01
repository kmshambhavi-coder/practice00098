
# GitSync

Sync Google SecOps integrations, playbooks, and settings with a GitHub, BitBucket or GitLab instance

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SOAR Password|Password for SOAR Username.|False|Password|*****|
|Repo URL|Repository URL. The URL must start with 'https' for HTTPS+Token or 'git@' for SSH+Cert.|True|String||
|Branch|Target branch|True|String||
|Git Server Fingerprint|SHA256 or MD5 fingerprint for secure Git server verification (optional). If provided, will enable secure host key verification. Format: 'SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8' or 'MD5:16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48'|False|String||
|Git Password/Token/SSH Key|Git Password/Token/SSH Key (Base64). RSA and Ed25519 are supported.|True|Password|*****|
|Git Username|Git Username|False|String||
|Commit Author|Commit Author. Must be in the following format: 'James Bond <james.bond@gmail.com>'|False|String||
|Siemplify Verify SSL|Siemplify Verify SSL|False|Boolean|true|
|Git Verify SSL|Git Verify SSL|False|Boolean|true|
|SOAR Username|Username with playbook edit permissions. Required if API Key fails due to permission limits.|False|String|None|


#### Dependencies
| |
|-|
|cryptography-45.0.5-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|requests-2.32.4-py3-none-any.whl|
|anyio-4.10.0-py3-none-any.whl|
|dulwich-0.24.1-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|bcrypt-4.3.0-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|typing_extensions-4.14.1-py3-none-any.whl|
|protobuf-6.31.1-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|MarkupSafe-3.0.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|sniffio-1.3.1-py3-none-any.whl|
|TIPCommon-2.2.9-py2.py3-none-any.whl|
|invoke-2.2.0-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|packaging-25.0-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|certifi-2025.8.3-py3-none-any.whl|
|jinja2-3.1.6-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|google_api_python_client-2.177.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|paramiko-4.0.0-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to GitSync
Timeout - 600 Seconds



##### JSON Results
```json
{}
```






## Jobs

#### Pull Connector
Imports a connector from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Connector Name|True|String||
|Include Visual Families|False|Boolean|false|
|Include Mappings|False|Boolean|false|

#### Pull Content
Installs content from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Repo URL|False|String||
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Integrations|False|Boolean|true|
|Playbooks|False|Boolean|true|
|Jobs|False|Boolean|true|
|Connectors|False|Boolean|true|
|Integration Instances|False|Boolean|true|
|Visual Families|False|Boolean|true|
|Mappings|False|Boolean|true|
|Environments|False|Boolean|true|
|Dynamic Parameters|False|Boolean|true|
|Logo|False|Boolean|true|
|Case Tags|False|Boolean|true|
|Case Stages|False|Boolean|true|
|Case Title Settings|False|Boolean|true|
|Case Close Reasons|False|Boolean|true|
|Networks|False|Boolean|true|
|Domains|False|Boolean|true|
|Custom Lists|False|Boolean|true|
|Email Templates|False|Boolean|true|
|Blacklists|False|Boolean|true|
|SLA Records|False|Boolean|true|
|Simulated Cases|False|Boolean|true|

#### Pull Custom Family
Imports a custom family from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Family Name|True|String||

#### Pull Integration
Install an integration or update an installed one.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Install Whitelist|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|

#### Pull Jobs
Imports a job from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Job Whitelist|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|

#### Pull Mappings
Imports mappings from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Source|True|String||

#### Pull Playbook
Pulls and Installs a playbook or block from the repo. NOTE: Please verify you're not overwriting existing playbooks

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Playbook Whitelist|True|String||
|Include Playbook Blocks|False|Boolean|true|

#### Pull Simulated Cases
Imports simulated cases from the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Simulated Cases|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|

#### Push Connectors
Exports a connector to the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Connectors|True|String||
|Branch|False|String||
|Git Server Fingerprint|False|String|None|
|Repo URL|False|String||
|Commit Author|False|String||
|Include Visual Families|False|Boolean|false|
|Include Mappings|False|Boolean|false|
|Readme Addon|False|String||

#### Push Content
Push all content of this platform to git

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Commit Passwords|False|Boolean|false|
|Integrations|False|Boolean|true|
|Playbooks|False|Boolean|true|
|Jobs|False|Boolean|true|
|Connectors|False|Boolean|true|
|Integration Instances|False|Boolean|true|
|Visual Families|False|Boolean|true|
|Mappings|False|Boolean|true|
|Environments|False|Boolean|true|
|Dynamic Parameters|False|Boolean|true|
|Logo|False|Boolean|true|
|Case Tags|False|Boolean|true|
|Case Stages|False|Boolean|true|
|Case Title Settings|False|Boolean|true|
|Case Close Reasons|False|Boolean|true|
|Networks|False|Boolean|true|
|Domains|False|Boolean|true|
|Custom Lists|False|Boolean|true|
|Email Templates|False|Boolean|true|
|Blacklists|False|Boolean|true|
|SLA Records|False|Boolean|true|
|Simulated Cases|False|Boolean|true|

#### Push Custom Family
Exports a custom family to the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Family Name|True|String||
|Readme Addon|False|String||

#### Push Integration
Push an integration to repo. This action will overwrite the entire folder.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Push Whitelist|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Readme Addon|False|String||

#### Push Job
Export a job to the repo

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit Author|False|String||
|Job Whitelist|True|String||
|Readme Addon|False|String||
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|

#### Push Mappings
Exports mappings  to the repo.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Source|True|String||
|Readme Addon|False|String||

#### Push Playbook
Exports playbooks or blocks to the repo

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Branch|False|String|None|
|Commit|True|String||
|Repo URL|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Folders Whitelist|False|String||
|Playbook Whitelist|False|String||
|Readme Addon|False|String||
|Include Playbook Blocks|False|Boolean|true|

#### Push Simulated Cases
Export simulate cases to the repo

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Simulated Cases|True|String||




Readme