# Microsoft.Kusto @ 2022-02-01

## Resource Microsoft.Kusto/clusters@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): A unique read-only string that changes whenever the resource is updated.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): Identity for the resource.
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ClusterProperties](#clusterproperties): Class representing the Kusto cluster properties.
* **sku**: [AzureSku](#azuresku) (Required): Azure SKU definition.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Kusto/clusters' (ReadOnly, DeployTimeConstant): The resource type
* **zones**: string[]: An array represents the availability zones of the cluster.

## Resource Microsoft.Kusto/clusters/attachedDatabaseConfigurations@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AttachedDatabaseConfigurationProperties](#attacheddatabaseconfigurationproperties): Class representing the an attached database configuration properties of kind specific.
* **type**: 'Microsoft.Kusto/clusters/attachedDatabaseConfigurations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/databases@2022-02-01
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.Kusto/clusters/databases' (ReadOnly, DeployTimeConstant): The resource type
### ReadOnlyFollowingDatabase
#### Properties
* **kind**: 'ReadOnlyFollowing' (Required): Kind of the database
* **properties**: [ReadOnlyFollowingDatabaseProperties](#readonlyfollowingdatabaseproperties): Class representing the Kusto database properties.

### ReadWriteDatabase
#### Properties
* **kind**: 'ReadWrite' (Required): Kind of the database
* **properties**: [ReadWriteDatabaseProperties](#readwritedatabaseproperties): Class representing the Kusto database properties.


## Resource Microsoft.Kusto/clusters/databases/dataConnections@2022-02-01
* **Valid Scope(s)**: ResourceGroup
* **Discriminator**: kind

### Base Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **type**: 'Microsoft.Kusto/clusters/databases/dataConnections' (ReadOnly, DeployTimeConstant): The resource type
### EventGridDataConnection
#### Properties
* **kind**: 'EventGrid' (Required): Kind of the endpoint for the data connection
* **properties**: [EventGridConnectionProperties](#eventgridconnectionproperties): Class representing the Kusto event grid connection properties.

### EventHubDataConnection
#### Properties
* **kind**: 'EventHub' (Required): Kind of the endpoint for the data connection
* **properties**: [EventHubConnectionProperties](#eventhubconnectionproperties): Class representing the Kusto event hub connection properties.

### IotHubDataConnection
#### Properties
* **kind**: 'IotHub' (Required): Kind of the endpoint for the data connection
* **properties**: [IotHubConnectionProperties](#iothubconnectionproperties): Class representing the Kusto Iot hub connection properties.


## Resource Microsoft.Kusto/clusters/databases/principalAssignments@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DatabasePrincipalProperties](#databaseprincipalproperties): A class representing database principal property.
* **type**: 'Microsoft.Kusto/clusters/databases/principalAssignments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/databases/scripts@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ScriptProperties](#scriptproperties): A class representing database script property.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Kusto/clusters/databases/scripts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/managedPrivateEndpoints@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedPrivateEndpointProperties](#managedprivateendpointproperties): A class representing the properties of a managed private endpoint object.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Kusto/clusters/managedPrivateEndpoints' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/principalAssignments@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ClusterPrincipalProperties](#clusterprincipalproperties): A class representing cluster principal property.
* **type**: 'Microsoft.Kusto/clusters/principalAssignments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Kusto/clusters/privateEndpointConnections@2022-02-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-02-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Kusto/clusters/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Function listFollowerDatabases (Microsoft.Kusto/clusters@2022-02-01)
* **Resource**: Microsoft.Kusto/clusters
* **ApiVersion**: 2022-02-01
* **Output**: [FollowerDatabaseListResult](#followerdatabaselistresult)

## Function listLanguageExtensions (Microsoft.Kusto/clusters@2022-02-01)
* **Resource**: Microsoft.Kusto/clusters
* **ApiVersion**: 2022-02-01
* **Output**: [LanguageExtensionsList](#languageextensionslist)

## Function listPrincipals (Microsoft.Kusto/clusters/databases@2022-02-01)
* **Resource**: Microsoft.Kusto/clusters/databases
* **ApiVersion**: 2022-02-01
* **Output**: [DatabasePrincipalListResult](#databaseprincipallistresult)

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned' (Required): The type of managed identity used. The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities. The type 'None' will remove all identities.
* **userAssignedIdentities**: [IdentityUserAssignedIdentities](#identityuserassignedidentities): The list of user identities associated with the Kusto cluster. The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## IdentityUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [ComponentsSgqdofSchemasIdentityPropertiesUserassignedidentitiesAdditionalproperties](#componentssgqdofschemasidentitypropertiesuserassignedidentitiesadditionalproperties)

## ComponentsSgqdofSchemasIdentityPropertiesUserassignedidentitiesAdditionalproperties
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## ClusterProperties
### Properties
* **acceptedAudiences**: [AcceptedAudiences](#acceptedaudiences)[]: The cluster's accepted audiences.
* **allowedFqdnList**: string[]: List of allowed FQDNs(Fully Qualified Domain Name) for egress from Cluster.
* **allowedIpRangeList**: string[]: The list of ips in the format of CIDR allowed to connect to the cluster.
* **dataIngestionUri**: string (ReadOnly): The cluster data ingestion URI.
* **enableAutoStop**: bool: A boolean value that indicates if the cluster could be automatically stopped (due to lack of data or no activity for many days).
* **enableDiskEncryption**: bool: A boolean value that indicates if the cluster's disks are encrypted.
* **enableDoubleEncryption**: bool: A boolean value that indicates if double encryption is enabled.
* **enablePurge**: bool: A boolean value that indicates if the purge operations are enabled.
* **enableStreamingIngest**: bool: A boolean value that indicates if the streaming ingest is enabled.
* **engineType**: 'V2' | 'V3': The engine type
* **keyVaultProperties**: [KeyVaultProperties](#keyvaultproperties): Properties of the key vault.
* **languageExtensions**: [LanguageExtensionsList](#languageextensionslist) (ReadOnly): The list of language extension objects.
* **optimizedAutoscale**: [OptimizedAutoscale](#optimizedautoscale): A class that contains the optimized auto scale definition.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly): A list of private endpoint connections.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **publicIPType**: 'DualStack' | 'IPv4': Indicates what public IP type to create - IPv4 (default), or DualStack (both IPv4 and IPv6)
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Public network access to the cluster is enabled by default. When disabled, only private endpoint connection to the cluster is allowed
* **restrictOutboundNetworkAccess**: 'Disabled' | 'Enabled': Whether or not to restrict outbound network access.  Value is optional but if passed in, must be 'Enabled' or 'Disabled'
* **state**: 'Creating' | 'Deleted' | 'Deleting' | 'Running' | 'Starting' | 'Stopped' | 'Stopping' | 'Unavailable' | 'Updating' (ReadOnly): The state of the resource.
* **stateReason**: string (ReadOnly): The reason for the cluster's current state.
* **trustedExternalTenants**: [TrustedExternalTenant](#trustedexternaltenant)[]: The cluster's external tenants.
* **uri**: string (ReadOnly): The cluster URI.
* **virtualClusterGraduationProperties**: string (WriteOnly): Virtual Cluster graduation properties
* **virtualNetworkConfiguration**: [VirtualNetworkConfiguration](#virtualnetworkconfiguration): A class that contains virtual network definition.

## AcceptedAudiences
### Properties
* **value**: string: GUID or valid URL representing an accepted audience.

## KeyVaultProperties
### Properties
* **keyName**: string: The name of the key vault key.
* **keyVaultUri**: string: The Uri of the key vault.
* **keyVersion**: string: The version of the key vault key.
* **userIdentity**: string: The user assigned identity (ARM resource id) that has access to the key.

## LanguageExtensionsList
### Properties
* **value**: [LanguageExtension](#languageextension)[]: The list of language extensions.

## LanguageExtension
### Properties
* **languageExtensionName**: 'PYTHON' | 'R': Language extension that can run within KQL query.

## OptimizedAutoscale
### Properties
* **isEnabled**: bool (Required): A boolean value that indicate if the optimized autoscale feature is enabled or not.
* **maximum**: int (Required): Maximum allowed instances count.
* **minimum**: int (Required): Minimum allowed instances count.
* **version**: int (Required): The version of the template defined, for instance 1.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of a private endpoint connection.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## PrivateEndpointConnectionProperties
### Properties
* **groupId**: string (ReadOnly): Group id of the private endpoint.
* **privateEndpoint**: [PrivateEndpointProperty](#privateendpointproperty) (ReadOnly): Private endpoint which the connection belongs to.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionStateProperty](#privatelinkserviceconnectionstateproperty) (Required): Connection State of the Private Endpoint Connection.
* **provisioningState**: string (ReadOnly): Provisioning state of the private endpoint.

## PrivateEndpointProperty
### Properties
* **id**: string (ReadOnly): Resource id of the private endpoint.

## PrivateLinkServiceConnectionStateProperty
### Properties
* **actionsRequired**: string (ReadOnly): Any action that is required beyond basic workflow (approve/ reject/ disconnect)
* **description**: string: The private link service connection description.
* **status**: string: The private link service connection status.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the resource.

## TrustedExternalTenant
### Properties
* **value**: string: GUID representing an external tenant.

## VirtualNetworkConfiguration
### Properties
* **dataManagementPublicIpId**: string (Required): Data management's service public IP address resource id.
* **enginePublicIpId**: string (Required): Engine service's public IP address resource id.
* **subnetId**: string (Required): The subnet resource id.

## AzureSku
### Properties
* **capacity**: int: The number of instances of the cluster.
* **name**: 'Dev(No SLA)_Standard_D11_v2' | 'Dev(No SLA)_Standard_E2a_v4' | 'Standard_D11_v2' | 'Standard_D12_v2' | 'Standard_D13_v2' | 'Standard_D14_v2' | 'Standard_D16d_v5' | 'Standard_D32d_v4' | 'Standard_D32d_v5' | 'Standard_DS13_v2+1TB_PS' | 'Standard_DS13_v2+2TB_PS' | 'Standard_DS14_v2+3TB_PS' | 'Standard_DS14_v2+4TB_PS' | 'Standard_E16a_v4' | 'Standard_E16ads_v5' | 'Standard_E16as_v4+3TB_PS' | 'Standard_E16as_v4+4TB_PS' | 'Standard_E16as_v5+3TB_PS' | 'Standard_E16as_v5+4TB_PS' | 'Standard_E16s_v4+3TB_PS' | 'Standard_E16s_v4+4TB_PS' | 'Standard_E16s_v5+3TB_PS' | 'Standard_E16s_v5+4TB_PS' | 'Standard_E2a_v4' | 'Standard_E2ads_v5' | 'Standard_E4a_v4' | 'Standard_E4ads_v5' | 'Standard_E64i_v3' | 'Standard_E80ids_v4' | 'Standard_E8a_v4' | 'Standard_E8ads_v5' | 'Standard_E8as_v4+1TB_PS' | 'Standard_E8as_v4+2TB_PS' | 'Standard_E8as_v5+1TB_PS' | 'Standard_E8as_v5+2TB_PS' | 'Standard_E8s_v4+1TB_PS' | 'Standard_E8s_v4+2TB_PS' | 'Standard_E8s_v5+1TB_PS' | 'Standard_E8s_v5+2TB_PS' | 'Standard_L16s' | 'Standard_L16s_v2' | 'Standard_L4s' | 'Standard_L8s' | 'Standard_L8s_v2' (Required): SKU name.
* **tier**: 'Basic' | 'Standard' (Required): SKU tier.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## AttachedDatabaseConfigurationProperties
### Properties
* **attachedDatabaseNames**: string[] (ReadOnly): The list of databases from the clusterResourceId which are currently attached to the cluster.
* **clusterResourceId**: string (Required): The resource id of the cluster where the databases you would like to attach reside.
* **databaseName**: string (Required): The name of the database which you would like to attach, use * if you want to follow all current and future databases.
* **defaultPrincipalsModificationKind**: 'None' | 'Replace' | 'Union' (Required): The default principals modification kind
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **tableLevelSharingProperties**: [TableLevelSharingProperties](#tablelevelsharingproperties): Tables that will be included and excluded in the follower database

## TableLevelSharingProperties
### Properties
* **externalTablesToExclude**: string[]: List of external tables exclude from the follower database
* **externalTablesToInclude**: string[]: List of external tables to include in the follower database
* **materializedViewsToExclude**: string[]: List of materialized views exclude from the follower database
* **materializedViewsToInclude**: string[]: List of materialized views to include in the follower database
* **tablesToExclude**: string[]: List of tables to exclude from the follower database
* **tablesToInclude**: string[]: List of tables to include in the follower database

## ReadOnlyFollowingDatabaseProperties
### Properties
* **attachedDatabaseConfigurationName**: string (ReadOnly): The name of the attached database configuration cluster
* **hotCachePeriod**: string: The time the data should be kept in cache for fast queries in TimeSpan.
* **leaderClusterResourceId**: string (ReadOnly): The name of the leader cluster
* **principalsModificationKind**: 'None' | 'Replace' | 'Union' (ReadOnly): The principals modification kind of the database
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **softDeletePeriod**: string (ReadOnly): The time the data should be kept before it stops being accessible to queries in TimeSpan.
* **statistics**: [DatabaseStatistics](#databasestatistics) (ReadOnly): A class that contains database statistics information.

## DatabaseStatistics
### Properties
* **size**: int: The database size - the total size of compressed data and index in bytes.

## ReadWriteDatabaseProperties
### Properties
* **hotCachePeriod**: string: The time the data should be kept in cache for fast queries in TimeSpan.
* **isFollowed**: bool (ReadOnly): Indicates whether the database is followed.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **softDeletePeriod**: string: The time the data should be kept before it stops being accessible to queries in TimeSpan.
* **statistics**: [DatabaseStatistics](#databasestatistics) (ReadOnly): A class that contains database statistics information.

## EventGridConnectionProperties
### Properties
* **blobStorageEventType**: 'Microsoft.Storage.BlobCreated' | 'Microsoft.Storage.BlobRenamed': The name of blob storage event type to process.
* **consumerGroup**: string (Required): The event hub consumer group.
* **databaseRouting**: 'Multi' | 'Single': Indication for database routing information from the data connection, by default only database routing information is allowed
* **dataFormat**: 'APACHEAVRO' | 'AVRO' | 'CSV' | 'JSON' | 'MULTIJSON' | 'ORC' | 'PARQUET' | 'PSV' | 'RAW' | 'SCSV' | 'SINGLEJSON' | 'SOHSV' | 'TSV' | 'TSVE' | 'TXT' | 'W3CLOGFILE': The data format of the message. Optionally the data format can be added to each message.
* **eventGridResourceId**: string: The resource ID of the event grid that is subscribed to the storage account events.
* **eventHubResourceId**: string (Required): The resource ID where the event grid is configured to send events.
* **ignoreFirstRecord**: bool: A Boolean value that, if set to true, indicates that ingestion should ignore the first record of every file
* **managedIdentityObjectId**: string (ReadOnly): The object ID of managedIdentityResourceId
* **managedIdentityResourceId**: string: The resource ID of a managed identity (system or user assigned) to be used to authenticate with event hub and storage account.
* **mappingRuleName**: string: The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **storageAccountResourceId**: string (Required): The resource ID of the storage account where the data resides.
* **tableName**: string: The table where the data should be ingested. Optionally the table information can be added to each message.

## EventHubConnectionProperties
### Properties
* **compression**: 'GZip' | 'None': The compression type
* **consumerGroup**: string (Required): The event hub consumer group.
* **databaseRouting**: 'Multi' | 'Single': Indication for database routing information from the data connection, by default only database routing information is allowed
* **dataFormat**: 'APACHEAVRO' | 'AVRO' | 'CSV' | 'JSON' | 'MULTIJSON' | 'ORC' | 'PARQUET' | 'PSV' | 'RAW' | 'SCSV' | 'SINGLEJSON' | 'SOHSV' | 'TSV' | 'TSVE' | 'TXT' | 'W3CLOGFILE': The data format of the message. Optionally the data format can be added to each message.
* **eventHubResourceId**: string (Required): The resource ID of the event hub to be used to create a data connection.
* **eventSystemProperties**: string[]: System properties of the event hub
* **managedIdentityObjectId**: string (ReadOnly): The object ID of the managedIdentityResourceId
* **managedIdentityResourceId**: string: Empty for non-managed identity based data connection. For system assigned identity, provide cluster resource Id.  For user assigned identity (UAI) provide the UAI resource Id.
* **mappingRuleName**: string: The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **tableName**: string: The table where the data should be ingested. Optionally the table information can be added to each message.

## IotHubConnectionProperties
### Properties
* **consumerGroup**: string (Required): The iot hub consumer group.
* **databaseRouting**: 'Multi' | 'Single': Indication for database routing information from the data connection, by default only database routing information is allowed
* **dataFormat**: 'APACHEAVRO' | 'AVRO' | 'CSV' | 'JSON' | 'MULTIJSON' | 'ORC' | 'PARQUET' | 'PSV' | 'RAW' | 'SCSV' | 'SINGLEJSON' | 'SOHSV' | 'TSV' | 'TSVE' | 'TXT' | 'W3CLOGFILE': The data format of the message. Optionally the data format can be added to each message.
* **eventSystemProperties**: string[]: System properties of the iot hub
* **iotHubResourceId**: string (Required): The resource ID of the Iot hub to be used to create a data connection.
* **mappingRuleName**: string: The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **sharedAccessPolicyName**: string (Required): The name of the share access policy
* **tableName**: string: The table where the data should be ingested. Optionally the table information can be added to each message.

## DatabasePrincipalProperties
### Properties
* **aadObjectId**: string (ReadOnly): The service principal object id in AAD (Azure active directory)
* **principalId**: string (Required): The principal ID assigned to the database principal. It can be a user email, application ID, or security group name.
* **principalName**: string (ReadOnly): The principal name
* **principalType**: 'App' | 'Group' | 'User' (Required): Principal type.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **role**: 'Admin' | 'Ingestor' | 'Monitor' | 'UnrestrictedViewer' | 'User' | 'Viewer' (Required): Database principal role.
* **tenantId**: string: The tenant id of the principal
* **tenantName**: string (ReadOnly): The tenant name of the principal

## ScriptProperties
### Properties
* **continueOnErrors**: bool: Flag that indicates whether to continue if one of the command fails.
* **forceUpdateTag**: string: A unique string. If changed the script will be applied again.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **scriptContent**: string (WriteOnly): The script content. This property should be used when the script is provide inline and not through file in a SA. Must not be used together with scriptUrl and scriptUrlSasToken properties.
* **scriptUrl**: string: The url to the KQL script blob file. Must not be used together with scriptContent property
* **scriptUrlSasToken**: string (WriteOnly): The SaS token that provide read access to the file which contain the script. Must be provided when using scriptUrl property.

## ManagedPrivateEndpointProperties
### Properties
* **groupId**: string (Required): The groupId in which the managed private endpoint is created.
* **privateLinkResourceId**: string (Required): The ARM resource ID of the resource for which the managed private endpoint is created.
* **privateLinkResourceRegion**: string: The region of the resource to which the managed private endpoint is created.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **requestMessage**: string: The user request message.

## ClusterPrincipalProperties
### Properties
* **aadObjectId**: string (ReadOnly): The service principal object id in AAD (Azure active directory)
* **principalId**: string (Required): The principal ID assigned to the cluster principal. It can be a user email, application ID, or security group name.
* **principalName**: string (ReadOnly): The principal name
* **principalType**: 'App' | 'Group' | 'User' (Required): Principal type.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Moving' | 'Running' | 'Succeeded' (ReadOnly): The provisioned state of the resource.
* **role**: 'AllDatabasesAdmin' | 'AllDatabasesViewer' (Required): Cluster principal role.
* **tenantId**: string: The tenant id of the principal
* **tenantName**: string (ReadOnly): The tenant name of the principal

## FollowerDatabaseListResult
### Properties
* **value**: [FollowerDatabaseDefinition](#followerdatabasedefinition)[] (ReadOnly): The list of follower database result.

## FollowerDatabaseDefinition
### Properties
* **attachedDatabaseConfigurationName**: string (ReadOnly): Resource name of the attached database configuration in the follower cluster.
* **clusterResourceId**: string (ReadOnly): Resource id of the cluster that follows a database owned by this cluster.
* **databaseName**: string (ReadOnly): The database name owned by this cluster that was followed. * in case following all databases.

## LanguageExtensionsList
### Properties
* **value**: [LanguageExtension](#languageextension)[]: The list of language extensions.

## DatabasePrincipalListResult
### Properties
* **value**: [DatabasePrincipal](#databaseprincipal)[] (ReadOnly): The list of Kusto database principals.

## DatabasePrincipal
### Properties
* **appId**: string (ReadOnly): Application id - relevant only for application principal type.
* **email**: string (ReadOnly): Database principal email if exists.
* **fqn**: string (ReadOnly): Database principal fully qualified name.
* **name**: string (ReadOnly): Database principal name.
* **role**: 'Admin' | 'Ingestor' | 'Monitor' | 'UnrestrictedViewer' | 'User' | 'Viewer' (ReadOnly): Database principal role.
* **tenantName**: string (ReadOnly): The tenant name of the principal
* **type**: 'App' | 'Group' | 'User' (ReadOnly): Database principal type.
