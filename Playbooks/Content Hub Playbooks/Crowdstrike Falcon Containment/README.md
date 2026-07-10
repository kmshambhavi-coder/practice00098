# Crowdstrike Falcon Containment
This block performs containment on endpoints by targeting case-related IPs and hostnames to prevent further compromise. A boolean input controls manual or automatic execution. In automatic mode, the Upload IOCs and Isolate Endpoint flags determine which actions run. It returns true if successful, false on failure, or empty if no action is taken.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False


##### Input Parameters
|Name|Default Value|
|----|-------------|
|Manual|True|
|Upload IOCs|True|
|Isolate Endpoint|True|


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Upload IOCs Auto|Add custom IOCs in Crowdstrike Falcon. Supported entities: Hostname, URL, IP address and Hash. Note: Hostname entities are treated as domain IOCs and action will extract domain part out of URLs. Only MD5 and SHA-256 hashes are supported.|CrowdStrikeFalcon|Upload IOCs|
|Contain Endpoint Auto|Contain endpoint in Crowdstrike Falcon. Supported entities: Hostname and IP address.|CrowdStrikeFalcon|Contain Endpoint|
|Contain Endpoint|Contain endpoint in Crowdstrike Falcon. Supported entities: Hostname and IP address.|CrowdStrikeFalcon|Contain Endpoint|
|Upload IOCs|Add custom IOCs in Crowdstrike Falcon. Supported entities: Hostname, URL, IP address and Hash. Note: Hostname entities are treated as domain IOCs and action will extract domain part out of URLs. Only MD5 and SHA-256 hashes are supported.|CrowdStrikeFalcon|Upload IOCs|

test