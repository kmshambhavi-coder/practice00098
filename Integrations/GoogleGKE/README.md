
# GoogleGKE

Google Kubernetes Engine (GKE) provides a managed environment for deploying, managing, and scaling your containerized applications using Google infrastructure. The GKE environment consists of multiple machines (specifically, Compute Engine instances) grouped together to form a cluster.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Google Kubernetes Engine instance.|False|String|https://container.googleapis.com|
|Account Type|Type of the Google Cloud account. Located at the “type” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|service_account|
|Project ID|Project ID of the Google Cloud account. Located at the “project_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Private Key ID|Private Key ID of the Google Cloud account. Located at the “private_key_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|Password|*****|
|Private Key|Private Key of the Google Cloud account. Located at the “private_key” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|Password|*****|
|Client Email|Client Email of the Google Cloud account. Located at the “client_email” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Client ID|Client ID of the Google Cloud account. Located at the “client_id” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Auth URI|Auth URI of the Google Cloud account. Located at the “auth_uri” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://accounts.google.com/o/oauth2/auth|
|Token URI|Token URI of the Google Cloud account. Located at the “token_uri” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://oauth2.googleapis.com/token|
|Auth Provider X509 URL|Auth Provider X509 URL of the Google Cloud account. Located at the “auth_provider_x509_cert_url” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String|https://www.googleapis.com/oauth2/v1/certs|
|Client X509 URL|Client X509 URL of the Google Cloud account. Located at the “client_x509_cert_url” parameter in the authentication JSON file. You need to copy the value and put it in this integration configuration parameter.|False|String||
|Service Account Json File Content|Optional: Instead of specifying private key id, private key and other parameters, specify here the full JSON content of the service account file. Other connection parameters will be ignored if this parameter is provided.|False|Password|*****|
|Workload Identity Email|A Service Account Client Email to replace the usage of "Service Account Json File Content", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Location ID|ID of the location that should be used in Google Kubernetes Engine integration. Defaults to "europe-central2-a".|False|String|europe-central2-a|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Kubernetes Engine service is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.3.2-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|pyparsing-3.1.4-py3-none-any.whl|
|setuptools-73.0.1-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|pyasn1-0.6.0-py2.py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|protobuf-5.27.3-cp38-abi3-manylinux2014_x86_64.whl|
|annotated_types-0.7.0-py3-none-any.whl|
|TIPCommon-1.1.9.1-py2.py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|httpcore-1.0.5-py3-none-any.whl|
|proto_plus-1.24.0-py3-none-any.whl|
|pyasn1_modules-0.4.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|anyio-4.4.0-py3-none-any.whl|
|googleapis_common_protos-1.65.0-py2.py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|google_api_python_client-2.142.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|pydantic-2.8.2-py3-none-any.whl|
|pydantic_core-2.20.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|httpx-0.27.2-py3-none-any.whl|


