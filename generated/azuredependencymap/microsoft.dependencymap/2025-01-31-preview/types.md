# Microsoft.DependencyMap @ 2025-01-31-preview

## Resource Microsoft.DependencyMap/maps@2025-01-31-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2025-01-31-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {pattern: "^[a-zA-Z][a-zA-Z0-9-]{2,23}$"} (Required, DeployTimeConstant): The resource name
* **properties**: [MapsResourceProperties](#mapsresourceproperties): The resource-specific properties for this resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.DependencyMap/maps' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DependencyMap/maps/discoverySources@2025-01-31-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2025-01-31-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {pattern: "^[a-zA-Z][a-zA-Z0-9-]{2,23}$"} (Required, DeployTimeConstant): The resource name
* **properties**: [DiscoverySourceResourceProperties](#discoverysourceresourceproperties): The resource-specific properties for this resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Azure Resource Manager metadata containing createdBy and modifiedBy information.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.DependencyMap/maps/discoverySources' (ReadOnly, DeployTimeConstant): The resource type

## Function exportDependencies (Microsoft.DependencyMap/maps@2025-01-31-preview)
* **Resource**: Microsoft.DependencyMap/maps
* **ApiVersion**: 2025-01-31-preview
* **Input**: [ExportDependenciesRequest](#exportdependenciesrequest)

## Function getConnectionsForProcessOnFocusedMachine (Microsoft.DependencyMap/maps@2025-01-31-preview)
* **Resource**: Microsoft.DependencyMap/maps
* **ApiVersion**: 2025-01-31-preview
* **Input**: [GetConnectionsForProcessOnFocusedMachineRequest](#getconnectionsforprocessonfocusedmachinerequest)

## Function getConnectionsWithConnectedMachineForFocusedMachine (Microsoft.DependencyMap/maps@2025-01-31-preview)
* **Resource**: Microsoft.DependencyMap/maps
* **ApiVersion**: 2025-01-31-preview
* **Input**: [GetConnectionsWithConnectedMachineForFocusedMachineRequest](#getconnectionswithconnectedmachineforfocusedmachinerequest)

## Function getDependencyViewForFocusedMachine (Microsoft.DependencyMap/maps@2025-01-31-preview)
* **Resource**: Microsoft.DependencyMap/maps
* **ApiVersion**: 2025-01-31-preview
* **Input**: [GetDependencyViewForFocusedMachineRequest](#getdependencyviewforfocusedmachinerequest)

## DateTimeFilter
### Properties
* **endDateTimeUtc**: string: End date time for dependency map visualization query
* **startDateTimeUtc**: string: Start date time for dependency map visualization query

## DependencyMapVisualizationFilter
### Properties
* **dateTime**: [DateTimeFilter](#datetimefilter): DateTime filter
* **processNameFilter**: [ProcessNameFilter](#processnamefilter): Process name filter

## DiscoverySourceResourceProperties
* **Discriminator**: sourceType

### Base Properties
* **provisioningState**: 'Accepted' | 'Canceled' | 'Deleting' | 'Failed' | 'Provisioning' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of Discovery Source resource.
* **sourceId**: string (Required): Source ArmId of Discovery Source resource

### OffAzureDiscoverySourceResourceProperties
#### Properties
* **sourceType**: 'OffAzure' (Required): Source type of Discovery Source resource.


## ExportDependenciesRequest
### Properties
* **filters**: [DependencyMapVisualizationFilter](#dependencymapvisualizationfilter): Filters for ExportDependencies
* **focusedMachineId**: string (Required): Machine arm id

## GetConnectionsForProcessOnFocusedMachineRequest
### Properties
* **filters**: [DependencyMapVisualizationFilter](#dependencymapvisualizationfilter): Filters for GetProcessNetworkConnections
* **focusedMachineId**: string (Required): Machine arm id
* **processIdOnFocusedMachine**: string (Required): Process id

## GetConnectionsWithConnectedMachineForFocusedMachineRequest
### Properties
* **connectedMachineId**: string (Required): Destination machine arm id
* **filters**: [DependencyMapVisualizationFilter](#dependencymapvisualizationfilter): Filters for GetNetworkConnectionsBetweenMachines
* **focusedMachineId**: string (Required): Source machine arm id

## GetDependencyViewForFocusedMachineRequest
### Properties
* **filters**: [DependencyMapVisualizationFilter](#dependencymapvisualizationfilter): Filters for GetSingleMachineDependencyView
* **focusedMachineId**: string (Required): Machine arm id

## MapsResourceProperties
### Properties
* **provisioningState**: 'Accepted' | 'Canceled' | 'Deleting' | 'Failed' | 'Provisioning' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of Maps resource.

## ProcessNameFilter
### Properties
* **operator**: 'contains' | 'notContains' | string (Required): Operator for process name filter
* **processNames**: string[] (Required): List of process names on which the operator should be applied

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

