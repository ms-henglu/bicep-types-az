# Microsoft.Cache @ 2021-03-01

## Resource Microsoft.Cache/redisEnterprise@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant)
* **id**: string (ReadOnly, DeployTimeConstant)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: [ClusterProperties](#clusterproperties)
* **sku**: [Sku](#sku) (Required)
* **tags**: [Dictionary<string,String>](#dictionarystringstring)
* **type**: 'Microsoft.Cache/redisEnterprise' (ReadOnly, DeployTimeConstant)
* **zones**: string[]

## Resource Microsoft.Cache/redisEnterprise/databases@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: [DatabaseProperties](#databaseproperties)
* **type**: 'Microsoft.Cache/redisEnterprise/databases' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.Cache/redisEnterprise/privateEndpointConnections@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant)
* **id**: string (ReadOnly, DeployTimeConstant)
* **name**: string (Required, DeployTimeConstant)
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties)
* **type**: 'Microsoft.Cache/redisEnterprise/privateEndpointConnections' (ReadOnly, DeployTimeConstant)

## ClusterProperties
### Properties
* **hostName**: string (ReadOnly)
* **minimumTlsVersion**: '1.0' | '1.1' | '1.2'
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly)
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly)
* **redisVersion**: string (ReadOnly)
* **resourceState**: 'CreateFailed' | 'Creating' | 'DeleteFailed' | 'Deleting' | 'Disabled' | 'DisableFailed' | 'Disabling' | 'EnableFailed' | 'Enabling' | 'Running' | 'UpdateFailed' | 'Updating' (ReadOnly)

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly)
* **name**: string (ReadOnly)
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties)
* **type**: string (ReadOnly)

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint)
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate) (Required)
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded'

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly)

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string
* **description**: string
* **status**: 'Approved' | 'Pending' | 'Rejected'

## Sku
### Properties
* **capacity**: int
* **name**: 'Enterprise_E10' | 'Enterprise_E100' | 'Enterprise_E20' | 'Enterprise_E50' | 'EnterpriseFlash_F1500' | 'EnterpriseFlash_F300' | 'EnterpriseFlash_F700' (Required)

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DatabaseProperties
### Properties
* **clientProtocol**: 'Encrypted' | 'Plaintext'
* **clusteringPolicy**: 'EnterpriseCluster' | 'OSSCluster'
* **evictionPolicy**: 'AllKeysLFU' | 'AllKeysLRU' | 'AllKeysRandom' | 'NoEviction' | 'VolatileLFU' | 'VolatileLRU' | 'VolatileRandom' | 'VolatileTTL'
* **modules**: [Module](#module)[]
* **persistence**: [Persistence](#persistence)
* **port**: int
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' (ReadOnly)
* **resourceState**: 'CreateFailed' | 'Creating' | 'DeleteFailed' | 'Deleting' | 'Disabled' | 'DisableFailed' | 'Disabling' | 'EnableFailed' | 'Enabling' | 'Running' | 'UpdateFailed' | 'Updating' (ReadOnly)

## Module
### Properties
* **args**: string
* **name**: string (Required)
* **version**: string (ReadOnly)

## Persistence
### Properties
* **aofEnabled**: bool
* **aofFrequency**: '1s' | 'always'
* **rdbEnabled**: bool
* **rdbFrequency**: '12h' | '1h' | '6h'
