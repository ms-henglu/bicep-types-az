# Microsoft.AgFoodPlatform @ 2020-05-12-preview

## Resource Microsoft.AgFoodPlatform/farmBeats@2020-05-12-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-05-12-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [FarmBeatsProperties](#farmbeatsproperties): FarmBeats ARM Resource properties.
* **sku**: [Sku](#sku): The resource model definition representing SKU
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.AgFoodPlatform/farmBeats' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AgFoodPlatform/farmBeats/extensions@2020-05-12-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-05-12-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string (ReadOnly): The ETag value to implement optimistic concurrency.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ExtensionProperties](#extensionproperties) (ReadOnly): Extension resource properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AgFoodPlatform/farmBeats/extensions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AgFoodPlatform/farmBeatsExtensionDefinitions@2020-05-12-preview (ReadOnly)
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-12-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {pattern: "^[a-zA-Z]{3,50}[.][a-zA-Z]{3,100}$"} (Required, DeployTimeConstant): The resource name
* **properties**: [FarmBeatsExtensionProperties](#farmbeatsextensionproperties) (ReadOnly): FarmBeatsExtension properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AgFoodPlatform/farmBeatsExtensionDefinitions' (ReadOnly, DeployTimeConstant): The resource type

## DetailedInformation
### Properties
* **apiInputParameters**: string[]: List of apiInputParameters.
* **apiName**: string: ApiName available for the farmBeatsExtension.
* **customParameters**: string[]: List of customParameters.
* **platformParameters**: string[]: List of platformParameters.
* **unitsSupported**: [UnitSystemsInfo](#unitsystemsinfo): Unit systems info for the data provider.

## ExtensionProperties
### Properties
* **extensionApiDocsLink**: string (ReadOnly): Extension api docs link.
* **extensionAuthLink**: string (ReadOnly): Extension auth link.
* **extensionCategory**: string (ReadOnly): Extension category. e.g. weather/sensor/satellite.
* **extensionId**: string {pattern: "^[a-zA-Z]{3,50}[.][a-zA-Z]{3,100}$"} (ReadOnly): Extension Id.
* **installedExtensionVersion**: string {pattern: "^([1-9]|10).\d$"} (ReadOnly): Installed extension version.

## FarmBeatsExtensionProperties
### Properties
* **description**: string {minLength: 2, maxLength: 500} (ReadOnly): Textual description.
* **detailedInformation**: [DetailedInformation](#detailedinformation)[] (ReadOnly): Detailed information which shows summary of requested data.
Used in descriptive get extension metadata call.
Information for weather category per api included are apisSupported,
customParameters, PlatformParameters and Units supported.
* **extensionApiDocsLink**: string (ReadOnly): FarmBeatsExtension api docs link.
* **extensionAuthLink**: string (ReadOnly): FarmBeatsExtension auth link.
* **extensionCategory**: string {minLength: 2, maxLength: 100} (ReadOnly): Category of the extension. e.g. weather/sensor/satellite.
* **farmBeatsExtensionId**: string {minLength: 2, maxLength: 100, pattern: "^[a-zA-Z]{3,50}[.][a-zA-Z]{3,100}$"} (ReadOnly): FarmBeatsExtension ID.
* **farmBeatsExtensionName**: string {minLength: 2, maxLength: 100} (ReadOnly): FarmBeatsExtension name.
* **farmBeatsExtensionVersion**: string {minLength: 2, maxLength: 100, pattern: "^([1-9]|10).\d$"} (ReadOnly): FarmBeatsExtension version.
* **publisherId**: string {minLength: 2, maxLength: 100} (ReadOnly): Publisher ID.
* **targetResourceType**: string (ReadOnly): Target ResourceType of the farmBeatsExtension.

## FarmBeatsProperties
### Properties
* **instanceUri**: string (ReadOnly): Uri of the FarmBeats instance.
* **provisioningState**: 'Failed' | 'Succeeded' | string (ReadOnly): FarmBeats instance provisioning state.

## Sku
### Properties
* **capacity**: int: If the SKU supports scale out/in then the capacity integer should be included. If scale out/in is not possible for the resource this may be omitted.
* **family**: string: If the service has different generations of hardware, for the same SKU, then that can be captured here.
* **name**: string (Required): The name of the SKU. Ex - P3. It is typically a letter+number code
* **size**: string: The SKU size. When the name field is the combination of tier and some other value, this would be the standalone code.
* **tier**: 'Basic' | 'Free' | 'Premium' | 'Standard': This field is required to be implemented by the Resource Provider if the service has more than one tier, but is not required on a PUT.

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

## UnitSystemsInfo
### Properties
* **key**: string {minLength: 2, maxLength: 100} (Required): UnitSystem key sent as part of ProviderInput.
* **values**: string[] (Required): List of unit systems supported by this data provider.

