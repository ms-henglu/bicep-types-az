# Microsoft.EventGrid @ 2021-12-01

## Resource Microsoft.EventGrid/domains@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityInfo](#identityinfo): Identity information for the Event Grid Domain resource.
* **location**: string (Required): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DomainProperties](#domainproperties): Properties of the Event Grid Domain resource.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to Domain resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Tags of the resource.
* **type**: 'Microsoft.EventGrid/domains' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/domains/privateEndpointConnections@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of the PrivateEndpointConnection.
* **type**: 'Microsoft.EventGrid/domains/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/domains/topics@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DomainTopicProperties](#domaintopicproperties) (ReadOnly): Properties of the Domain Topic.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to Domain Topic resource.
* **type**: 'Microsoft.EventGrid/domains/topics' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/eventSubscriptions@2021-12-01
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [EventSubscriptionProperties](#eventsubscriptionproperties): Properties of the event subscription.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to Event Subscription resource.
* **type**: 'Microsoft.EventGrid/eventSubscriptions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/extensionTopics@2021-12-01 (ReadOnly)
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ExtensionTopicProperties](#extensiontopicproperties) (ReadOnly): Properties of the extension topic
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to the Extension Topic resource.
* **type**: 'Microsoft.EventGrid/extensionTopics' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/systemTopics@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityInfo](#identityinfo): Identity information for the resource.
* **location**: string (Required): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SystemTopicProperties](#systemtopicproperties): Properties of the system topic.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to System Topic resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Tags of the resource.
* **type**: 'Microsoft.EventGrid/systemTopics' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/systemTopics/eventSubscriptions@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [EventSubscriptionProperties](#eventsubscriptionproperties): Properties of the event subscription.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to Event Subscription resource.
* **type**: 'Microsoft.EventGrid/systemTopics/eventSubscriptions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/topics@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityInfo](#identityinfo): Identity information for the resource.
* **location**: string (Required): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [TopicProperties](#topicproperties): Properties of the topic.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to Topic resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Tags of the resource.
* **type**: 'Microsoft.EventGrid/topics' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/topics/privateEndpointConnections@2021-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of the PrivateEndpointConnection.
* **type**: 'Microsoft.EventGrid/topics/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.EventGrid/topicTypes@2021-12-01 (ReadOnly)
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [TopicTypeProperties](#topictypeproperties) (ReadOnly): Properties of the topic type info
* **type**: 'Microsoft.EventGrid/topicTypes' (ReadOnly, DeployTimeConstant): The resource type

## Function listKeys (Microsoft.EventGrid/domains@2021-12-01)
* **Resource**: Microsoft.EventGrid/domains
* **ApiVersion**: 2021-12-01
* **Output**: [DomainSharedAccessKeys](#domainsharedaccesskeys)

## Function listKeys (Microsoft.EventGrid/topics@2021-12-01)
* **Resource**: Microsoft.EventGrid/topics
* **ApiVersion**: 2021-12-01
* **Output**: [TopicSharedAccessKeys](#topicsharedaccesskeys)

## AdvancedFilter
* **Discriminator**: operatorType

### Base Properties
* **key**: string: The field/property in the event based on which you want to filter.

### BoolEqualsAdvancedFilter
#### Properties
* **operatorType**: 'BoolEquals' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **value**: bool: The boolean filter value.

### IsNotNullAdvancedFilter
#### Properties
* **operatorType**: 'IsNotNull' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.

### IsNullOrUndefinedAdvancedFilter
#### Properties
* **operatorType**: 'IsNullOrUndefined' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.

### NumberGreaterThanAdvancedFilter
#### Properties
* **operatorType**: 'NumberGreaterThan' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **value**: int: The filter value.

### NumberGreaterThanOrEqualsAdvancedFilter
#### Properties
* **operatorType**: 'NumberGreaterThanOrEquals' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **value**: int: The filter value.

### NumberInAdvancedFilter
#### Properties
* **operatorType**: 'NumberIn' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: int[]: The set of filter values.

### NumberInRangeAdvancedFilter
#### Properties
* **operatorType**: 'NumberInRange' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: int[][]: The set of filter values.

### NumberLessThanAdvancedFilter
#### Properties
* **operatorType**: 'NumberLessThan' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **value**: int: The filter value.

### NumberLessThanOrEqualsAdvancedFilter
#### Properties
* **operatorType**: 'NumberLessThanOrEquals' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **value**: int: The filter value.

### NumberNotInAdvancedFilter
#### Properties
* **operatorType**: 'NumberNotIn' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: int[]: The set of filter values.

### NumberNotInRangeAdvancedFilter
#### Properties
* **operatorType**: 'NumberNotInRange' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: int[][]: The set of filter values.

### StringBeginsWithAdvancedFilter
#### Properties
* **operatorType**: 'StringBeginsWith' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringContainsAdvancedFilter
#### Properties
* **operatorType**: 'StringContains' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringEndsWithAdvancedFilter
#### Properties
* **operatorType**: 'StringEndsWith' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringInAdvancedFilter
#### Properties
* **operatorType**: 'StringIn' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringNotBeginsWithAdvancedFilter
#### Properties
* **operatorType**: 'StringNotBeginsWith' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringNotContainsAdvancedFilter
#### Properties
* **operatorType**: 'StringNotContains' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringNotEndsWithAdvancedFilter
#### Properties
* **operatorType**: 'StringNotEndsWith' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.

### StringNotInAdvancedFilter
#### Properties
* **operatorType**: 'StringNotIn' (Required): The operator type used for filtering, e.g., NumberIn, StringContains, BoolEquals and others.
* **values**: string[]: The set of filter values.


## AzureFunctionEventSubscriptionDestinationProperties
### Properties
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **maxEventsPerBatch**: int: Maximum number of events per batch.
* **preferredBatchSizeInKilobytes**: int: Preferred batch size in Kilobytes.
* **resourceId**: string: The Azure Resource Id that represents the endpoint of the Azure Function destination of an event subscription.

## ConnectionState
### Properties
* **actionsRequired**: string: Actions required (if any).
* **description**: string: Description of the connection state.
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' | string: Status of the connection.

## DeadLetterDestination
* **Discriminator**: endpointType

### Base Properties

### StorageBlobDeadLetterDestination
#### Properties
* **endpointType**: 'StorageBlob' (Required): Type of the endpoint for the dead letter destination
* **properties**: [StorageBlobDeadLetterDestinationProperties](#storageblobdeadletterdestinationproperties): The properties of the Storage Blob based deadletter destination


## DeadLetterWithResourceIdentity
### Properties
* **deadLetterDestination**: [DeadLetterDestination](#deadletterdestination): Information about the destination where events have to be delivered for the event subscription.
Uses the managed identity setup on the parent resource (namely, topic or domain) to acquire the authentication tokens being used during delivery / dead-lettering.
* **identity**: [EventSubscriptionIdentity](#eventsubscriptionidentity): The identity to use when dead-lettering events.

## DeliveryAttributeMapping
* **Discriminator**: type

### Base Properties
* **name**: string: Name of the delivery attribute or header.

### DynamicDeliveryAttributeMapping
#### Properties
* **properties**: [DynamicDeliveryAttributeMappingProperties](#dynamicdeliveryattributemappingproperties): Properties of dynamic delivery attribute mapping.
* **type**: 'Dynamic' (Required): Type of the delivery attribute or header name.

### StaticDeliveryAttributeMapping
#### Properties
* **properties**: [StaticDeliveryAttributeMappingProperties](#staticdeliveryattributemappingproperties): Properties of static delivery attribute mapping.
* **type**: 'Static' (Required): Type of the delivery attribute or header name.


## DeliveryWithResourceIdentity
### Properties
* **destination**: [EventSubscriptionDestination](#eventsubscriptiondestination): Information about the destination where events have to be delivered for the event subscription.
Uses Azure Event Grid's identity to acquire the authentication tokens being used during delivery / dead-lettering.
* **identity**: [EventSubscriptionIdentity](#eventsubscriptionidentity): The identity to use when delivering events.

## DomainProperties
### Properties
* **autoCreateTopicWithFirstSubscription**: bool: This Boolean is used to specify the creation mechanism for 'all' the Event Grid Domain Topics associated with this Event Grid Domain resource.
In this context, creation of domain topic can be auto-managed (when true) or self-managed (when false). The default value for this property is true.
When this property is null or set to true, Event Grid is responsible of automatically creating the domain topic when the first event subscription is
created at the scope of the domain topic. If this property is set to false, then creating the first event subscription will require creating a domain topic
by the user. The self-management mode can be used if the user wants full control of when the domain topic is created, while auto-managed mode provides the
flexibility to perform less operations and manage fewer resources by the user. Also, note that in auto-managed creation mode, user is allowed to create the
domain topic on demand if needed.
* **autoDeleteTopicWithLastSubscription**: bool: This Boolean is used to specify the deletion mechanism for 'all' the Event Grid Domain Topics associated with this Event Grid Domain resource.
In this context, deletion of domain topic can be auto-managed (when true) or self-managed (when false). The default value for this property is true.
When this property is set to true, Event Grid is responsible of automatically deleting the domain topic when the last event subscription at the scope
of the domain topic is deleted. If this property is set to false, then the user needs to manually delete the domain topic when it is no longer needed
(e.g., when last event subscription is deleted and the resource needs to be cleaned up). The self-management mode can be used if the user wants full
control of when the domain topic needs to be deleted, while auto-managed mode provides the flexibility to perform less operations and manage fewer
resources by the user.
* **disableLocalAuth**: bool: This boolean is used to enable or disable local auth. Default value is false. When the property is set to true, only AAD token will be used to authenticate if user is allowed to publish to the domain.
* **endpoint**: string (ReadOnly): Endpoint for the domain.
* **inboundIpRules**: [InboundIpRule](#inboundiprule)[]: This can be used to restrict traffic from specific IPs instead of all IPs. Note: These are considered only if PublicNetworkAccess is enabled.
* **inputSchema**: 'CloudEventSchemaV1_0' | 'CustomEventSchema' | 'EventGridSchema' | string: This determines the format that Event Grid should expect for incoming events published to the domain.
* **inputSchemaMapping**: [InputSchemaMapping](#inputschemamapping): Information about the InputSchemaMapping which specified the info about mapping event payload.
* **metricResourceId**: string (ReadOnly): Metric resource id for the domain.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly): List of private endpoint connections.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the Event Grid Domain Resource.
* **publicNetworkAccess**: 'Disabled' | 'Enabled' | string: This determines if traffic is allowed over public network. By default it is enabled. 
You can further restrict to specific IPs by configuring <seealso cref="P:Microsoft.Azure.Events.ResourceProvider.Common.Contracts.DomainProperties.InboundIpRules" />

## DomainSharedAccessKeys
### Properties
* **key1**: string: Shared access key1 for the domain.
* **key2**: string: Shared access key2 for the domain.

## DomainTopicProperties
### Properties
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the domain topic.

## DynamicDeliveryAttributeMappingProperties
### Properties
* **sourceField**: string: JSON path in the event which contains attribute value.

## EventHubEventSubscriptionDestinationProperties
### Properties
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **resourceId**: string: The Azure Resource Id that represents the endpoint of an Event Hub destination of an event subscription.

## EventSubscriptionDestination
* **Discriminator**: endpointType

### Base Properties

### AzureFunctionEventSubscriptionDestination
#### Properties
* **endpointType**: 'AzureFunction' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [AzureFunctionEventSubscriptionDestinationProperties](#azurefunctioneventsubscriptiondestinationproperties): Azure Function Properties of the event subscription destination.

### EventHubEventSubscriptionDestination
#### Properties
* **endpointType**: 'EventHub' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [EventHubEventSubscriptionDestinationProperties](#eventhubeventsubscriptiondestinationproperties): Event Hub Properties of the event subscription destination.

### HybridConnectionEventSubscriptionDestination
#### Properties
* **endpointType**: 'HybridConnection' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [HybridConnectionEventSubscriptionDestinationProperties](#hybridconnectioneventsubscriptiondestinationproperties): Hybrid connection Properties of the event subscription destination.

### ServiceBusQueueEventSubscriptionDestination
#### Properties
* **endpointType**: 'ServiceBusQueue' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [ServiceBusQueueEventSubscriptionDestinationProperties](#servicebusqueueeventsubscriptiondestinationproperties): Service Bus Properties of the event subscription destination.

### ServiceBusTopicEventSubscriptionDestination
#### Properties
* **endpointType**: 'ServiceBusTopic' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [ServiceBusTopicEventSubscriptionDestinationProperties](#servicebustopiceventsubscriptiondestinationproperties): Service Bus Topic Properties of the event subscription destination.

### StorageQueueEventSubscriptionDestination
#### Properties
* **endpointType**: 'StorageQueue' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [StorageQueueEventSubscriptionDestinationProperties](#storagequeueeventsubscriptiondestinationproperties): Storage Queue Properties of the event subscription destination.

### WebHookEventSubscriptionDestination
#### Properties
* **endpointType**: 'WebHook' (Required): Type of the endpoint for the event subscription destination.
* **properties**: [WebHookEventSubscriptionDestinationProperties](#webhookeventsubscriptiondestinationproperties): WebHook Properties of the event subscription destination.


## EventSubscriptionFilter
### Properties
* **advancedFilters**: [AdvancedFilter](#advancedfilter)[]: An array of advanced filters that are used for filtering event subscriptions.
* **enableAdvancedFilteringOnArrays**: bool: Allows advanced filters to be evaluated against an array of values instead of expecting a singular value.
* **includedEventTypes**: string[]: A list of applicable event types that need to be part of the event subscription. If it is desired to subscribe to all default event types, set the IncludedEventTypes to null.
* **isSubjectCaseSensitive**: bool: Specifies if the SubjectBeginsWith and SubjectEndsWith properties of the filter
should be compared in a case sensitive manner.
* **subjectBeginsWith**: string: An optional string to filter events for an event subscription based on a resource path prefix.
The format of this depends on the publisher of the events.
Wildcard characters are not supported in this path.
* **subjectEndsWith**: string: An optional string to filter events for an event subscription based on a resource path suffix.
Wildcard characters are not supported in this path.

## EventSubscriptionIdentity
### Properties
* **type**: 'SystemAssigned' | 'UserAssigned' | string: The type of managed identity used. The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities. The type 'None' will remove any identity.
* **userAssignedIdentity**: string: The user identity associated with the resource.

## EventSubscriptionProperties
### Properties
* **deadLetterDestination**: [DeadLetterDestination](#deadletterdestination): The DeadLetter destination of the event subscription.
* **deadLetterWithResourceIdentity**: [DeadLetterWithResourceIdentity](#deadletterwithresourceidentity): The dead letter destination of the event subscription. Any event that cannot be delivered to its' destination is sent to the dead letter destination.
Uses the managed identity setup on the parent resource (namely, topic or domain) to acquire the authentication tokens being used during delivery / dead-lettering.
* **deliveryWithResourceIdentity**: [DeliveryWithResourceIdentity](#deliverywithresourceidentity): Information about the destination where events have to be delivered for the event subscription.
Uses the managed identity setup on the parent resource (namely, topic or domain) to acquire the authentication tokens being used during delivery / dead-lettering.
* **destination**: [EventSubscriptionDestination](#eventsubscriptiondestination): Information about the destination where events have to be delivered for the event subscription.
* **eventDeliverySchema**: 'CloudEventSchemaV1_0' | 'CustomInputSchema' | 'EventGridSchema' | string: The event delivery schema for the event subscription.
* **expirationTimeUtc**: string: Expiration time of the event subscription.
* **filter**: [EventSubscriptionFilter](#eventsubscriptionfilter): Information about the filter for the event subscription.
* **labels**: string[]: List of user defined labels.
* **provisioningState**: 'AwaitingManualAction' | 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the event subscription.
* **retryPolicy**: [RetryPolicy](#retrypolicy): The retry policy for events. This can be used to configure maximum number of delivery attempts and time to live for events.
* **topic**: string (ReadOnly): Name of the topic of the event subscription.

## ExtensionTopicProperties
### Properties
* **description**: string: Description of the extension topic.
* **systemTopic**: string: System topic resource id which is mapped to the source.

## HybridConnectionEventSubscriptionDestinationProperties
### Properties
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **resourceId**: string: The Azure Resource ID of an hybrid connection that is the destination of an event subscription.

## IdentityInfo
### Properties
* **principalId**: string: The principal ID of resource identity.
* **tenantId**: string: The tenant ID of resource.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned, UserAssigned' | 'UserAssigned' | string: The type of managed identity used. The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities. The type 'None' will remove any identity.
* **userAssignedIdentities**: [IdentityInfoUserAssignedIdentities](#identityinfouserassignedidentities): The list of user identities associated with the resource. The user identity dictionary key references will be ARM resource ids in the form:
'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.
This property is currently not used and reserved for future usage.

## IdentityInfoUserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserIdentityProperties](#useridentityproperties)

## InboundIpRule
### Properties
* **action**: 'Allow' | string: Action to perform based on the match or no match of the IpMask.
* **ipMask**: string: IP Address in CIDR notation e.g., 10.0.0.0/8.

## InputSchemaMapping
* **Discriminator**: inputSchemaMappingType

### Base Properties

### JsonInputSchemaMapping
#### Properties
* **inputSchemaMappingType**: 'Json' (Required): Type of the custom mapping
* **properties**: [JsonInputSchemaMappingProperties](#jsoninputschemamappingproperties): JSON Properties of the input schema mapping


## JsonField
### Properties
* **sourceField**: string: Name of a field in the input event schema that's to be used as the source of a mapping.

## JsonFieldWithDefault
### Properties
* **defaultValue**: string: The default value to be used for mapping when a SourceField is not provided or if there's no property with the specified name in the published JSON event payload.
* **sourceField**: string: Name of a field in the input event schema that's to be used as the source of a mapping.

## JsonInputSchemaMappingProperties
### Properties
* **dataVersion**: [JsonFieldWithDefault](#jsonfieldwithdefault): The mapping information for the DataVersion property of the Event Grid Event.
* **eventTime**: [JsonField](#jsonfield): The mapping information for the EventTime property of the Event Grid Event.
* **eventType**: [JsonFieldWithDefault](#jsonfieldwithdefault): The mapping information for the EventType property of the Event Grid Event.
* **id**: [JsonField](#jsonfield): The mapping information for the Id property of the Event Grid Event.
* **subject**: [JsonFieldWithDefault](#jsonfieldwithdefault): The mapping information for the Subject property of the Event Grid Event.
* **topic**: [JsonField](#jsonfield): The mapping information for the Topic property of the Event Grid Event.

## PrivateEndpoint
### Properties
* **id**: string: The ARM identifier for Private Endpoint.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Fully qualified identifier of the resource.
* **name**: string (ReadOnly): Name of the resource.
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties): Properties of the PrivateEndpointConnection.
* **type**: string (ReadOnly): Type of the resource.

## PrivateEndpointConnectionProperties
### Properties
* **groupIds**: string[]: GroupIds from the private link service resource.
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The Private Endpoint resource for this Connection.
* **privateLinkServiceConnectionState**: [ConnectionState](#connectionstate): Details about the state of the connection.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string: Provisioning state of the Private Endpoint Connection.

## RetryPolicy
### Properties
* **eventTimeToLiveInMinutes**: int: Time To Live (in minutes) for events.
* **maxDeliveryAttempts**: int: Maximum number of delivery retry attempts for events.

## ServiceBusQueueEventSubscriptionDestinationProperties
### Properties
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **resourceId**: string: The Azure Resource Id that represents the endpoint of the Service Bus destination of an event subscription.

## ServiceBusTopicEventSubscriptionDestinationProperties
### Properties
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **resourceId**: string: The Azure Resource Id that represents the endpoint of the Service Bus Topic destination of an event subscription.

## StaticDeliveryAttributeMappingProperties
### Properties
* **isSecret**: bool: Boolean flag to tell if the attribute contains sensitive information .
* **value**: string: Value of the delivery attribute.

## StorageBlobDeadLetterDestinationProperties
### Properties
* **blobContainerName**: string: The name of the Storage blob container that is the destination of the deadletter events
* **resourceId**: string: The Azure Resource ID of the storage account that is the destination of the deadletter events

## StorageQueueEventSubscriptionDestinationProperties
### Properties
* **queueMessageTimeToLiveInSeconds**: int: Storage queue message time to live in seconds.
* **queueName**: string: The name of the Storage queue under a storage account that is the destination of an event subscription.
* **resourceId**: string: The Azure Resource ID of the storage account that contains the queue that is the destination of an event subscription.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## SystemTopicProperties
### Properties
* **metricResourceId**: string (ReadOnly): Metric resource id for the system topic.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the system topic.
* **source**: string: Source for the system topic.
* **topicType**: string: TopicType for the system topic.

## TopicProperties
### Properties
* **disableLocalAuth**: bool: This boolean is used to enable or disable local auth. Default value is false. When the property is set to true, only AAD token will be used to authenticate if user is allowed to publish to the topic.
* **endpoint**: string (ReadOnly): Endpoint for the topic.
* **inboundIpRules**: [InboundIpRule](#inboundiprule)[]: This can be used to restrict traffic from specific IPs instead of all IPs. Note: These are considered only if PublicNetworkAccess is enabled.
* **inputSchema**: 'CloudEventSchemaV1_0' | 'CustomEventSchema' | 'EventGridSchema' | string: This determines the format that Event Grid should expect for incoming events published to the topic.
* **inputSchemaMapping**: [InputSchemaMapping](#inputschemamapping): This enables publishing using custom event schemas. An InputSchemaMapping can be specified to map various properties of a source schema to various required properties of the EventGridEvent schema.
* **metricResourceId**: string (ReadOnly): Metric resource id for the topic.
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[] (ReadOnly)
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the topic.
* **publicNetworkAccess**: 'Disabled' | 'Enabled' | string: This determines if traffic is allowed over public network. By default it is enabled. 
You can further restrict to specific IPs by configuring <seealso cref="P:Microsoft.Azure.Events.ResourceProvider.Common.Contracts.TopicProperties.InboundIpRules" />

## TopicSharedAccessKeys
### Properties
* **key1**: string: Shared access key1 for the topic.
* **key2**: string: Shared access key2 for the topic.

## TopicTypeProperties
### Properties
* **description**: string: Description of the topic type.
* **displayName**: string: Display Name for the topic type.
* **provider**: string: Namespace of the provider of the topic type.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string: Provisioning state of the topic type
* **resourceRegionType**: 'GlobalResource' | 'RegionalResource' | string: Region type of the resource.
* **sourceResourceFormat**: string: Source resource format.
* **supportedLocations**: string[]: List of locations supported by this topic type.
* **supportedScopesForSource**: ('AzureSubscription' | 'Resource' | 'ResourceGroup' | string)[]: Supported source scopes.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## UserIdentityProperties
### Properties
* **clientId**: string: The client id of user assigned identity.
* **principalId**: string: The principal id of user assigned identity.

## WebHookEventSubscriptionDestinationProperties
### Properties
* **azureActiveDirectoryApplicationIdOrUri**: string: The Azure Active Directory Application ID or URI to get the access token that will be included as the bearer token in delivery requests.
* **azureActiveDirectoryTenantId**: string: The Azure Active Directory Tenant ID to get the access token that will be included as the bearer token in delivery requests.
* **deliveryAttributeMappings**: [DeliveryAttributeMapping](#deliveryattributemapping)[]: Delivery attribute details.
* **endpointBaseUrl**: string (ReadOnly): The base URL that represents the endpoint of the destination of an event subscription.
* **endpointUrl**: string {sensitive}: The URL that represents the endpoint of the destination of an event subscription.
* **maxEventsPerBatch**: int: Maximum number of events per batch.
* **preferredBatchSizeInKilobytes**: int: Preferred batch size in Kilobytes.

