# Microsoft.ManagedIdentity @ 2021-09-30-preview

## Resource Microsoft.ManagedIdentity/identities@2021-09-30-preview (ReadOnly)
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2021-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): The geo-location where the resource lives
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [SystemAssignedIdentityProperties](#systemassignedidentityproperties) (ReadOnly): The properties associated with the identity.
* **tags**: [SystemAssignedIdentityTags](#systemassignedidentitytags) (ReadOnly): Resource tags
* **type**: 'Microsoft.ManagedIdentity/identities' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ManagedIdentity/userAssignedIdentities@2021-09-30-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-09-30-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [UserAssignedIdentityProperties](#userassignedidentityproperties) (ReadOnly): The properties associated with the identity.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.ManagedIdentity/userAssignedIdentities' (ReadOnly, DeployTimeConstant): The resource type

## Function listAssociatedResources (Microsoft.ManagedIdentity/userAssignedIdentities@2021-09-30-preview)
* **Resource**: Microsoft.ManagedIdentity/userAssignedIdentities
* **ApiVersion**: 2021-09-30-preview
* **Output**: [AssociatedResourcesListResult](#associatedresourceslistresult)

## AssociatedResourcesListResult
### Properties
* **nextLink**: string (ReadOnly): The url to get the next page of results, if any.
* **totalCount**: int (ReadOnly): Total number of Azure resources assigned to the identity.
* **value**: [AzureResource](#azureresource)[] (ReadOnly): The collection of Azure resources returned by the resource action to get a list of assigned resources.

## AzureResource
### Properties
* **id**: string (ReadOnly): The ID of this resource.
* **name**: string (ReadOnly): The name of this resource.
* **resourceGroup**: string (ReadOnly): The name of the resource group this resource belongs to.
* **subscriptionDisplayName**: string (ReadOnly): The name of the subscription this resource belongs to.
* **subscriptionId**: string (ReadOnly): The ID of the subscription this resource belongs to.
* **type**: string (ReadOnly): The type of this resource.

## SystemAssignedIdentityProperties
### Properties
* **clientId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the app associated with the identity. This is a random generated UUID by MSI.
* **clientSecretUrl**: string (ReadOnly): The ManagedServiceIdentity DataPlane URL that can be queried to obtain the identity credentials.
* **principalId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the service principal object associated with the created identity.
* **tenantId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the tenant which the identity belongs to.

## SystemAssignedIdentityTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## UserAssignedIdentityProperties
### Properties
* **clientId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the app associated with the identity. This is a random generated UUID by MSI.
* **principalId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the service principal object associated with the created identity.
* **tenantId**: string {minLength: 36, maxLength: 36, pattern: "^[0-9a-fA-F]{8}-([0-9a-fA-F]{4}-){3}[0-9a-fA-F]{12}$"} (ReadOnly): The id of the tenant which the identity belongs to.

