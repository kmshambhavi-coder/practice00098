# GitSync

## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Crowdstrike - Alerts Connector|Pull alerts from Crowdstrike. Dynamic List works with the "display_name" parameter. Note: To fetch identity protection detections use "Identity Protection Detections Connector".|False|


## Playbooks
|Name|Description|
|----|-----------|
|Custom  Playbook|Test Description|
|custom Block one|An embedded workflow that can receive inputs and return an output.|
|custom Block two|An embedded workflow that can receive inputs and return an output.|


## Visual Families
|Name|Description|
|----|-----------|
|AV_0005|manually added VF|


## Jobs
|Name|Description|
|----|-----------|
|Sync Alerts|This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.|

