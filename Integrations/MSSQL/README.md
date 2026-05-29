
# MSSQL

Microsoft SQL Server is a relational database management system developed by Microsoft.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|None|x.x.x.x|
|Username||False|String||
|Password||False|Password|*****|
|Port||False|String|1433|
|Database Name For Testing||True|String||
|Windows Authentication||False|Boolean|False|
|Use Kerberos Authentication||False|Boolean|False|
|Kerberos Realm||False|String||
|Kerberos Username||False|String||
|Kerberos Password||False|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|certifi-2026.4.22-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|pyodbc-5.1.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Ping
Test connectivity to SQL Server
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Database Name|Database Name|True|String|siemplify_integrations_db|



#### RunSQLQuery
Run a SQL query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Database Name|The DB name to run the query on|True|String||
|Query|The query to run. Default: SELECT * FROM <>|True|String||
|Commit|If set to true, will commit the changes to the DB|False|Boolean|false|



##### JSON Results
```json
[{"Name": "Actions Monitor Siemplify System", "Creator": "System", "Integration": "Siemplify", "VersionId": "AAAAAAAAAAAA", "ModificationTimenixTimeInMs": 1558278307098, "Description": "Notifies of all the actions, that have individually failed at least 3 times, in the last 3 hours"}, {"Name": "Jobs Monitor Siemplify System", "Creator": "System", "Integration": "Siemplify", "VersionId": "ZZZZZZZZZZZZZ", "ModificationTimenixTimeInMs": 1558278307098, "Description": "Notifies of all the jobs, that have individually failed at least 3 times, in the last 3 hours"}]
```









