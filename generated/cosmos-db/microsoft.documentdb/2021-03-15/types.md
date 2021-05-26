# Microsoft.DocumentDB @ 2021-03-15

## Resource Microsoft.DocumentDB/databaseAccounts@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ManagedServiceIdentity](#managedserviceidentity): Identity for the resource.
* **kind**: 'GlobalDocumentDB' | 'MongoDB' | 'Parse': Indicates the type of database account. This can only be set at database account creation.
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DatabaseAccountCreateUpdateProperties](#databaseaccountcreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB database accounts.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CassandraKeyspaceCreateUpdateProperties](#cassandrakeyspacecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB Cassandra keyspace.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/tables@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CassandraTableCreateUpdateProperties](#cassandratablecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB Cassandra table.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/tables' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/tables/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/tables/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/cassandraKeyspaces/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/gremlinDatabases@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [GremlinDatabaseCreateUpdateProperties](#gremlindatabasecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB Gremlin database.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/gremlinDatabases' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/graphs@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [GremlinGraphCreateUpdateProperties](#gremlingraphcreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB Gremlin graph.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/graphs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/graphs/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/graphs/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/gremlinDatabases/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/mongodbDatabases@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MongoDBDatabaseCreateUpdateProperties](#mongodbdatabasecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB MongoDB database.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/mongodbDatabases' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/collections@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MongoDBCollectionCreateUpdateProperties](#mongodbcollectioncreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB MongoDB collection.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/collections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/collections/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/collections/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/mongodbDatabases/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/notebookWorkspaces@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [NotebookWorkspaceProperties](#notebookworkspaceproperties) (ReadOnly): Properties of a notebook workspace resource.
* **type**: 'Microsoft.DocumentDB/databaseAccounts/notebookWorkspaces' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/privateEndpointConnections@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of a private endpoint connection.
* **type**: 'Microsoft.DocumentDB/databaseAccounts/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlDatabaseCreateUpdateProperties](#sqldatabasecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB SQL database.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlContainerCreateUpdateProperties](#sqlcontainercreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB container.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/storedProcedures@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlStoredProcedureCreateUpdateProperties](#sqlstoredprocedurecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB storedProcedure.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/storedProcedures' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/triggers@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlTriggerCreateUpdateProperties](#sqltriggercreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB trigger.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/triggers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/userDefinedFunctions@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SqlUserDefinedFunctionCreateUpdateProperties](#sqluserdefinedfunctioncreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB userDefinedFunction.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/userDefinedFunctions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/sqlDatabases/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/sqlDatabases/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/tables@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [TableCreateUpdateProperties](#tablecreateupdateproperties) (Required): Properties to create and update Azure Cosmos DB Table.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/tables' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DocumentDB/databaseAccounts/tables/throughputSettings@2021-03-15
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-15' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location of the resource group to which the resource belongs.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ThroughputSettingsUpdateProperties](#throughputsettingsupdateproperties) (Required): Properties to update Azure Cosmos DB resource throughput.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Tags are a list of key-value pairs that describe the resource. These tags can be used in viewing and grouping this resource (across resource groups). A maximum of 15 tags can be provided for a resource. Each tag must have a key no greater than 128 characters and value no greater than 256 characters. For example, the default experience for a template type is set with "defaultExperience": "Cassandra". Current "defaultExperience" values also include "Table", "Graph", "DocumentDB", and "MongoDB".
* **type**: 'Microsoft.DocumentDB/databaseAccounts/tables/throughputSettings' (ReadOnly, DeployTimeConstant): The resource type

## ManagedServiceIdentity
### Properties
* **principalId**: string (ReadOnly): The principal id of the system assigned identity. This property will only be provided for a system assigned identity.
* **tenantId**: string (ReadOnly): The tenant id of the system assigned identity. This property will only be provided for a system assigned identity.
* **type**: 'None' | 'SystemAssigned,UserAssigned' | 'SystemAssigned' | 'UserAssigned': The type of identity used for the resource. The type 'SystemAssigned,UserAssigned' includes both an implicitly created identity and a set of user assigned identities. The type 'None' will remove any identities from the service.
* **userAssignedIdentities**: [Dictionary<string,Schemas131UserAssignedIdentitiesValue>](#dictionarystringschemas131userassignedidentitiesvalue): The list of user identities associated with resource. The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## Dictionary<string,Schemas131UserAssignedIdentitiesValue>
### Properties
### Additional Properties
* **Additional Properties Type**: [schemas:131_userAssignedIdentitiesValue](#schemas131userassignedidentitiesvalue)

## schemas:131_userAssignedIdentitiesValue
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## DatabaseAccountCreateUpdateProperties
### Properties
* **apiProperties**: [ApiProperties](#apiproperties)
* **backupPolicy**: [BackupPolicy](#backuppolicy): The object representing the policy for taking backups on an account.
* **capabilities**: [Capability](#capability)[]: List of Cosmos DB capabilities for the account
* **connectorOffer**: 'Small': The cassandra connector offer type for the Cosmos DB database C* account.
* **consistencyPolicy**: [ConsistencyPolicy](#consistencypolicy): The consistency policy for the Cosmos DB database account.
* **cors**: [CorsPolicy](#corspolicy)[]: The CORS policy for the Cosmos DB database account.
* **databaseAccountOfferType**: string (Required): The offer type for the database
* **defaultIdentity**: string: The default identity for accessing key vault used in features like customer managed keys. The default identity needs to be explicitly set by the users. It can be "FirstPartyIdentity", "SystemAssignedIdentity" and more.
* **disableKeyBasedMetadataWriteAccess**: bool: Disable write operations on metadata resources (databases, containers, throughput) via account keys
* **documentEndpoint**: string (ReadOnly): The connection endpoint for the Cosmos DB database account.
* **enableAnalyticalStorage**: bool: Flag to indicate whether to enable storage analytics.
* **enableAutomaticFailover**: bool: Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage. Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.
* **enableCassandraConnector**: bool: Enables the cassandra connector on the Cosmos DB C* account
* **enableFreeTier**: bool: Flag to indicate whether Free Tier is enabled.
* **enableMultipleWriteLocations**: bool: Enables the account to write in multiple locations
* **failoverPolicies**: [FailoverPolicy](#failoverpolicy)[] (ReadOnly): An array that contains the regions ordered by their failover priorities.
* **ipRules**: [IpAddressOrRange](#ipaddressorrange)[]: Array of IpAddressOrRange objects.
* **isVirtualNetworkFilterEnabled**: bool: Flag to indicate whether to enable/disable Virtual Network ACL rules.
* **keyVaultKeyUri**: string: The URI of the key vault
* **locations**: [Location](#location)[] (Required): An array that contains the georeplication locations enabled for the Cosmos DB account.
* **networkAclBypass**: 'AzureServices' | 'None': Indicates what services are allowed to bypass firewall checks.
* **networkAclBypassResourceIds**: string[]: An array that contains the Resource Ids for Network Acl Bypass for the Cosmos DB account.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly): List of Private Endpoint Connections configured for the Cosmos DB account.
* **provisioningState**: string (ReadOnly): The status of the Cosmos DB account at the time the operation was called. The status can be one of following. 'Creating' – the Cosmos DB account is being created. When an account is in Creating state, only properties that are specified as input for the Create Cosmos DB account operation are returned. 'Succeeded' – the Cosmos DB account is active for use. 'Updating' – the Cosmos DB account is being updated. 'Deleting' – the Cosmos DB account is being deleted. 'Failed' – the Cosmos DB account failed creation. 'DeletionFailed' – the Cosmos DB account deletion failed.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Whether requests from Public Network are allowed.
* **readLocations**: [Location](#location)[] (ReadOnly): An array that contains of the read locations enabled for the Cosmos DB account.
* **virtualNetworkRules**: [VirtualNetworkRule](#virtualnetworkrule)[]: List of Virtual Network ACL rules configured for the Cosmos DB account.
* **writeLocations**: [Location](#location)[] (ReadOnly): An array that contains the write location for the Cosmos DB account.

## ApiProperties
### Properties
* **serverVersion**: '3.2' | '3.6' | '4.0': Describes the ServerVersion of an a MongoDB account.

## BackupPolicy
* **Discriminator**: type
### Base Properties
### Continuous
#### Properties
* **type**: 'Continuous' (Required): The object representing continuous mode backup policy.

### Periodic
#### Properties
* **periodicModeProperties**: [PeriodicModeProperties](#periodicmodeproperties): Configuration values for periodic mode backup
* **type**: 'Periodic' (Required): The object representing periodic mode backup policy.


## Continuous
### Properties
* **type**: 'Continuous' (Required): The object representing continuous mode backup policy.

## Periodic
### Properties
* **periodicModeProperties**: [PeriodicModeProperties](#periodicmodeproperties): Configuration values for periodic mode backup
* **type**: 'Periodic' (Required): The object representing periodic mode backup policy.

## PeriodicModeProperties
### Properties
* **backupIntervalInMinutes**: int: An integer representing the interval in minutes between two backups
* **backupRetentionIntervalInHours**: int: An integer representing the time (in hours) that each backup is retained

## Capability
### Properties
* **name**: string: Name of the Cosmos DB capability. For example, "name": "EnableCassandra". Current values also include "EnableTable" and "EnableGremlin".

## ConsistencyPolicy
### Properties
* **defaultConsistencyLevel**: 'BoundedStaleness' | 'ConsistentPrefix' | 'Eventual' | 'Session' | 'Strong' (Required): The default consistency level and configuration settings of the Cosmos DB account.
* **maxIntervalInSeconds**: int: When used with the Bounded Staleness consistency level, this value represents the time amount of staleness (in seconds) tolerated. Accepted range for this value is 5 - 86400. Required when defaultConsistencyPolicy is set to 'BoundedStaleness'.
* **maxStalenessPrefix**: int: When used with the Bounded Staleness consistency level, this value represents the number of stale requests tolerated. Accepted range for this value is 1 – 2,147,483,647. Required when defaultConsistencyPolicy is set to 'BoundedStaleness'.

## CorsPolicy
### Properties
* **allowedHeaders**: string: The request headers that the origin domain may specify on the CORS request.
* **allowedMethods**: string: The methods (HTTP request verbs) that the origin domain may use for a CORS request.
* **allowedOrigins**: string (Required): The origin domains that are permitted to make a request against the service via CORS.
* **exposedHeaders**: string: The response headers that may be sent in the response to the CORS request and exposed by the browser to the request issuer.
* **maxAgeInSeconds**: int: The maximum amount time that a browser should cache the preflight OPTIONS request.

## FailoverPolicy
### Properties
* **failoverPriority**: int (ReadOnly): The failover priority of the region. A failover priority of 0 indicates a write region. The maximum value for a failover priority = (total number of regions - 1). Failover priority values must be unique for each of the regions in which the database account exists.
* **id**: string (ReadOnly): The unique identifier of the region in which the database account replicates to. Example: &lt;accountName&gt;-&lt;locationName&gt;.
* **locationName**: string (ReadOnly): The name of the region in which the database account exists.

## IpAddressOrRange
### Properties
* **ipAddressOrRange**: string: A single IPv4 address or a single IPv4 address range in CIDR format. Provided IPs must be well-formatted and cannot be contained in one of the following ranges: 10.0.0.0/8, 100.64.0.0/10, 172.16.0.0/12, 192.168.0.0/16, since these are not enforceable by the IP address filter. Example of valid inputs: “23.40.210.245” or “23.40.210.0/8”.

## Location
### Properties
* **documentEndpoint**: string (ReadOnly): The connection endpoint for the specific region. Example: https://&lt;accountName&gt;-&lt;locationName&gt;.documents.azure.com:443/
* **failoverPriority**: int: The failover priority of the region. A failover priority of 0 indicates a write region. The maximum value for a failover priority = (total number of regions - 1). Failover priority values must be unique for each of the regions in which the database account exists.
* **id**: string (ReadOnly): The unique identifier of the region within the database account. Example: &lt;accountName&gt;-&lt;locationName&gt;.
* **isZoneRedundant**: bool: Flag to indicate whether or not this region is an AvailabilityZone region
* **locationName**: string: The name of the region.
* **provisioningState**: string: The status of the Cosmos DB account at the time the operation was called. The status can be one of following. 'Creating' – the Cosmos DB account is being created. When an account is in Creating state, only properties that are specified as input for the Create Cosmos DB account operation are returned. 'Succeeded' – the Cosmos DB account is active for use. 'Updating' – the Cosmos DB account is being updated. 'Deleting' – the Cosmos DB account is being deleted. 'Failed' – the Cosmos DB account failed creation. 'DeletionFailed' – the Cosmos DB account deletion failed.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties) (ReadOnly): Properties of a private endpoint connection.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## PrivateEndpointConnectionProperties
### Properties
* **groupId**: string (ReadOnly): Group id of the private endpoint.
* **privateEndpoint**: [PrivateEndpointProperty](#privateendpointproperty) (ReadOnly): Private endpoint which the connection belongs to.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionStateProperty](#privatelinkserviceconnectionstateproperty) (ReadOnly): Connection State of the Private Endpoint Connection.
* **provisioningState**: string (ReadOnly): Provisioning state of the private endpoint.

## PrivateEndpointProperty
### Properties
* **id**: string (ReadOnly): Resource id of the private endpoint.

## PrivateLinkServiceConnectionStateProperty
### Properties
* **actionsRequired**: string (ReadOnly): Any action that is required beyond basic workflow (approve/ reject/ disconnect)
* **description**: string (ReadOnly): The private link service connection description.
* **status**: string (ReadOnly): The private link service connection status.

## VirtualNetworkRule
### Properties
* **id**: string: Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}.
* **ignoreMissingVNetServiceEndpoint**: bool: Create firewall rule before the virtual network has vnet service endpoint enabled.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## CassandraKeyspaceCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [CassandraKeyspaceResource](#cassandrakeyspaceresource) (Required): Cosmos DB Cassandra keyspace resource object

## CreateUpdateOptions
### Properties
* **autoscaleSettings**: [AutoscaleSettings](#autoscalesettings) (WriteOnly)
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **throughput**: int (WriteOnly): Request Units per second. For example, "throughput": 10000.

## AutoscaleSettings
### Properties
* **maxThroughput**: int (WriteOnly): Represents maximum throughput, the resource can scale up to.

## CassandraKeyspaceResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB Cassandra keyspace
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## CassandraTableCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [CassandraTableResource](#cassandratableresource) (Required): Cosmos DB Cassandra table resource object

## CassandraTableResource
### Properties
* **analyticalStorageTtl**: int (WriteOnly): Analytical TTL.
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **defaultTtl**: int (WriteOnly): Time to live of the Cosmos DB Cassandra table
* **id**: string (Required, WriteOnly): Name of the Cosmos DB Cassandra table
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **schema**: [CassandraSchema](#cassandraschema) (WriteOnly): Cosmos DB Cassandra table schema

## CassandraSchema
### Properties
* **clusterKeys**: [ClusterKey](#clusterkey)[] (WriteOnly): List of cluster key.
* **columns**: [Column](#column)[] (WriteOnly): List of Cassandra table columns.
* **partitionKeys**: [CassandraPartitionKey](#cassandrapartitionkey)[] (WriteOnly): List of partition key.

## ClusterKey
### Properties
* **name**: string (WriteOnly): Name of the Cosmos DB Cassandra table cluster key
* **orderBy**: string (WriteOnly): Order of the Cosmos DB Cassandra table cluster key, only support "Asc" and "Desc"

## Column
### Properties
* **name**: string (WriteOnly): Name of the Cosmos DB Cassandra table column
* **type**: string (WriteOnly): Type of the Cosmos DB Cassandra table column

## CassandraPartitionKey
### Properties
* **name**: string (WriteOnly): Name of the Cosmos DB Cassandra table partition key

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ThroughputSettingsUpdateProperties
### Properties
* **resource**: [ThroughputSettingsResource](#throughputsettingsresource) (Required): Cosmos DB resource throughput object. Either throughput is required or autoscaleSettings is required, but not both.

## ThroughputSettingsResource
### Properties
* **autoscaleSettings**: [AutoscaleSettingsResource](#autoscalesettingsresource) (WriteOnly): Cosmos DB provisioned throughput settings object
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **minimumThroughput**: string (ReadOnly, WriteOnly): The minimum throughput of the resource
* **offerReplacePending**: string (ReadOnly, WriteOnly): The throughput replace is pending
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **throughput**: int (WriteOnly): Value of the Cosmos DB resource throughput. Either throughput is required or autoscaleSettings is required, but not both.

## AutoscaleSettingsResource
### Properties
* **autoUpgradePolicy**: [AutoUpgradePolicyResource](#autoupgradepolicyresource) (WriteOnly): Cosmos DB resource auto-upgrade policy
* **maxThroughput**: int (Required, WriteOnly): Represents maximum throughput container can scale up to.
* **targetMaxThroughput**: int (ReadOnly, WriteOnly): Represents target maximum throughput container can scale up to once offer is no longer in pending state.

## AutoUpgradePolicyResource
### Properties
* **throughputPolicy**: [ThroughputPolicyResource](#throughputpolicyresource) (WriteOnly): Cosmos DB resource throughput policy

## ThroughputPolicyResource
### Properties
* **incrementPercent**: int (WriteOnly): Represents the percentage by which throughput can increase every time throughput policy kicks in.
* **isEnabled**: bool (WriteOnly): Determines whether the ThroughputPolicy is active or not

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GremlinDatabaseCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [GremlinDatabaseResource](#gremlindatabaseresource) (Required): Cosmos DB Gremlin database resource object

## GremlinDatabaseResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB Gremlin database
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GremlinGraphCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [GremlinGraphResource](#gremlingraphresource) (Required): Cosmos DB Gremlin graph resource object

## GremlinGraphResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **conflictResolutionPolicy**: [ConflictResolutionPolicy](#conflictresolutionpolicy) (WriteOnly): The conflict resolution policy for the container.
* **defaultTtl**: int (WriteOnly): Default time to live
* **id**: string (Required, WriteOnly): Name of the Cosmos DB Gremlin graph
* **indexingPolicy**: [IndexingPolicy](#indexingpolicy) (WriteOnly): Cosmos DB indexing policy
* **partitionKey**: [ContainerPartitionKey](#containerpartitionkey) (WriteOnly): The configuration of the partition key to be used for partitioning data into multiple partitions
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **uniqueKeyPolicy**: [UniqueKeyPolicy](#uniquekeypolicy) (WriteOnly): The unique key policy configuration for specifying uniqueness constraints on documents in the collection in the Azure Cosmos DB service.

## ConflictResolutionPolicy
### Properties
* **conflictResolutionPath**: string (WriteOnly): The conflict resolution path in the case of LastWriterWins mode.
* **conflictResolutionProcedure**: string (WriteOnly): The procedure to resolve conflicts in the case of custom mode.
* **mode**: 'Custom' | 'LastWriterWins' (WriteOnly): Indicates the conflict resolution mode.

## IndexingPolicy
### Properties
* **automatic**: bool (WriteOnly): Indicates if the indexing policy is automatic
* **compositeIndexes**: [CompositePath](#compositepath)[][] (WriteOnly): List of composite path list
* **excludedPaths**: [ExcludedPath](#excludedpath)[] (WriteOnly): List of paths to exclude from indexing
* **includedPaths**: [IncludedPath](#includedpath)[] (WriteOnly): List of paths to include in the indexing
* **indexingMode**: 'consistent' | 'lazy' | 'none' (WriteOnly): Indicates the indexing mode.
* **spatialIndexes**: [SpatialSpec](#spatialspec)[] (WriteOnly): List of spatial specifics

## CompositePath
### Properties
* **order**: 'ascending' | 'descending' (WriteOnly): Sort order for composite paths.
* **path**: string (WriteOnly): The path for which the indexing behavior applies to. Index paths typically start with root and end with wildcard (/path/*)

## ExcludedPath
### Properties
* **path**: string (WriteOnly): The path for which the indexing behavior applies to. Index paths typically start with root and end with wildcard (/path/*)

## IncludedPath
### Properties
* **indexes**: [Indexes](#indexes)[] (WriteOnly): List of indexes for this path
* **path**: string (WriteOnly): The path for which the indexing behavior applies to. Index paths typically start with root and end with wildcard (/path/*)

## Indexes
### Properties
* **dataType**: 'LineString' | 'MultiPolygon' | 'Number' | 'Point' | 'Polygon' | 'String' (WriteOnly): The datatype for which the indexing behavior is applied to.
* **kind**: 'Hash' | 'Range' | 'Spatial' (WriteOnly): Indicates the type of index.
* **precision**: int (WriteOnly): The precision of the index. -1 is maximum precision.

## SpatialSpec
### Properties
* **path**: string (WriteOnly): The path for which the indexing behavior applies to. Index paths typically start with root and end with wildcard (/path/*)
* **types**: 'LineString' | 'MultiPolygon' | 'Point' | 'Polygon'[] (WriteOnly): List of path's spatial type

## ContainerPartitionKey
### Properties
* **kind**: 'Hash' | 'MultiHash' | 'Range' (WriteOnly): Indicates the kind of algorithm used for partitioning. For MultiHash, multiple partition keys (upto three maximum) are supported for container create.
* **paths**: string[] (WriteOnly): List of paths using which data within the container can be partitioned
* **systemKey**: bool (ReadOnly, WriteOnly): Indicates if the container is using a system generated partition key
* **version**: int (WriteOnly): Indicates the version of the partition key definition

## UniqueKeyPolicy
### Properties
* **uniqueKeys**: [UniqueKey](#uniquekey)[] (WriteOnly): List of unique keys on that enforces uniqueness constraint on documents in the collection in the Azure Cosmos DB service.

## UniqueKey
### Properties
* **paths**: string[] (WriteOnly): List of paths must be unique for each document in the Azure Cosmos DB service

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## MongoDBDatabaseCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [MongoDBDatabaseResource](#mongodbdatabaseresource) (Required): Cosmos DB MongoDB database resource object

## MongoDBDatabaseResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB MongoDB database
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## MongoDBCollectionCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [MongoDBCollectionResource](#mongodbcollectionresource) (Required): Cosmos DB MongoDB collection resource object

## MongoDBCollectionResource
### Properties
* **analyticalStorageTtl**: int (WriteOnly): Analytical TTL.
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB MongoDB collection
* **indexes**: [MongoIndex](#mongoindex)[] (WriteOnly): List of index keys
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **shardKey**: [Dictionary<string,String>](#dictionarystringstring) (WriteOnly): The shard key and partition kind pair, only support "Hash" partition kind

## MongoIndex
### Properties
* **key**: [MongoIndexKeys](#mongoindexkeys) (WriteOnly): Cosmos DB MongoDB collection resource object
* **options**: [MongoIndexOptions](#mongoindexoptions) (WriteOnly): Cosmos DB MongoDB collection index options

## MongoIndexKeys
### Properties
* **keys**: string[] (WriteOnly): List of keys for each MongoDB collection in the Azure Cosmos DB service

## MongoIndexOptions
### Properties
* **expireAfterSeconds**: int (WriteOnly): Expire after seconds
* **unique**: bool (WriteOnly): Is unique or not

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## NotebookWorkspaceProperties
### Properties
* **notebookServerEndpoint**: string (ReadOnly): Specifies the endpoint of Notebook server.
* **status**: string (ReadOnly): Status of the notebook workspace. Possible values are: Creating, Online, Deleting, Failed, Updating.

## SqlDatabaseCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [SqlDatabaseResource](#sqldatabaseresource) (Required): Cosmos DB SQL database resource object

## SqlDatabaseResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB SQL database
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SqlContainerCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [SqlContainerResource](#sqlcontainerresource) (Required): Cosmos DB SQL container resource object

## SqlContainerResource
### Properties
* **analyticalStorageTtl**: int (WriteOnly): Analytical TTL.
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **conflictResolutionPolicy**: [ConflictResolutionPolicy](#conflictresolutionpolicy) (WriteOnly): The conflict resolution policy for the container.
* **defaultTtl**: int (WriteOnly): Default time to live
* **id**: string (Required, WriteOnly): Name of the Cosmos DB SQL container
* **indexingPolicy**: [IndexingPolicy](#indexingpolicy) (WriteOnly): Cosmos DB indexing policy
* **partitionKey**: [ContainerPartitionKey](#containerpartitionkey) (WriteOnly): The configuration of the partition key to be used for partitioning data into multiple partitions
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **uniqueKeyPolicy**: [UniqueKeyPolicy](#uniquekeypolicy) (WriteOnly): The unique key policy configuration for specifying uniqueness constraints on documents in the collection in the Azure Cosmos DB service.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SqlStoredProcedureCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions) (WriteOnly): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [SqlStoredProcedureResource](#sqlstoredprocedureresource) (Required): Cosmos DB SQL storedProcedure resource object

## SqlStoredProcedureResource
### Properties
* **body**: string (WriteOnly): Body of the Stored Procedure
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB SQL storedProcedure
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SqlTriggerCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions) (WriteOnly): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [SqlTriggerResource](#sqltriggerresource) (Required): Cosmos DB SQL trigger resource object

## SqlTriggerResource
### Properties
* **body**: string (WriteOnly): Body of the Trigger
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB SQL trigger
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **triggerOperation**: 'All' | 'Create' | 'Delete' | 'Replace' | 'Update' (WriteOnly): The operation the trigger is associated with.
* **triggerType**: 'Post' | 'Pre' (WriteOnly): Type of the Trigger.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SqlUserDefinedFunctionCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions) (WriteOnly): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [SqlUserDefinedFunctionResource](#sqluserdefinedfunctionresource) (Required): Cosmos DB SQL userDefinedFunction resource object

## SqlUserDefinedFunctionResource
### Properties
* **body**: string (WriteOnly): Body of the User Defined Function
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB SQL userDefinedFunction
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TableCreateUpdateProperties
### Properties
* **options**: [CreateUpdateOptions](#createupdateoptions): CreateUpdateOptions are a list of key-value pairs that describe the resource. Supported keys are "If-Match", "If-None-Match", "Session-Token" and "Throughput"
* **resource**: [TableResource](#tableresource) (Required): Cosmos DB table resource object

## TableResource
### Properties
* **clientId**: string (ReadOnly): The client id of user assigned identity.
* **id**: string (Required, WriteOnly): Name of the Cosmos DB table
* **principalId**: string (ReadOnly): The principal id of user assigned identity.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