## Actions
#### Get Operation Status
Get the Google Kubernetes Engine operation status. Action is async. Note that action is not working on Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project for which to fetch operation status for. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Location|Specify Google Compute Engine location for which to fetch operation status for. Example: europe-central2-a|True|String||
|Operation Name|Specify Google Compute Engine operation to fetch.|True|String||
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"UPDATE_CLUSTER","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ"}
```



#### List Clusters
List Google Kubernetes Engine clusters based on the specified search criteria. Note that action is not working on Siemplify entities. Additionally, filtering logic is working based on the cluster name field.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the cluster name field.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action should will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain the substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the cluster name field.|False|String||
|Max Records To Return|Specify how many records to return.|False|String|50|



##### JSON Results
```json
{"clusters":[{"name":"cluster-XXXX","description":"XXXXXXXXXXX","nodeConfig":{"machineType":"e2-micro","diskSizeGb":"15","oauthScopes":["https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append"],"metadata":{"disable-legacy-endpoints":"true"},"imageType":"COS","tags":["pod-net-tag"],"serviceAccount":"XXXXX","diskType":"pd-standard","shieldedInstanceConfig":{"enableIntegrityMonitoring":"true"}},"masterAuth":{"clusterCaCertificate":"XXXXXXXXXXXXXXX"},"loggingService":"logging.googleapis.com/kubernetes","monitoringService":"monitoring.googleapis.com/kubernetes","network":"default","clusterIpv4Cidr":"XX.X.X.X/XX","addonsConfig":{"httpLoadBalancing":{},"horizontalPodAutoscaling":{},"kubernetesDashboard":{"disabled":"true"},"networkPolicyConfig":{"disabled":"true"},"dnsCacheConfig":{},"gcePersistentDiskCsiDriverConfig":{"enabled":"true"}},"subnetwork":"default","nodePools":[{"name":"default-XXXXX","config":{"machineType":"e2-XXXXX","diskSizeGb":"15","oauthScopes":["https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append"],"metadata":{"disable-legacy-endpoints":"true"},"imageType":"COS","tags":["pod-net-tag"],"serviceAccount":"default","diskType":"pd-standard","shieldedInstanceConfig":{"enableIntegrityMonitoring":"true"}},"initialNodeCount":"3","autoscaling":{},"management":{"autoUpgrade":"true","autoRepair":"true"},"maxPodsConstraint":{"maxPodsPerNode":"X"},"podIpv4CidrSize":"XX","locations":["europe-XXXXXX-X"],"networkConfig":{"podRange":"gke-XXXXXX-XXXXX-XXXXX-XXXXXX","podIpv4CidrBlock":"XX.X.X.X/XX"},"selfLink":"https://container.googleapis.com/v1/projects/XXXXX-XXXXX-XXXXXX/zones/europe-XXXXXXX-X/clusters/cluster-XXXX/nodePools/default-XXXXXX","version":"X.XX.XX-XXX.XXX","instanceGroupUrls":["https://www.googleapis.com/compute/v1/projects/XXXXX-XXXXX-XXXXXX/zones/europe-XXXXXXX-X/instanceGroupManagers/gke-XXXXXXXXXX"],"status":"RUNNING","upgradeSettings":{"maxSurge":"1"}}],"locations":["europe-XXXXXXX-X"],"resourceLabels":{"XXXX":"XXXX","XXXX":"XXXX"},"labelFingerprint":"XXXXXXX","legacyAbac":{},"ipAllocationPolicy":{"useIpAliases":"true","clusterIpv4Cidr":"XX.X.X.X/XX","servicesIpv4Cidr":"XX.X.X.X/XX","clusterSecondaryRangeName":"gke-XXXXXX-XXXX-XXXX-XXXXXXXX","servicesSecondaryRangeName":"gke-XXXXXX-XXXX-XXXX-XXXXXXXX","clusterIpv4CidrBlock":"XX.X.X.X/XX","servicesIpv4CidrBlock":"XX.X.X.X/XX"},"masterAuthorizedNetworksConfig":{"enabled":"true"},"maintenancePolicy":{"resourceVersion":"XXXXXXX"},"autoscaling":{"autoscalingProfile":"BALANCED"},"networkConfig":{"network":"projects/XXXXX-XXXXX-XXXXXX/global/networks/XXXXXXX","subnetwork":"projects/XXXXX-XXXXX-XXXXXX/regions/europe-XXXXXXX-X/subnetworks/XXXXXXX","defaultSnatStatus":{},"datapathProvider":"LEGACY_DATAPATH"},"defaultMaxPodsConstraint":{"maxPodsPerNode":"10"},"authenticatorGroupsConfig":{},"privateClusterConfig":{"enablePrivateNodes":"true","masterIpv4CidrBlock":"XXX.XX.X.X/XX","privateEndpoint":"XXX.XX.X.X","publicEndpoint":"XX.XXX.XX.XXX","peeringName":"gke-XXXXXXXXXX-XXXX-XXXX-XXXX"},"databaseEncryption":{"state":"DECRYPTED"},"shieldedNodes":{"enabled":"true"},"releaseChannel":{"channel":"STABLE"},"notificationConfig":{"pubsub":{}},"selfLink":"https://container.googleapis.com/v1/projects/XXXXX-XXXXX-XXXXXX/zones/europe-XXXXXXX-X/clusters/cluster-test","zone":"europe-XXXXXXX-X","endpoint":"XX.XXX.XX.XXX","initialClusterVersion":"1.18.XX-gke.XXXX","currentMasterVersion":"1.18.XX-gke.XXX","currentNodeVersion":"1.18.XX-gke.XXX","createTime":"XXXX-XX-XXTXX:XX:XX+00:00","status":"RUNNING","servicesIpv4Cidr":"XXX.XX.X.X/XX","instanceGroupUrls":["https://www.googleapis.com/compute/v1/projects/XXXXX-XXXXX-XXXXXX/zones/europe-XXXXXXX-X/instanceGroupManagers/gke-cluster-test-default-pool-66b31b29-grp"],"location":"europe-XXXXXXX-X","id":"684222eecbdd4cb5838087f026760021d88e1bc7d9894aXXXXXXXXXXXXX","loggingConfig":{"componentConfig":{"enableComponents":["SYSTEM_COMPONENTS","WORKLOADS"]}},"monitoringConfig":{"componentConfig":{"enableComponents":["SYSTEM_COMPONENTS"]}}}]}
```



#### List Node Pools
List node pools for the Google Kubernetes Engine cluster based on the specified search criteria. Note that action is not working on Siemplify entities. Additionally, filtering logic is working based on the node pool name field.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the node pool name field.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action should will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain the substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the node pool name field.|False|String||
|Max Records To Return|Specify how many records to return.|False|String|50|



##### JSON Results
```json
{"nodePools":[{"name":"XXXXX-XXXX","config":{"machineType":"XX-XXX","diskSizeGb":"XX","oauthScopes":["https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append"], "metadata":{"disable-legacy-endpoints":"true"},"imageType":"COS","tags":["pod-net-tag"],"serviceAccount":"default", "diskType":"pd-standard","shieldedInstanceConfig":{"enableIntegrityMonitoring":"true"}},"initialNodeCount":"3", "autoscaling":{"enabled":"true","minNodeCount":"2","maxNodeCount":"10"},"management":{"autoUpgrade":"true","autoRepair":"true"},"maxPodsConstraint":{"maxPodsPerNode":"8"},"podIpv4CidrSize":"28", "locations":["europe-XXXXXXX-X"],"networkConfig":{"podRange":"gke-XXXXXX-XXXX-XXXX-XXXXXXX","podIpv4CidrBlock":"XX.X.X.X/XX"},"selfLink":"https://container.googleapis.com/v1/projects/XXXXXX-XXXXXX-XXXXXXX/zones/europe-XXXXXXX-X/clusters/XXXXX-XXXX/nodePools/XXXXX-XXXX","version":"1.18.20-XXX.XXX","instanceGroupUrls":["https://www.googleapis.com/compute/v1/projects/XXXXXX-XXXXXX-XXXXXXX/zones/XXXXX-XXXX/instanceGroupManagers/gke-XXXXXX-XXXX-XXXX-XXXXXXX"],"status":"RUNNING","upgradeSettings":{"maxSurge":"X"}}],"cluster_name":"XXXXXXXX"}
```



#### List Operations
List Google Kubernetes Engine operations for a location based on the specified search criteria. Note that action is not working on Siemplify entities. Additionally, filtering logic is working based on the operation name field.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project for which to fetch the operations for. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Location|Specify Google Compute Engine location for which to fetch the operations for. Example: europe-central2-a|True|String||
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action should will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain the substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the operation name field.|False|String||
|Max Records To Return|Specify how many records to return. Default: 50.|False|String|50|



##### JSON Results
```json
{"operations":[{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"UPDATE_CLUSTER","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXXX/zones/europe-XXXXXXX-X/operations/operation-XXXXXXXXXXX-XXXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXXX/zones/europe-XXXXXXX-X/clusters/XXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ"}]}
```



#### Ping
Test connectivity to the Google Kubernetes Engine service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Set Cluster Addons
Create an operation to set addons for the Google Kubernetes Engine cluster. Action is async. Note that action is not working on Siemplify entities. Additionally, if the target cluster is already going under configuration change, new configuration changes will not be accepted until current configuration changes finish.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|HTTP Load Balancing|Specify the value for the HTTP Load Balancing addon configuration.|False|List|Not Changed|
|Horizontal Pod Autoscaling|Specify the value for the Horizontal Pod Autoscaling addon configuration.|False|List|Not Changed|
|Network Policy Config|Specify the value for the Network Policy Config addon configuration.|False|List|Not Changed|
|Cloud Run Config|Specify the value for the Cloud Run Config addon configuration.|False|List|Not Changed|
|DNS Cache Config|Specify the value for the DNS Cache Config addon configuration.|False|List|Not Changed|
|Config Connector Config|Specify the value for the Config Connector Config addon.|False|List|Not Changed|
|GCE Persistent Disk Csi Driver Config|Specify the value for the GCE Persistent Disk Csi Driver Config addon.|False|List|Not Changed|
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"UPDATE_CLUSTER","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","cluster_name":"XXXXXXXX"}
```



