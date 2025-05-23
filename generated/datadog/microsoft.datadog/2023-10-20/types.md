# Microsoft.Datadog @ 2023-10-20

## Resource Microsoft.Datadog/agreements@2023-10-20
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2023-10-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [DatadogAgreementProperties](#datadogagreementproperties): Represents the properties of the resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Datadog/agreements' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Datadog/monitors@2023-10-20
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-10-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityProperties](#identityproperties)
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MonitorProperties](#monitorproperties): Properties specific to the monitor resource.
* **sku**: [ResourceSku](#resourcesku)
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [DatadogMonitorResourceTags](#datadogmonitorresourcetags): Dictionary of <string>
* **type**: 'Microsoft.Datadog/monitors' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Datadog/monitors/monitoredSubscriptions@2023-10-20
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-10-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SubscriptionList](#subscriptionlist): The request to update subscriptions needed to be monitored by the Datadog monitor resource.
* **type**: 'Microsoft.Datadog/monitors/monitoredSubscriptions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Datadog/monitors/singleSignOnConfigurations@2023-10-20
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-10-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DatadogSingleSignOnProperties](#datadogsinglesignonproperties)
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Datadog/monitors/singleSignOnConfigurations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Datadog/monitors/tagRules@2023-10-20
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2023-10-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [MonitoringTagRulesProperties](#monitoringtagrulesproperties): Definition of the properties for a TagRules resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.Datadog/monitors/tagRules' (ReadOnly, DeployTimeConstant): The resource type

## Function listApiKeys (Microsoft.Datadog/monitors@2023-10-20)
* **Resource**: Microsoft.Datadog/monitors
* **ApiVersion**: 2023-10-20
* **Output**: [DatadogApiKeyListResponse](#datadogapikeylistresponse)

## Function listHosts (Microsoft.Datadog/monitors@2023-10-20)
* **Resource**: Microsoft.Datadog/monitors
* **ApiVersion**: 2023-10-20
* **Output**: [DatadogHostListResponse](#datadoghostlistresponse)

## Function listLinkedResources (Microsoft.Datadog/monitors@2023-10-20)
* **Resource**: Microsoft.Datadog/monitors
* **ApiVersion**: 2023-10-20
* **Output**: [LinkedResourceListResponse](#linkedresourcelistresponse)

## Function listMonitoredResources (Microsoft.Datadog/monitors@2023-10-20)
* **Resource**: Microsoft.Datadog/monitors
* **ApiVersion**: 2023-10-20
* **Output**: [MonitoredResourceListResponse](#monitoredresourcelistresponse)

## DatadogAgreementProperties
### Properties
* **accepted**: bool: If any version of the terms have been accepted, otherwise false.
* **licenseTextLink**: string: Link to HTML with Microsoft and Publisher terms.
* **plan**: string: Plan identifier string.
* **privacyPolicyLink**: string: Link to the privacy policy of the publisher.
* **product**: string: Product identifier string.
* **publisher**: string: Publisher identifier string.
* **retrieveDatetime**: string: Date and time in UTC of when the terms were accepted. This is empty if Accepted is false.
* **signature**: string: Terms signature.

## DatadogApiKey
### Properties
* **created**: string: The time of creation of the API key.
* **createdBy**: string: The user that created the API key.
* **key**: string (Required): The value of the API key.
* **name**: string: The name of the API key.

## DatadogApiKeyListResponse
### Properties
* **nextLink**: string: Link to the next set of results, if any.
* **value**: [DatadogApiKey](#datadogapikey)[]: Results of a list operation.

## DatadogHost
### Properties
* **aliases**: string[]: The aliases for the host installed via the Datadog agent.
* **apps**: string[]: The Datadog integrations reporting metrics for the host.
* **meta**: [DatadogHostMetadata](#datadoghostmetadata)
* **name**: string: The name of the host.

## DatadogHostListResponse
### Properties
* **nextLink**: string: Link to the next set of results, if any.
* **value**: [DatadogHost](#datadoghost)[]: Results of a list operation.

## DatadogHostMetadata
### Properties
* **agentVersion**: string: The agent version.
* **installMethod**: [DatadogInstallMethod](#datadoginstallmethod)
* **logsAgent**: [DatadogLogsAgent](#datadoglogsagent)

## DatadogInstallMethod
### Properties
* **installerVersion**: string: The installer version.
* **tool**: string: The tool.
* **toolVersion**: string: The tool version.

## DatadogLogsAgent
### Properties
* **transport**: string: The transport.

## DatadogMonitorResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DatadogOrganizationProperties
### Properties
* **apiKey**: string {sensitive} (WriteOnly): Api key associated to the Datadog organization.
* **applicationKey**: string {sensitive} (WriteOnly): Application key associated to the Datadog organization.
* **cspm**: bool: The configuration which describes the state of cloud security posture management. This collects configuration information for all resources in a subscription and track conformance to industry benchmarks.
* **enterpriseAppId**: string (WriteOnly): The Id of the Enterprise App used for Single sign on.
* **id**: string: Id of the Datadog organization.
* **linkingAuthCode**: string {sensitive} (WriteOnly): The auth code used to linking to an existing Datadog organization.
* **linkingClientId**: string {sensitive} (WriteOnly): The client_id from an existing in exchange for an auth token to link organization.
* **name**: string: Name of the Datadog organization.
* **redirectUri**: string (WriteOnly): The redirect URI for linking.

## DatadogSingleSignOnProperties
### Properties
* **enterpriseAppId**: string: The Id of the Enterprise App used for Single sign-on.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Succeeded' | 'Updating' | string (ReadOnly)
* **singleSignOnState**: 'Disable' | 'Enable' | 'Existing' | 'Initial' | string: Various states of the SSO resource
* **singleSignOnUrl**: string (ReadOnly): The login URL specific to this Datadog Organization.

## FilteringTag
### Properties
* **action**: 'Exclude' | 'Include' | string: Valid actions for a filtering tag. Exclusion takes priority over inclusion.
* **name**: string: The name (also known as the key) of the tag.
* **value**: string: The value of the tag.

## IdentityProperties
### Properties
* **principalId**: string (ReadOnly): The identity ID.
* **tenantId**: string (ReadOnly): The tenant ID of resource.
* **type**: 'SystemAssigned' | 'UserAssigned' | string: Specifies the identity type of the Datadog Monitor. At this time the only allowed value is 'SystemAssigned'.

## LinkedResource
### Properties
* **id**: string: The ARM id of the linked resource.
* **location**: string: The location of the linked resource.

## LinkedResourceListResponse
### Properties
* **nextLink**: string: Link to the next set of results, if any.
* **value**: [LinkedResource](#linkedresource)[]: Results of a list operation.

## LogRules
### Properties
* **filteringTags**: [FilteringTag](#filteringtag)[]: List of filtering tags to be used for capturing logs. This only takes effect if SendResourceLogs flag is enabled. If empty, all resources will be captured. If only Exclude action is specified, the rules will apply to the list of all available resources. If Include actions are specified, the rules will only include resources with the associated tags.
* **sendAadLogs**: bool: Flag specifying if AAD logs should be sent for the Monitor resource.
* **sendResourceLogs**: bool: Flag specifying if Azure resource logs should be sent for the Monitor resource.
* **sendSubscriptionLogs**: bool: Flag specifying if Azure subscription logs should be sent for the Monitor resource.

## MetricRules
### Properties
* **filteringTags**: [FilteringTag](#filteringtag)[]: List of filtering tags to be used for capturing metrics. If empty, all resources will be captured. If only Exclude action is specified, the rules will apply to the list of all available resources. If Include actions are specified, the rules will only include resources with the associated tags.

## MonitoredResource
### Properties
* **id**: string: The ARM id of the resource.
* **reasonForLogsStatus**: string: Reason for why the resource is sending logs (or why it is not sending).
* **reasonForMetricsStatus**: string: Reason for why the resource is sending metrics (or why it is not sending).
* **sendingLogs**: bool: Flag indicating if resource is sending logs to Datadog.
* **sendingMetrics**: bool: Flag indicating if resource is sending metrics to Datadog.

## MonitoredResourceListResponse
### Properties
* **nextLink**: string: Link to the next set of results, if any.
* **value**: [MonitoredResource](#monitoredresource)[]: Results of a list operation.

## MonitoredSubscription
### Properties
* **error**: string: The reason of not monitoring the subscription.
* **status**: 'Active' | 'Deleting' | 'Failed' | 'InProgress' | string: The state of monitoring.
* **subscriptionId**: string: The subscriptionId to be monitored.
* **tagRules**: [MonitoringTagRulesProperties](#monitoringtagrulesproperties): Definition of the properties for a TagRules resource.

## MonitoringTagRulesProperties
### Properties
* **automuting**: bool: Configuration to enable/disable auto-muting flag
* **customMetrics**: bool: Configuration to enable/disable custom metrics. If enabled, custom metrics from app insights will be sent.
* **logRules**: [LogRules](#logrules): Set of rules for sending logs for the Monitor resource.
* **metricRules**: [MetricRules](#metricrules): Set of rules for sending metrics for the Monitor resource.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Succeeded' | 'Updating' | string (ReadOnly)

## MonitorProperties
### Properties
* **datadogOrganizationProperties**: [DatadogOrganizationProperties](#datadogorganizationproperties): Specify the Datadog organization name. In the case of linking to existing organizations, Id, ApiKey, and Applicationkey is required as well.
* **liftrResourceCategory**: 'MonitorLogs' | 'Unknown' | string (ReadOnly)
* **liftrResourcePreference**: int (ReadOnly): The priority of the resource.
* **marketplaceSubscriptionStatus**: 'Active' | 'Provisioning' | 'Suspended' | 'Unsubscribed' | string (ReadOnly): Flag specifying the Marketplace Subscription Status of the resource. If payment is not made in time, the resource will go in Suspended state.
* **monitoringStatus**: 'Disabled' | 'Enabled' | string: Flag specifying if the resource monitoring is enabled or disabled.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'NotSpecified' | 'Succeeded' | 'Updating' | string (ReadOnly)
* **userInfo**: [UserInfo](#userinfo): Includes name, email and optionally, phone number. User Information can't be null.

## ResourceSku
### Properties
* **name**: string (Required): Name of the SKU in {PlanId} format. For Terraform, the only allowed value is 'Linked'.

## SubscriptionList
### Properties
* **monitoredSubscriptionList**: [MonitoredSubscription](#monitoredsubscription)[]: List of subscriptions and the state of the monitoring.
* **operation**: 'Active' | 'AddBegin' | 'AddComplete' | 'DeleteBegin' | 'DeleteComplete' | string (WriteOnly): The operation for the patch on the resource.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## UserInfo
*Sensitive*
### Properties
* **emailAddress**: string {pattern: "^[A-Za-z0-9._%+-]+@(?:[A-Za-z0-9-]+\.)+[A-Za-z]{2,}$"}: Email of the user used by Datadog for contacting them if needed
* **name**: string {maxLength: 50}: Name of the user
* **phoneNumber**: string {maxLength: 40}: Phone number of the user used by Datadog for contacting them if needed

