
# GoogleChronicle

Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|UI Root|UI root of the Chronicle instance. It will be used to create a link that points back to Chronicle across multiple actions.|True|String|https://{instance}.chronicle.security|
|API Root|API root of the Chronicle instance.|True|String|https://{region}-chronicle.googleapis.com/v1/projects/{project}/locations/{location}/instances/{instance_id}|
|User's Service Account|Service Account that is used for authentication. You can configure either this parameter or the Workload Identity Email parameter. If both this and Workload Identity Email not provided, the default Service Account of the SecOps Instance will be used to authenticate.|False|Password|*****|
|Workload Identity Email|The client email address of your workload identity. You can configure either this parameter or the User's Service Account parameter. To impersonate service accounts with the workload identity email address, grant the Service Account Token Creator role to your service account. If both this and User's Service Account not provided, the default Service Account of the SecOps Instance will be used to authenticate.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Chronicle server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|googleapis_common_protos-1.67.0-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|urllib3-2.3.0-py3-none-any.whl|
|charset_normalizer-3.4.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth-2.38.0-py2.py3-none-any.whl|
|tldextract-5.1.3-py3-none-any.whl|
|certifi-2025.1.31-py3-none-any.whl|
|anyio-4.8.0-py3-none-any.whl|
|regex-2024.11.6-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|pyparsing-3.2.1-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|protobuf-5.29.3-cp38-abi3-manylinux2014_x86_64.whl|
|google_api_python_client-2.161.0-py2.py3-none-any.whl|
|cachetools-5.5.1-py3-none-any.whl|
|TIPCommon-2.2.10-py2.py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|google_api_core-2.24.1-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|filelock-3.16.1-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|proto_plus-1.26.0-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|






