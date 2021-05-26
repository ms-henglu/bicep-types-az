# Microsoft.Devices @ 2021-03-03-preview

## Resource Microsoft.Devices/IotHubs@2021-03-03-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-03-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: The Etag field is *not* required. If it is provided in the response body, it must also be provided as a header per the normal ETag convention.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ArmIdentity](#armidentity)
* **location**: string (Required): The resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [IotHubProperties](#iothubproperties): The properties of an IoT hub.
* **sku**: [IotHubSkuInfo](#iothubskuinfo) (Required): Information about the SKU of the IoT hub.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): The resource tags.
* **type**: 'Microsoft.Devices/IotHubs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Devices/IotHubs/certificates@2021-03-03-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-03-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): The entity tag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateProperties](#certificateproperties): The description of an X509 CA Certificate.
* **type**: 'Microsoft.Devices/IotHubs/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Devices/IotHubs/eventHubEndpoints/ConsumerGroups@2021-03-03-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-03-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string (ReadOnly): The etag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [EventHubConsumerGroupName](#eventhubconsumergroupname): The EventHub consumer group name.
* **type**: 'Microsoft.Devices/IotHubs/eventHubEndpoints/ConsumerGroups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Devices/iotHubs/privateEndpointConnections@2021-03-03-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-03-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties) (Required): The properties of a private endpoint connection
* **type**: 'Microsoft.Devices/iotHubs/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## ArmIdentity
### Properties
* **principalId**: string (ReadOnly): Principal Id
* **tenantId**: string (ReadOnly): Tenant Id
* **type**: 'None' | 'SystemAssigned, UserAssigned' | 'SystemAssigned' | 'UserAssigned': The type of identity used for the resource. The type 'SystemAssigned,UserAssigned' includes both an implicitly created identity and a set of user assigned identities. The type 'None' will remove any identities from the service.
* **userAssignedIdentities**: [Dictionary<string,ArmUserIdentity>](#dictionarystringarmuseridentity)

## Dictionary<string,ArmUserIdentity>
### Properties
### Additional Properties
* **Additional Properties Type**: [ArmUserIdentity](#armuseridentity)

## ArmUserIdentity
### Properties
* **clientId**: string (ReadOnly)
* **principalId**: string (ReadOnly)

## IotHubProperties
### Properties
* **authorizationPolicies**: [SharedAccessSignatureAuthorizationRule](#sharedaccesssignatureauthorizationrule)[]: The shared access policies you can use to secure a connection to the IoT hub.
* **cloudToDevice**: [CloudToDeviceProperties](#cloudtodeviceproperties): The IoT hub cloud-to-device messaging properties.
* **comments**: string: IoT hub comments.
* **deviceStreams**: [schemas:8_deviceStreams](#schemas8devicestreams): The device streams properties of iothub.
* **enableFileUploadNotifications**: bool: If True, file upload notifications are enabled.
* **encryption**: [EncryptionPropertiesDescription](#encryptionpropertiesdescription): The encryption properties for the IoT hub.
* **eventHubEndpoints**: [Dictionary<string,EventHubProperties>](#dictionarystringeventhubproperties): The Event Hub-compatible endpoint properties. The only possible keys to this dictionary is events. This key has to be present in the dictionary while making create or update calls for the IoT hub.
* **features**: 'DeviceManagement' | 'None': The capabilities and features enabled for the IoT hub.
* **hostName**: string (ReadOnly): The name of the host.
* **ipFilterRules**: [IpFilterRule](#ipfilterrule)[]: The IP filter rules.
* **locations**: [IotHubLocationDescription](#iothublocationdescription)[] (ReadOnly): Primary and secondary location for iot hub
* **messagingEndpoints**: [Dictionary<string,MessagingEndpointProperties>](#dictionarystringmessagingendpointproperties): The messaging endpoint properties for the file upload notification queue.
* **minTlsVersion**: string: Specifies the minimum TLS version to support for this hub. Can be set to "1.2" to have clients that use a TLS version below 1.2 to be rejected.
* **networkRuleSets**: [NetworkRuleSetProperties](#networkrulesetproperties): Network Rule Set Properties of IotHub
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[]: Private endpoint connections created on this IotHub
* **provisioningState**: string (ReadOnly): The provisioning state.
* **publicNetworkAccess**: 'Disabled' | 'Enabled': Whether requests from Public Network are allowed.
* **routing**: [RoutingProperties](#routingproperties): The routing related properties of the IoT hub. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging
* **state**: string (ReadOnly): The hub state.
* **storageEndpoints**: [Dictionary<string,StorageEndpointProperties>](#dictionarystringstorageendpointproperties): The list of Azure Storage endpoints where you can upload files. Currently you can configure only one Azure Storage account and that MUST have its key as $default. Specifying more than one storage account causes an error to be thrown. Not specifying a value for this property when the enableFileUploadNotifications property is set to True, causes an error to be thrown.

## SharedAccessSignatureAuthorizationRule
### Properties
* **keyName**: string (Required): The name of the shared access policy.
* **primaryKey**: string: The primary key.
* **rights**: 'DeviceConnect' | 'RegistryRead, DeviceConnect' | 'RegistryRead, RegistryWrite, DeviceConnect' | 'RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect' | 'RegistryRead, RegistryWrite, ServiceConnect' | 'RegistryRead, RegistryWrite' | 'RegistryRead, ServiceConnect, DeviceConnect' | 'RegistryRead, ServiceConnect' | 'RegistryRead' | 'RegistryWrite, DeviceConnect' | 'RegistryWrite, ServiceConnect, DeviceConnect' | 'RegistryWrite, ServiceConnect' | 'RegistryWrite' | 'ServiceConnect, DeviceConnect' | 'ServiceConnect' (Required): The permissions assigned to the shared access policy.
* **secondaryKey**: string: The secondary key.

## CloudToDeviceProperties
### Properties
* **defaultTtlAsIso8601**: string: The default time to live for cloud-to-device messages in the device queue. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#cloud-to-device-messages.
* **feedback**: [FeedbackProperties](#feedbackproperties): The properties of the feedback queue for cloud-to-device messages.
* **maxDeliveryCount**: int: The max delivery count for cloud-to-device messages in the device queue. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#cloud-to-device-messages.

## FeedbackProperties
### Properties
* **lockDurationAsIso8601**: string: The lock duration for the feedback queue. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#cloud-to-device-messages.
* **maxDeliveryCount**: int: The number of times the IoT hub attempts to deliver a message on the feedback queue. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#cloud-to-device-messages.
* **ttlAsIso8601**: string: The period of time for which a message is available to consume before it is expired by the IoT hub. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#cloud-to-device-messages.

## schemas:8_deviceStreams
### Properties
* **streamingEndpoints**: string[]: List of Device Streams Endpoints.

## EncryptionPropertiesDescription
### Properties
* **keySource**: string: The source of the key.
* **keyVaultProperties**: [KeyVaultKeyProperties](#keyvaultkeyproperties)[]: The properties of the KeyVault key.

## KeyVaultKeyProperties
### Properties
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **keyIdentifier**: string: The identifier of the key.

## ManagedIdentity
### Properties
* **userAssignedIdentity**: string: The user assigned identity.

## Dictionary<string,EventHubProperties>
### Properties
### Additional Properties
* **Additional Properties Type**: [EventHubProperties](#eventhubproperties)

## EventHubProperties
### Properties
* **endpoint**: string (ReadOnly): The Event Hub-compatible endpoint.
* **partitionCount**: int: The number of partitions for receiving device-to-cloud messages in the Event Hub-compatible endpoint. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#device-to-cloud-messages.
* **partitionIds**: string[] (ReadOnly): The partition ids in the Event Hub-compatible endpoint.
* **path**: string (ReadOnly): The Event Hub-compatible name.
* **retentionTimeInDays**: int: The retention time for device-to-cloud messages in days. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messaging#device-to-cloud-messages

## IpFilterRule
### Properties
* **action**: 'Accept' | 'Reject' (Required): The desired action for requests captured by this rule.
* **filterName**: string (Required): The name of the IP filter rule.
* **ipMask**: string (Required): A string that contains the IP address range in CIDR notation for the rule.

## IotHubLocationDescription
### Properties
* **location**: string: The name of the Azure region
* **role**: 'primary' | 'secondary': The role of the region, can be either primary or secondary. The primary region is where the IoT hub is currently provisioned. The secondary region is the Azure disaster recovery (DR) paired region and also the region where the IoT hub can failover to.

## Dictionary<string,MessagingEndpointProperties>
### Properties
### Additional Properties
* **Additional Properties Type**: [MessagingEndpointProperties](#messagingendpointproperties)

## MessagingEndpointProperties
### Properties
* **lockDurationAsIso8601**: string: The lock duration. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload.
* **maxDeliveryCount**: int: The number of times the IoT hub attempts to deliver a message. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload.
* **ttlAsIso8601**: string: The period of time for which a message is available to consume before it is expired by the IoT hub. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload.

## NetworkRuleSetProperties
### Properties
* **applyToBuiltInEventHubEndpoint**: bool (Required): If True, then Network Rule Set is also applied to BuiltIn EventHub EndPoint of IotHub
* **defaultAction**: 'Allow' | 'Deny': Default Action for Network Rule Set.
* **ipRules**: [NetworkRuleSetIpRule](#networkrulesetiprule)[] (Required): List of IP Rules

## NetworkRuleSetIpRule
### Properties
* **action**: 'Allow': IP Filter Action.
* **filterName**: string (Required): Name of the IP filter rule.
* **ipMask**: string (Required): A string that contains the IP address range in CIDR notation for the rule.

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): The resource identifier.
* **name**: string (ReadOnly): The resource name.
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties) (Required): The properties of a private endpoint connection
* **type**: string (ReadOnly): The resource type.

## PrivateEndpointConnectionProperties
### Properties
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The private endpoint property of a private endpoint connection
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate) (Required): The current state of a private endpoint connection

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly): The resource identifier.

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string: Actions required for a private endpoint connection
* **description**: string (Required): The description for the current state of a private endpoint connection
* **status**: 'Approved' | 'Disconnected' | 'Pending' | 'Rejected' (Required): The status of a private endpoint connection.

## RoutingProperties
### Properties
* **endpoints**: [RoutingEndpoints](#routingendpoints): The properties related to the custom endpoints to which your IoT hub routes messages based on the routing rules. A maximum of 10 custom endpoints are allowed across all endpoint types for paid hubs and only 1 custom endpoint is allowed across all endpoint types for free hubs.
* **enrichments**: [EnrichmentProperties](#enrichmentproperties)[]: The list of user-provided enrichments that the IoT hub applies to messages to be delivered to built-in and custom endpoints. See: https://aka.ms/telemetryoneventgrid
* **fallbackRoute**: [FallbackRouteProperties](#fallbackrouteproperties): The properties of the fallback route. IoT Hub uses these properties when it routes messages to the fallback endpoint.
* **routes**: [RouteProperties](#routeproperties)[]: The list of user-provided routing rules that the IoT hub uses to route messages to built-in and custom endpoints. A maximum of 100 routing rules are allowed for paid hubs and a maximum of 5 routing rules are allowed for free hubs.

## RoutingEndpoints
### Properties
* **eventHubs**: [RoutingEventHubProperties](#routingeventhubproperties)[]: The list of Event Hubs endpoints that IoT hub routes messages to, based on the routing rules. This list does not include the built-in Event Hubs endpoint.
* **serviceBusQueues**: [RoutingServiceBusQueueEndpointProperties](#routingservicebusqueueendpointproperties)[]: The list of Service Bus queue endpoints that IoT hub routes the messages to, based on the routing rules.
* **serviceBusTopics**: [RoutingServiceBusTopicEndpointProperties](#routingservicebustopicendpointproperties)[]: The list of Service Bus topic endpoints that the IoT hub routes the messages to, based on the routing rules.
* **storageContainers**: [RoutingStorageContainerProperties](#routingstoragecontainerproperties)[]: The list of storage container endpoints that IoT hub routes messages to, based on the routing rules.

## RoutingEventHubProperties
### Properties
* **authenticationType**: 'identityBased' | 'keyBased': Method used to authenticate against the event hub endpoint.
* **connectionString**: string: The connection string of the event hub endpoint.
* **endpointUri**: string: The url of the event hub endpoint. It must include the protocol sb://
* **entityPath**: string: Event hub name on the event hub namespace
* **id**: string: Id of the event hub endpoint
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **name**: string (Required): The name that identifies this endpoint. The name can only include alphanumeric characters, periods, underscores, hyphens and has a maximum length of 64 characters. The following names are reserved:  events, fileNotifications, $default. Endpoint names must be unique across endpoint types.
* **resourceGroup**: string: The name of the resource group of the event hub endpoint.
* **subscriptionId**: string: The subscription identifier of the event hub endpoint.

## RoutingServiceBusQueueEndpointProperties
### Properties
* **authenticationType**: 'identityBased' | 'keyBased': Method used to authenticate against the service bus queue endpoint.
* **connectionString**: string: The connection string of the service bus queue endpoint.
* **endpointUri**: string: The url of the service bus queue endpoint. It must include the protocol sb://
* **entityPath**: string: Queue name on the service bus namespace
* **id**: string: Id of the service bus queue endpoint
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **name**: string (Required): The name that identifies this endpoint. The name can only include alphanumeric characters, periods, underscores, hyphens and has a maximum length of 64 characters. The following names are reserved:  events, fileNotifications, $default. Endpoint names must be unique across endpoint types. The name need not be the same as the actual queue name.
* **resourceGroup**: string: The name of the resource group of the service bus queue endpoint.
* **subscriptionId**: string: The subscription identifier of the service bus queue endpoint.

## RoutingServiceBusTopicEndpointProperties
### Properties
* **authenticationType**: 'identityBased' | 'keyBased': Method used to authenticate against the service bus topic endpoint.
* **connectionString**: string: The connection string of the service bus topic endpoint.
* **endpointUri**: string: The url of the service bus topic endpoint. It must include the protocol sb://
* **entityPath**: string: Queue name on the service bus topic
* **id**: string: Id of the service bus topic endpoint
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **name**: string (Required): The name that identifies this endpoint. The name can only include alphanumeric characters, periods, underscores, hyphens and has a maximum length of 64 characters. The following names are reserved:  events, fileNotifications, $default. Endpoint names must be unique across endpoint types.  The name need not be the same as the actual topic name.
* **resourceGroup**: string: The name of the resource group of the service bus topic endpoint.
* **subscriptionId**: string: The subscription identifier of the service bus topic endpoint.

## RoutingStorageContainerProperties
### Properties
* **authenticationType**: 'identityBased' | 'keyBased': Method used to authenticate against the storage endpoint.
* **batchFrequencyInSeconds**: int: Time interval at which blobs are written to storage. Value should be between 60 and 720 seconds. Default value is 300 seconds.
* **connectionString**: string: The connection string of the storage account.
* **containerName**: string (Required): The name of storage container in the storage account.
* **encoding**: 'Avro' | 'AvroDeflate' | 'JSON': Encoding that is used to serialize messages to blobs. Supported values are 'avro', 'avrodeflate', and 'JSON'. Default value is 'avro'.
* **endpointUri**: string: The url of the storage endpoint. It must include the protocol https://
* **fileNameFormat**: string: File name format for the blob. Default format is {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}. All parameters are mandatory but can be reordered.
* **id**: string: Id of the storage container endpoint
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **maxChunkSizeInBytes**: int: Maximum number of bytes for each blob written to storage. Value should be between 10485760(10MB) and 524288000(500MB). Default value is 314572800(300MB).
* **name**: string (Required): The name that identifies this endpoint. The name can only include alphanumeric characters, periods, underscores, hyphens and has a maximum length of 64 characters. The following names are reserved:  events, fileNotifications, $default. Endpoint names must be unique across endpoint types.
* **resourceGroup**: string: The name of the resource group of the storage account.
* **subscriptionId**: string: The subscription identifier of the storage account.

## EnrichmentProperties
### Properties
* **endpointNames**: string[] (Required): The list of endpoints for which the enrichment is applied to the message.
* **key**: string (Required): The key or name for the enrichment property.
* **value**: string (Required): The value for the enrichment property.

## FallbackRouteProperties
### Properties
* **condition**: string: The condition which is evaluated in order to apply the fallback route. If the condition is not provided it will evaluate to true by default. For grammar, See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language
* **endpointNames**: string[] (Required): The list of endpoints to which the messages that satisfy the condition are routed to. Currently only 1 endpoint is allowed.
* **isEnabled**: bool (Required): Used to specify whether the fallback route is enabled.
* **name**: string: The name of the route. The name can only include alphanumeric characters, periods, underscores, hyphens, has a maximum length of 64 characters, and must be unique.
* **source**: string (Required): The source to which the routing rule is to be applied to. For example, DeviceMessages

## RouteProperties
### Properties
* **condition**: string: The condition that is evaluated to apply the routing rule. If no condition is provided, it evaluates to true by default. For grammar, see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language
* **endpointNames**: string[] (Required): The list of endpoints to which messages that satisfy the condition are routed. Currently only one endpoint is allowed.
* **isEnabled**: bool (Required): Used to specify whether a route is enabled.
* **name**: string (Required): The name of the route. The name can only include alphanumeric characters, periods, underscores, hyphens, has a maximum length of 64 characters, and must be unique.
* **source**: 'DeviceConnectionStateEvents' | 'DeviceJobLifecycleEvents' | 'DeviceLifecycleEvents' | 'DeviceMessages' | 'DigitalTwinChangeEvents' | 'Invalid' | 'TwinChangeEvents' (Required): The source that the routing rule is to be applied to, such as DeviceMessages.

## Dictionary<string,StorageEndpointProperties>
### Properties
### Additional Properties
* **Additional Properties Type**: [StorageEndpointProperties](#storageendpointproperties)

## StorageEndpointProperties
### Properties
* **authenticationType**: 'identityBased' | 'keyBased': Specifies authentication type being used for connecting to the storage account.
* **connectionString**: string (Required): The connection string for the Azure Storage account to which files are uploaded.
* **containerName**: string (Required): The name of the root container where you upload files. The container need not exist but should be creatable using the connectionString specified.
* **identity**: [ManagedIdentity](#managedidentity): The properties of the Managed identity.
* **sasTtlAsIso8601**: string: The period of time for which the SAS URI generated by IoT Hub for file upload is valid. See: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload#file-upload-notification-configuration-options.

## IotHubSkuInfo
### Properties
* **capacity**: int: The number of provisioned IoT Hub units. See: https://docs.microsoft.com/azure/azure-subscription-service-limits#iot-hub-limits.
* **name**: 'B1' | 'B2' | 'B3' | 'F1' | 'S1' | 'S2' | 'S3' (Required): The name of the SKU.
* **tier**: 'Basic' | 'Free' | 'Standard' (ReadOnly): The billing tier for the IoT hub.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## CertificateProperties
### Properties
* **certificate**: string: The certificate content
* **created**: string (ReadOnly): The certificate's create date and time.
* **expiry**: string (ReadOnly): The certificate's expiration date and time.
* **isVerified**: bool (ReadOnly): Determines whether certificate has been verified.
* **subject**: string (ReadOnly): The certificate's subject name.
* **thumbprint**: string (ReadOnly): The certificate's thumbprint.
* **updated**: string (ReadOnly): The certificate's last update date and time.

## EventHubConsumerGroupName
### Properties
* **name**: string (WriteOnly): EventHub consumer group name
