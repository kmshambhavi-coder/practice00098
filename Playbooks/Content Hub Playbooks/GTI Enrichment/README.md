# GTI Enrichment
This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.



**Enabled:** True

**Version:** 0

**Type:** Block

**Priority:** 2

**Playbook Simulator:** False


##### Input Parameters
|Name|Default Value|
|----|-------------|


### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Enrich Entities|Use the Enrich Entities action to enrich the Google SecOps entities using information from Google Threat Intelligence. This action runs on the following Google Secops entities: IP address, URL, Hostname, Domain, Hash, Threat Actor, CVE. This action supports only MD5, SHA-1, and SHA-256 hashes.|GoogleThreatIntelligence|Enrich Entities|
|Add Alert Scoring Information|This action will add an entry to the alert scoring database.  Alert score is based off the ratio: 5 Low = 1 Medium.  3 Medium = 1 High.  2 High = 1 Critical.  Optional tag added to case.|Tools|Add Alert Scoring Information|
|Add Alert Scoring Information Risky|This action will add an entry to the alert scoring database.  Alert score is based off the ratio: 5 Low = 1 Medium.  3 Medium = 1 High.  2 High = 1 Critical.  Optional tag added to case.|Tools|Add Alert Scoring Information|

