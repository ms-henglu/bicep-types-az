# Microsoft.Solutions @ 2020-08-21-preview

## Resource Microsoft.Solutions/applicationDefinitions@2020-08-21-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-08-21-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location
* **managedBy**: string: ID of the resource that manages this resource.
* **name**: string {minLength: 3, maxLength: 64} (Required, DeployTimeConstant): The resource name
* **properties**: [ApplicationDefinitionProperties](#applicationdefinitionproperties) (Required): The managed application definition properties.
* **sku**: [Sku](#sku): The SKU of the resource.
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.Solutions/applicationDefinitions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Solutions/applications@2020-08-21-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-08-21-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [Identity](#identity): The identity of the resource.
* **kind**: string {pattern: "^[-\w\._,\(\)]+$"} (Required): The kind of the managed application. Allowed values are MarketPlace and ServiceCatalog.
* **location**: string: Resource location
* **managedBy**: string: ID of the resource that manages this resource.
* **name**: string {minLength: 3, maxLength: 64} (Required, DeployTimeConstant): The resource name
* **plan**: [Plan](#plan): The plan information.
* **properties**: [ApplicationProperties](#applicationproperties) (Required): The managed application properties.
* **sku**: [Sku](#sku): The SKU of the resource.
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.Solutions/applications' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Solutions/jitRequests@2020-08-21-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-08-21-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [JitRequestProperties](#jitrequestproperties): The JIT request properties.
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.Solutions/jitRequests' (ReadOnly, DeployTimeConstant): The resource type

## ApplicationArtifact
### Properties
* **name**: 'Authorizations' | 'CustomRoleDefinition' | 'NotSpecified' | 'ViewDefinition' | string (Required): The managed application artifact name.
* **type**: 'Custom' | 'NotSpecified' | 'Template' (Required): The managed application artifact type.
* **uri**: string (Required): The managed application artifact blob uri.

## ApplicationAuthorization
### Properties
* **principalId**: string (Required): The provider's principal identifier. This is the identity that the provider will use to call ARM to manage the managed application resources.
* **roleDefinitionId**: string (Required): The provider's role definition identifier. This role will define all the permissions that the provider must have on the managed application's container resource group. This role definition cannot have permission to delete the resource group.

## ApplicationBillingDetailsDefinition
### Properties
* **resourceUsageId**: string: The managed application resource usage Id.

## ApplicationClientDetails
### Properties
* **applicationId**: string: The client application Id.
* **oid**: string: The client Oid.
* **puid**: string: The client Puid

## ApplicationDefinitionArtifact
### Properties
* **name**: 'ApplicationResourceTemplate' | 'CreateUiDefinition' | 'MainTemplateParameters' | 'NotSpecified' | string (Required): The managed application definition artifact name.
* **type**: 'Custom' | 'NotSpecified' | 'Template' (Required): The managed application definition artifact type.
* **uri**: string (Required): The managed application definition artifact blob uri.

## ApplicationDefinitionProperties
### Properties
* **artifacts**: [ApplicationDefinitionArtifact](#applicationdefinitionartifact)[]: The collection of managed application artifacts. The portal will use the files specified as artifacts to construct the user experience of creating a managed application from a managed application definition.
* **authorizations**: [ApplicationAuthorization](#applicationauthorization)[]: The managed application provider authorizations.
* **createUiDefinition**: any: The createUiDefinition json for the backing template with Microsoft.Solutions/applications resource. It can be a JObject or well-formed JSON string.
* **deploymentPolicy**: [ApplicationDeploymentPolicy](#applicationdeploymentpolicy): The managed application deployment policy.
* **description**: string: The managed application definition description.
* **displayName**: string: The managed application definition display name.
* **isEnabled**: bool: A value indicating whether the package is enabled or not.
* **lockingPolicy**: [ApplicationPackageLockingPolicyDefinition](#applicationpackagelockingpolicydefinition): The managed application locking policy.
* **lockLevel**: 'CanNotDelete' | 'None' | 'ReadOnly' (Required): The managed application lock level.
* **mainTemplate**: any: The inline main template json which has resources to be provisioned. It can be a JObject or well-formed JSON string.
* **managementPolicy**: [ApplicationManagementPolicy](#applicationmanagementpolicy): The managed application management policy that determines publisher's access to the managed resource group.
* **notificationPolicy**: [ApplicationNotificationPolicy](#applicationnotificationpolicy): The managed application notification policy.
* **packageFileUri**: string: The managed application definition package file Uri. Use this element
* **policies**: [ApplicationPolicy](#applicationpolicy)[]: The managed application provider policies.
* **storageAccountId**: string: The storage account id for bring your own storage scenario.

## ApplicationDeploymentPolicy
### Properties
* **deploymentMode**: 'Complete' | 'Incremental' | 'NotSpecified' | string (Required): The managed application deployment mode.

## ApplicationJitAccessPolicy
### Properties
* **jitAccessEnabled**: bool (Required): Whether the JIT access is enabled.
* **jitApprovalMode**: 'AutoApprove' | 'ManualApprove' | 'NotSpecified' | string: JIT approval mode.
* **jitApprovers**: [JitApproverDefinition](#jitapproverdefinition)[]: The JIT approvers
* **maximumJitAccessDuration**: string: The maximum duration JIT access is granted. This is an ISO8601 time period value.

## ApplicationManagementPolicy
### Properties
* **mode**: 'Managed' | 'NotSpecified' | 'Unmanaged' | string: The managed application management mode.

## ApplicationNotificationEndpoint
### Properties
* **uri**: string (Required): The managed application notification endpoint uri.

## ApplicationNotificationPolicy
### Properties
* **notificationEndpoints**: [ApplicationNotificationEndpoint](#applicationnotificationendpoint)[] (Required): The managed application notification endpoint.

## ApplicationPackageContact
### Properties
* **contactName**: string: The contact name.
* **email**: string (Required): The contact email.
* **phone**: string (Required): The contact phone number.

## ApplicationPackageLockingPolicyDefinition
### Properties
* **allowedActions**: string[]: The deny assignment excluded actions.
* **allowedDataActions**: string[]: The deny assignment excluded data actions.

## ApplicationPackageSupportUrls
### Properties
* **governmentCloud**: string: The government cloud support URL.
* **publicAzure**: string: The public azure support URL.

## ApplicationPolicy
### Properties
* **name**: string: The policy name
* **parameters**: string: The policy parameters.
* **policyDefinitionId**: string: The policy definition Id.

## ApplicationProperties
### Properties
* **applicationDefinitionId**: string: The fully qualified path of managed application definition Id.
* **artifacts**: [ApplicationArtifact](#applicationartifact)[] (ReadOnly): The collection of managed application artifacts.
* **authorizations**: [ApplicationAuthorization](#applicationauthorization)[] (ReadOnly): The  read-only authorizations property that is retrieved from the application package.
* **billingDetails**: [ApplicationBillingDetailsDefinition](#applicationbillingdetailsdefinition) (ReadOnly): The managed application billing details.
* **createdBy**: [ApplicationClientDetails](#applicationclientdetails) (ReadOnly): The client entity that created the JIT request.
* **customerSupport**: [ApplicationPackageContact](#applicationpackagecontact) (ReadOnly): The read-only customer support property that is retrieved from the application package.
* **jitAccessPolicy**: [ApplicationJitAccessPolicy](#applicationjitaccesspolicy): The managed application Jit access policy.
* **managedResourceGroupId**: string: The managed resource group Id.
* **managementMode**: 'Managed' | 'NotSpecified' | 'Unmanaged' | string (ReadOnly): The managed application management mode.
* **outputs**: any (ReadOnly): Name and value pairs that define the managed application outputs.
* **parameters**: any: Name and value pairs that define the managed application parameters. It can be a JObject or a well formed JSON string.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Ready' | 'Running' | 'Succeeded' | 'Updating' | string (ReadOnly): The managed application provisioning state.
* **publisherTenantId**: string (ReadOnly): The publisher tenant Id.
* **supportUrls**: [ApplicationPackageSupportUrls](#applicationpackagesupporturls) (ReadOnly): The read-only support URLs property that is retrieved from the application package.
* **updatedBy**: [ApplicationClientDetails](#applicationclientdetails) (ReadOnly): The client entity that last updated the JIT request.

## Identity
### Properties
* **principalId**: string (ReadOnly): The principal ID of resource identity.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned': The identity type.
* **userAssignedIdentities**: [IdentityUserAssignedIdentities](#identityuserassignedidentities): The list of user identities associated with the resource. The user identity dictionary key references will be resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.

## IdentityUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserAssignedResourceIdentity](#userassignedresourceidentity)

## JitApproverDefinition
### Properties
* **displayName**: string: The approver display name.
* **id**: string (Required): The approver service principal Id.
* **type**: 'group' | 'user' | string: The approver type.

## JitAuthorizationPolicies
### Properties
* **principalId**: string (Required): The the principal id that will be granted JIT access.
* **roleDefinitionId**: string (Required): The role definition id that will be granted to the Principal.

## JitRequestProperties
### Properties
* **applicationResourceId**: string (Required): The parent application id.
* **createdBy**: [ApplicationClientDetails](#applicationclientdetails) (ReadOnly): The client entity that created the JIT request.
* **jitAuthorizationPolicies**: [JitAuthorizationPolicies](#jitauthorizationpolicies)[] (Required): The JIT authorization policies.
* **jitRequestState**: 'Approved' | 'Canceled' | 'Denied' | 'Expired' | 'Failed' | 'NotSpecified' | 'Pending' | 'Timeout' | string (ReadOnly): The JIT request state.
* **jitSchedulingPolicy**: [JitSchedulingPolicy](#jitschedulingpolicy) (Required): The JIT request properties.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Created' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Ready' | 'Running' | 'Succeeded' | 'Updating' | string (ReadOnly): The JIT request provisioning state.
* **publisherTenantId**: string (ReadOnly): The publisher tenant id.
* **updatedBy**: [ApplicationClientDetails](#applicationclientdetails) (ReadOnly): The client entity that last updated the JIT request.

## JitSchedulingPolicy
### Properties
* **duration**: string (Required): The required duration of the JIT request.
* **startTime**: string (Required): The start time of the request.
* **type**: 'NotSpecified' | 'Once' | 'Recurring' | string (Required, ReadOnly): The type of JIT schedule.

## Plan
### Properties
* **name**: string (Required): The plan name.
* **product**: string (Required): The product code.
* **promotionCode**: string: The promotion code.
* **publisher**: string (Required): The publisher ID.
* **version**: string (Required): The plan's version.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Sku
### Properties
* **capacity**: int: The SKU capacity.
* **family**: string: The SKU family.
* **model**: string: The SKU model.
* **name**: string (Required): The SKU name.
* **size**: string: The SKU size.
* **tier**: string: The SKU tier.

## UserAssignedResourceIdentity
### Properties
* **principalId**: string (ReadOnly): The principal id of user assigned identity.
* **tenantId**: string (ReadOnly): The tenant id of user assigned identity.

