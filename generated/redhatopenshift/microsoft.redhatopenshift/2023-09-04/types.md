# Microsoft.RedHatOpenShift @ 2023-09-04

## Resource Microsoft.RedHatOpenShift/openShiftClusters@2023-09-04
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-09-04' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [OpenShiftClusterProperties](#openshiftclusterproperties): The cluster properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.RedHatOpenShift/openShiftClusters' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RedHatOpenShift/openshiftclusters/machinePool@2023-09-04
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-09-04' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1, maxLength: 63, pattern: "^[a-zA-Z0-9]$|^[a-zA-Z0-9][-_a-zA-Z0-9]*[a-zA-Z0-9]$"} (Required, DeployTimeConstant): The resource name
* **properties**: [MachinePoolProperties](#machinepoolproperties): The MachinePool Properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.RedHatOpenShift/openshiftclusters/machinePool' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RedHatOpenShift/openshiftclusters/secret@2023-09-04
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-09-04' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1, maxLength: 63, pattern: "^[a-zA-Z0-9]$|^[a-zA-Z0-9][-_a-zA-Z0-9]*[a-zA-Z0-9]$"} (Required, DeployTimeConstant): The resource name
* **properties**: [SecretProperties](#secretproperties): The Secret Properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.RedHatOpenShift/openshiftclusters/secret' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RedHatOpenShift/openshiftclusters/syncIdentityProvider@2023-09-04
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-09-04' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1, maxLength: 63, pattern: "^[a-zA-Z0-9]$|^[a-zA-Z0-9][-_a-zA-Z0-9]*[a-zA-Z0-9]$"} (Required, DeployTimeConstant): The resource name
* **properties**: [SyncIdentityProviderProperties](#syncidentityproviderproperties): The SyncIdentityProvider Properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.RedHatOpenShift/openshiftclusters/syncIdentityProvider' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RedHatOpenShift/openshiftclusters/syncSet@2023-09-04
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-09-04' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1, maxLength: 63, pattern: "^[a-zA-Z0-9]$|^[a-zA-Z0-9][-_a-zA-Z0-9]*[a-zA-Z0-9]$"} (Required, DeployTimeConstant): The resource name
* **properties**: [SyncSetProperties](#syncsetproperties): The Syncsets properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.RedHatOpenShift/openshiftclusters/syncSet' (ReadOnly, DeployTimeConstant): The resource type

## Function listAdminCredentials (Microsoft.RedHatOpenShift/openShiftClusters@2023-09-04)
* **Resource**: Microsoft.RedHatOpenShift/openShiftClusters
* **ApiVersion**: 2023-09-04
* **Output**: [OpenShiftClusterAdminKubeconfig](#openshiftclusteradminkubeconfig)

## Function listCredentials (Microsoft.RedHatOpenShift/openShiftClusters@2023-09-04)
* **Resource**: Microsoft.RedHatOpenShift/openShiftClusters
* **ApiVersion**: 2023-09-04
* **Output**: [OpenShiftClusterCredentials](#openshiftclustercredentials)

## APIServerProfile
### Properties
* **ip**: string: The IP of the cluster API server.
* **url**: string: The URL to access the cluster API server.
* **visibility**: 'Private' | 'Public' | string: API server visibility.

## ClusterProfile
### Properties
* **domain**: string: The domain for the cluster.
* **fipsValidatedModules**: 'Disabled' | 'Enabled' | string: If FIPS validated crypto modules are used
* **pullSecret**: string: The pull secret for the cluster.
* **resourceGroupId**: string: The ID of the cluster resource group.
* **version**: string: The version of the cluster.

## ConsoleProfile
### Properties
* **url**: string: The URL to access the cluster console.

## IngressProfile
### Properties
* **ip**: string: The IP of the ingress.
* **name**: string: The ingress profile name.
* **visibility**: 'Private' | 'Public' | string: Ingress visibility.

## MachinePoolProperties
### Properties
* **resources**: string

## MasterProfile
### Properties
* **diskEncryptionSetId**: string: The resource ID of an associated DiskEncryptionSet, if applicable.
* **encryptionAtHost**: 'Disabled' | 'Enabled' | string: Whether master virtual machines are encrypted at host.
* **subnetId**: string: The Azure resource ID of the master subnet.
* **vmSize**: string: The size of the master VMs.

## NetworkProfile
### Properties
* **outboundType**: 'Loadbalancer' | 'UserDefinedRouting' | string: The OutboundType used for egress traffic.
* **podCidr**: string: The CIDR used for OpenShift/Kubernetes Pods.
* **preconfiguredNSG**: 'Disabled' | 'Enabled' | string: Specifies whether subnets are pre-attached with an NSG
* **serviceCidr**: string: The CIDR used for OpenShift/Kubernetes Services.

## OpenShiftClusterAdminKubeconfig
### Properties
* **kubeconfig**: string {sensitive}: The base64-encoded kubeconfig file.

## OpenShiftClusterCredentials
### Properties
* **kubeadminPassword**: string {sensitive}: The password for the kubeadmin user.
* **kubeadminUsername**: string: The username for the kubeadmin user.

## OpenShiftClusterProperties
### Properties
* **apiserverProfile**: [APIServerProfile](#apiserverprofile): The cluster API server profile.
* **clusterProfile**: [ClusterProfile](#clusterprofile): The cluster profile.
* **consoleProfile**: [ConsoleProfile](#consoleprofile): The console profile.
* **ingressProfiles**: [IngressProfile](#ingressprofile)[]: The cluster ingress profiles.
* **masterProfile**: [MasterProfile](#masterprofile): The cluster master profile.
* **networkProfile**: [NetworkProfile](#networkprofile): The cluster network profile.
* **provisioningState**: 'AdminUpdating' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string: The cluster provisioning state.
* **servicePrincipalProfile**: [ServicePrincipalProfile](#serviceprincipalprofile): The cluster service principal profile.
* **workerProfiles**: [WorkerProfile](#workerprofile)[]: The cluster worker profiles.
* **workerProfilesStatus**: [WorkerProfile](#workerprofile)[] (ReadOnly): The cluster worker profiles status.

## SecretProperties
### Properties
* **secretResources**: string {sensitive}: The Secrets Resources.

## ServicePrincipalProfile
### Properties
* **clientId**: string: The client ID used for the cluster.
* **clientSecret**: string: The client secret used for the cluster.

## SyncIdentityProviderProperties
### Properties
* **resources**: string

## SyncSetProperties
### Properties
* **resources**: string: Resources represents the SyncSets configuration.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WorkerProfile
### Properties
* **count**: int: The number of worker VMs.
* **diskEncryptionSetId**: string: The resource ID of an associated DiskEncryptionSet, if applicable.
* **diskSizeGB**: int: The disk size of the worker VMs.
* **encryptionAtHost**: 'Disabled' | 'Enabled' | string: Whether master virtual machines are encrypted at host.
* **name**: string: The worker profile name.
* **subnetId**: string: The Azure resource ID of the worker subnet.
* **vmSize**: string: The size of the worker VMs.