#### Set Cluster Labels
Create an operation to set labels for the Google Kubernetes Engine cluster. Action is async. Action appends new labels to any existing cluster labels. Note that action is not working on Siemplify entities. Additionally, if the target cluster is already going under configuration change, new configuration changes will not be accepted until current configuration changes finish.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|Cluster Labels|Specify a JSON object that contains labels to add to the cluster. Please consider default value for the format reference. Action appends new labels to any existing cluster labels.|True|String||
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"UPDATE_CLUSTER","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","cluster_name":"XXXXXXXX"}
```



#### Set Node Autoscaling
Create an operation to set node pool autoscaling configuration for the Google Kubernetes Engine cluster. Action is async. Note that action is not working on Siemplify entities. Additionally, if the target cluster is already going under configuration change, new configuration changes will not be accepted until current configuration changes finish.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|Node Pool Name|Specify node pool name for the Google Kubernetes Engine cluster.|True|String||
|Autoscaling Mode|Specify autoscaling mode status for the node pool.|False|List|Not Changed|
|Minimum Node Count|Specify minimum node count for the node pool configuration.|False|String||
|Maximum Node Count|Specify maximum node count for the node pool configuration.|False|String||
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"UPDATE_CLUSTER","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","cluster_name":"XXXXXXXX"}
```



