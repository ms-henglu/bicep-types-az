# Microsoft.DBforMySQL @ 2022-09-30-preview

## Resource Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): The cmk identity for the server.
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ServerProperties](#serverproperties): Properties of the server.
* **sku**: [Sku](#sku): The SKU (pricing tier) of the server.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.DBforMySQL/flexibleServers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DBforMySQL/flexibleServers/backups@2022-09-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ServerBackupProperties](#serverbackupproperties) (ReadOnly): The properties of a server backup.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: 'Microsoft.DBforMySQL/flexibleServers/backups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DBforMySQL/flexibleServers/privateEndpointConnections@2022-09-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.DBforMySQL/flexibleServers/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DBforMySQL/flexibleServers/privateLinkResources@2022-09-30-preview (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateLinkResourceProperties](#privatelinkresourceproperties) (ReadOnly): Resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.DBforMySQL/flexibleServers/privateLinkResources' (ReadOnly, DeployTimeConstant): The resource type

## Function backupAndExport (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview
* **Input**: [BackupAndExportRequest](#backupandexportrequest)
* **Output**: [BackupAndExportResponse](#backupandexportresponse)

## Function failover (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview

## Function resetGtid (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview
* **Input**: [ServerGtidSetParameter](#servergtidsetparameter)

## Function restart (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview
* **Input**: [ServerRestartParameter](#serverrestartparameter)

## Function start (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview

## Function stop (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview

## Function validateBackup (Microsoft.DBforMySQL/flexibleServers@2022-09-30-preview)
* **Resource**: Microsoft.DBforMySQL/flexibleServers
* **ApiVersion**: 2022-09-30-preview
* **Output**: [ValidateBackupResponse](#validatebackupresponse)

## Backup
### Properties
* **backupRetentionDays**: int: Backup retention days for the server.
* **earliestRestoreDate**: string (ReadOnly): Earliest restore point creation time (ISO8601 format)
* **geoRedundantBackup**: 'Disabled' | 'Enabled' | string: Whether or not geo redundant backup is enabled.

## BackupAndExportRequest
### Properties
* **backupSettings**: [BackupSettings](#backupsettings) (Required): Backup Settings
* **targetDetails**: [BackupStoreDetails](#backupstoredetails) (Required): Backup Target Store Details

## BackupAndExportResponse
### Properties
* **endTime**: string: End time
* **error**: [ErrorResponse](#errorresponse): The BackupAndExport operation error response.
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **percentComplete**: int: Operation progress (0-100).
* **properties**: [BackupAndExportResponseProperties](#backupandexportresponseproperties): The response properties of a backup and export operation.
* **startTime**: string: Start time
* **status**: 'CancelInProgress' | 'Canceled' | 'Failed' | 'InProgress' | 'Pending' | 'Succeeded': The operation status
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## BackupAndExportResponseProperties
### Properties
* **backupMetadata**: string: Metadata related to backup to be stored for restoring resource in key-value pairs.
* **datasourceSizeInBytes**: int: Size of datasource in bytes
* **dataTransferredInBytes**: int: Data transferred in bytes

## BackupSettings
### Properties
* **backupFormat**: 'CollatedFormat' | 'None' | string: Backup Format for the current backup. (CollatedFormat is INTERNAL – DO NOT USE)
* **backupName**: string (Required): The name of the backup.

## BackupStoreDetails
* **Discriminator**: objectType

### Base Properties

### FullBackupStoreDetails
#### Properties
* **objectType**: 'FullBackupStoreDetails' (Required): Type of the specific object - used for deserializing
* **sasUriList**: string[] (Required): SASUriList of storage containers where backup data is to be streamed/copied.


## DataEncryption
### Properties
* **geoBackupKeyURI**: string: Geo backup key uri as key vault can't cross region, need cmk in same region as geo backup
* **geoBackupUserAssignedIdentityId**: string: Geo backup user identity resource id as identity can't cross region, need identity in same region as geo backup
* **primaryKeyURI**: string: Primary key uri
* **primaryUserAssignedIdentityId**: string: Primary user identity resource id
* **type**: 'AzureKeyVault' | 'SystemManaged': The key type, AzureKeyVault for enable cmk, SystemManaged for disable cmk.

## ErrorAdditionalInfo
### Properties
* **info**: any (ReadOnly): The additional info.
* **type**: string (ReadOnly): The additional info type.

## ErrorResponse
### Properties
* **additionalInfo**: [ErrorAdditionalInfo](#erroradditionalinfo)[] (ReadOnly): The error additional info.
* **code**: string (ReadOnly): The error code.
* **details**: [ErrorResponse](#errorresponse)[] (ReadOnly): The error details.
* **message**: string (ReadOnly): The error message.
* **target**: string (ReadOnly): The error target.

## HighAvailability
### Properties
* **mode**: 'Disabled' | 'SameZone' | 'ZoneRedundant' | string: High availability mode for a server.
* **standbyAvailabilityZone**: string: Availability zone of the standby server.
* **state**: 'CreatingStandby' | 'FailingOver' | 'Healthy' | 'NotEnabled' | 'RemovingStandby' | string (ReadOnly): The state of server high availability.

## Identity
### Properties
* **principalId**: string (ReadOnly): ObjectId from the KeyVault
* **tenantId**: string (ReadOnly): TenantId from the KeyVault
* **type**: 'UserAssigned' | string: Type of managed service identity.
* **userAssignedIdentities**: [IdentityUserAssignedIdentities](#identityuserassignedidentities): Metadata of user assigned identity.

## IdentityUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: any

## MaintenanceWindow
### Properties
* **customWindow**: string: indicates whether custom window is enabled or disabled
* **dayOfWeek**: int: day of week for maintenance window
* **startHour**: int: start hour for maintenance window
* **startMinute**: int: start minute for maintenance window

## Network
### Properties
* **delegatedSubnetResourceId**: string: Delegated subnet resource id used to setup vnet for a server.
* **privateDnsZoneResourceId**: string: Private DNS zone resource id.
* **publicNetworkAccess**: 'Disabled' | 'Enabled' | string: Whether or not public network access is allowed for this server. Value is 'Disabled' when server has VNet integration.

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly): The ARM identifier for private endpoint.

## PrivateEndpointConnectionProperties
### Properties
* **groupIds**: string[] (ReadOnly): The group ids for the private endpoint resource.
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The private endpoint resource.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate) (Required): A collection of information about the state of the connection between service consumer and provider.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | string (ReadOnly): The provisioning state of the private endpoint connection resource.

## PrivateLinkResourceProperties
### Properties
* **groupId**: string (ReadOnly): The private link resource group id.
* **requiredMembers**: string[] (ReadOnly): The private link resource required member names.
* **requiredZoneNames**: string[]: The private link resource private link DNS zone name.

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string: A message indicating if changes on the service provider require any updates on the consumer.
* **description**: string: The reason for approval/rejection of the connection.
* **status**: 'Approved' | 'Pending' | 'Rejected' | string: Indicates whether the connection has been Approved/Rejected/Removed by the owner of the service.

## ServerBackupProperties
### Properties
* **backupType**: string: Backup type.
* **completedTime**: string: Backup completed time (ISO8601 format).
* **source**: string: Backup source

## ServerGtidSetParameter
### Properties
* **gtidSet**: string: The gtid set of server.

## ServerProperties
### Properties
* **administratorLogin**: string: The administrator's login name of a server. Can only be specified when the server is being created (and is required for creation).
* **administratorLoginPassword**: string (WriteOnly): The password of the administrator login (required for server creation).
* **availabilityZone**: string: availability Zone information of the server.
* **backup**: [Backup](#backup): Backup related properties of a server.
* **createMode**: 'Default' | 'GeoRestore' | 'PointInTimeRestore' | 'Replica' | string (WriteOnly): The mode to create a new MySQL server.
* **dataEncryption**: [DataEncryption](#dataencryption): The Data Encryption for CMK.
* **fullyQualifiedDomainName**: string (ReadOnly): The fully qualified domain name of a server.
* **highAvailability**: [HighAvailability](#highavailability): High availability related properties of a server.
* **maintenanceWindow**: [MaintenanceWindow](#maintenancewindow): Maintenance window of a server.
* **network**: [Network](#network): Network related properties of a server.
* **replicaCapacity**: int (ReadOnly): The maximum number of replicas that a primary server can have.
* **replicationRole**: 'None' | 'Replica' | 'Source' | string: The replication role.
* **restorePointInTime**: string (WriteOnly): Restore point creation time (ISO8601 format), specifying the time to restore from.
* **sourceServerResourceId**: string: The source MySQL server id.
* **state**: 'Disabled' | 'Dropping' | 'Ready' | 'Starting' | 'Stopped' | 'Stopping' | 'Updating' | string (ReadOnly): The state of a server.
* **storage**: [Storage](#storage): Storage related properties of a server.
* **version**: '5.7' | '8.0.21' | string: Server version.

## ServerRestartParameter
### Properties
* **maxFailoverSeconds**: int: The maximum allowed failover time in seconds.
* **restartWithFailover**: 'Disabled' | 'Enabled' | string: Whether or not failover to standby server when restarting a server with high availability enabled.

## Sku
### Properties
* **name**: string (Required): The name of the sku, e.g. Standard_D32s_v3.
* **tier**: 'Burstable' | 'GeneralPurpose' | 'MemoryOptimized' | string (Required): The tier of the particular SKU, e.g. GeneralPurpose.

## Storage
### Properties
* **autoGrow**: 'Disabled' | 'Enabled' | string: Enable Storage Auto Grow or not.
* **autoIoScaling**: 'Disabled' | 'Enabled' | string: Enable IO Auto Scaling or not.
* **iops**: int: Storage IOPS for a server.
* **logOnDisk**: 'Disabled' | 'Enabled' | string: Enable Log On Disk or not.
* **storageSizeGB**: int: Max storage size allowed for a server.
* **storageSku**: string (ReadOnly): The sku name of the server storage.

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

## ValidateBackupResponse
### Properties
* **properties**: [ValidateBackupResponseProperties](#validatebackupresponseproperties): The response properties of a pre backup operation.

## ValidateBackupResponseProperties
### Properties
* **numberOfContainers**: int: Estimated no of storage containers required for resource data to be backed up.

