# Microsoft.MixedReality @ 2019-02-28-preview

## Resource Microsoft.MixedReality/spatialAnchorsAccounts@2019-02-28-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2019-02-28-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): The identity associated with this account
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {minLength: 1, maxLength: 90, pattern: "^[-\w\._\(\)]+$"} (Required, DeployTimeConstant): The resource name
* **properties**: [SpatialAnchorsAccountProperties](#spatialanchorsaccountproperties): Property bag.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.MixedReality/spatialAnchorsAccounts' (ReadOnly, DeployTimeConstant): The resource type

## Function checkNameAvailability (Microsoft.MixedReality/locations@2019-02-28-preview)
* **Resource**: Microsoft.MixedReality/locations
* **ApiVersion**: 2019-02-28-preview
* **Input**: [CheckNameAvailabilityRequest](#checknameavailabilityrequest)
* **Output**: [CheckNameAvailabilityResponse](#checknameavailabilityresponse)

## Function keys (Microsoft.MixedReality/spatialAnchorsAccounts@2019-02-28-preview)
* **Resource**: Microsoft.MixedReality/spatialAnchorsAccounts
* **ApiVersion**: 2019-02-28-preview
* **Input**: [SpatialAnchorsAccountKeyRegenerateRequest](#spatialanchorsaccountkeyregeneraterequest)
* **Output**: [SpatialAnchorsAccountKeys](#spatialanchorsaccountkeys)

## CheckNameAvailabilityRequest
### Properties
* **name**: string (Required): Resource Name To Verify
* **type**: string (Required): Fully qualified resource type which includes provider namespace

## CheckNameAvailabilityResponse
### Properties
* **message**: string: detail message
* **nameAvailable**: bool (Required): if name Available
* **reason**: 'AlreadyExists' | 'Invalid' | string: Resource Name To Verify

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned': The identity type.

## SpatialAnchorsAccountKeyRegenerateRequest
### Properties
* **serial**: int: serial of key to be regenerated

## SpatialAnchorsAccountKeys
### Properties
* **primaryKey**: string (ReadOnly): value of primary key.
* **secondaryKey**: string (ReadOnly): value of secondary key.

## SpatialAnchorsAccountProperties
### Properties
* **accountDomain**: string (ReadOnly): Correspond domain name of certain Spatial Anchors Account
* **accountId**: string (ReadOnly): unique id of certain Spatial Anchors Account data contract.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

