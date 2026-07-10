# Playbooks
|Name|Folder|Description|
|----|------|-----------|
|Crowdstrike Falcon Containment|Content Hub Playbooks|This block performs containment on endpoints by targeting case-related IPs and hostnames to prevent further compromise. A boolean input controls manual or automatic execution. In automatic mode, the Upload IOCs and Isolate Endpoint flags determine which actions run. It returns true if successful, false on failure, or empty if no action is taken.|
