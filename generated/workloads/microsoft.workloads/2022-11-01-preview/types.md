# Microsoft.Workloads @ 2022-11-01-preview

## Resource Microsoft.Workloads/monitors@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [UserAssignedServiceIdentity](#userassignedserviceidentity): Managed service identity (user assigned identities)
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MonitorProperties](#monitorproperties): SAP monitor properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Workloads/monitors' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/monitors/providerInstances@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [UserAssignedServiceIdentity](#userassignedserviceidentity): Managed service identity (user assigned identities)
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProviderInstanceProperties](#providerinstanceproperties): Provider Instance properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.Workloads/monitors/providerInstances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/monitors/sapLandscapeMonitor@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [SapLandscapeMonitorProperties](#saplandscapemonitorproperties): Sap Landscape Monitor properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.Workloads/monitors/sapLandscapeMonitor' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/sapVirtualInstances@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [UserAssignedServiceIdentity](#userassignedserviceidentity): Managed service identity (user assigned identities)
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SAPVirtualInstanceProperties](#sapvirtualinstanceproperties) (Required): Defines the Virtual Instance for SAP solutions resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Workloads/sapVirtualInstances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/sapVirtualInstances/applicationInstances@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SAPApplicationServerProperties](#sapapplicationserverproperties): Defines the SAP Application Server instance properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Workloads/sapVirtualInstances/applicationInstances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/sapVirtualInstances/centralInstances@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SAPCentralServerProperties](#sapcentralserverproperties): Defines the SAP Central Services Instance properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Workloads/sapVirtualInstances/centralInstances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Workloads/sapVirtualInstances/databaseInstances@2022-11-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SAPDatabaseProperties](#sapdatabaseproperties): Defines the Database properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Workloads/sapVirtualInstances/databaseInstances' (ReadOnly, DeployTimeConstant): The resource type

## ApplicationServerConfiguration
### Properties
* **instanceCount**: int (Required): The number of app server instances.
* **subnetId**: string (Required): The subnet id.
* **virtualMachineConfiguration**: [VirtualMachineConfiguration](#virtualmachineconfiguration) (Required): Gets or sets the virtual machine configuration.

## ApplicationServerFullResourceNames
### Properties
* **availabilitySetName**: string: The full name for availability set. In case name is not provided, it will be defaulted to {SID}-App-AvSet.
* **virtualMachines**: [VirtualMachineResourceNames](#virtualmachineresourcenames)[]: The list of virtual machine naming details.

## ApplicationServerVmDetails
### Properties
* **storageDetails**: [StorageInformation](#storageinformation)[] (ReadOnly): Storage details of all the Storage Accounts attached to the App Virtual Machine. For e.g. NFS on AFS Shared Storage.
* **type**: 'Active' | 'Standby' | 'Unknown' | string (ReadOnly): Defines the type of application server VM.
* **virtualMachineId**: string (ReadOnly)

## CentralServerConfiguration
### Properties
* **instanceCount**: int (Required): The number of central server VMs.
* **subnetId**: string (Required): The subnet id.
* **virtualMachineConfiguration**: [VirtualMachineConfiguration](#virtualmachineconfiguration) (Required): Gets or sets the virtual machine configuration.

## CentralServerFullResourceNames
### Properties
* **availabilitySetName**: string: The full name for availability set. In case name is not provided, it will be defaulted to {SID}-ASCS-AvSet.
* **loadBalancer**: [LoadBalancerResourceNames](#loadbalancerresourcenames): The resource names object for load balancer and related resources.
* **virtualMachines**: [VirtualMachineResourceNames](#virtualmachineresourcenames)[] {maxLength: 2}: The list of names for all ASCS virtual machines to be deployed. The number of entries in this list should be equal to the number VMs to be created for ASCS layer. At maximum, there can be two virtual machines at this layer: ASCS and ERS.

## CentralServerVmDetails
### Properties
* **storageDetails**: [StorageInformation](#storageinformation)[] (ReadOnly): Storage details of all the Storage Accounts attached to the ASCS Virtual Machine. For e.g. NFS on AFS Shared Storage.
* **type**: 'ASCS' | 'ERS' | 'ERSInactive' | 'Primary' | 'Secondary' | 'Standby' | 'Unknown' | string (ReadOnly): Defines the type of central server VM.
* **virtualMachineId**: string (ReadOnly)

## DatabaseConfiguration
### Properties
* **databaseType**: 'DB2' | 'HANA' | string: The database type.
* **diskConfiguration**: [DiskConfiguration](#diskconfiguration): Gets or sets the disk configuration.
* **instanceCount**: int (Required): The number of database VMs.
* **subnetId**: string (Required): The subnet id.
* **virtualMachineConfiguration**: [VirtualMachineConfiguration](#virtualmachineconfiguration) (Required): Gets or sets the virtual machine configuration.

## DatabaseServerFullResourceNames
### Properties
* **availabilitySetName**: string: The full name for availability set. In case name is not provided, it will be defaulted to {SID}-DB-AvSet.
* **loadBalancer**: [LoadBalancerResourceNames](#loadbalancerresourcenames): The resource names object for load balancer and related resources.
* **virtualMachines**: [VirtualMachineResourceNames](#virtualmachineresourcenames)[] {maxLength: 2}: The list of virtual machine naming details.

## DatabaseVmDetails
### Properties
* **status**: 'Offline' | 'PartiallyRunning' | 'Running' | 'SoftShutdown' | 'Starting' | 'Stopping' | 'Unavailable' | string (ReadOnly): Defines the SAP Instance status.
* **storageDetails**: [StorageInformation](#storageinformation)[] (ReadOnly): Storage details of all the Storage Accounts attached to the Database Virtual Machine. For e.g. NFS on AFS Shared Storage.
* **virtualMachineId**: string (ReadOnly)

## DeployerVmPackages
### Properties
* **storageAccountId**: string: The deployer VM packages storage account id
* **url**: string: The URL to the deployer VM packages file.

## DiskConfiguration
### Properties
* **diskVolumeConfigurations**: [DiskConfigurationDiskVolumeConfigurations](#diskconfigurationdiskvolumeconfigurations): The disk configuration for the db volume. For HANA, Required volumes are: ['hana/data', 'hana/log', hana/shared', 'usr/sap', 'os'], Optional volume : ['backup'].

## DiskConfigurationDiskVolumeConfigurations
### Properties
### Additional Properties
* **Additional Properties Type**: [DiskVolumeConfiguration](#diskvolumeconfiguration)

## DiskSku
### Properties
* **name**: 'PremiumV2_LRS' | 'Premium_LRS' | 'Premium_ZRS' | 'StandardSSD_LRS' | 'StandardSSD_ZRS' | 'Standard_LRS' | 'UltraSSD_LRS' | string: Defines the disk sku name.

## DiskVolumeConfiguration
### Properties
* **count**: int: The total number of disks required for the concerned volume.
* **sizeGB**: int: The disk size in GB.
* **sku**: [DiskSku](#disksku): The disk SKU details.

## EnqueueReplicationServerProperties
### Properties
* **ersVersion**: 'EnqueueReplicator1' | 'EnqueueReplicator2' | string (ReadOnly): Defines the type of Enqueue Replication Server.
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **hostname**: string (ReadOnly): ERS SAP Hostname.
* **instanceNo**: string (ReadOnly): ERS Instance Number.
* **ipAddress**: string (ReadOnly): ERS SAP IP Address.
* **kernelPatch**: string (ReadOnly): ERS SAP Kernel Patch level.
* **kernelVersion**: string (ReadOnly): ERS SAP Kernel Version.

## EnqueueServerProperties
### Properties
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **hostname**: string (ReadOnly): Enqueue Server SAP Hostname.
* **ipAddress**: string (ReadOnly): Enqueue Server SAP IP Address.
* **port**: int (ReadOnly): Enqueue Server Port.

## Error
### Properties
* **code**: string (ReadOnly): Server-defined set of error codes.
* **details**: [Error](#error)[] (ReadOnly): Array of details about specific errors that led to this reported error.
* **innerError**: [ErrorInnerError](#errorinnererror) (ReadOnly): Object containing more specific information than  the current object about the error.
* **message**: string (ReadOnly): Human-readable representation of the error.
* **target**: string (ReadOnly): Target of the error.

## ErrorDefinition
### Properties
* **code**: string (ReadOnly): Service specific error code which serves as the substatus for the HTTP error code.
* **details**: [ErrorDefinition](#errordefinition)[] (ReadOnly): Internal error details.
* **message**: string (ReadOnly): Description of the error.

## ErrorInnerError
### Properties
* **innerError**: [Error](#error): Standard error object.

## FileShareConfiguration
* **Discriminator**: configurationType

### Base Properties

### CreateAndMountFileShareConfiguration
#### Properties
* **configurationType**: 'CreateAndMount' (Required): The type of file share config.
* **resourceGroup**: string: The name of file share resource group. The app rg is used in case of missing input.
* **storageAccountName**: string: The name of file share storage account name . A custom name is used in case of missing input.

### MountFileShareConfiguration
#### Properties
* **configurationType**: 'Mount' (Required): The type of file share config.
* **id**: string (Required): The fileshare resource ID
* **privateEndpointId**: string (Required): The private endpoint resource ID

### SkipFileShareConfiguration
#### Properties
* **configurationType**: 'Skip' (Required): The type of file share config.


## GatewayServerProperties
### Properties
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **port**: int (ReadOnly): Gateway Port.

## HighAvailabilityConfiguration
### Properties
* **highAvailabilityType**: 'AvailabilitySet' | 'AvailabilityZone' | string (Required): The high availability type.

## HighAvailabilitySoftwareConfiguration
### Properties
* **fencingClientId**: string (Required): The fencing client id.
* **fencingClientPassword**: string {sensitive} (Required): The fencing client id secret/password. The secret should never expire. This will be used pacemaker to start/stop the cluster VMs.

## ImageReference
### Properties
* **exactVersion**: string (ReadOnly): Specifies in decimal numbers, the version of platform image or marketplace image used to create the virtual machine. This readonly field differs from 'version', only if the value specified in 'version' field is 'latest'.
* **offer**: string: Specifies the offer of the platform image or marketplace image used to create the virtual machine.
* **publisher**: string: The image publisher.
* **sharedGalleryImageId**: string: Specified the shared gallery image unique id for vm deployment. This can be fetched from shared gallery image GET call.
* **sku**: string: The image SKU.
* **version**: string: Specifies the version of the platform image or marketplace image used to create the virtual machine. The allowed formats are Major.Minor.Build or 'latest'. Major, Minor, and Build are decimal numbers. Specify 'latest' to use the latest version of an image available at deploy time. Even if you use 'latest', the VM image will not automatically update after deploy time even if a new version becomes available.

## InfrastructureConfiguration
* **Discriminator**: deploymentType

### Base Properties
* **appResourceGroup**: string (Required): The application resource group where SAP system resources will be deployed.

### SingleServerConfiguration
#### Properties
* **customResourceNames**: [SingleServerCustomResourceNames](#singleservercustomresourcenames): The set of custom names to be used for underlying azure resources that are part of the SAP system.
* **databaseType**: 'DB2' | 'HANA' | string: The database type.
* **dbDiskConfiguration**: [DiskConfiguration](#diskconfiguration): Gets or sets the disk configuration.
* **deploymentType**: 'SingleServer' (Required): The type of SAP deployment, single server or Three tier.
* **networkConfiguration**: [NetworkConfiguration](#networkconfiguration): Network configuration for the server
* **subnetId**: string (Required): The subnet id.
* **virtualMachineConfiguration**: [VirtualMachineConfiguration](#virtualmachineconfiguration) (Required): Gets or sets the virtual machine configuration.

### ThreeTierConfiguration
#### Properties
* **applicationServer**: [ApplicationServerConfiguration](#applicationserverconfiguration) (Required): The application server configuration.
* **centralServer**: [CentralServerConfiguration](#centralserverconfiguration) (Required): The central server configuration.
* **customResourceNames**: [ThreeTierCustomResourceNames](#threetiercustomresourcenames): The set of custom names to be used for underlying azure resources that are part of the SAP system.
* **databaseServer**: [DatabaseConfiguration](#databaseconfiguration) (Required): The database configuration.
* **deploymentType**: 'ThreeTier' (Required): The type of SAP deployment, single server or Three tier.
* **highAvailabilityConfig**: [HighAvailabilityConfiguration](#highavailabilityconfiguration): The high availability configuration.
* **networkConfiguration**: [NetworkConfiguration](#networkconfiguration): Network configuration common to all servers
* **storageConfiguration**: [StorageConfiguration](#storageconfiguration): The storage configuration.


## LoadBalancerDetails
### Properties
* **id**: string (ReadOnly)

## LoadBalancerResourceNames
### Properties
* **backendPoolNames**: string[] {maxLength: 1}: The list of backend pool names. Currently, ACSS deploys only one backend pool and hence, size of this list should be 1
* **frontendIpConfigurationNames**: string[] {maxLength: 2}: The list of frontend IP configuration names. If provided as input, size of this list should be 2 for cs layer and should be 1 for database layer.
* **healthProbeNames**: string[] {maxLength: 2}: The list of health probe names. If provided as input, size of this list should be 2 for cs layer and should be 1 for database layer.
* **loadBalancerName**: string: The full resource name for load balancer. If this value is not provided, load balancer will be name as {ASCS/DB}-loadBalancer.

## ManagedRGConfiguration
### Properties
* **name**: string: Managed resource group name

## MessageServerProperties
### Properties
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **hostname**: string (ReadOnly): Message Server SAP Hostname.
* **httpPort**: int (ReadOnly): Message Server HTTP Port.
* **httpsPort**: int (ReadOnly): Message Server HTTPS Port.
* **internalMsPort**: int (ReadOnly): Message Server internal MS port.
* **ipAddress**: string (ReadOnly): Message server IP Address.
* **msPort**: int (ReadOnly): Message Server port.

## MonitorProperties
### Properties
* **appLocation**: string: The SAP monitor resources will be deployed in the SAP monitoring region. The subnet region should be same as the SAP monitoring region.
* **errors**: [MonitorPropertiesErrors](#monitorpropertieserrors) (ReadOnly): Defines the SAP monitor errors.
* **logAnalyticsWorkspaceArmId**: string: The ARM ID of the Log Analytics Workspace that is used for SAP monitoring.
* **managedResourceGroupConfiguration**: [ManagedRGConfiguration](#managedrgconfiguration): Managed resource group configuration
* **monitorSubnet**: string: The subnet which the SAP monitor will be deployed in
* **msiArmId**: string (ReadOnly): The ARM ID of the MSI used for SAP monitoring.
* **provisioningState**: 'Accepted' | 'Creating' | 'Deleting' | 'Failed' | 'Migrating' | 'Succeeded' | 'Updating' | string (ReadOnly): State of provisioning of the SAP monitor.
* **routingPreference**: 'Default' | 'RouteAll' | string: Sets the routing preference of the SAP monitor. By default only RFC1918 traffic is routed to the customer VNET.
* **storageAccountArmId**: string (ReadOnly): The ARM ID of the Storage account used for SAP monitoring.
* **zoneRedundancyPreference**: string: Sets the preference for zone redundancy on resources created for the SAP monitor. By default resources will be created which do not support zone redundancy.

## MonitorPropertiesErrors
### Properties
* **code**: string (ReadOnly): Server-defined set of error codes.
* **details**: [Error](#error)[] (ReadOnly): Array of details about specific errors that led to this reported error.
* **innerError**: [ErrorInnerError](#errorinnererror) (ReadOnly): Object containing more specific information than  the current object about the error.
* **message**: string (ReadOnly): Human-readable representation of the error.
* **target**: string (ReadOnly): Target of the error.

## NetworkConfiguration
### Properties
* **isSecondaryIpEnabled**: bool: Specifies whether a secondary IP address should be added to the network interface on all VMs of the SAP system being deployed

## NetworkInterfaceResourceNames
### Properties
* **networkInterfaceName**: string: The full name for network interface. If name is not provided, service uses a default name based on the deployment type. For SingleServer, default name is {SID}-Nic. In case of HA-AvZone systems, default name will be {SID}-{App/ASCS/DB}-Zone{A/B}-Nic with an incrementor at the end in case of more than 1 instance per layer. For distributed and HA-AvSet systems, default name will be {SID}-{App/ASCS/DB}-Nic with an incrementor at the end in case of more than 1 instance per layer.

## OSConfiguration
* **Discriminator**: osType

### Base Properties

### LinuxConfiguration
#### Properties
* **disablePasswordAuthentication**: bool: Specifies whether password authentication should be disabled.
* **osType**: 'Linux' (Required): The OS Type
* **ssh**: [SshConfiguration](#sshconfiguration): Specifies the ssh key configuration for a Linux OS. (This property is deprecated, please use 'sshKeyPair' instead)
* **sshKeyPair**: [SshKeyPair](#sshkeypair): The SSH Key-pair used to authenticate with the VM's.

### WindowsConfiguration
#### Properties
* **osType**: 'Windows' (Required): The OS Type


## OSProfile
### Properties
* **adminPassword**: string {sensitive}: Specifies the password of the administrator account. <br><br> **Minimum-length (Windows):** 8 characters <br><br> **Minimum-length (Linux):** 6 characters <br><br> **Max-length (Windows):** 123 characters <br><br> **Max-length (Linux):** 72 characters <br><br> **Complexity requirements:** 3 out of 4 conditions below need to be fulfilled <br> Has lower characters <br>Has upper characters <br> Has a digit <br> Has a special character (Regex match [\W_]) <br><br> **Disallowed values:** "abc@123", "P@$$w0rd", "P@ssw0rd", "P@ssword123", "Pa$$word", "pass@word1", "Password!", "Password1", "Password22", "iloveyou!" <br><br> For resetting the password, see [How to reset the Remote Desktop service or its login password in a Windows VM](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/reset-rdp) <br><br> For resetting root password, see [Manage users, SSH, and check or repair disks on Azure Linux VMs using the VMAccess Extension](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/troubleshoot-ssh-connection)
* **adminUsername**: string: Specifies the name of the administrator account. <br><br> This property cannot be updated after the VM is created. <br><br> **Windows-only restriction:** Cannot end in "." <br><br> **Disallowed values:** "administrator", "admin", "user", "user1", "test", "user2", "test1", "user3", "admin1", "1", "123", "a", "actuser", "adm", "admin2", "aspnet", "backup", "console", "david", "guest", "john", "owner", "root", "server", "sql", "support", "support_388945a0", "sys", "test2", "test3", "user4", "user5". <br><br> **Minimum-length (Linux):** 1  character <br><br> **Max-length (Linux):** 64 characters <br><br> **Max-length (Windows):** 20 characters.
* **osConfiguration**: [OSConfiguration](#osconfiguration): Specifies Windows operating system settings on the virtual machine.

## OsSapConfiguration
### Properties
* **deployerVmPackages**: [DeployerVmPackages](#deployervmpackages): The url and storage account ID where deployer VM packages are uploaded
* **sapFqdn**: string: The FQDN to set for the SAP system

## ProviderInstanceProperties
### Properties
* **errors**: [ProviderInstancePropertiesErrors](#providerinstancepropertieserrors) (ReadOnly): Defines the provider instance errors.
* **providerSettings**: [ProviderSpecificProperties](#providerspecificproperties): Defines the provider instance errors.
* **provisioningState**: 'Accepted' | 'Creating' | 'Deleting' | 'Failed' | 'Migrating' | 'Succeeded' | 'Updating' | string (ReadOnly): State of provisioning of the provider instance

## ProviderInstancePropertiesErrors
### Properties
* **code**: string (ReadOnly): Server-defined set of error codes.
* **details**: [Error](#error)[] (ReadOnly): Array of details about specific errors that led to this reported error.
* **innerError**: [ErrorInnerError](#errorinnererror) (ReadOnly): Object containing more specific information than  the current object about the error.
* **message**: string (ReadOnly): Human-readable representation of the error.
* **target**: string (ReadOnly): Target of the error.

## ProviderSpecificProperties
* **Discriminator**: providerType

### Base Properties

### DB2ProviderInstanceProperties
#### Properties
* **dbName**: string: Gets or sets the db2 database name.
* **dbPassword**: string {sensitive}: Gets or sets the db2 database password.
* **dbPasswordUri**: string: Gets or sets the key vault URI to secret with the database password.
* **dbPort**: string: Gets or sets the db2 database sql port.
* **dbUsername**: string: Gets or sets the db2 database user name.
* **hostname**: string: Gets or sets the target virtual machine name.
* **providerType**: 'Db2' (Required): The provider type. For example, the value can be SapHana.
* **sapSid**: string: Gets or sets the SAP System Identifier
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the DB2 Database.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.

### MsSqlServerProviderInstanceProperties
#### Properties
* **dbPassword**: string {sensitive}: Gets or sets the database password.
* **dbPasswordUri**: string: Gets or sets the key vault URI to secret with the database password.
* **dbPort**: string: Gets or sets the database sql port.
* **dbUsername**: string: Gets or sets the database user name.
* **hostname**: string: Gets or sets the SQL server host name.
* **providerType**: 'MsSqlServer' (Required): The provider type. For example, the value can be SapHana.
* **sapSid**: string: Gets or sets the SAP System Identifier
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the SQL Database.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.

### PrometheusHaClusterProviderInstanceProperties
#### Properties
* **clusterName**: string: Gets or sets the clusterName.
* **hostname**: string: Gets or sets the target machine name.
* **prometheusUrl**: string: URL of the Node Exporter endpoint.
* **providerType**: 'PrometheusHaCluster' (Required): The provider type. For example, the value can be SapHana.
* **sid**: string: Gets or sets the cluster sid.
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the HA cluster exporter.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.

### PrometheusOSProviderInstanceProperties
#### Properties
* **prometheusUrl**: string: URL of the Node Exporter endpoint
* **providerType**: 'PrometheusOS' (Required): The provider type. For example, the value can be SapHana.
* **sapSid**: string: Gets or sets the SAP System Identifier
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the prometheus node exporter.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.

### HanaDbProviderInstanceProperties
#### Properties
* **dbName**: string: Gets or sets the hana database name.
* **dbPassword**: string {sensitive}: Gets or sets the database password.
* **dbPasswordUri**: string: Gets or sets the key vault URI to secret with the database password.
* **dbUsername**: string: Gets or sets the database user name.
* **hostname**: string: Gets or sets the target virtual machine size.
* **instanceNumber**: string: Gets or sets the database instance number.
* **providerType**: 'SapHana' (Required): The provider type. For example, the value can be SapHana.
* **sapSid**: string: Gets or sets the SAP System Identifier.
* **sqlPort**: string: Gets or sets the database sql port.
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the DB.
* **sslHostNameInCertificate**: string: Gets or sets the hostname(s) in the SSL certificate.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.

### SapNetWeaverProviderInstanceProperties
#### Properties
* **providerType**: 'SapNetWeaver' (Required): The provider type. For example, the value can be SapHana.
* **sapClientId**: string: Gets or sets the SAP Client ID.
* **sapHostFileEntries**: string[]: Gets or sets the list of HostFile Entries
* **sapHostname**: string: Gets or sets the target virtual machine IP Address/FQDN.
* **sapInstanceNr**: string: Gets or sets the instance number of SAP NetWeaver.
* **sapPassword**: string {sensitive}: Sets the SAP password.
* **sapPasswordUri**: string: Gets or sets the key vault URI to secret with the SAP password.
* **sapPortNumber**: string: Gets or sets the SAP HTTP port number.
* **sapSid**: string: Gets or sets the SAP System Identifier
* **sapUsername**: string: Gets or sets the SAP user name.
* **sslCertificateUri**: string: Gets or sets the blob URI to SSL certificate for the SAP system.
* **sslPreference**: 'Disabled' | 'RootCertificate' | 'ServerCertificate' | string: Gets or sets certificate preference if secure communication is enabled.


## SAPApplicationServerProperties
### Properties
* **errors**: [SAPVirtualInstanceError](#sapvirtualinstanceerror) (ReadOnly): Defines the Application Instance errors.
* **gatewayPort**: int (ReadOnly): Application server instance gateway Port.
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **hostname**: string (ReadOnly): Application server instance SAP hostname.
* **icmHttpPort**: int (ReadOnly): Application server instance ICM HTTP Port.
* **icmHttpsPort**: int (ReadOnly): Application server instance ICM HTTPS Port.
* **instanceNo**: string (ReadOnly): Application server Instance Number.
* **ipAddress**: string (ReadOnly): Application server instance SAP IP Address.
* **kernelPatch**: string (ReadOnly): Application server instance SAP Kernel Patch level.
* **kernelVersion**: string (ReadOnly): Application server instance SAP Kernel Version.
* **loadBalancerDetails**: [LoadBalancerDetails](#loadbalancerdetails) (ReadOnly): The Load Balancer details such as LoadBalancer ID attached to Application Server Virtual Machines
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Defines the provisioning states.
* **status**: 'Offline' | 'PartiallyRunning' | 'Running' | 'SoftShutdown' | 'Starting' | 'Stopping' | 'Unavailable' | string (ReadOnly): Defines the SAP Instance status.
* **subnet**: string (ReadOnly): Application server Subnet.
* **vmDetails**: [ApplicationServerVmDetails](#applicationservervmdetails)[] (ReadOnly): The list of virtual machines.

## SAPCentralServerProperties
### Properties
* **enqueueReplicationServerProperties**: [EnqueueReplicationServerProperties](#enqueuereplicationserverproperties): Defines the SAP Enqueue Replication Server (ERS) properties.
* **enqueueServerProperties**: [EnqueueServerProperties](#enqueueserverproperties): Defines the SAP Enqueue Server properties.
* **errors**: [SAPVirtualInstanceError](#sapvirtualinstanceerror) (ReadOnly): Defines the errors related to SAP Central Services Instance resource.
* **gatewayServerProperties**: [GatewayServerProperties](#gatewayserverproperties): Defines the SAP Gateway Server properties.
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **instanceNo**: string (ReadOnly): The central services instance number.
* **kernelPatch**: string (ReadOnly): The central services instance Kernel Patch level.
* **kernelVersion**: string (ReadOnly): The central services instance Kernel Version.
* **loadBalancerDetails**: [LoadBalancerDetails](#loadbalancerdetails) (ReadOnly): The Load Balancer details such as LoadBalancer ID attached to ASCS Virtual Machines
* **messageServerProperties**: [MessageServerProperties](#messageserverproperties): Defines the SAP Message Server properties.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Defines the provisioning states.
* **status**: 'Offline' | 'PartiallyRunning' | 'Running' | 'SoftShutdown' | 'Starting' | 'Stopping' | 'Unavailable' | string (ReadOnly): Defines the SAP Instance status.
* **subnet**: string (ReadOnly): The central services instance subnet.
* **vmDetails**: [CentralServerVmDetails](#centralservervmdetails)[] (ReadOnly): The list of virtual machines corresponding to the Central Services instance.

## SAPConfiguration
* **Discriminator**: configurationType

### Base Properties

### DeploymentConfiguration
#### Properties
* **appLocation**: string: The geo-location where the SAP system is to be created.
* **configurationType**: 'Deployment' (Required): The configuration Type.
* **infrastructureConfiguration**: [InfrastructureConfiguration](#infrastructureconfiguration): The infrastructure configuration.
* **softwareConfiguration**: [SoftwareConfiguration](#softwareconfiguration): The software configuration.

### DeploymentWithOSConfiguration
#### Properties
* **appLocation**: string: The geo-location where the SAP system is to be created.
* **configurationType**: 'DeploymentWithOSConfig' (Required): The configuration Type.
* **infrastructureConfiguration**: [InfrastructureConfiguration](#infrastructureconfiguration): The infrastructure configuration.
* **osSapConfiguration**: [OsSapConfiguration](#ossapconfiguration): The OS and SAP configuration.
* **softwareConfiguration**: [SoftwareConfiguration](#softwareconfiguration): The software configuration.

### DiscoveryConfiguration
#### Properties
* **appLocation**: string (ReadOnly): The geo-location where the SAP system exists.
* **centralServerVmId**: string: The virtual machine ID of the Central Server.
* **configurationType**: 'Discovery' (Required): The configuration Type.
* **managedRgStorageAccountName**: string {minLength: 3, maxLength: 24}: The custom storage account name for the storage account created by the service in the managed resource group created as part of VIS deployment.<br><br>Refer to the storage account naming rules [here](https://learn.microsoft.com/azure/azure-resource-manager/management/resource-name-rules#microsoftstorage).<br><br>If not provided, the service will create the storage account with a random name.


## SAPDatabaseProperties
### Properties
* **databaseSid**: string (ReadOnly): Database SID name.
* **databaseType**: string (ReadOnly): Database type, that is if the DB is HANA, DB2, Oracle, SAP ASE, Max DB or MS SQL Server.
* **errors**: [SAPVirtualInstanceError](#sapvirtualinstanceerror) (ReadOnly): Defines the errors related to Database resource.
* **ipAddress**: string (ReadOnly): Database IP Address.
* **loadBalancerDetails**: [LoadBalancerDetails](#loadbalancerdetails) (ReadOnly): The Load Balancer details such as LoadBalancer ID attached to Database Virtual Machines
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Defines the provisioning states.
* **status**: 'Offline' | 'PartiallyRunning' | 'Running' | 'SoftShutdown' | 'Starting' | 'Stopping' | 'Unavailable' | string (ReadOnly): Defines the SAP Instance status.
* **subnet**: string (ReadOnly): Database subnet.
* **vmDetails**: [DatabaseVmDetails](#databasevmdetails)[] (ReadOnly): The list of virtual machines corresponding to the Database resource.

## SapLandscapeMonitorMetricThresholds
### Properties
* **green**: int: Gets or sets the threshold value for Green.
* **name**: string: Gets or sets the name of the threshold.
* **red**: int: Gets or sets the threshold value for Red.
* **yellow**: int: Gets or sets the threshold value for Yellow.

## SapLandscapeMonitorProperties
### Properties
* **grouping**: [SapLandscapeMonitorPropertiesGrouping](#saplandscapemonitorpropertiesgrouping): Gets or sets the SID groupings by landscape and Environment.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Failed' | 'Succeeded' | string (ReadOnly): State of provisioning of the SAP monitor.
* **topMetricsThresholds**: [SapLandscapeMonitorMetricThresholds](#saplandscapemonitormetricthresholds)[]: Gets or sets the list Top Metric Thresholds for SAP Landscape Monitor Dashboard

## SapLandscapeMonitorPropertiesGrouping
### Properties
* **landscape**: [SapLandscapeMonitorSidMapping](#saplandscapemonitorsidmapping)[]: Gets or sets the list of landscape to SID mappings.
* **sapApplication**: [SapLandscapeMonitorSidMapping](#saplandscapemonitorsidmapping)[]: Gets or sets the list of Sap Applications to SID mappings.

## SapLandscapeMonitorSidMapping
### Properties
* **name**: string: Gets or sets the name of the grouping.
* **topSid**: string[]: Gets or sets the list of SID's.

## SAPVirtualInstanceError
### Properties
* **properties**: [ErrorDefinition](#errordefinition): The Virtual Instance for SAP error body.

## SAPVirtualInstanceProperties
### Properties
* **configuration**: [SAPConfiguration](#sapconfiguration) (Required): Defines if the SAP system is being created using Azure Center for SAP solutions (ACSS) or if an existing SAP system is being registered with ACSS
* **environment**: 'NonProd' | 'Prod' | string (Required): Defines the environment type - Production/Non Production.
* **errors**: [SAPVirtualInstanceError](#sapvirtualinstanceerror) (ReadOnly): Indicates any errors on the Virtual Instance for SAP solutions resource.
* **health**: 'Degraded' | 'Healthy' | 'Unhealthy' | 'Unknown' | string (ReadOnly): Defines the health of SAP Instances.
* **managedResourceGroupConfiguration**: [ManagedRGConfiguration](#managedrgconfiguration): Managed resource group configuration
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Defines the provisioning states.
* **sapProduct**: 'ECC' | 'Other' | 'S4HANA' | string (Required): Defines the SAP Product type.
* **state**: 'DiscoveryFailed' | 'DiscoveryInProgress' | 'DiscoveryPending' | 'InfrastructureDeploymentFailed' | 'InfrastructureDeploymentInProgress' | 'InfrastructureDeploymentPending' | 'RegistrationComplete' | 'SoftwareDetectionFailed' | 'SoftwareDetectionInProgress' | 'SoftwareInstallationFailed' | 'SoftwareInstallationInProgress' | 'SoftwareInstallationPending' | string (ReadOnly): Defines the Virtual Instance for SAP state.
* **status**: 'Offline' | 'PartiallyRunning' | 'Running' | 'SoftShutdown' | 'Starting' | 'Stopping' | 'Unavailable' | string (ReadOnly): Defines the SAP Instance status.

## SharedStorageResourceNames
### Properties
* **sharedStorageAccountName**: string: The full name of the shared storage account. If it is not provided, it will be defaulted to {SID}nfs{guid of 15 chars}.
* **sharedStorageAccountPrivateEndPointName**: string: The full name of private end point for the shared storage account. If it is not provided, it will be defaulted to {storageAccountName}_pe

## SingleServerCustomResourceNames
* **Discriminator**: namingPatternType

### Base Properties

### SingleServerFullResourceNames
#### Properties
* **namingPatternType**: 'FullResourceName' (Required): The pattern type to be used for resource naming.
* **virtualMachine**: [VirtualMachineResourceNames](#virtualmachineresourcenames): The resource names object for virtual machine and related resources.


## SoftwareConfiguration
* **Discriminator**: softwareInstallationType

### Base Properties

### ExternalInstallationSoftwareConfiguration
#### Properties
* **centralServerVmId**: string: The resource ID of the virtual machine containing the central server instance.
* **softwareInstallationType**: 'External' (Required): The SAP software installation Type.

### SAPInstallWithoutOSConfigSoftwareConfiguration
#### Properties
* **bomUrl**: string (Required): The URL to the SAP Build of Materials(BOM) file.
* **highAvailabilitySoftwareConfiguration**: [HighAvailabilitySoftwareConfiguration](#highavailabilitysoftwareconfiguration): Gets or sets the HA software configuration.
* **sapBitsStorageAccountId**: string (Required): The SAP bits storage account id.
* **softwareInstallationType**: 'SAPInstallWithoutOSConfig' (Required): The SAP software installation Type.
* **softwareVersion**: string (Required): The software version to install.

### ServiceInitiatedSoftwareConfiguration
#### Properties
* **bomUrl**: string (Required): The URL to the SAP Build of Materials(BOM) file.
* **highAvailabilitySoftwareConfiguration**: [HighAvailabilitySoftwareConfiguration](#highavailabilitysoftwareconfiguration): Gets or sets the HA software configuration.
* **sapBitsStorageAccountId**: string (Required): The SAP bits storage account id.
* **sapFqdn**: string (Required): The FQDN to set for the SAP system during install.
* **softwareInstallationType**: 'ServiceInitiated' (Required): The SAP software installation Type.
* **softwareVersion**: string (Required): The software version to install.
* **sshPrivateKey**: string {sensitive} (Required): The SSH private key.


## SshConfiguration
### Properties
* **publicKeys**: [SshPublicKey](#sshpublickey)[]: The list of SSH public keys used to authenticate with linux based VMs.

## SshKeyPair
### Properties
* **privateKey**: string {sensitive}: SSH private key.
* **publicKey**: string: SSH public key

## SshPublicKey
### Properties
* **keyData**: string: SSH public key certificate used to authenticate with the VM through ssh. The key needs to be at least 2048-bit and in ssh-rsa format. <br><br> For creating ssh keys, see [Create SSH keys on Linux and Mac for Linux VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/create-ssh-keys-detailed).

## StorageConfiguration
### Properties
* **transportFileShareConfiguration**: [FileShareConfiguration](#fileshareconfiguration): The properties of the transport directory attached to the VIS. The default for transportFileShareConfiguration is the createAndMount flow if storage configuration is missing.

## StorageInformation
### Properties
* **id**: string (ReadOnly)

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## ThreeTierCustomResourceNames
* **Discriminator**: namingPatternType

### Base Properties

### ThreeTierFullResourceNames
#### Properties
* **applicationServer**: [ApplicationServerFullResourceNames](#applicationserverfullresourcenames): The full resource names object for application layer resources. The number of entries in this list should be equal to the number VMs to be created for application layer.
* **centralServer**: [CentralServerFullResourceNames](#centralserverfullresourcenames): The full resource names object for central server layer resources.
* **databaseServer**: [DatabaseServerFullResourceNames](#databaseserverfullresourcenames): The full resource names object for database layer resources. The number of entries in this list should be equal to the number VMs to be created for database layer.
* **namingPatternType**: 'FullResourceName' (Required): The pattern type to be used for resource naming.
* **sharedStorage**: [SharedStorageResourceNames](#sharedstorageresourcenames): The resource names object for shared storage.


## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## UserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserAssignedIdentity](#userassignedidentity)

## UserAssignedIdentity
### Properties
* **clientId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The client ID of the assigned identity.
* **principalId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The principal ID of the assigned identity.

## UserAssignedServiceIdentity
### Properties
* **type**: 'None' | 'UserAssigned' | string (Required): Type of manage identity
* **userAssignedIdentities**: [UserAssignedIdentities](#userassignedidentities): User assigned identities dictionary

## VirtualMachineConfiguration
### Properties
* **imageReference**: [ImageReference](#imagereference) (Required): The image reference.
* **osProfile**: [OSProfile](#osprofile) (Required): The OS profile.
* **vmSize**: string (Required): The virtual machine size.

## VirtualMachineResourceNames
### Properties
* **dataDiskNames**: [VirtualMachineResourceNamesDataDiskNames](#virtualmachineresourcenamesdatadisknames): The full resource names for virtual machine data disks. This is a dictionary containing list of names of data disks per volume. Currently supported volumes for database layer are ['hana/data', 'hana/log', hana/shared', 'usr/sap', 'os', 'backup']. For application and cs layers, only 'default' volume is supported
* **hostName**: string: The full name for virtual-machine's host (computer name). Currently, ACSS only supports host names which are less than or equal to 13 characters long. If this value is not provided, vmName will be used as host name.
* **networkInterfaces**: [NetworkInterfaceResourceNames](#networkinterfaceresourcenames)[] {maxLength: 1}: The list of network interface name objects for the selected virtual machine. Currently, only one network interface is supported per virtual machine.
* **osDiskName**: string: The full name for OS disk attached to the VM. If this value is not provided, it will be named by ARM as per its default naming standards (prefixed with vm name). There is only one OS disk attached per Virtual Machine.
* **vmName**: string: The full name for virtual machine. The length of this field can be upto 64 characters. If name is not provided, service uses a default name based on the deployment type. For SingleServer, default name is {SID}vm. In case of HA-AvZone systems, default name will be {SID}{app/ascs/db}z{a/b}vm with an incrementor at the end in case of more than 1 vm per layer. For distributed and HA-AvSet systems, default name will be {SID}{app/ascs/db}vm with an incrementor at the end in case of more than 1 vm per layer.

## VirtualMachineResourceNamesDataDiskNames
### Properties
### Additional Properties
* **Additional Properties Type**: string[]

