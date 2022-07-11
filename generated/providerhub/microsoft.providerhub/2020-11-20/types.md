# Microsoft.ProviderHub @ 2020-11-20

## Resource Microsoft.ProviderHub/providerRegistrations@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProviderRegistrationProperties](#providerregistrationproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/customRollouts@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CustomRolloutProperties](#customrolloutproperties) (Required): Properties of the rollout.
* **type**: 'Microsoft.ProviderHub/providerRegistrations/customRollouts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/defaultRollouts@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DefaultRolloutProperties](#defaultrolloutproperties): Properties of the rollout.
* **type**: 'Microsoft.ProviderHub/providerRegistrations/defaultRollouts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/notificationRegistrations@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [NotificationRegistrationProperties](#notificationregistrationproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/notificationRegistrations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/operations@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **contents**: [OperationsDefinition](#operationsdefinition)[] (Required, WriteOnly)
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.ProviderHub/providerRegistrations/operations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ResourceTypeRegistrationProperties](#resourcetyperegistrationproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SkuResourceProperties](#skuresourceproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SkuResourceProperties](#skuresourceproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SkuResourceProperties](#skuresourceproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/skus@2020-11-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SkuResourceProperties](#skuresourceproperties)
* **type**: 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/skus' (ReadOnly, DeployTimeConstant): The resource type

## Function checkinManifest (Microsoft.ProviderHub/providerRegistrations@2020-11-20)
* **Resource**: Microsoft.ProviderHub/providerRegistrations
* **ApiVersion**: 2020-11-20
* **Input**: [CheckinManifestParams](#checkinmanifestparams)
* **Output**: [CheckinManifestInfo](#checkinmanifestinfo)

## Function generateManifest (Microsoft.ProviderHub/providerRegistrations@2020-11-20)
* **Resource**: Microsoft.ProviderHub/providerRegistrations
* **ApiVersion**: 2020-11-20
* **Output**: [ResourceProviderManifest](#resourceprovidermanifest)

## Function generateOperations (Microsoft.ProviderHub/providerRegistrations@2020-11-20)
* **Resource**: Microsoft.ProviderHub/providerRegistrations
* **ApiVersion**: 2020-11-20
* **Output**: [OperationsDefinition](#operationsdefinition)[]

## Function stop (Microsoft.ProviderHub/providerRegistrations/defaultRollouts@2020-11-20)
* **Resource**: Microsoft.ProviderHub/providerRegistrations/defaultRollouts
* **ApiVersion**: 2020-11-20

## AuthorizationActionMapping
### Properties
* **desired**: string
* **original**: string

## CheckinManifestInfo
### Properties
* **commitId**: string
* **isCheckedIn**: bool (Required)
* **pullRequest**: string
* **statusMessage**: string (Required)

## CheckinManifestParams
### Properties
* **baselineArmManifestLocation**: string (Required): The baseline ARM manifest location supplied to the checkin manifest operation.
* **environment**: string (Required): The environment supplied to the checkin manifest operation.

## CustomRolloutProperties
### Properties
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string
* **specification**: [CustomRolloutPropertiesSpecification](#customrolloutpropertiesspecification) (Required)
* **status**: [CustomRolloutPropertiesStatus](#customrolloutpropertiesstatus)

## CustomRolloutPropertiesSpecification
### Properties
* **canary**: [CustomRolloutSpecificationCanary](#customrolloutspecificationcanary) (Required)
* **providerRegistration**: [CustomRolloutSpecificationProviderRegistration](#customrolloutspecificationproviderregistration)
* **resourceTypeRegistrations**: [ResourceTypeRegistration](#resourcetyperegistration)[]

## CustomRolloutPropertiesStatus
### Properties
* **completedRegions**: string[]
* **failedOrSkippedRegions**: [CustomRolloutStatusFailedOrSkippedRegions](#customrolloutstatusfailedorskippedregions): Dictionary of <ExtendedErrorInfo>

## CustomRolloutSpecificationCanary
### Properties
* **regions**: string[]

## CustomRolloutSpecificationProviderRegistration
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [ProviderRegistrationProperties](#providerregistrationproperties)
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## CustomRolloutStatusFailedOrSkippedRegions
### Properties
### Additional Properties
* **Additional Properties Type**: [ExtendedErrorInfo](#extendederrorinfo)

## DefaultRolloutProperties
### Properties
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string
* **specification**: [DefaultRolloutPropertiesSpecification](#defaultrolloutpropertiesspecification)
* **status**: [DefaultRolloutPropertiesStatus](#defaultrolloutpropertiesstatus)

## DefaultRolloutPropertiesSpecification
### Properties
* **canary**: [DefaultRolloutSpecificationCanary](#defaultrolloutspecificationcanary)
* **highTraffic**: [DefaultRolloutSpecificationHighTraffic](#defaultrolloutspecificationhightraffic)
* **lowTraffic**: [DefaultRolloutSpecificationLowTraffic](#defaultrolloutspecificationlowtraffic)
* **mediumTraffic**: [DefaultRolloutSpecificationMediumTraffic](#defaultrolloutspecificationmediumtraffic)
* **providerRegistration**: [DefaultRolloutSpecificationProviderRegistration](#defaultrolloutspecificationproviderregistration)
* **resourceTypeRegistrations**: [ResourceTypeRegistration](#resourcetyperegistration)[]
* **restOfTheWorldGroupOne**: [DefaultRolloutSpecificationRestOfTheWorldGroupOne](#defaultrolloutspecificationrestoftheworldgroupone)
* **restOfTheWorldGroupTwo**: [DefaultRolloutSpecificationRestOfTheWorldGroupTwo](#defaultrolloutspecificationrestoftheworldgrouptwo)

## DefaultRolloutPropertiesStatus
### Properties
* **completedRegions**: string[]
* **failedOrSkippedRegions**: [RolloutStatusBaseFailedOrSkippedRegions](#rolloutstatusbasefailedorskippedregions): Dictionary of <ExtendedErrorInfo>
* **nextTrafficRegion**: 'Canary' | 'HighTraffic' | 'LowTraffic' | 'MediumTraffic' | 'None' | 'NotSpecified' | 'RestOfTheWorldGroupOne' | 'RestOfTheWorldGroupTwo' | string
* **nextTrafficRegionScheduledTime**: string
* **subscriptionReregistrationResult**: 'ConditionalUpdate' | 'Failed' | 'ForcedUpdate' | 'NotApplicable' | string

## DefaultRolloutSpecificationCanary
### Properties
* **regions**: string[]
* **skipRegions**: string[]

## DefaultRolloutSpecificationHighTraffic
### Properties
* **regions**: string[]
* **waitDuration**: string

## DefaultRolloutSpecificationLowTraffic
### Properties
* **regions**: string[]
* **waitDuration**: string

## DefaultRolloutSpecificationMediumTraffic
### Properties
* **regions**: string[]
* **waitDuration**: string

## DefaultRolloutSpecificationProviderRegistration
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [ProviderRegistrationProperties](#providerregistrationproperties)
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## DefaultRolloutSpecificationRestOfTheWorldGroupOne
### Properties
* **regions**: string[]
* **waitDuration**: string

## DefaultRolloutSpecificationRestOfTheWorldGroupTwo
### Properties
* **regions**: string[]
* **waitDuration**: string

## ExtendedErrorInfo
### Properties
* **additionalInfo**: [TypedErrorInfo](#typederrorinfo)[]
* **code**: string
* **details**: [ExtendedErrorInfo](#extendederrorinfo)[]
* **message**: string
* **target**: string

## ExtendedLocationOptions
### Properties
* **supportedPolicy**: string
* **type**: string

## LightHouseAuthorization
### Properties
* **principalId**: string (Required)
* **roleDefinitionId**: string (Required)

## LinkedAccessCheck
### Properties
* **actionName**: string
* **linkedAction**: string
* **linkedActionVerb**: string
* **linkedProperty**: string
* **linkedType**: string

## LinkedOperationRule
### Properties
* **linkedAction**: 'Blocked' | 'Enabled' | 'NotSpecified' | 'Validate' | string (Required)
* **linkedOperation**: 'CrossResourceGroupResourceMove' | 'CrossSubscriptionResourceMove' | 'None' | string (Required)

## LoggingRule
### Properties
* **action**: string (Required)
* **detailLevel**: 'Body' | 'None' | string (Required)
* **direction**: 'None' | 'Request' | 'Response' | string (Required)
* **hiddenPropertyPaths**: [LoggingRuleHiddenPropertyPaths](#loggingrulehiddenpropertypaths)

## LoggingRuleHiddenPropertyPaths
### Properties
* **hiddenPathsOnRequest**: string[]
* **hiddenPathsOnResponse**: string[]

## NotificationEndpoint
### Properties
* **locations**: string[]
* **notificationDestination**: string

## NotificationRegistrationProperties
### Properties
* **includedEvents**: string[]
* **messageScope**: 'NotSpecified' | 'RegisteredSubscriptions' | string
* **notificationEndpoints**: [NotificationEndpoint](#notificationendpoint)[]
* **notificationMode**: 'EventHub' | 'NotSpecified' | 'WebHook' | string
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string

## OperationsDefinition
### Properties
* **actionType**: 'Internal' | 'NotSpecified'
* **display**: [OperationsDefinitionDisplay](#operationsdefinitiondisplay) (Required): Display information of the operation.
* **isDataAction**: bool: Indicates whether the operation applies to data-plane.
* **name**: string (Required): Name of the operation.
* **origin**: 'NotSpecified' | 'System' | 'User'
* **properties**: any: Anything

## OperationsDefinitionDisplay
### Properties
* **description**: string (Required)
* **operation**: string (Required)
* **provider**: string (Required)
* **resource**: string (Required)

## ProviderHubMetadataProviderAuthentication
### Properties
* **allowedAudiences**: string[] (Required)

## ProviderHubMetadataThirdPartyProviderAuthorization
### Properties
* **authorizations**: [LightHouseAuthorization](#lighthouseauthorization)[]
* **managedByTenantId**: string

## ProviderRegistrationProperties
### Properties
* **capabilities**: [ResourceProviderCapabilities](#resourceprovidercapabilities)[]
* **featuresRule**: [ResourceProviderManifestPropertiesFeaturesRule](#resourceprovidermanifestpropertiesfeaturesrule)
* **management**: [ResourceProviderManifestPropertiesManagement](#resourceprovidermanifestpropertiesmanagement)
* **metadata**: any: Anything
* **namespace**: string
* **providerAuthentication**: [ResourceProviderManifestPropertiesProviderAuthentication](#resourceprovidermanifestpropertiesproviderauthentication)
* **providerAuthorizations**: [ResourceProviderAuthorization](#resourceproviderauthorization)[]
* **providerHubMetadata**: [ProviderRegistrationPropertiesProviderHubMetadata](#providerregistrationpropertiesproviderhubmetadata)
* **providerType**: 'AuthorizationFree' | 'External' | 'Hidden' | 'Internal' | 'LegacyRegistrationRequired' | 'NotSpecified' | 'RegistrationFree' | 'TenantOnly' | string
* **providerVersion**: string
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string
* **requestHeaderOptions**: [ResourceProviderManifestPropertiesRequestHeaderOptions](#resourceprovidermanifestpropertiesrequestheaderoptions)
* **requiredFeatures**: string[]
* **subscriptionLifecycleNotificationSpecifications**: [ProviderRegistrationPropertiesSubscriptionLifecycleNotificationSpecifications](#providerregistrationpropertiessubscriptionlifecyclenotificationspecifications)
* **templateDeploymentOptions**: [ResourceProviderManifestPropertiesTemplateDeploymentOptions](#resourceprovidermanifestpropertiestemplatedeploymentoptions)

## ProviderRegistrationPropertiesProviderHubMetadata
### Properties
* **providerAuthentication**: [ProviderHubMetadataProviderAuthentication](#providerhubmetadataproviderauthentication)
* **providerAuthorizations**: [ResourceProviderAuthorization](#resourceproviderauthorization)[]
* **thirdPartyProviderAuthorization**: [ProviderHubMetadataThirdPartyProviderAuthorization](#providerhubmetadatathirdpartyproviderauthorization)

## ProviderRegistrationPropertiesSubscriptionLifecycleNotificationSpecifications
### Properties
* **softDeleteTTL**: string
* **subscriptionStateOverrideActions**: [SubscriptionStateOverrideAction](#subscriptionstateoverrideaction)[]

## ResourceProviderAuthorization
### Properties
* **applicationId**: string
* **managedByRoleDefinitionId**: string
* **roleDefinitionId**: string

## ResourceProviderCapabilities
### Properties
* **effect**: 'Allow' | 'Disallow' | 'NotSpecified' | string (Required)
* **quotaId**: string (Required)
* **requiredFeatures**: string[]

## ResourceProviderEndpoint
### Properties
* **apiVersions**: string[]
* **enabled**: bool
* **endpointUri**: string
* **featuresRule**: [ResourceProviderEndpointFeaturesRule](#resourceproviderendpointfeaturesrule)
* **locations**: string[]
* **requiredFeatures**: string[]
* **timeout**: string

## ResourceProviderEndpointFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceProviderManifest
### Properties
* **capabilities**: [ResourceProviderCapabilities](#resourceprovidercapabilities)[]
* **featuresRule**: [ResourceProviderManifestFeaturesRule](#resourceprovidermanifestfeaturesrule)
* **globalNotificationEndpoints**: [ResourceProviderEndpoint](#resourceproviderendpoint)[]
* **management**: [ResourceProviderManifestManagement](#resourceprovidermanifestmanagement)
* **metadata**: any: Anything
* **namespace**: string
* **providerAuthentication**: [ResourceProviderManifestProviderAuthentication](#resourceprovidermanifestproviderauthentication)
* **providerAuthorizations**: [ResourceProviderAuthorization](#resourceproviderauthorization)[]
* **providerType**: 'AuthorizationFree' | 'External' | 'Hidden' | 'Internal' | 'LegacyRegistrationRequired' | 'NotSpecified' | 'RegistrationFree' | 'TenantOnly' | string
* **providerVersion**: string
* **requestHeaderOptions**: [ResourceProviderManifestRequestHeaderOptions](#resourceprovidermanifestrequestheaderoptions)
* **requiredFeatures**: string[]
* **reRegisterSubscriptionMetadata**: [ResourceProviderManifestReRegisterSubscriptionMetadata](#resourceprovidermanifestreregistersubscriptionmetadata)
* **resourceTypes**: [ResourceType](#resourcetype)[]

## ResourceProviderManifestFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceProviderManifestManagement
### Properties
* **incidentContactEmail**: string
* **incidentRoutingService**: string
* **incidentRoutingTeam**: string
* **manifestOwners**: string[]
* **resourceAccessPolicy**: 'AcisActionAllowed' | 'AcisReadAllowed' | 'NotSpecified'
* **resourceAccessRoles**: any[]
* **schemaOwners**: string[]
* **serviceTreeInfos**: [ServiceTreeInfo](#servicetreeinfo)[]

## ResourceProviderManifestPropertiesFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceProviderManifestPropertiesManagement
### Properties
* **incidentContactEmail**: string
* **incidentRoutingService**: string
* **incidentRoutingTeam**: string
* **manifestOwners**: string[]
* **resourceAccessPolicy**: 'AcisActionAllowed' | 'AcisReadAllowed' | 'NotSpecified'
* **resourceAccessRoles**: any[]
* **schemaOwners**: string[]
* **serviceTreeInfos**: [ServiceTreeInfo](#servicetreeinfo)[]

## ResourceProviderManifestPropertiesProviderAuthentication
### Properties
* **allowedAudiences**: string[] (Required)

## ResourceProviderManifestPropertiesRequestHeaderOptions
### Properties
* **optInHeaders**: 'ClientGroupMembership' | 'NotSpecified' | 'SignedAuxiliaryTokens' | 'SignedUserToken' | 'UnboundedClientGroupMembership' | string

## ResourceProviderManifestPropertiesTemplateDeploymentOptions
### Properties
* **preflightOptions**: 'ContinueDeploymentOnFailure' | 'DefaultValidationOnly' | 'None' | string[]
* **preflightSupported**: bool

## ResourceProviderManifestProviderAuthentication
### Properties
* **allowedAudiences**: string[] (Required)

## ResourceProviderManifestRequestHeaderOptions
### Properties
* **optInHeaders**: 'ClientGroupMembership' | 'NotSpecified' | 'SignedAuxiliaryTokens' | 'SignedUserToken' | 'UnboundedClientGroupMembership' | string

## ResourceProviderManifestReRegisterSubscriptionMetadata
### Properties
* **concurrencyLimit**: int
* **enabled**: bool (Required)

## ResourceType
### Properties
* **allowedUnauthorizedActions**: string[]
* **authorizationActionMappings**: [AuthorizationActionMapping](#authorizationactionmapping)[]
* **defaultApiVersion**: string
* **disallowedActionVerbs**: string[]
* **endpoints**: [ResourceProviderEndpoint](#resourceproviderendpoint)[]
* **extendedLocations**: [ExtendedLocationOptions](#extendedlocationoptions)[]
* **featuresRule**: [ResourceTypeFeaturesRule](#resourcetypefeaturesrule)
* **identityManagement**: [ResourceTypeIdentityManagement](#resourcetypeidentitymanagement)
* **linkedAccessChecks**: [LinkedAccessCheck](#linkedaccesscheck)[]
* **linkedOperationRules**: [LinkedOperationRule](#linkedoperationrule)[]
* **loggingRules**: [LoggingRule](#loggingrule)[]
* **marketplaceType**: 'AddOn' | 'Bypass' | 'NotSpecified' | 'Store'
* **metadata**: any: Anything
* **name**: string
* **requestHeaderOptions**: [ResourceTypeRequestHeaderOptions](#resourcetyperequestheaderoptions)
* **requiredFeatures**: string[]
* **resourceDeletionPolicy**: 'Cascade' | 'Force' | 'NotSpecified' | string
* **resourceValidation**: 'NotSpecified' | 'ProfaneWords' | 'ReservedWords' | string
* **routingType**: 'CascadeExtension' | 'Default' | 'Extension' | 'Failover' | 'Fanout' | 'HostBased' | 'LocationBased' | 'ProxyOnly' | 'Tenant' | string
* **serviceTreeInfos**: [ServiceTreeInfo](#servicetreeinfo)[]
* **skuLink**: string
* **subscriptionStateRules**: [SubscriptionStateRule](#subscriptionstaterule)[]
* **templateDeploymentPolicy**: [ResourceTypeTemplateDeploymentPolicy](#resourcetypetemplatedeploymentpolicy)
* **throttlingRules**: [ThrottlingRule](#throttlingrule)[]

## ResourceTypeEndpoint
### Properties
* **apiVersions**: string[]
* **enabled**: bool
* **extensions**: [ResourceTypeExtension](#resourcetypeextension)[]
* **featuresRule**: [ResourceTypeEndpointFeaturesRule](#resourcetypeendpointfeaturesrule)
* **locations**: string[]
* **requiredFeatures**: string[]
* **timeout**: string

## ResourceTypeEndpointFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceTypeExtension
### Properties
* **endpointUri**: string
* **extensionCategories**: 'NotSpecified' | 'ResourceCreationBegin' | 'ResourceCreationCompleted' | 'ResourceCreationValidate' | 'ResourceDeletionBegin' | 'ResourceDeletionCompleted' | 'ResourceDeletionValidate' | 'ResourceMoveBegin' | 'ResourceMoveCompleted' | 'ResourcePatchBegin' | 'ResourcePatchCompleted' | 'ResourcePatchValidate' | 'ResourcePostAction' | 'ResourceReadBegin' | 'ResourceReadValidate' | 'SubscriptionLifecycleNotification' | string[]
* **timeout**: string

## ResourceTypeExtensionOptionsResourceCreationBegin
### Properties
* **request**: 'DoNotMergeExistingReadOnlyAndSecretProperties' | 'IncludeInternalMetadata' | 'NotSpecified' | string[]
* **response**: 'DoNotMergeExistingReadOnlyAndSecretProperties' | 'IncludeInternalMetadata' | 'NotSpecified' | string[]

## ResourceTypeFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceTypeIdentityManagement
### Properties
* **type**: 'Actor' | 'DelegatedResourceIdentity' | 'NotSpecified' | 'SystemAssigned' | 'UserAssigned' | string

## ResourceTypeRegistration
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [ResourceTypeRegistrationProperties](#resourcetyperegistrationproperties)
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## ResourceTypeRegistrationProperties
### Properties
* **allowedUnauthorizedActions**: string[]
* **authorizationActionMappings**: [AuthorizationActionMapping](#authorizationactionmapping)[]
* **checkNameAvailabilitySpecifications**: [ResourceTypeRegistrationPropertiesCheckNameAvailabilitySpecifications](#resourcetyperegistrationpropertieschecknameavailabilityspecifications)
* **defaultApiVersion**: string
* **disallowedActionVerbs**: string[]
* **enableAsyncOperation**: bool
* **enableThirdPartyS2S**: bool
* **endpoints**: [ResourceTypeEndpoint](#resourcetypeendpoint)[]
* **extendedLocations**: [ExtendedLocationOptions](#extendedlocationoptions)[]
* **extensionOptions**: [ResourceTypeRegistrationPropertiesExtensionOptions](#resourcetyperegistrationpropertiesextensionoptions)
* **featuresRule**: [ResourceTypeRegistrationPropertiesFeaturesRule](#resourcetyperegistrationpropertiesfeaturesrule)
* **identityManagement**: [ResourceTypeRegistrationPropertiesIdentityManagement](#resourcetyperegistrationpropertiesidentitymanagement)
* **isPureProxy**: bool
* **linkedAccessChecks**: [LinkedAccessCheck](#linkedaccesscheck)[]
* **loggingRules**: [LoggingRule](#loggingrule)[]
* **marketplaceType**: 'AddOn' | 'Bypass' | 'NotSpecified' | 'Store'
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string
* **regionality**: 'Global' | 'NotSpecified' | 'Regional' | string
* **requestHeaderOptions**: [ResourceTypeRegistrationPropertiesRequestHeaderOptions](#resourcetyperegistrationpropertiesrequestheaderoptions)
* **requiredFeatures**: string[]
* **resourceDeletionPolicy**: 'CascadeDeleteAll' | 'CascadeDeleteProxyOnlyChildren' | 'NotSpecified' | string
* **resourceMovePolicy**: [ResourceTypeRegistrationPropertiesResourceMovePolicy](#resourcetyperegistrationpropertiesresourcemovepolicy)
* **routingType**: 'CascadeExtension' | 'Default' | 'Extension' | 'Failover' | 'Fanout' | 'HostBased' | 'LocationBased' | 'ProxyOnly' | 'Tenant' | string
* **serviceTreeInfos**: [ServiceTreeInfo](#servicetreeinfo)[]
* **subscriptionLifecycleNotificationSpecifications**: [ResourceTypeRegistrationPropertiesSubscriptionLifecycleNotificationSpecifications](#resourcetyperegistrationpropertiessubscriptionlifecyclenotificationspecifications)
* **subscriptionStateRules**: [SubscriptionStateRule](#subscriptionstaterule)[]
* **swaggerSpecifications**: [SwaggerSpecification](#swaggerspecification)[]
* **templateDeploymentOptions**: [ResourceTypeRegistrationPropertiesTemplateDeploymentOptions](#resourcetyperegistrationpropertiestemplatedeploymentoptions)
* **throttlingRules**: [ThrottlingRule](#throttlingrule)[]

## ResourceTypeRegistrationPropertiesCheckNameAvailabilitySpecifications
### Properties
* **enableDefaultValidation**: bool
* **resourceTypesWithCustomValidation**: string[]

## ResourceTypeRegistrationPropertiesExtensionOptions
### Properties
* **resourceCreationBegin**: [ResourceTypeExtensionOptionsResourceCreationBegin](#resourcetypeextensionoptionsresourcecreationbegin)

## ResourceTypeRegistrationPropertiesFeaturesRule
### Properties
* **requiredFeaturesPolicy**: 'All' | 'Any' | string (Required)

## ResourceTypeRegistrationPropertiesIdentityManagement
### Properties
* **applicationId**: string
* **type**: 'Actor' | 'DelegatedResourceIdentity' | 'NotSpecified' | 'SystemAssigned' | 'UserAssigned' | string

## ResourceTypeRegistrationPropertiesRequestHeaderOptions
### Properties
* **optInHeaders**: 'ClientGroupMembership' | 'NotSpecified' | 'SignedAuxiliaryTokens' | 'SignedUserToken' | 'UnboundedClientGroupMembership' | string

## ResourceTypeRegistrationPropertiesResourceMovePolicy
### Properties
* **crossResourceGroupMoveEnabled**: bool
* **crossSubscriptionMoveEnabled**: bool
* **validationRequired**: bool

## ResourceTypeRegistrationPropertiesSubscriptionLifecycleNotificationSpecifications
### Properties
* **softDeleteTTL**: string
* **subscriptionStateOverrideActions**: [SubscriptionStateOverrideAction](#subscriptionstateoverrideaction)[]

## ResourceTypeRegistrationPropertiesTemplateDeploymentOptions
### Properties
* **preflightOptions**: 'ContinueDeploymentOnFailure' | 'DefaultValidationOnly' | 'None' | string[]
* **preflightSupported**: bool

## ResourceTypeRequestHeaderOptions
### Properties
* **optInHeaders**: 'ClientGroupMembership' | 'NotSpecified' | 'SignedAuxiliaryTokens' | 'SignedUserToken' | 'UnboundedClientGroupMembership' | string

## ResourceTypeTemplateDeploymentPolicy
### Properties
* **capabilities**: 'Default' | 'Preflight' | string (Required)
* **preflightOptions**: 'DeploymentRequests' | 'None' | 'RegisteredOnly' | 'TestOnly' | 'ValidationRequests' | string (Required)

## RolloutStatusBaseFailedOrSkippedRegions
### Properties
### Additional Properties
* **Additional Properties Type**: [ExtendedErrorInfo](#extendederrorinfo)

## ServiceTreeInfo
### Properties
* **componentId**: string
* **serviceId**: string

## SkuCapability
### Properties
* **name**: string (Required)
* **value**: string (Required)

## SkuCost
### Properties
* **extendedUnit**: string
* **meterId**: string (Required)
* **quantity**: int

## SkuLocationInfo
### Properties
* **extendedLocations**: string[]
* **location**: string (Required)
* **type**: 'ArcZone' | 'EdgeZone' | 'NotSpecified'
* **zoneDetails**: [SkuZoneDetail](#skuzonedetail)[]
* **zones**: string[]

## SkuResourceProperties
### Properties
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MovingResources' | 'NotSpecified' | 'RolloutInProgress' | 'Running' | 'Succeeded' | 'TransientFailure' | string
* **skuSettings**: [SkuSetting](#skusetting)[] (Required)

## SkuSetting
### Properties
* **capabilities**: [SkuCapability](#skucapability)[]
* **capacity**: [SkuSettingCapacity](#skusettingcapacity)
* **costs**: [SkuCost](#skucost)[]
* **family**: string
* **kind**: string
* **locationInfo**: [SkuLocationInfo](#skulocationinfo)[]
* **locations**: string[]
* **name**: string (Required)
* **requiredFeatures**: string[]
* **requiredQuotaIds**: string[]
* **size**: string
* **tier**: string

## SkuSettingCapacity
### Properties
* **default**: int
* **maximum**: int
* **minimum**: int (Required)
* **scaleType**: 'Automatic' | 'Manual' | 'None' | string

## SkuZoneDetail
### Properties
* **capabilities**: [SkuCapability](#skucapability)[]
* **name**: string[]

## SubscriptionStateOverrideAction
### Properties
* **action**: 'BillingCancellation' | 'DeleteAllResources' | 'NoOp' | 'NotDefined' | 'SoftDeleteAllResources' | 'UndoSoftDelete' | string (Required)
* **state**: 'Deleted' | 'Registered' | 'Suspended' | 'SuspendedToDeleted' | 'SuspendedToRegistered' | 'SuspendedToUnregistered' | 'SuspendedToWarned' | 'Unregistered' | 'Warned' | 'WarnedToDeleted' | 'WarnedToRegistered' | 'WarnedToSuspended' | 'WarnedToUnregistered' | string (Required)

## SubscriptionStateRule
### Properties
* **allowedActions**: string[]
* **state**: 'Deleted' | 'Disabled' | 'Enabled' | 'NotDefined' | 'PastDue' | 'Warned' | string

## SwaggerSpecification
### Properties
* **apiVersions**: string[]
* **swaggerSpecFolderUri**: string

## ThrottlingMetric
### Properties
* **interval**: string
* **limit**: int (Required)
* **type**: 'NotSpecified' | 'NumberOfRequests' | 'NumberOfResources' | string (Required)

## ThrottlingRule
### Properties
* **action**: string (Required)
* **metrics**: [ThrottlingMetric](#throttlingmetric)[] (Required)
* **requiredFeatures**: string[]

## TypedErrorInfo
### Properties
* **info**: any (ReadOnly): Any object
* **type**: string (Required)

