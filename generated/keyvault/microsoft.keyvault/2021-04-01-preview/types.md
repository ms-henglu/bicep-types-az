# Microsoft.KeyVault @ 2021-04-01-preview

## Resource Microsoft.KeyVault/managedHSMs@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The supported Azure location where the managed HSM Pool should be created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedHsmProperties](#managedhsmproperties): Properties of the managed HSM Pool
* **sku**: [ManagedHsmSku](#managedhsmsku): SKU details
* **systemData**: [SystemData](#systemdata): Metadata pertaining to creation and last modification of the key vault resource.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Resource tags
* **type**: 'Microsoft.KeyVault/managedHSMs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KeyVault/managedHSMs/privateEndpointConnections@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: Modified whenever there is a change in the state of private endpoint connection.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The supported Azure location where the managed HSM Pool should be created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MHSMPrivateEndpointConnectionProperties](#mhsmprivateendpointconnectionproperties): Properties of the private endpoint connection resource.
* **sku**: [ManagedHsmSku](#managedhsmsku): SKU details
* **systemData**: [SystemData](#systemdata): Metadata pertaining to creation and last modification of the key vault resource.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Resource tags
* **type**: 'Microsoft.KeyVault/managedHSMs/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KeyVault/vaults@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The supported Azure location where the key vault should be created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VaultProperties](#vaultproperties) (Required): Properties of the vault
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the key vault resource.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): The tags that will be assigned to the key vault.
* **type**: 'Microsoft.KeyVault/vaults' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KeyVault/vaults/accessPolicies@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): The resource type of the access policy.
* **name**: 'add' | 'remove' | 'replace' (Required, DeployTimeConstant): The resource name
* **properties**: [VaultAccessPolicyProperties](#vaultaccesspolicyproperties) (Required): Properties of the vault access policy
* **type**: 'Microsoft.KeyVault/vaults/accessPolicies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KeyVault/vaults/privateEndpointConnections@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: Modified whenever there is a change in the state of private endpoint connection.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Azure location of the key vault resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of the private endpoint connection resource.
* **tags**: [Dictionary<string,String>](#dictionarystringstring) (ReadOnly): Tags assigned to the key vault resource.
* **type**: 'Microsoft.KeyVault/vaults/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.KeyVault/vaults/secrets@2021-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Azure location of the key vault resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SecretProperties](#secretproperties) (Required): Properties of the secret
* **tags**: [Dictionary<string,String>](#dictionarystringstring): The tags that will be assigned to the secret.
* **type**: 'Microsoft.KeyVault/vaults/secrets' (ReadOnly, DeployTimeConstant): The resource type

## ManagedHsmProperties
### Properties
* **createMode**: 'default' | 'recover': The create mode to indicate whether the resource is being created or is being recovered from a deleted resource.
* **enablePurgeProtection**: bool: Property specifying whether protection against purge is enabled for this managed HSM pool. Setting this property to true activates protection against purge for this managed HSM pool and its content - only the Managed HSM service may initiate a hard, irrecoverable deletion. The setting is effective only if soft delete is also enabled. Enabling this functionality is irreversible.
* **enableSoftDelete**: bool: Property to specify whether the 'soft delete' functionality is enabled for this managed HSM pool. If it's not set to any value(true or false) when creating new managed HSM pool, it will be set to true by default. Once set to true, it cannot be reverted to false.
* **hsmUri**: string (ReadOnly): The URI of the managed hsm pool for performing operations on keys.
* **initialAdminObjectIds**: string[]: Array of initial administrators object ids for this managed hsm pool.
* **networkAcls**: [MHSMNetworkRuleSet](#mhsmnetworkruleset): A set of rules governing the network accessibility of a managed hsm pool.
* **privateEndpointConnections**: [MHSMPrivateEndpointConnectionItem](#mhsmprivateendpointconnectionitem)[] (ReadOnly): List of private endpoint connections associated with the managed hsm pool.
* **provisioningState**: 'Activated' | 'Deleting' | 'Failed' | 'Provisioning' | 'Restoring' | 'SecurityDomainRestore' | 'Succeeded' | 'Updating' (ReadOnly): Provisioning state.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Control permission for data plane traffic coming from public networks while private endpoint is enabled.
* **scheduledPurgeDate**: string (ReadOnly): The scheduled purge date in UTC.
* **softDeleteRetentionInDays**: int: softDelete data retention days. It accepts >=7 and <=90.
* **statusMessage**: string (ReadOnly): Resource Status Message.
* **tenantId**: string: The Azure Active Directory tenant ID that should be used for authenticating requests to the managed HSM pool.

## MHSMNetworkRuleSet
### Properties
* **bypass**: 'AzureServices' | 'None': Tells what traffic can bypass network rules. This can be 'AzureServices' or 'None'.  If not specified the default is 'AzureServices'.
* **defaultAction**: 'Allow' | 'Deny': The default action when no rule from ipRules and from virtualNetworkRules match. This is only used after the bypass property has been evaluated.
* **ipRules**: [MHSMIPRule](#mhsmiprule)[]: The list of IP address rules.
* **virtualNetworkRules**: [MHSMVirtualNetworkRule](#mhsmvirtualnetworkrule)[]: The list of virtual network rules.

## MHSMIPRule
### Properties
* **value**: string (Required): An IPv4 address range in CIDR notation, such as '124.56.78.91' (simple IP address) or '124.56.78.0/24' (all addresses that start with 124.56.78).

## MHSMVirtualNetworkRule
### Properties
* **id**: string (Required): Full resource id of a vnet subnet, such as '/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/test-vnet/subnets/subnet1'.

## MHSMPrivateEndpointConnectionItem
### Properties
* **properties**: [MHSMPrivateEndpointConnectionProperties](#mhsmprivateendpointconnectionproperties): Properties of the private endpoint connection resource.

## MHSMPrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [MHSMPrivateEndpoint](#mhsmprivateendpoint): Private endpoint object properties.
* **privateLinkServiceConnectionState**: [MHSMPrivateLinkServiceConnectionState](#mhsmprivatelinkserviceconnectionstate): An object that represents the approval state of the private link connection.
* **provisioningState**: 'Creating' | 'Deleting' | 'Disconnected' | 'Failed' | 'Succeeded' | 'Updating': Provisioning state of the private endpoint connection.

## MHSMPrivateEndpoint
### Properties
* **id**: string (ReadOnly): Full identifier of the private endpoint resource.

## MHSMPrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: 'None': A message indicating if changes on the service provider require any updates on the consumer.
* **description**: string: The reason for approval or rejection.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': Indicates whether the connection has been approved, rejected or removed by the key vault owner.

## ManagedHsmSku
### Properties
* **family**: string (Required): SKU Family of the managed HSM Pool
* **name**: 'Custom_B32' | 'Standard_B1' (Required): SKU of the managed HSM Pool.

## SystemData
### Properties
* **createdAt**: string: The timestamp of the key vault resource creation (UTC).
* **createdBy**: string: The identity that created the key vault resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that created the key vault resource.
* **lastModifiedAt**: string: The timestamp of the key vault resource last modification (UTC).
* **lastModifiedBy**: string: The identity that last modified the key vault resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User': The type of identity that last modified the key vault resource.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## VaultProperties
### Properties
* **accessPolicies**: [AccessPolicyEntry](#accesspolicyentry)[]: An array of 0 to 1024 identities that have access to the key vault. All identities in the array must use the same tenant ID as the key vault's tenant ID. When `createMode` is set to `recover`, access policies are not required. Otherwise, access policies are required.
* **createMode**: 'default' | 'recover': The vault's create mode to indicate whether the vault need to be recovered or not.
* **enabledForDeployment**: bool: Property to specify whether Azure Virtual Machines are permitted to retrieve certificates stored as secrets from the key vault.
* **enabledForDiskEncryption**: bool: Property to specify whether Azure Disk Encryption is permitted to retrieve secrets from the vault and unwrap keys.
* **enabledForTemplateDeployment**: bool: Property to specify whether Azure Resource Manager is permitted to retrieve secrets from the key vault.
* **enablePurgeProtection**: bool: Property specifying whether protection against purge is enabled for this vault. Setting this property to true activates protection against purge for this vault and its content - only the Key Vault service may initiate a hard, irrecoverable deletion. The setting is effective only if soft delete is also enabled. Enabling this functionality is irreversible - that is, the property does not accept false as its value.
* **enableRbacAuthorization**: bool: Property that controls how data actions are authorized. When true, the key vault will use Role Based Access Control (RBAC) for authorization of data actions, and the access policies specified in vault properties will be  ignored (warning: this is a preview feature). When false, the key vault will use the access policies specified in vault properties, and any policy stored on Azure Resource Manager will be ignored. If null or not specified, the vault is created with the default value of false. Note that management actions are always authorized with RBAC.
* **enableSoftDelete**: bool: Property to specify whether the 'soft delete' functionality is enabled for this key vault. If it's not set to any value(true or false) when creating new key vault, it will be set to true by default. Once set to true, it cannot be reverted to false.
* **networkAcls**: [NetworkRuleSet](#networkruleset): A set of rules governing the network accessibility of a vault.
* **privateEndpointConnections**: [PrivateEndpointConnectionItem](#privateendpointconnectionitem)[] (ReadOnly): List of private endpoint connections associated with the key vault.
* **provisioningState**: 'RegisteringDns' | 'Succeeded': Provisioning state of the vault.
* **sku**: [Sku](#sku) (Required): SKU details
* **softDeleteRetentionInDays**: int: softDelete data retention days. It accepts >=7 and <=90.
* **tenantId**: string (Required): The Azure Active Directory tenant ID that should be used for authenticating requests to the key vault.
* **vaultUri**: string: The URI of the vault for performing operations on keys and secrets.

## AccessPolicyEntry
### Properties
* **applicationId**: string:  Application ID of the client making request on behalf of a principal
* **objectId**: string (Required): The object ID of a user, service principal or security group in the Azure Active Directory tenant for the vault. The object ID must be unique for the list of access policies.
* **permissions**: [Permissions](#permissions) (Required): Permissions the identity has for keys, secrets, certificates and storage.
* **tenantId**: string (Required): The Azure Active Directory tenant ID that should be used for authenticating requests to the key vault.

## Permissions
### Properties
* **certificates**: 'backup' | 'create' | 'delete' | 'deleteissuers' | 'get' | 'getissuers' | 'import' | 'list' | 'listissuers' | 'managecontacts' | 'manageissuers' | 'purge' | 'recover' | 'restore' | 'setissuers' | 'update'[]: Permissions to certificates
* **keys**: 'backup' | 'create' | 'decrypt' | 'delete' | 'encrypt' | 'get' | 'import' | 'list' | 'purge' | 'recover' | 'restore' | 'sign' | 'unwrapKey' | 'update' | 'verify' | 'wrapKey'[]: Permissions to keys
* **secrets**: 'backup' | 'delete' | 'get' | 'list' | 'purge' | 'recover' | 'restore' | 'set'[]: Permissions to secrets
* **storage**: 'backup' | 'delete' | 'deletesas' | 'get' | 'getsas' | 'list' | 'listsas' | 'purge' | 'recover' | 'regeneratekey' | 'restore' | 'set' | 'setsas' | 'update'[]: Permissions to storage accounts

## NetworkRuleSet
### Properties
* **bypass**: 'AzureServices' | 'None': Tells what traffic can bypass network rules. This can be 'AzureServices' or 'None'.  If not specified the default is 'AzureServices'.
* **defaultAction**: 'Allow' | 'Deny': The default action when no rule from ipRules and from virtualNetworkRules match. This is only used after the bypass property has been evaluated.
* **ipRules**: [IPRule](#iprule)[]: The list of IP address rules.
* **virtualNetworkRules**: [VirtualNetworkRule](#virtualnetworkrule)[]: The list of virtual network rules.

## IPRule
### Properties
* **value**: string (Required): An IPv4 address range in CIDR notation, such as '124.56.78.91' (simple IP address) or '124.56.78.0/24' (all addresses that start with 124.56.78).

## VirtualNetworkRule
### Properties
* **id**: string (Required): Full resource id of a vnet subnet, such as '/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/test-vnet/subnets/subnet1'.

## PrivateEndpointConnectionItem
### Properties
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of the private endpoint connection resource.

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): Private endpoint object properties.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate): An object that represents the approval state of the private link connection.
* **provisioningState**: 'Creating' | 'Deleting' | 'Disconnected' | 'Failed' | 'Succeeded' | 'Updating': Provisioning state of the private endpoint connection.

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly): Full identifier of the private endpoint resource.

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: 'None': A message indicating if changes on the service provider require any updates on the consumer.
* **description**: string: The reason for approval or rejection.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected': Indicates whether the connection has been approved, rejected or removed by the key vault owner.

## Sku
### Properties
* **family**: string (Required): SKU family name
* **name**: 'premium' | 'standard' (Required): SKU name to specify whether the key vault is a standard vault or a premium vault.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## VaultAccessPolicyProperties
### Properties
* **accessPolicies**: [AccessPolicyEntry](#accesspolicyentry)[] (Required): An array of 0 to 16 identities that have access to the key vault. All identities in the array must use the same tenant ID as the key vault's tenant ID.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SecretProperties
### Properties
* **attributes**: [SecretAttributes](#secretattributes): The secret management attributes.
* **contentType**: string: The content type of the secret.
* **secretUri**: string (ReadOnly): The URI to retrieve the current version of the secret.
* **secretUriWithVersion**: string (ReadOnly): The URI to retrieve the specific version of the secret.
* **value**: string: The value of the secret. NOTE: 'value' will never be returned from the service, as APIs using this model are is intended for internal use in ARM deployments. Users should use the data-plane REST service for interaction with vault secrets.

## SecretAttributes
### Properties
* **created**: int (ReadOnly): Creation time in seconds since 1970-01-01T00:00:00Z.
* **enabled**: bool: Determines whether the object is enabled.
* **exp**: int: Expiry date in seconds since 1970-01-01T00:00:00Z.
* **nbf**: int: Not before date in seconds since 1970-01-01T00:00:00Z.
* **updated**: int (ReadOnly): Last updated time in seconds since 1970-01-01T00:00:00Z.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
