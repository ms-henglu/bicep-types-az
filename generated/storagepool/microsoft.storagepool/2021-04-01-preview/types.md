# Microsoft.StoragePool @ 2021-04-01-preview

## Resource Microsoft.StoragePool/diskPools@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DiskPoolCreateProperties](#diskpoolcreateproperties) (Required): Properties for Disk Pool create or update request.
* **sku**: [Sku](#sku) (Required): Sku for ARM resource
* **systemData**: [SystemMetadata](#systemmetadata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Resource tags.
* **type**: 'Microsoft.StoragePool/diskPools' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.StoragePool/diskPools/iscsiTargets@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [IscsiTargetCreateProperties](#iscsitargetcreateproperties) (Required): Properties for iSCSI Target create or update request.
* **systemData**: [SystemMetadata](#systemmetadata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.StoragePool/diskPools/iscsiTargets' (ReadOnly, DeployTimeConstant): The resource type

## DiskPoolCreateProperties
### Properties
* **additionalCapabilities**: string[]: List of additional capabilities for a Disk Pool.
* **availabilityZones**: string[]: Logical zone for Disk Pool resource; example: ["1"].
* **disks**: [Disk](#disk)[]: List of Azure Managed Disks to attach to a Disk Pool.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Invalid' | 'Pending' | 'Succeeded' | 'Updating' (ReadOnly): State of the operation on the resource.
* **status**: 'Healthy' | 'Invalid' | 'Running' | 'Stopped (deallocated)' | 'Stopped' | 'Unhealthy' | 'Unknown' | 'Updating' (ReadOnly): Operational status of the Disk Pool.
* **subnetId**: string (Required): Azure Resource ID of a Subnet for the Disk Pool.

## Disk
### Properties
* **id**: string (Required): Unique Azure Resource ID of the Managed Disk.

## Sku
### Properties
* **name**: string (Required): Sku name
* **tier**: string: Sku tier

## SystemMetadata
### Properties
* **createdAt**: string (ReadOnly): The timestamp of resource creation (UTC).
* **createdBy**: string (ReadOnly): The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that created the resource.
* **lastModifiedAt**: string (ReadOnly): The type of identity that last modified the resource.
* **lastModifiedBy**: string (ReadOnly): The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that last modified the resource.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## IscsiTargetCreateProperties
### Properties
* **aclMode**: 'Dynamic' | 'Static' (Required): Mode for Target connectivity.
* **endpoints**: string[] (ReadOnly): List of private IPv4 addresses to connect to the iSCSI Target.
* **luns**: [IscsiLun](#iscsilun)[]: List of LUNs to be exposed through iSCSI Target.
* **port**: int (ReadOnly): The port used by iSCSI Target portal group.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Invalid' | 'Pending' | 'Succeeded' | 'Updating' (ReadOnly): State of the operation on the resource.
* **staticAcls**: [Acl](#acl)[]: Access Control List (ACL) for an iSCSI Target; defines LUN masking policy
* **status**: 'Healthy' | 'Invalid' | 'Running' | 'Stopped (deallocated)' | 'Stopped' | 'Unhealthy' | 'Unknown' | 'Updating' (ReadOnly): Operational status of the iSCSI Target.
* **targetIqn**: string: iSCSI Target IQN (iSCSI Qualified Name); example: "iqn.2005-03.org.iscsi:server".

## IscsiLun
### Properties
* **lun**: int (ReadOnly): Specifies the Logical Unit Number of the iSCSI LUN.
* **managedDiskAzureResourceId**: string (Required): Azure Resource ID of the Managed Disk.
* **name**: string (Required): User defined name for iSCSI LUN; example: "lun0"

## Acl
### Properties
* **initiatorIqn**: string (Required): iSCSI initiator IQN (iSCSI Qualified Name); example: "iqn.2005-03.org.iscsi:client".
* **mappedLuns**: string[] (Required): List of LUN names mapped to the ACL.