#### Set Node Count
Create an operation to set node count for the Google Kubernetes Engine cluster node pool. Action is async. Note that action is not working on Siemplify entities. Additionally, if the target cluster is already going under configuration change, new configuration changes will not be accepted until current configuration changes finish.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|Node Pool Name|Specify node pool name for the Google Kubernetes Engine cluster.|True|String||
|Node Count|Specify node count for the Google Kubernetes Engine cluster node pool.|True|String||
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"SET_NODE_POOL_SIZE","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","cluster_name":"XXXXXXXX"}
```



#### Set Node Pool Management
Create an operation to set node pool management configuration for the Google Kubernetes Engine cluster. Action is async. Note that action is not working on Siemplify entities. Additionally, if the target cluster is already going under configuration change, new configuration changes will not be accepted until current configuration changes finish.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Project ID|Specify the name of the project in which to search for clusters in. If nothing is provided, the project will be extracted from integration configuration.|False|String||
|Cluster Location|Specify Google Compute Engine location in which to search for clusters in. Example: europe-central2-a|True|String||
|Cluster Name|Specify Google Kubernetes Engine cluster name.|True|String||
|Node Pool Name|Specify node pool name for the Google Kubernetes Engine cluster.|True|String||
|Auto Upgrade|Specify the status of auto upgrade management feature.|False|List|Not Changed|
|Auto Repair|Specify the status of auto repair management feature.|False|List|Not Changed|
|Wait for cluster configuration change operation to finish|If enabled, action will wait for the results of the cluster configuration change operation.|False|Boolean|false|



##### JSON Results
```json
{"name":"operation-XXXXXXXXXXX-XXXXXXXXX","zone":"europe-XXXXXXX-X","operationType":"SET_NODE_POOL_MANAGEMENT","status":"DONE","selfLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/operations/operation-XXXXXXXXXXXXX-XXXXXXXX","targetLink":"https://container.googleapis.com/v1/projects/XXXXXXXXXXXX/zones/europe-XXXXXXXX-X/clusters/XXXXXXX-XXXX","startTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","endTime":"XXXX-XX-XXTXX:XX:XX.XXXXXXXXXZ","cluster_name":"XXXXXXXX"}
```









