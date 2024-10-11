# Microsoft.HybridCompute @ 2022-12-27

## Resource Microsoft.HybridCompute/locations/publishers/extensionTypes/versions@2022-12-27 (ReadOnly)
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ExtensionValueProperties](#extensionvalueproperties) (ReadOnly): The single extension based on search criteria
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.HybridCompute/locations/publishers/extensionTypes/versions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/machines@2022-12-27
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): Identity for the resource.
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {minLength: 1, maxLength: 54, pattern: "^[a-zA-Z0-9-_\.]{1,54}$"} (Required, DeployTimeConstant): The resource name
* **properties**: [MachineProperties](#machineproperties): Hybrid Compute Machine properties
* **resources**: [MachineExtension](#machineextension)[] (ReadOnly): The list of extensions affiliated to the machine
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/machines/extensions@2022-12-27
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MachineExtensionProperties](#machineextensionproperties): Describes Machine Extension Properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.HybridCompute/machines/extensions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/privateLinkScopes@2022-12-27
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [HybridComputePrivateLinkScopeProperties](#hybridcomputeprivatelinkscopeproperties): Properties that define a Azure Arc PrivateLinkScope resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system meta data relating to this resource.
* **tags**: [PrivateLinkScopesResourceTags](#privatelinkscopesresourcetags): Resource tags
* **type**: 'Microsoft.HybridCompute/privateLinkScopes' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/privateLinkScopes/privateEndpointConnections@2022-12-27
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.HybridCompute/privateLinkScopes/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.HybridCompute/privateLinkScopes/privateLinkResources@2022-12-27 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-12-27' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateLinkResourceProperties](#privatelinkresourceproperties) (ReadOnly): Resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **type**: 'Microsoft.HybridCompute/privateLinkScopes/privateLinkResources' (ReadOnly, DeployTimeConstant): The resource type

## Function assessPatches (Microsoft.HybridCompute/machines@2022-12-27)
* **Resource**: Microsoft.HybridCompute/machines
* **ApiVersion**: 2022-12-27
* **Output**: [MachineAssessPatchesResult](#machineassesspatchesresult)

## Function installPatches (Microsoft.HybridCompute/machines@2022-12-27)
* **Resource**: Microsoft.HybridCompute/machines
* **ApiVersion**: 2022-12-27
* **Input**: [MachineInstallPatchesParameters](#machineinstallpatchesparameters)
* **Output**: [MachineInstallPatchesResult](#machineinstallpatchesresult)

## Function upgradeExtensions (Microsoft.HybridCompute/machines@2022-12-27)
* **Resource**: Microsoft.HybridCompute/machines
* **ApiVersion**: 2022-12-27
* **Input**: [MachineExtensionUpgrade](#machineextensionupgrade)

## AgentConfiguration
### Properties
* **configMode**: 'full' | 'monitor' | string (ReadOnly): Name of configuration mode to use. Modes are pre-defined configurations of security controls, extension allowlists and guest configuration, maintained by Microsoft.
* **extensionsAllowList**: [ConfigurationExtension](#configurationextension)[] (ReadOnly): Array of extensions that are allowed to be installed or updated.
* **extensionsBlockList**: [ConfigurationExtension](#configurationextension)[] (ReadOnly): Array of extensions that are blocked (cannot be installed or updated)
* **extensionsEnabled**: string (ReadOnly): Specifies whether the extension service is enabled or disabled.
* **guestConfigurationEnabled**: string (ReadOnly): Specified whether the guest configuration service is enabled or disabled.
* **incomingConnectionsPorts**: string[] (ReadOnly): Specifies the list of ports that the agent will be able to listen on.
* **proxyBypass**: string[] (ReadOnly): List of service names which should not use the specified proxy server.
* **proxyUrl**: string (ReadOnly): Specifies the URL of the proxy to be used.

## AgentUpgrade
### Properties
* **correlationId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"}: The correlation ID passed in from RSM per upgrade.
* **desiredVersion**: string: Specifies the version info w.r.t AgentUpgrade for the machine.
* **enableAutomaticUpgrade**: bool: Specifies if RSM should try to upgrade this machine
* **lastAttemptMessage**: string (ReadOnly): Failure message of last upgrade attempt if any.
* **lastAttemptStatus**: 'Failed' | 'Success' | string (ReadOnly): Specifies the status of Agent Upgrade.
* **lastAttemptTimestamp**: string (ReadOnly): Timestamp of last upgrade attempt

## AvailablePatchCountByClassification
### Properties
* **critical**: int (ReadOnly): Number of critical patches available for installation.
* **definition**: int (ReadOnly): Number of definition patches available for installation.
* **featurePack**: int (ReadOnly): Number of feature pack patches available for installation.
* **other**: int (ReadOnly): Number of other patches available for installation.
* **security**: int (ReadOnly): Number of security patches available for installation.
* **servicePack**: int (ReadOnly): Number of service pack patches available for installation.
* **tools**: int (ReadOnly): Number of tools patches available for installation.
* **updateRollup**: int (ReadOnly): Number of update Rollup patches available for installation.
* **updates**: int (ReadOnly): Number of updates category patches available for installation.

## CloudMetadata
### Properties
* **provider**: string (ReadOnly): Specifies the cloud provider (Azure/AWS/GCP...).

## ConfigurationExtension
### Properties
* **publisher**: string (ReadOnly): Publisher of the extension.
* **type**: string (ReadOnly): Type of the extension.

## DetectedProperties
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ErrorAdditionalInfo
### Properties
* **info**: any (ReadOnly): The additional info.
* **type**: string (ReadOnly): The additional info type.

## ErrorDetail
### Properties
* **additionalInfo**: [ErrorAdditionalInfo](#erroradditionalinfo)[] (ReadOnly): The error additional info.
* **code**: string (ReadOnly): The error code.
* **details**: [ErrorDetail](#errordetail)[] (ReadOnly): The error details.
* **message**: string (ReadOnly): The error message.
* **target**: string (ReadOnly): The error target.

## ExtensionTarget
### Properties
### Additional Properties
* **Additional Properties Type**: [ExtensionTargetProperties](#extensiontargetproperties)

## ExtensionTargetProperties
### Properties
* **targetVersion**: string: Properties for the specified Extension to Upgrade.

## ExtensionValueProperties
### Properties
* **extensionType**: string (ReadOnly): The type of the Extension being received.
* **publisher**: string (ReadOnly): The publisher of the Extension being received.
* **version**: string (ReadOnly): The version of the Extension being received.

## HybridComputePrivateLinkScopeProperties
### Properties
* **privateEndpointConnections**: [PrivateEndpointConnectionDataModel](#privateendpointconnectiondatamodel)[] (ReadOnly): The collection of associated Private Endpoint Connections.
* **privateLinkScopeId**: string (ReadOnly): The Guid id of the private link scope.
* **provisioningState**: string (ReadOnly): Current state of this PrivateLinkScope: whether or not is has been provisioned within the resource group it is defined. Users cannot change this value but are able to read from it. Values will include Provisioning ,Succeeded, Canceled and Failed.
* **publicNetworkAccess**: 'Disabled' | 'Enabled' | string: Indicates whether machines associated with the private link scope can also use public Azure Arc service endpoints.

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## LinuxParameters
### Properties
* **classificationsToInclude**: ('Critical' | 'Other' | 'Security' | string)[]: The update classifications to select when installing patches for Linux.
* **packageNameMasksToExclude**: string[]: packages to exclude in the patch operation. Format: packageName_packageVersion
* **packageNameMasksToInclude**: string[]: packages to include in the patch operation. Format: packageName_packageVersion

## LocationData
### Properties
* **city**: string: The city or locality where the resource is located.
* **countryOrRegion**: string: The country or region where the resource is located
* **district**: string: The district, state, or province where the resource is located.
* **name**: string {maxLength: 256} (Required): A canonical name for the geographic or physical location.

## MachineAssessPatchesResult
### Properties
* **assessmentActivityId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The activity ID of the operation that produced this result.
* **availablePatchCountByClassification**: [AvailablePatchCountByClassification](#availablepatchcountbyclassification): Summarization of patches available for installation on the machine by classification.
* **errorDetails**: [ErrorDetail](#errordetail) (ReadOnly): The errors that were encountered during execution of the operation. The details array contains the list of them.
* **lastModifiedDateTime**: string (ReadOnly): The UTC timestamp when the operation finished.
* **osType**: 'Linux' | 'Windows' | string (ReadOnly): The operating system type of the machine.
* **patchServiceUsed**: 'APT' | 'Unknown' | 'WU' | 'WU_WSUS' | 'YUM' | 'Zypper' | string (ReadOnly): Specifies the patch service used for the operation.
* **rebootPending**: bool (ReadOnly): The overall reboot status of the VM. It will be true when partially installed patches require a reboot to complete installation but the reboot has not yet occurred.
* **startDateTime**: string (ReadOnly): The UTC timestamp when the operation began.
* **startedBy**: 'Platform' | 'User' | string (ReadOnly): Indicates if operation was triggered by user or by platform.
* **status**: 'CompletedWithWarnings' | 'Failed' | 'InProgress' | 'Succeeded' | 'Unknown' | string (ReadOnly): The overall success or failure status of the operation. It remains "InProgress" until the operation completes. At that point it will become "Unknown", "Failed", "Succeeded", or "CompletedWithWarnings."

## MachineExtension
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (ReadOnly): The name of the resource
* **properties**: [MachineExtensionProperties](#machineextensionproperties): Describes Machine Extension Properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## MachineExtensionInstanceView
### Properties
* **name**: string: The machine extension name.
* **status**: [MachineExtensionInstanceViewStatus](#machineextensioninstanceviewstatus): Instance view status.
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## MachineExtensionInstanceViewStatus
### Properties
* **code**: string: The status code.
* **displayStatus**: string: The short localizable label for the status.
* **level**: 'Error' | 'Info' | 'Warning' | string: The level code.
* **message**: string: The detailed status message, including for alerts and error messages.
* **time**: string: The time of the status.

## MachineExtensionProperties
### Properties
* **autoUpgradeMinorVersion**: bool: Indicates whether the extension should use a newer minor version if one is available at deployment time. Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.
* **enableAutomaticUpgrade**: bool: Indicates whether the extension should be automatically upgraded by the platform if there is a newer version available.
* **forceUpdateTag**: string: How the extension handler should be forced to update even if the extension configuration has not changed.
* **instanceView**: [MachineExtensionInstanceView](#machineextensioninstanceview): The machine extension instance view.
* **protectedSettings**: [MachineExtensionPropertiesProtectedSettings](#machineextensionpropertiesprotectedsettings): The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **publisher**: string: The name of the extension handler publisher.
* **settings**: [MachineExtensionPropertiesSettings](#machineextensionpropertiessettings): Json formatted public settings for the extension.
* **type**: string: Specifies the type of the extension; an example is "CustomScriptExtension".
* **typeHandlerVersion**: string: Specifies the version of the script handler.

## MachineExtensionPropertiesProtectedSettings
### Properties
### Additional Properties
* **Additional Properties Type**: any

## MachineExtensionPropertiesSettings
### Properties
### Additional Properties
* **Additional Properties Type**: any

## MachineExtensionUpgrade
### Properties
* **extensionTargets**: [ExtensionTarget](#extensiontarget): Describes the Extension Target Properties.

## MachineInstallPatchesParameters
### Properties
* **linuxParameters**: [LinuxParameters](#linuxparameters): Input for InstallPatches on a Linux VM, as directly received by the API
* **maximumDuration**: string (Required): Specifies the maximum amount of time that the operation will run. It must be an ISO 8601-compliant duration string such as PT4H (4 hours)
* **rebootSetting**: 'Always' | 'IfRequired' | 'Never' | string (Required): Defines when it is acceptable to reboot a VM during a software update operation.
* **windowsParameters**: [WindowsParameters](#windowsparameters): Input for InstallPatches on a Windows VM, as directly received by the API

## MachineInstallPatchesResult
### Properties
* **errorDetails**: [ErrorDetail](#errordetail) (ReadOnly): The errors that were encountered during execution of the operation. The details array contains the list of them.
* **excludedPatchCount**: int (ReadOnly): The number of patches that were not installed due to the user blocking their installation.
* **failedPatchCount**: int (ReadOnly): The number of patches that could not be installed due to some issue. See errors for details.
* **installationActivityId**: string (ReadOnly): The activity ID of the operation that produced this result.
* **installedPatchCount**: int (ReadOnly): The number of patches successfully installed.
* **lastModifiedDateTime**: string (ReadOnly): The UTC timestamp when the operation finished.
* **maintenanceWindowExceeded**: bool (ReadOnly): Whether the operation ran out of time before it completed all its intended actions.
* **notSelectedPatchCount**: int (ReadOnly): The number of patches that were detected as available for install, but did not meet the operation's criteria.
* **osType**: 'Linux' | 'Windows' | string (ReadOnly): The operating system type of the machine.
* **patchServiceUsed**: 'APT' | 'Unknown' | 'WU' | 'WU_WSUS' | 'YUM' | 'Zypper' | string (ReadOnly): Specifies the patch service used for the operation.
* **pendingPatchCount**: int (ReadOnly): The number of patches that were identified as meeting the installation criteria, but were not able to be installed. Typically this happens when maintenanceWindowExceeded == true.
* **rebootStatus**: 'Completed' | 'Failed' | 'NotNeeded' | 'Required' | 'Started' | 'Unknown' | string (ReadOnly): The reboot state of the VM following completion of the operation.
* **startDateTime**: string (ReadOnly): The UTC timestamp when the operation began.
* **startedBy**: 'Platform' | 'User' | string (ReadOnly): Indicates if operation was triggered by user or by platform.
* **status**: 'CompletedWithWarnings' | 'Failed' | 'InProgress' | 'Succeeded' | 'Unknown' | string (ReadOnly): The overall success or failure status of the operation. It remains "InProgress" until the operation completes. At that point it will become "Failed", "Succeeded", "Unknown" or "CompletedWithWarnings."

## MachineProperties
### Properties
* **adFqdn**: string (ReadOnly): Specifies the AD fully qualified display name.
* **agentConfiguration**: [AgentConfiguration](#agentconfiguration) (ReadOnly): Configurable properties that the user can set locally via the azcmagent config command, or remotely via ARM.
* **agentUpgrade**: [AgentUpgrade](#agentupgrade): The info of the machine w.r.t Agent Upgrade
* **agentVersion**: string (ReadOnly): The hybrid machine agent full version.
* **clientPublicKey**: string: Public Key that the client provides to be used during initial resource onboarding
* **cloudMetadata**: [CloudMetadata](#cloudmetadata): The metadata of the cloud environment (Azure/GCP/AWS/OCI...).
* **detectedProperties**: [DetectedProperties](#detectedproperties) (ReadOnly): Detected properties from the machine.
* **displayName**: string (ReadOnly): Specifies the hybrid machine display name.
* **dnsFqdn**: string (ReadOnly): Specifies the DNS fully qualified display name.
* **domainName**: string (ReadOnly): Specifies the Windows domain name.
* **errorDetails**: [ErrorDetail](#errordetail)[] (ReadOnly): Details about the error state.
* **extensions**: [MachineExtensionInstanceView](#machineextensioninstanceview)[]: Machine Extensions information (deprecated field)
* **lastStatusChange**: string (ReadOnly): The time of the last status change.
* **locationData**: [LocationData](#locationdata): Metadata pertaining to the geographic location of the resource.
* **machineFqdn**: string (ReadOnly): Specifies the hybrid machine FQDN.
* **mssqlDiscovered**: string: Specifies whether any MS SQL instance is discovered on the machine.
* **osName**: string (ReadOnly): The Operating System running on the hybrid machine.
* **osProfile**: [OSProfile](#osprofile): Specifies the operating system settings for the hybrid machine.
* **osSku**: string (ReadOnly): Specifies the Operating System product SKU.
* **osType**: string: The type of Operating System (windows/linux).
* **osVersion**: string (ReadOnly): The version of Operating System running on the hybrid machine.
* **parentClusterResourceId**: string: The resource id of the parent cluster (Azure HCI) this machine is assigned to, if any.
* **privateLinkScopeResourceId**: string: The resource id of the private link scope this machine is assigned to, if any.
* **provisioningState**: string (ReadOnly): The provisioning state, which only appears in the response.
* **serviceStatuses**: [ServiceStatuses](#servicestatuses): Statuses of dependent services that are reported back to ARM.
* **status**: 'Connected' | 'Disconnected' | 'Error' | string (ReadOnly): The status of the hybrid machine agent.
* **vmId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"}: Specifies the hybrid machine unique ID.
* **vmUuid**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): Specifies the Arc Machine's unique SMBIOS ID

## OSProfile
### Properties
* **computerName**: string (ReadOnly): Specifies the host OS name of the hybrid machine.
* **linuxConfiguration**: [OSProfileLinuxConfiguration](#osprofilelinuxconfiguration): Specifies the linux configuration for update management.
* **windowsConfiguration**: [OSProfileWindowsConfiguration](#osprofilewindowsconfiguration): Specifies the windows configuration for update management.

## OSProfileLinuxConfiguration
### Properties
* **patchSettings**: [PatchSettings](#patchsettings): Specifies the patch settings.

## OSProfileWindowsConfiguration
### Properties
* **patchSettings**: [PatchSettings](#patchsettings): Specifies the patch settings.

## PatchSettings
### Properties
* **assessmentMode**: 'AutomaticByPlatform' | 'ImageDefault' | string: Specifies the assessment mode.
* **patchMode**: 'AutomaticByOS' | 'AutomaticByPlatform' | 'ImageDefault' | 'Manual' | string: Specifies the patch mode.

## PrivateEndpointConnectionDataModel
### Properties
* **id**: string (ReadOnly): The ARM Resource Id of the Private Endpoint.
* **name**: string (ReadOnly): The Name of the Private Endpoint.
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): The Private Endpoint Connection properties.
* **type**: string (ReadOnly): Azure resource type

## PrivateEndpointConnectionProperties
### Properties
* **groupIds**: string[] (ReadOnly): List of group IDs.
* **privateEndpoint**: [PrivateEndpointProperty](#privateendpointproperty): Private endpoint which the connection belongs to.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionStateProperty](#privatelinkserviceconnectionstateproperty): Connection state of the private endpoint connection.
* **provisioningState**: string (ReadOnly): State of the private endpoint connection.

## PrivateEndpointProperty
### Properties
* **id**: string: Resource id of the private endpoint.

## PrivateLinkResourceProperties
### Properties
* **groupId**: string (ReadOnly): The private link resource group id.
* **requiredMembers**: string[] (ReadOnly): The private link resource required member names.
* **requiredZoneNames**: string[] (ReadOnly): Required DNS zone names of the the private link resource.

## PrivateLinkScopesResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## PrivateLinkServiceConnectionStateProperty
### Properties
* **actionsRequired**: string (ReadOnly): The actions required for private link service connection.
* **description**: string (Required): The private link service connection description.
* **status**: string (Required): The private link service connection status.

## ServiceStatus
### Properties
* **startupType**: string: The behavior of the service when the Arc-enabled machine starts up.
* **status**: string: The current status of the service.

## ServiceStatuses
### Properties
* **extensionService**: [ServiceStatus](#servicestatus): The state of the extension service on the Arc-enabled machine.
* **guestConfigurationService**: [ServiceStatus](#servicestatus): The state of the guest configuration service on the Arc-enabled machine.

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

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WindowsParameters
### Properties
* **classificationsToInclude**: ('Critical' | 'Definition' | 'FeaturePack' | 'Security' | 'ServicePack' | 'Tools' | 'UpdateRollUp' | 'Updates' | string)[]: The update classifications to select when installing patches for Windows.
* **excludeKbsRequiringReboot**: bool: Filters out Kbs that don't have an InstallationRebootBehavior of 'NeverReboots' when this is set to true.
* **kbNumbersToExclude**: string[]: Kbs to exclude in the patch operation
* **kbNumbersToInclude**: string[]: Kbs to include in the patch operation
* **maxPatchPublishDate**: string: This is used to install patches that were published on or before this given max published date.

