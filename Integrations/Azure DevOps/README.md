
# Azure DevOps

Azure DevOps Server is a Microsoft product that provides version control, reporting, requirements management, project management, automated builds, testing and release management capabilities. It covers the entire application lifecycle, and enables DevOps capabilities.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project|The project name|True|String|project_name|
|Organization|The organization name|True|String|organization_name|
|Personal Access Token||True|Password|*****|
|Base URL|For exmaple: https://dev.azure|True|String|https://dev.azure|


#### Dependencies
| |
|-|
|isodate-0.7.2-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|msrest-0.7.1-py3-none-any.whl|
|azure_core-1.34.0-py3-none-any.whl|
|azure_devops-7.1.0b4-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|oauthlib-3.3.1-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests_oauthlib-2.0.0-py2.py3-none-any.whl|


## Actions
#### Ping
Test Connectivity with Azure Devops
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Trigger Azure Build
Trigger a pipeline for a given build definition ID and variables
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Build Definition Id|The build definition ID of the pipeline you want to trigger.|True|String|111|
|Build Variables|The variables to pass for the given pipeline.|True|Code|{
	"CUSTOMER": "testprod",
	"DB_IDENTIFIER": "testprod",
	"DNS_NAME": "test.com",
	"ENV": "test"
}|



##### JSON Results
```json
{"build_status": "success", "build_result": "result", "cloud_customer_id": "customerA", "build_id": "351"}
```



#### Wait Until Web Resource Is Up
Wait until the Web Resource is up
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL|The URL of the Web Resource|True|String|None|



##### JSON Results
```json
{}
```









