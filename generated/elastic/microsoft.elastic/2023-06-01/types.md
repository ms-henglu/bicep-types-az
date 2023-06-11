# Microsoft.Elastic @ 2023-06-01

## Resource Microsoft.Elastic/monitors@2023-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityProperties](#identityproperties): Identity properties of the monitor resource.
* **location**: string (Required): The location of the monitor resource
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MonitorProperties](#monitorproperties): Properties of the monitor resource.
* **sku**: [ResourceSku](#resourcesku): SKU of the monitor resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource
* **tags**: [ElasticMonitorResourceTags](#elasticmonitorresourcetags): The tags of the monitor resource.
* **type**: 'Microsoft.Elastic/monitors' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Elastic/monitors/tagRules@2023-06-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MonitoringTagRulesProperties](#monitoringtagrulesproperties): Properties of the monitoring tag rules.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource
* **type**: 'Microsoft.Elastic/monitors/tagRules' (ReadOnly, DeployTimeConstant): The resource type

## Function associateTrafficFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function createAndAssociateIPFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function createAndAssociatePLFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function createOrUpdateExternalUser (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Input**: [ExternalUserInfo](#externaluserinfo)
* **Output**: [ExternalUserCreationResponse](#externalusercreationresponse)

## Function deleteTrafficFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function detachAndDeleteTrafficFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function detachTrafficFilter (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01

## Function listAllTrafficFilters (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [ElasticTrafficFilterResponse](#elastictrafficfilterresponse)

## Function listAssociatedTrafficFilters (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [ElasticTrafficFilterResponse](#elastictrafficfilterresponse)

## Function listDeploymentInfo (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [DeploymentInfoResponse](#deploymentinforesponse)

## Function listMonitoredResources (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [MonitoredResourceListResponse](#monitoredresourcelistresponse)

## Function listUpgradableVersions (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [UpgradableVersionsList](#upgradableversionslist)

## Function listVMHost (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [VMHostListResponse](#vmhostlistresponse)

## Function upgrade (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Input**: [ElasticMonitorUpgrade](#elasticmonitorupgrade)

## Function vmCollectionUpdate (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Input**: [VMCollectionUpdate](#vmcollectionupdate)

## Function vmIngestionDetails (Microsoft.Elastic/monitors@2023-06-01)
* **Resource**: Microsoft.Elastic/monitors
* **ApiVersion**: 2023-06-01
* **Output**: [VMIngestionDetailsResponse](#vmingestiondetailsresponse)

## CompanyInfo
### Properties
* **business**: string: Business of the company
* **country**: string: Country of the company location.
* **domain**: string: Domain of the company
* **employeesNumber**: string: Number of employees in the company
* **state**: string: State of the company location.

## DeploymentInfoResponse
### Properties
* **deploymentUrl**: string (ReadOnly): Deployment URL of the elasticsearch in Elastic cloud deployment.
* **diskCapacity**: string (ReadOnly): Disk capacity of the elasticsearch in Elastic cloud deployment.
* **marketplaceSaasInfo**: [MarketplaceSaaSInfo](#marketplacesaasinfo) (ReadOnly): Marketplace SaaS Info of the resource.
* **memoryCapacity**: string (ReadOnly): RAM capacity of the elasticsearch in Elastic cloud deployment.
* **status**: 'Healthy' | 'Unhealthy' | string (ReadOnly): The Elastic deployment status.
* **version**: string (ReadOnly): Version of the elasticsearch in Elastic cloud deployment.

## ElasticCloudDeployment
### Properties
* **azureSubscriptionId**: string (ReadOnly): Associated Azure subscription Id for the elastic deployment.
* **deploymentId**: string (ReadOnly): Elastic deployment Id
* **elasticsearchRegion**: string (ReadOnly): Region where Deployment at Elastic side took place.
* **elasticsearchServiceUrl**: string (ReadOnly): Elasticsearch ingestion endpoint of the Elastic deployment.
* **kibanaServiceUrl**: string (ReadOnly): Kibana endpoint of the Elastic deployment.
* **kibanaSsoUrl**: string (ReadOnly): Kibana dashboard sso URL of the Elastic deployment.
* **name**: string (ReadOnly): Elastic deployment name

## ElasticCloudUser
### Properties
* **elasticCloudSsoDefaultUrl**: string (ReadOnly): Elastic cloud default dashboard sso URL of the Elastic user account.
* **emailAddress**: string (ReadOnly): Email of the Elastic User Account.
* **id**: string (ReadOnly): User Id of the elastic account of the User.

## ElasticMonitorResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ElasticMonitorUpgrade
### Properties
* **version**: string: Version to which the elastic monitor should be upgraded to

## ElasticProperties
### Properties
* **elasticCloudDeployment**: [ElasticCloudDeployment](#elasticclouddeployment): Details of the elastic cloud deployment.
* **elasticCloudUser**: [ElasticCloudUser](#elasticclouduser): Details of the user's elastic account.

## ElasticTrafficFilter
### Properties
* **description**: string: Description of the elastic filter
* **id**: string: Id of the elastic filter
* **includeByDefault**: bool: IncludeByDefault for the elastic filter
* **name**: string: Name of the elastic filter
* **region**: string: Region of the elastic filter
* **rules**: [ElasticTrafficFilterRule](#elastictrafficfilterrule)[]: Rules in the elastic filter
* **type**: 'azure_private_endpoint' | 'ip' | string: Type of the elastic filter

## ElasticTrafficFilterResponse
### Properties
* **rulesets**: [ElasticTrafficFilter](#elastictrafficfilter)[]: List of elastic traffic filters in the account

## ElasticTrafficFilterResponse
### Properties
* **rulesets**: [ElasticTrafficFilter](#elastictrafficfilter)[]: List of elastic traffic filters in the account

## ElasticTrafficFilterRule
### Properties
* **azureEndpointGuid**: string: Guid of Private Endpoint in the elastic filter rule
* **azureEndpointName**: string: Name of the Private Endpoint in the elastic filter rule
* **description**: string: Description of the elastic filter rule
* **id**: string: Id of the elastic filter rule
* **source**: string: IP of the elastic filter rule

## ExternalUserCreationResponse
### Properties
* **created**: bool (ReadOnly): Shows if user is created or updated

## ExternalUserInfo
### Properties
* **emailId**: string: Email id of the user to be created or updated
* **fullName**: string: Full name of the user to be created or updated
* **password**: string: Password of the user to be created or updated
* **roles**: string[]: Roles to be assigned for  created or updated user
* **userName**: string: Username of the user to be created or updated

## FilteringTag
### Properties
* **action**: 'Exclude' | 'Include' | string: Valid actions for a filtering tag.
* **name**: string: The name (also known as the key) of the tag.
* **value**: string: The value of the tag.

## IdentityProperties
### Properties
* **principalId**: string (ReadOnly): The identity ID.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned' | string: Managed identity type.

## LogRules
### Properties
* **filteringTags**: [FilteringTag](#filteringtag)[]: List of filtering tags to be used for capturing logs. This only takes effect if SendActivityLogs flag is enabled. If empty, all resources will be captured. If only Exclude action is specified, the rules will apply to the list of all available resources. If Include actions are specified, the rules will only include resources with the associated tags.
* **sendAadLogs**: bool: Flag specifying if AAD logs should be sent for the Monitor resource.
* **sendActivityLogs**: bool: Flag specifying if activity logs from Azure resources should be sent for the Monitor resource.
* **sendSubscriptionLogs**: bool: Flag specifying if subscription logs should be sent for the Monitor resource.

## MarketplaceSaaSInfo
### Properties
* **marketplaceName**: string: Marketplace Subscription Details: SAAS Name
* **marketplaceResourceId**: string: Marketplace Subscription Details: Resource URI
* **marketplaceStatus**: string: Marketplace Subscription Details: SaaS Subscription Status
* **marketplaceSubscription**: [MarketplaceSaaSInfoMarketplaceSubscription](#marketplacesaasinfomarketplacesubscription): Marketplace Subscription

## MarketplaceSaaSInfoMarketplaceSubscription
### Properties
* **id**: string: Marketplace Subscription Id. This is a GUID-formatted string.

## MonitoredResource
### Properties
* **id**: string: The ARM id of the resource.
* **reasonForLogsStatus**: string: Reason for why the resource is sending logs (or why it is not sending).
* **sendingLogs**: 'False' | 'True' | string: Flag indicating the status of the resource for sending logs operation to Elastic.

## MonitoredResourceListResponse
### Properties
* **nextLink**: string: Link to the next set of results, if any.
* **value**: [MonitoredResource](#monitoredresource)[]: Results of a list operation.

## MonitoringTagRulesProperties
### Properties
* **logRules**: [LogRules](#logrules): Rules for sending logs.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Succeeded' | 'Updating' | string: Provisioning state of the monitoring tag rules.

## MonitorProperties
### Properties
* **elasticProperties**: [ElasticProperties](#elasticproperties): Elastic cloud properties.
* **generateApiKey**: bool: Flag to determine if User API Key has to be generated and shared.
* **liftrResourceCategory**: 'MonitorLogs' | 'Unknown' | string (ReadOnly)
* **liftrResourcePreference**: int (ReadOnly): The priority of the resource.
* **monitoringStatus**: 'Disabled' | 'Enabled' | string: Flag specifying if the resource monitoring is enabled or disabled.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Succeeded' | 'Updating' | string: Provisioning state of the monitor resource.
* **userInfo**: [UserInfo](#userinfo) (WriteOnly): User information.
* **version**: string: Version of elastic of the monitor resource

## ResourceSku
### Properties
* **name**: string (Required): Name of the SKU.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## UpgradableVersionsList
### Properties
* **currentVersion**: string: Current version of the elastic monitor
* **upgradableVersions**: string[]: Stack Versions that this version can upgrade to

## UserInfo
### Properties
* **companyInfo**: [CompanyInfo](#companyinfo): Company information of the user to be passed to partners.
* **companyName**: string: Company name of the user
* **emailAddress**: string: Email of the user used by Elastic for contacting them if needed
* **firstName**: string: First name of the user
* **lastName**: string: Last name of the user

## VMCollectionUpdate
### Properties
* **operationName**: 'Add' | 'Delete' | string: Operation to be performed for given VM.
* **vmResourceId**: string: ARM id of the VM resource.

## VMHostListResponse
### Properties
* **nextLink**: string: Link to the next Vm resource Id, if any.
* **value**: [VMResources](#vmresources)[]: Results of a list operation.

## VMIngestionDetailsResponse
### Properties
* **cloudId**: string: The cloudId of given Elastic monitor resource.
* **ingestionKey**: string: Ingestion details to install agent on given VM.

## VMResources
### Properties
* **vmResourceId**: string: The ARM id of the VM resource.

