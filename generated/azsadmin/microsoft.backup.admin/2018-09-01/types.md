# Microsoft.Backup.Admin @ 2018-09-01

## Resource Microsoft.Backup.Admin/backupLocations@2018-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BackupLocationModel](#backuplocationmodel): Properties of a backup location.
* **tags**: [ResourceTags](#resourcetags): List of key value pairs.
* **type**: 'Microsoft.Backup.Admin/backupLocations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Backup.Admin/backupLocations/backups@2018-09-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BackupModel](#backupmodel) (ReadOnly): Properties for a backup.
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): List of key value pairs.
* **type**: 'Microsoft.Backup.Admin/backupLocations/backups' (ReadOnly, DeployTimeConstant): The resource type

## Function createBackup (Microsoft.Backup.Admin/backupLocations@2018-09-01)
* **Resource**: Microsoft.Backup.Admin/backupLocations
* **ApiVersion**: 2018-09-01
* **Output**: [Backup](#backup)

## Function pruneExternalStore (Microsoft.Backup.Admin/backupLocations@2018-09-01)
* **Resource**: Microsoft.Backup.Admin/backupLocations
* **ApiVersion**: 2018-09-01
* **Input**: [PruneBackupStoreOperationOptionModel](#prunebackupstoreoperationoptionmodel)
* **Output**: [PruneList](#prunelist)

## Function restore (Microsoft.Backup.Admin/backupLocations/backups@2018-09-01)
* **Resource**: Microsoft.Backup.Admin/backupLocations/backups
* **ApiVersion**: 2018-09-01
* **Input**: [RestoreOptions](#restoreoptions)

## Backup
### Properties
* **id**: string (ReadOnly): URI of the resource.
* **location**: string: Location of the resource.
* **name**: string (ReadOnly): Name of the resource.
* **properties**: [BackupModel](#backupmodel): Properties for a backup.
* **tags**: [ResourceTags](#resourcetags): List of key value pairs.
* **type**: string (ReadOnly): Type of resource.

## BackupInfo
### Properties
* **backupDataVersion**: string (ReadOnly): Version of the backup data.
* **createdDateTime**: string (ReadOnly): Creation time of the backup.
* **deploymentID**: string (ReadOnly): Deployment Id of the stamp.
* **encryptionCertThumbprint**: string (ReadOnly): The thumbprint of the certificate used to encrypt the backup encryption key.
* **isCloudRecoveryReady**: bool (ReadOnly): True if the backup can be used for cloud recovery scenario.
* **oemVersion**: string (ReadOnly): OEM version.
* **roleStatus**: [RoleOperationStatus](#roleoperationstatus)[] (ReadOnly): Backup status for each role.
* **stampVersion**: string (ReadOnly): Azure Stack stamp version of the backup.
* **status**: 'Creating' | 'Deleted' | 'Failed' | 'PartialSucceeded' | 'Queued' | 'Running' | 'Succeeded' (ReadOnly): Current status of the backup.
* **timeTakenToCreate**: string (ReadOnly): Duration to create the backup.

## BackupLocationModel
### Properties
* **externalStoreDefault**: [ExternalStore](#externalstore): Information about an external storage location.

## BackupModel
### Properties
* **backupInfo**: [BackupInfo](#backupinfo): Holds information for a backup.

## ExternalStore
### Properties
* **availableCapacity**: string (ReadOnly): Free space at the backup location.
* **backupFrequencyInHours**: int: The interval, in hours, for the frequency that the scheduler takes a backup.
* **backupRetentionPeriodInDays**: int: The retention period, in days, for backs in the storage location.
* **encryptionCertBase64**: string: The base64 raw data for the backup encryption certificate.
* **encryptionCertThumbprint**: string (ReadOnly): The thumbprint of the encryption certificate.
* **isBackupSchedulerEnabled**: bool: True if the backup scheduler is enabled.
* **lastBackupTime**: string (ReadOnly): Time of backup.
* **nextBackupTime**: string (ReadOnly): The scheduled time of the next backup.
* **password**: string: Password to access the location.
* **path**: string: Path to the update location
* **userName**: string: Username to access the location.

## PruneBackupStoreOperationOptionModel
### Properties
* **operationType**: 'Default' | 'DryRun': Operation type.

## PruneList
### Properties
* **properties**: [PruneModel](#prunemodel): Holds information for a backup.

## PruneModel
### Properties
* **pathsToDelete**: string[]: Garbage file list.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## RestoreOptions
### Properties
* **decryptionCertBase64**: string: The certificate file raw data in Base64 string. This should be the .pfx file with the private key.
* **decryptionCertPassword**: string: The password for the decryption certificate.
* **roleName**: string: The Azure Stack role name for restore, set it to empty for all infrastructure role

## RoleOperationStatus
### Properties
* **roleName**: string: Name of the role.
* **status**: 'Creating' | 'Deleted' | 'Failed' | 'PartialSucceeded' | 'Queued' | 'Running' | 'Succeeded': Status of the role.

