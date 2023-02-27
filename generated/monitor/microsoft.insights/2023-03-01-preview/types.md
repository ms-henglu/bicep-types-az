# Microsoft.Insights @ 2023-03-01-preview

## Resource Microsoft.Insights/tenantActionGroups@2023-03-01-preview
* **Valid Scope(s)**: ManagementGroup
### Properties
* **apiVersion**: '2023-03-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [TenantActionGroup](#tenantactiongroup): The tenant action groups properties of the resource.
* **tags**: [AzureResourceTags](#azureresourcetags): Resource tags
* **type**: 'Microsoft.Insights/tenantActionGroups' (ReadOnly, DeployTimeConstant): The resource type

## AzureAppPushReceiver
### Properties
* **emailAddress**: string (Required): The email address registered for the Azure mobile app.
* **name**: string (Required): The name of the Azure mobile app push receiver. Names must be unique across all receivers within a tenant action group.

## AzureResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## EmailReceiver
### Properties
* **emailAddress**: string (Required): The email address of this receiver.
* **name**: string (Required): The name of the email receiver. Names must be unique across all receivers within a tenant action group.
* **status**: 'Disabled' | 'Enabled' | 'NotSpecified' (ReadOnly): The receiver status of the e-mail.
* **useCommonAlertSchema**: bool: Indicates whether to use common alert schema.

## SmsReceiver
### Properties
* **countryCode**: string (Required): The country code of the SMS receiver.
* **name**: string (Required): The name of the SMS receiver. Names must be unique across all receivers within a tenant action group.
* **phoneNumber**: string (Required): The phone number of the SMS receiver.
* **status**: 'Disabled' | 'Enabled' | 'NotSpecified' (ReadOnly): The status of the receiver.

## TenantActionGroup
### Properties
* **azureAppPushReceivers**: [AzureAppPushReceiver](#azureapppushreceiver)[]: The list of AzureAppPush receivers that are part of this tenant action group.
* **emailReceivers**: [EmailReceiver](#emailreceiver)[]: The list of email receivers that are part of this tenant action group.
* **enabled**: bool (Required): Indicates whether this tenant action group is enabled. If a tenant action group is not enabled, then none of its receivers will receive communications.
* **groupShortName**: string (Required): The short name of the action group. This will be used in SMS messages.
* **smsReceivers**: [SmsReceiver](#smsreceiver)[]: The list of SMS receivers that are part of this tenant action group.
* **voiceReceivers**: [VoiceReceiver](#voicereceiver)[]: The list of voice receivers that are part of this tenant action group.
* **webhookReceivers**: [WebhookReceiver](#webhookreceiver)[]: The list of webhook receivers that are part of this tenant action group.

## VoiceReceiver
### Properties
* **countryCode**: string (Required): The country code of the voice receiver.
* **name**: string (Required): The name of the voice receiver. Names must be unique across all receivers within a tenant action group.
* **phoneNumber**: string (Required): The phone number of the voice receiver.

## WebhookReceiver
### Properties
* **identifierUri**: string: Indicates the identifier uri for aad auth.
* **name**: string (Required): The name of the webhook receiver. Names must be unique across all receivers within a tenant action group.
* **objectId**: string: Indicates the webhook app object Id for aad auth.
* **serviceUri**: string (Required): The URI where webhooks should be sent.
* **tenantId**: string: Indicates the tenant id for aad auth.
* **useAadAuth**: bool: Indicates whether or not use AAD authentication.
* **useCommonAlertSchema**: bool: Indicates whether to use common alert schema.

