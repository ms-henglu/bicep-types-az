# Microsoft.Billing @ 2020-05-01

## Resource Microsoft.Billing/billingAccounts/billingProfiles@2020-05-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BillingProfileProperties](#billingprofileproperties): The properties of the billing profile.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/instructions@2020-05-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InstructionProperties](#instructionproperties): A billing instruction used during invoice generation.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/instructions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections@2020-05-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties): The properties of an invoice section.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/policies@2020-05-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [PolicyProperties](#policyproperties): The properties of a policy.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/policies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/customers/policies@2020-05-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2020-05-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [CustomerPolicyProperties](#customerpolicyproperties): The properties of a customer's policy.
* **type**: 'Microsoft.Billing/billingAccounts/customers/policies' (ReadOnly, DeployTimeConstant): The resource type

## Function download (Microsoft.Billing/billingAccounts/invoices@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/invoices
* **ApiVersion**: 2020-05-01
* **Output**: [DownloadUrl](#downloadurl)

## Function download (Microsoft.Billing/billingAccounts/billingSubscriptions/invoices@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/billingSubscriptions/invoices
* **ApiVersion**: 2020-05-01
* **Output**: [DownloadUrl](#downloadurl)

## Function downloadDocuments (Microsoft.Billing/billingAccounts@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2020-05-01
* **Input**: string[]
* **Output**: [DownloadUrl](#downloadurl)

## Function downloadDocuments (Microsoft.Billing/billingAccounts/billingSubscriptions@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/billingSubscriptions
* **ApiVersion**: 2020-05-01
* **Input**: string[]
* **Output**: [DownloadUrl](#downloadurl)

## Function listInvoiceSectionsWithCreateSubscriptionPermission (Microsoft.Billing/billingAccounts@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2020-05-01
* **Output**: [InvoiceSectionListWithCreateSubPermissionResult](#invoicesectionlistwithcreatesubpermissionresult)

## Function move (Microsoft.Billing/billingAccounts/billingSubscriptions@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/billingSubscriptions
* **ApiVersion**: 2020-05-01
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [BillingSubscription](#billingsubscription)

## Function move (Microsoft.Billing/billingAccounts/products@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/products
* **ApiVersion**: 2020-05-01
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [Product](#product)

## Function validateMoveEligibility (Microsoft.Billing/billingAccounts/billingSubscriptions@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/billingSubscriptions
* **ApiVersion**: 2020-05-01
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [ValidateSubscriptionTransferEligibilityResult](#validatesubscriptiontransfereligibilityresult)

## Function validateMoveEligibility (Microsoft.Billing/billingAccounts/products@2020-05-01)
* **Resource**: Microsoft.Billing/billingAccounts/products
* **ApiVersion**: 2020-05-01
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [ValidateProductTransferEligibilityResult](#validateproducttransfereligibilityresult)

## AddressDetails
### Properties
* **addressLine1**: string (Required): Address line 1.
* **addressLine2**: string: Address line 2.
* **addressLine3**: string: Address line 3.
* **city**: string: Address city.
* **companyName**: string: Company name.
* **country**: string (Required): Country code uses ISO2, 2-digit format.
* **district**: string: Address district.
* **email**: string: Email address.
* **firstName**: string: First name.
* **lastName**: string: Last name.
* **middleName**: string: Middle name.
* **phoneNumber**: string: Phone number.
* **postalCode**: string: Postal code.
* **region**: string: Address region.

## Amount
### Properties
* **currency**: string (ReadOnly): The currency for the amount value.
* **value**: int: Amount value.

## AzurePlan
### Properties
* **skuDescription**: string (ReadOnly): The sku description.
* **skuId**: string: The sku id.

## BillingProfileProperties
### Properties
* **billingRelationshipType**: 'CSPPartner' | 'Direct' | 'IndirectCustomer' | 'IndirectPartner' | string (ReadOnly): Identifies which services and purchases are paid by a billing profile.
* **billTo**: [AddressDetails](#addressdetails): Billing address.
* **currency**: string (ReadOnly): The currency in which the charges for the billing profile are billed.
* **displayName**: string: The name of the billing profile.
* **enabledAzurePlans**: [AzurePlan](#azureplan)[]: Information about the enabled azure plans.
* **hasReadAccess**: bool (ReadOnly): Indicates whether user has read access to the billing profile.
* **indirectRelationshipInfo**: [IndirectRelationshipInfo](#indirectrelationshipinfo) (ReadOnly): Identifies the billing profile that is linked to another billing profile in indirect purchase motion.
* **invoiceDay**: int (ReadOnly): The day of the month when the invoice for the billing profile is generated.
* **invoiceEmailOptIn**: bool: Flag controlling whether the invoices for the billing profile are sent through email.
* **invoiceSections**: [InvoiceSectionsOnExpand](#invoicesectionsonexpand): The invoice sections associated to the billing profile. By default this is not populated, unless it's specified in $expand.
* **poNumber**: string: The purchase order name that will appear on the invoices generated for the billing profile.
* **spendingLimit**: 'Off' | 'On' | string (ReadOnly): The billing profile spending limit.
* **status**: 'Active' | 'Disabled' | 'Warned' | string (ReadOnly): The status of the billing profile.
* **statusReasonCode**: 'PastDue' | 'SpendingLimitExpired' | 'SpendingLimitReached' | string (ReadOnly): Reason for the specified billing profile status.
* **systemId**: string (ReadOnly): The system generated unique identifier for a billing profile.
* **tags**: [BillingProfilePropertiesTags](#billingprofilepropertiestags): Tags of billing profiles.
* **targetClouds**: 'USGov' | 'USNat' | 'USSec' | string[] (ReadOnly): Identifies the cloud environments that are associated with a billing profile. This is a system managed optional field and gets updated as the billing profile gets associated with accounts in various clouds.

## BillingProfilePropertiesTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BillingSubscription
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [BillingSubscriptionProperties](#billingsubscriptionproperties): The billing properties of a subscription.
* **type**: string (ReadOnly): Resource type.

## BillingSubscriptionProperties
### Properties
* **billingProfileDisplayName**: string (ReadOnly): The name of the billing profile to which the subscription is billed.
* **billingProfileId**: string (ReadOnly): The ID of the billing profile to which the subscription is billed.
* **costCenter**: string: The cost center applied to the subscription.
* **customerDisplayName**: string (ReadOnly): The name of the customer for whom the subscription was created. The field is applicable only for Microsoft Partner Agreement billing account.
* **customerId**: string (ReadOnly): The ID of the customer for whom the subscription was created. The field is applicable only for Microsoft Partner Agreement billing account.
* **displayName**: string (ReadOnly): The name of the subscription.
* **invoiceSectionDisplayName**: string (ReadOnly): The name of the invoice section to which the subscription is billed.
* **invoiceSectionId**: string (ReadOnly): The ID of the invoice section to which the subscription is billed.
* **lastMonthCharges**: [Amount](#amount) (ReadOnly): The last month charges.
* **monthToDateCharges**: [Amount](#amount) (ReadOnly): The current month to date charges.
* **reseller**: [Reseller](#reseller) (ReadOnly): Reseller for this subscription.
* **skuDescription**: string (ReadOnly): The sku description of the Azure plan for the subscription.
* **skuId**: string: The sku ID of the Azure plan for the subscription.
* **subscriptionBillingStatus**: 'Abandoned' | 'Active' | 'Deleted' | 'Inactive' | 'Warning' | string: The current billing status of the subscription.
* **subscriptionId**: string (ReadOnly): The ID of the subscription.
* **suspensionReasons**: string[] (ReadOnly): The suspension reason for a subscription. Applies only to subscriptions in Microsoft Online Services Program billing accounts.

## CustomerPolicyProperties
### Properties
* **viewCharges**: 'Allowed' | 'NotAllowed' | string: The policy that controls whether the users in customer's organization can view charges at pay-as-you-go prices.

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC when the download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC when the download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC when the download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC when the download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## IndirectRelationshipInfo
### Properties
* **billingAccountName**: string: The billing account name of the partner or the customer for an indirect motion.
* **billingProfileName**: string: The billing profile name of the partner or the customer for an indirect motion.
* **displayName**: string: The display name of the partner or customer for an indirect motion.

## InstructionProperties
### Properties
* **amount**: int (Required): The amount budgeted for this billing instruction.
* **creationDate**: string: The date this billing instruction was created.
* **endDate**: string (Required): The date this billing instruction is no longer in effect.
* **startDate**: string (Required): The date this billing instruction goes into effect.

## InvoiceSection
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties): The properties of an invoice section.
* **type**: string (ReadOnly): Resource type.

## InvoiceSectionListWithCreateSubPermissionResult
### Properties
* **nextLink**: string (ReadOnly): The link (url) to the next page of results.
* **value**: [InvoiceSectionWithCreateSubPermission](#invoicesectionwithcreatesubpermission)[]: The list of invoice section properties with create subscription permission.

## InvoiceSectionProperties
### Properties
* **displayName**: string: The name of the invoice section.
* **labels**: [InvoiceSectionPropertiesLabels](#invoicesectionpropertieslabels): Dictionary of metadata associated with the invoice section.
* **state**: 'Active' | 'Restricted' | string (ReadOnly): Identifies the state of an invoice section.
* **systemId**: string (ReadOnly): The system generated unique identifier for an invoice section.
* **tags**: [InvoiceSectionPropertiesTags](#invoicesectionpropertiestags): Dictionary of metadata associated with the invoice section. Maximum key/value length supported of 256 characters. Keys/value should not empty value nor null. Keys can not contain < > % & \ ? /
* **targetCloud**: 'USGov' | 'USNat' | 'USSec' | string (ReadOnly): Identifies the cloud environments that are associated with an invoice section. This is a system managed optional field and gets updated as the invoice section gets associated with accounts in various clouds.

## InvoiceSectionPropertiesLabels
### Properties
### Additional Properties
* **Additional Properties Type**: string

## InvoiceSectionPropertiesTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## InvoiceSectionsOnExpand
### Properties
* **hasMoreResults**: bool (ReadOnly): Indicates whether there are more invoice sections than the ones listed in this collection. The collection lists a maximum of 50 invoice sections. To get all invoice sections, use the list invoice sections API.
* **value**: [InvoiceSection](#invoicesection)[]: The invoice sections associated to the billing profile.

## InvoiceSectionWithCreateSubPermission
### Properties
* **billingProfileDisplayName**: string (ReadOnly): The name of the billing profile for the invoice section.
* **billingProfileId**: string (ReadOnly): The ID of the billing profile for the invoice section.
* **billingProfileSpendingLimit**: 'Off' | 'On' | string (ReadOnly): The billing profile spending limit.
* **billingProfileStatus**: 'Active' | 'Disabled' | 'Warned' | string (ReadOnly): The status of the billing profile.
* **billingProfileStatusReasonCode**: 'PastDue' | 'SpendingLimitExpired' | 'SpendingLimitReached' | string (ReadOnly): Reason for the specified billing profile status.
* **billingProfileSystemId**: string (ReadOnly): The system generated unique identifier for a billing profile.
* **enabledAzurePlans**: [AzurePlan](#azureplan)[]: Enabled azure plans for the associated billing profile.
* **invoiceSectionDisplayName**: string (ReadOnly): The name of the invoice section.
* **invoiceSectionId**: string (ReadOnly): The ID of the invoice section.
* **invoiceSectionSystemId**: string (ReadOnly): The system generated unique identifier for an invoice section.

## PolicyProperties
### Properties
* **marketplacePurchases**: 'AllAllowed' | 'NotAllowed' | 'OnlyFreeAllowed' | string: The policy that controls whether Azure marketplace purchases are allowed for a billing profile.
* **reservationPurchases**: 'Allowed' | 'NotAllowed' | string: The policy that controls whether Azure reservation purchases are allowed for a billing profile.
* **viewCharges**: 'Allowed' | 'NotAllowed' | string: The policy that controls whether users with Azure RBAC access to a subscription can view its charges.

## Product
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [ProductProperties](#productproperties): The properties of a product.
* **type**: string (ReadOnly): Resource type.

## ProductProperties
### Properties
* **autoRenew**: 'Off' | 'On' | string: Indicates whether auto renewal is turned on or off for a product.
* **availabilityId**: string (ReadOnly): The availability of the product.
* **billingFrequency**: 'Monthly' | 'OneTime' | 'UsageBased' | string: The frequency at which the product will be billed.
* **billingProfileDisplayName**: string (ReadOnly): The name of the billing profile to which the product is billed.
* **billingProfileId**: string (ReadOnly): The ID of the billing profile to which the product is billed.
* **customerDisplayName**: string (ReadOnly): The name of the customer for whom the product was purchased. The field is applicable only for Microsoft Partner Agreement billing account.
* **customerId**: string (ReadOnly): The ID of the customer for whom the product was purchased. The field is applicable only for Microsoft Partner Agreement billing account.
* **displayName**: string (ReadOnly): The display name of the product.
* **endDate**: string (ReadOnly): The date when the product will be renewed or canceled.
* **invoiceSectionDisplayName**: string (ReadOnly): The name of the invoice section to which the product is billed.
* **invoiceSectionId**: string (ReadOnly): The ID of the invoice section to which the product is billed.
* **lastCharge**: [Amount](#amount) (ReadOnly): The last month charges.
* **lastChargeDate**: string (ReadOnly): The date of the last charge.
* **productType**: string (ReadOnly): The description of the type of product.
* **productTypeId**: string (ReadOnly): The ID of the type of product.
* **purchaseDate**: string (ReadOnly): The date when the product was purchased.
* **quantity**: int (ReadOnly): The quantity purchased for the product.
* **reseller**: [Reseller](#reseller) (ReadOnly): Reseller for this product.
* **skuDescription**: string (ReadOnly): The sku description of the product.
* **skuId**: string (ReadOnly): The sku ID of the product.
* **status**: 'Active' | 'AutoRenew' | 'Cancelled' | 'Disabled' | 'Expired' | 'Expiring' | 'Inactive' | 'PastDue' | string: The current status of the product.
* **tenantId**: string (ReadOnly): The id of the tenant in which the product is used.

## Reseller
### Properties
* **description**: string (ReadOnly): The name of the reseller.
* **resellerId**: string (ReadOnly): The MPN ID of the reseller.

## TransferBillingSubscriptionRequestProperties
### Properties
* **destinationInvoiceSectionId**: string (Required): The destination invoice section id.

## TransferBillingSubscriptionRequestProperties
### Properties
* **destinationInvoiceSectionId**: string (Required): The destination invoice section id.

## TransferProductRequestProperties
### Properties
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## TransferProductRequestProperties
### Properties
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## ValidateProductTransferEligibilityError
### Properties
* **code**: 'CrossBillingAccountNotAllowed' | 'DestinationBillingProfilePastDue' | 'InsufficientPermissionOnDestination' | 'InsufficientPermissionOnSource' | 'InvalidSource' | 'NotAvailableForDestinationMarket' | 'OneTimePurchaseProductTransferNotAllowed' | 'ProductNotActive' | 'ProductTypeNotSupported' | string: Error code for the product transfer validation.
* **details**: string: Detailed error message explaining the error.
* **message**: string: The error message.

## ValidateProductTransferEligibilityResult
### Properties
* **errorDetails**: [ValidateProductTransferEligibilityError](#validateproducttransfereligibilityerror): Validation error details.
* **isMoveEligible**: bool (ReadOnly): Specifies whether the transfer is eligible or not.

## ValidateSubscriptionTransferEligibilityError
### Properties
* **code**: 'BillingAccountInactive' | 'CrossBillingAccountNotAllowed' | 'DestinationBillingProfileInactive' | 'DestinationBillingProfileNotFound' | 'DestinationBillingProfilePastDue' | 'DestinationInvoiceSectionInactive' | 'DestinationInvoiceSectionNotFound' | 'InsufficientPermissionOnDestination' | 'InsufficientPermissionOnSource' | 'InvalidDestination' | 'InvalidSource' | 'MarketplaceNotEnabledOnDestination' | 'NotAvailableForDestinationMarket' | 'ProductInactive' | 'ProductNotFound' | 'ProductTypeNotSupported' | 'SourceBillingProfilePastDue' | 'SourceInvoiceSectionInactive' | 'SubscriptionNotActive' | 'SubscriptionTypeNotSupported' | string: Error code for the product transfer validation.
* **details**: string: Detailed error message explaining the error.
* **message**: string: The error message.

## ValidateSubscriptionTransferEligibilityResult
### Properties
* **errorDetails**: [ValidateSubscriptionTransferEligibilityError](#validatesubscriptiontransfereligibilityerror): Validation error details.
* **isMoveEligible**: bool (ReadOnly): Specifies whether the subscription is eligible to be transferred.

