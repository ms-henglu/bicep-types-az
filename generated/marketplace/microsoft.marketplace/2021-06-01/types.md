# Microsoft.Marketplace @ 2021-06-01

## Resource Microsoft.Marketplace/privateStores@2021-06-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateStoreProperties](#privatestoreproperties): The PrivateStore data structure.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource
* **type**: 'Microsoft.Marketplace/privateStores' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Marketplace/privateStores/adminRequestApprovals@2021-06-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AdminRequestApprovalProperties](#adminrequestapprovalproperties): The privateStore admin Approval request data structure.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource
* **type**: 'Microsoft.Marketplace/privateStores/adminRequestApprovals' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Marketplace/privateStores/collections@2021-06-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CollectionProperties](#collectionproperties): The collection data structure.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource
* **type**: 'Microsoft.Marketplace/privateStores/collections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Marketplace/privateStores/collections/offers@2021-06-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [OfferProperties](#offerproperties): The privateStore offer data structure.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource
* **type**: 'Microsoft.Marketplace/privateStores/collections/offers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Marketplace/privateStores/requestApprovals@2021-06-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2021-06-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [RequestApprovalProperties](#requestapprovalproperties): The privateStore approval request data structure.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource
* **type**: 'Microsoft.Marketplace/privateStores/requestApprovals' (ReadOnly, DeployTimeConstant): The resource type

## Function billingAccounts (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Output**: [BillingAccountsResponse](#billingaccountsresponse)

## Function bulkCollectionsAction (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Input**: [BulkCollectionsPayload](#bulkcollectionspayload)
* **Output**: [BulkCollectionsResponse](#bulkcollectionsresponse)

## Function collectionsToSubscriptionsMapping (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Input**: [CollectionsToSubscriptionsMappingPayload](#collectionstosubscriptionsmappingpayload)
* **Output**: [CollectionsToSubscriptionsMappingResponse](#collectionstosubscriptionsmappingresponse)

## Function query (Microsoft.Marketplace/privateStores/requestApprovals@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores/requestApprovals
* **ApiVersion**: 2021-06-01
* **Input**: [QueryRequestApprovalProperties](#queryrequestapprovalproperties)
* **Output**: [QueryRequestApproval](#queryrequestapproval)

## Function queryApprovedPlans (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Input**: [QueryApprovedPlansPayload](#queryapprovedplanspayload)
* **Output**: [QueryApprovedPlansResponse](#queryapprovedplansresponse)

## Function queryNotificationsState (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Output**: [PrivateStoreNotificationsState](#privatestorenotificationsstate)

## Function queryOffers (Microsoft.Marketplace/privateStores@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores
* **ApiVersion**: 2021-06-01
* **Output**: [QueryOffers](#queryoffers)

## Function transferOffers (Microsoft.Marketplace/privateStores/collections@2021-06-01)
* **Resource**: Microsoft.Marketplace/privateStores/collections
* **ApiVersion**: 2021-06-01
* **Input**: [TransferOffersProperties](#transferoffersproperties)
* **Output**: [TransferOffersResponse](#transferoffersresponse)

## AdminRequestApprovalProperties
### Properties
* **adminAction**: 'Approved' | 'Rejected' | string: Gets or sets admin action
* **administrator**: string: Gets or sets admin details
* **approvedPlans**: string[]: Gets or sets Approved plans ids, empty in case of rejected
* **collectionIds**: string[]: Gets or sets list of associated collection ids
* **comment**: string: Gets or sets admin comment
* **displayName**: string (ReadOnly): Gets display name
* **offerId**: string: Gets or sets offer Id
* **plans**: [PlanRequesterDetails](#planrequesterdetails)[] (ReadOnly): Gets list of plans with requesters details
* **publisherId**: string: Gets or sets publisher Id

## BillingAccountsResponse
### Properties
* **billingAccounts**: string[]: Billing accounts list

## BulkCollectionsDetails
### Properties
* **action**: string: Action to perform (For example: EnableCollections, DisableCollections)
* **collectionIds**: string[]: collection ids list that the action is performed on

## BulkCollectionsPayload
### Properties
* **properties**: [BulkCollectionsDetails](#bulkcollectionsdetails): bulk collections properties details

## BulkCollectionsResponse
### Properties
* **failed**: [CollectionsDetails](#collectionsdetails)[]: Failed collections
* **succeeded**: [CollectionsDetails](#collectionsdetails)[]: Succeeded collections

## CollectionProperties
### Properties
* **allSubscriptions**: bool: Indicating whether all subscriptions are selected (=true) or not (=false).
* **claim**: string: Gets or sets the association with Commercial's Billing Account.
* **collectionId**: string (ReadOnly): Gets collection Id.
* **collectionName**: string: Gets or sets collection name.
* **enabled**: bool: Indicating whether the collection is enabled or disabled.
* **numberOfOffers**: int (ReadOnly): Gets the number of offers associated with the collection.
* **subscriptionsList**: string[]: Gets or sets subscription ids list. Empty list indicates all subscriptions are selected, null indicates no update is done, explicit list indicates the explicit selected subscriptions. On insert, null is considered as bad request

## CollectionsDetails
### Properties
* **collectionId**: string: Collection id.
* **collectionName**: string: Collection name.

## CollectionsSubscriptionsMappingDetails
### Properties
* **collectionName**: string: Collection name
* **subscriptions**: string[]: Subscriptions ids list

## CollectionsToSubscriptionsMappingPayload
### Properties
* **properties**: [CollectionsToSubscriptionsMappingProperties](#collectionstosubscriptionsmappingproperties): Subscriptions ids list

## CollectionsToSubscriptionsMappingProperties
### Properties
* **subscriptionIds**: string[]: Subscriptions ids list

## CollectionsToSubscriptionsMappingResponse
### Properties
* **details**: [CollectionsToSubscriptionsMappingResponseProperties](#collectionstosubscriptionsmappingresponseproperties): The map of collections subscriptions

## CollectionsToSubscriptionsMappingResponseProperties
### Properties
### Additional Properties
* **Additional Properties Type**: [CollectionsSubscriptionsMappingDetails](#collectionssubscriptionsmappingdetails)

## NewNotifications
### Properties
* **displayName**: string: Gets offer display name
* **icon**: string: Gets or sets the icon url
* **isFuturePlansEnabled**: bool: Gets a value indicating whether future plans is enabled.
* **messageCode**: int: Gets or sets the notification message id
* **offerId**: string: Gets offer id
* **plans**: [PlanNotificationDetails](#plannotificationdetails)[]: Gets or sets removed plans notifications

## NotificationsSettingsProperties
### Properties
* **recipients**: [Recipient](#recipient)[]: Gets or sets list of notified recipients for new requests
* **sendToAllMarketplaceAdmins**: bool: Gets or sets whether to send email to all marketplace admins for new requests

## OfferProperties
### Properties
* **createdAt**: string (ReadOnly): Private store offer creation date
* **eTag**: string: Identifier for purposes of race condition
* **iconFileUris**: [OfferPropertiesIconFileUris](#offerpropertiesiconfileuris): Icon File Uris
* **modifiedAt**: string (ReadOnly): Private store offer modification date
* **offerDisplayName**: string (ReadOnly): It will be displayed prominently in the marketplace
* **plans**: [Plan](#plan)[]: Offer plans
* **privateStoreId**: string (ReadOnly): Private store unique id
* **publisherDisplayName**: string (ReadOnly): Publisher name that will be displayed prominently in the marketplace
* **specificPlanIdsLimitation**: string[]: Plan ids limitation for this offer
* **uniqueOfferId**: string (ReadOnly): Offers unique id
* **updateSuppressedDueIdempotence**: bool: Indicating whether the offer was not updated to db (true = not updated). If the allow list is identical to the existed one in db, the offer would not be updated.

## OfferPropertiesIconFileUris
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Plan
### Properties
* **accessibility**: 'PrivateSubscriptionOnLevel' | 'PrivateTenantOnLevel' | 'Public' | 'Unknown' | string: Plan accessibility
* **altStackReference**: string (ReadOnly): Alternative stack type
* **planDisplayName**: string (ReadOnly): Friendly name for the plan for display in the marketplace
* **planId**: string (ReadOnly): Text identifier for this plan
* **skuId**: string (ReadOnly): Identifier for this plan
* **stackType**: string (ReadOnly): Stack type (classic or arm)

## PlanDetails
### Properties
* **justification**: string: Gets or sets user's justification for the plan's request
* **planId**: string: Gets or sets Plan Id
* **requestDate**: any (ReadOnly): Gets request date
* **status**: 'Approved' | 'None' | 'Pending' | 'Rejected' | string (ReadOnly): Gets the plan status
* **subscriptionId**: string: Gets or sets the subscription id that the user is requesting to add the plan to
* **subscriptionName**: string: Gets or sets the subscription name that the user is requesting to add the plan to

## PlanNotificationDetails
### Properties
* **planDisplayName**: string: Gets or sets the plan display name
* **planId**: string: Gets or sets the plan id

## PlanRequesterDetails
### Properties
* **planDisplayName**: string (ReadOnly): Gets the plan display name
* **planId**: string (ReadOnly): Gets the plan id
* **requesters**: [UserRequestDetails](#userrequestdetails)[] (ReadOnly): Gets requesters details list

## PrivateStoreNotificationsState
### Properties
* **approvalRequests**: [RequestApprovalsDetails](#requestapprovalsdetails)[]
* **newNotifications**: [NewNotifications](#newnotifications)[]
* **stopSellNotifications**: [StopSellNotifications](#stopsellnotifications)[]

## PrivateStoreProperties
### Properties
* **availability**: 'disabled' | 'enabled' | string: Indicates private store availability
* **branding**: [PrivateStorePropertiesBranding](#privatestorepropertiesbranding): Gets or sets list of branding characteristics
* **collectionIds**: string[] (ReadOnly): Gets list of associated collection ids
* **eTag**: string: Identifier for purposes of race condition
* **isGov**: bool: Is government
* **notificationsSettings**: [NotificationsSettingsProperties](#notificationssettingsproperties): Gets or sets notifications settings
* **privateStoreId**: string (ReadOnly): Private Store id
* **privateStoreName**: string: Private Store Name
* **tenantId**: string: Tenant id

## PrivateStorePropertiesBranding
### Properties
### Additional Properties
* **Additional Properties Type**: string

## QueryApprovedPlans
### Properties
* **offerId**: string: Offer id
* **planIds**: string[]: Offer plan ids

## QueryApprovedPlansDetails
### Properties
* **allSubscriptions**: bool: Indicates whether all subscriptions are approved for this plan
* **planId**: string: Plan id
* **subscriptionIds**: string[]: Approved subscription ids list. In case all subscriptions are approved for a plan, allSubscriptions flag is true and list is empty ( else flag is set to false). In case both subscriptions list is empty and allSubscriptions flag is false, the plan is not approved for any subscription.

## QueryApprovedPlansPayload
### Properties
* **properties**: [QueryApprovedPlans](#queryapprovedplans): Query approved plans details

## QueryApprovedPlansResponse
### Properties
* **details**: [QueryApprovedPlansDetails](#queryapprovedplansdetails)[]: A list indicating for each plan which subscriptions are approved. Plan Id is unique

## QueryOffers
### Properties
* **nextLink**: string: URL to get the next set of PrivateStore list results if there are any.
* **value**: [OfferProperties](#offerproperties)[]

## QueryRequestApproval
### Properties
* **etag**: string: Gets or sets e-tag field
* **messageCode**: int: Gets or sets the notification message id
* **plansDetails**: [QueryRequestApprovalPlansDetails](#queryrequestapprovalplansdetails): Gets or sets the plans details
* **uniqueOfferId**: string: Gets or sets unique offer id.

## QueryRequestApprovalPlansDetails
### Properties
### Additional Properties
* **Additional Properties Type**: [PlanDetails](#plandetails)

## QueryRequestApprovalProperties
### Properties
* **properties**: [RequestDetails](#requestdetails): The details to get the request plans statuses

## Recipient
### Properties
* **displayName**: string (ReadOnly): Display Name
* **emailAddress**: string (ReadOnly): Email Address
* **principalId**: string: Principal ID

## RequestApprovalProperties
### Properties
* **isClosed**: bool (ReadOnly): Gets a value indicating whether the request is closed
* **messageCode**: int: Gets or sets the request approval message code
* **offerDisplayName**: string (ReadOnly): Gets offer display name
* **offerId**: string: Gets or sets unique offer id.
* **plansDetails**: [PlanDetails](#plandetails)[]: Gets or sets the plans details
* **publisherId**: string: The offer's publisher id

## RequestApprovalsDetails
### Properties
* **displayName**: string: Gets offer display name
* **icon**: string: Gets or sets the icon url
* **messageCode**: int: Gets or sets the notification message id
* **offerId**: string: Gets offer id
* **plans**: [PlanNotificationDetails](#plannotificationdetails)[]: Gets or sets removed plans notifications
* **publisherId**: string: Gets or sets publisher id

## RequestDetails
### Properties
* **planIds**: string[]: Current plans list
* **publisherId**: string: The offer's publisher id
* **subscriptionId**: string: Gets or sets the subscription id

## StopSellNotifications
### Properties
* **displayName**: string: Gets offer display name
* **icon**: string: Gets or sets the icon url
* **isEntire**: bool: Gets a value indicating whether entire offer is in stop sell or only few of its plans
* **messageCode**: int: Gets or sets the notification message id
* **offerId**: string: Gets offer id
* **plans**: [PlanNotificationDetails](#plannotificationdetails)[]: Gets or sets removed plans notifications

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC)
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource

## TransferOffersDetails
### Properties
* **offerIdsList**: string[]: Offers ids list to transfer from source collection to target collection(s)
* **operation**: string: Operation to perform (For example: Copy or Move)
* **targetCollections**: string[]: Target collections ids

## TransferOffersProperties
### Properties
* **properties**: [TransferOffersDetails](#transferoffersdetails): transfer offers properties details

## TransferOffersResponse
### Properties
* **failed**: [CollectionsDetails](#collectionsdetails)[]: Failed collections
* **succeeded**: [CollectionsDetails](#collectionsdetails)[]: Succeeded collections

## UserRequestDetails
### Properties
* **date**: string (ReadOnly): Gets request date
* **justification**: string (ReadOnly): Gets justification
* **subscriptionId**: string: Gets the subscription id that the user is requesting to add the plan to
* **subscriptionName**: string: Gets the subscription name that the user is requesting to add the plan to
* **user**: string (ReadOnly): Gets user id

