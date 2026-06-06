## Google Chronicle Alerts Creator Job
This job will sync new SOAR alerts with Chronicle SIEM.
Note: This job is only supported from Chronicle SOAR version 6.2.30 and higher.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Verify SSL|Boolean|False|true|
|User's Service Account|Password|False|*****|
|Workload Identity Email|Password|False|*****|


readme## Google Chronicle Sync Job
This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM.
 Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://backstory.googleapis.com|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|User's Service Account|Password|False|*****|
|Workload Identity Email|Password|False|*****|


readme## Refresh Token Renewal Job
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** 14400

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


readme## Sync Incidents
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 10800

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Api Root|String|False|gfds|
|Api Key ID|String|True|hgfd|
|Max Hours Backwards|Integer|True|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|True|*****|


readme