# Microsoft.IoTSecurity @ 2021-02-01-preview

## Resource Microsoft.IoTSecurity/defenderSettings@2021-02-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2021-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [DefenderSettingsProperties](#defendersettingsproperties): IoT Defender settings properties
* **type**: 'Microsoft.IoTSecurity/defenderSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.IoTSecurity/locations/deviceGroups@2021-02-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2021-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: any: Device group properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.IoTSecurity/locations/deviceGroups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.IoTSecurity/onPremiseSensors@2021-02-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2021-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: any (ReadOnly): On-premise IoT sensor properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.IoTSecurity/onPremiseSensors' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.IoTSecurity/sensors@2021-02-01-preview
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2021-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SensorProperties](#sensorproperties): IoT sensor properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.IoTSecurity/sensors' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.IoTSecurity/sites@2021-02-01-preview
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2021-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [SiteProperties](#siteproperties): IoT site properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.IoTSecurity/sites' (ReadOnly, DeployTimeConstant): The resource type

## Function packageDownloads (Microsoft.IoTSecurity/defenderSettings@2021-02-01-preview)
* **Resource**: Microsoft.IoTSecurity/defenderSettings
* **ApiVersion**: 2021-02-01-preview
* **Output**: [PackageDownloads](#packagedownloads)

## DefenderSettingsProperties
### Properties
* **deviceQuota**: int (Required): Size of the device quota. Value is required to be in multiples of 100.
* **evaluationEndTime**: string (ReadOnly): End time of the evaluation period, if such exist
* **mdeIntegration**: [DefenderSettingsPropertiesMdeIntegration](#defendersettingspropertiesmdeintegration) (Required): MDE integration configuration
* **onboardingKind**: 'Default' | 'Evaluation' | 'MigratedToAzure' | 'Purchased' | string (Required): The kind of onboarding for the subscription
* **sentinelWorkspaceResourceIds**: string[] (Required): Sentinel Workspace Resource Ids

## DefenderSettingsPropertiesMdeIntegration
### Properties
* **status**: 'Disabled' | 'Enabled' | string (Required): Integration status

## PackageDownloadInfo
### Properties
* **link**: string (ReadOnly): Download link
* **version**: string (ReadOnly): Version number
* **versionKind**: 'Latest' | 'Preview' | 'Previous' | string (ReadOnly): Kind of the version

## PackageDownloads
### Properties
* **authorizedDevicesImportTemplate**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Authorized devices import template
* **centralManager**: [PackageDownloadsCentralManager](#packagedownloadscentralmanager) (ReadOnly): All downloads for Central Manager
* **deviceInformationUpdateImportTemplate**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Authorized devices import template
* **sensor**: [PackageDownloadsSensor](#packagedownloadssensor) (ReadOnly): Contains all Sensor binary downloads
* **snmp**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): SNMP Server file
* **threatIntelligence**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): All downloads for threat intelligence
* **wmiTool**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Used for local configuration export

## PackageDownloadsCentralManager
### Properties
* **full**: [PackageDownloadsCentralManagerFull](#packagedownloadscentralmanagerfull) (ReadOnly): Contains full package downloads
* **upgrade**: [UpgradePackageDownloadInfo](#upgradepackagedownloadinfo)[] (ReadOnly): Central Manager upgrade package downloads (on existing installations)

## PackageDownloadsCentralManagerFull
### Properties
* **iso**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Contains all ISO full versions of the Central Manager
* **ovf**: [PackageDownloadsCentralManagerFullOvf](#packagedownloadscentralmanagerfullovf) (ReadOnly): Contains all OVF (virtual machine) full versions of the Central Manager

## PackageDownloadsCentralManagerFullOvf
### Properties
* **enterprise**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): The Enterprise package type
* **enterpriseHighAvailability**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): The EnterpriseHighAvailability package type
* **medium**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): The Medium package type
* **mediumHighAvailability**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): The MediumHighAvailability package type

## PackageDownloadsSensor
### Properties
* **full**: [PackageDownloadsSensorFull](#packagedownloadssensorfull) (ReadOnly): Contains full package downloads
* **upgrade**: [UpgradePackageDownloadInfo](#upgradepackagedownloadinfo)[]: Sensor upgrade package downloads (on existing installations)

## PackageDownloadsSensorFull
### Properties
* **iso**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Contains all ISO full versions for the sensor
* **ovf**: [PackageDownloadsSensorFullOvf](#packagedownloadssensorfullovf): Contains all OVF (virtual machine) full versions for the sensor

## PackageDownloadsSensorFullOvf
### Properties
* **enterprise**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Enterprise package type
* **line**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Line package type
* **medium**: [PackageDownloadInfo](#packagedownloadinfo)[] (ReadOnly): Medium package type

## SensorProperties
### Properties
* **connectivityTime**: string (ReadOnly): Last connectivity time of the IoT sensor
* **dynamicLearning**: bool (ReadOnly): Dynamic mode status of the IoT sensor
* **learningMode**: bool (ReadOnly): Learning mode status of the IoT sensor
* **sensorStatus**: 'Disconnected' | 'Ok' | 'Unavailable' | string (ReadOnly): Status of the IoT sensor
* **sensorType**: 'Enterprise' | 'Ot' | string: Type of sensor
* **sensorVersion**: string (ReadOnly): Version of the IoT sensor
* **tiAutomaticUpdates**: bool: TI Automatic mode status of the IoT sensor
* **tiStatus**: 'Failed' | 'InProgress' | 'Ok' | 'UpdateAvailable' | string (ReadOnly): TI Status of the IoT sensor
* **tiVersion**: string (ReadOnly): TI Version of the IoT sensor
* **zone**: string: Zone of the IoT sensor

## SiteProperties
### Properties
* **displayName**: string (Required): Display name of the IoT site
* **tags**: [SitePropertiesTags](#sitepropertiestags): Tags of the IoT site

## SitePropertiesTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## UpgradePackageDownloadInfo
### Properties
* **fromVersion**: string (ReadOnly): Minimum base version for upgrade
* **link**: string (ReadOnly): Download link
* **version**: string (ReadOnly): Version number
* **versionKind**: 'Latest' | 'Preview' | 'Previous' | string (ReadOnly): Kind of the version

