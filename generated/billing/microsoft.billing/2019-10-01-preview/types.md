# Microsoft.Billing @ 2019-10-01-preview

## Resource Microsoft.Billing/billingAccounts/billingProfiles@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **address**: [AddressDetails](#addressdetails) (WriteOnly): Billing address.
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **displayName**: string (WriteOnly): The name of the billing profile.
* **enabledAzurePlans**: [AzurePlan](#azureplan)[] (WriteOnly): Enabled azure plans for the billing profile.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **invoiceEmailOptIn**: bool (WriteOnly): Flag controlling whether the invoices for the billing profile are sent through email.
* **name**: string (Required, DeployTimeConstant): The resource name
* **poNumber**: string (WriteOnly): The purchase order name that will appear on the invoices generated for the billing profile.
* **properties**: [BillingProfileProperties](#billingprofileproperties) (ReadOnly): The properties of the billing profile.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/instructions@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InstructionProperties](#instructionproperties): A billing instruction used during invoice generation.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/instructions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **displayName**: string (WriteOnly): The name of the invoice section.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties) (ReadOnly): The properties of an invoice section.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/policies@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [PolicyProperties](#policyproperties): The properties of a policy.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/policies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingRoleAssignments@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BillingRoleAssignmentProperties](#billingroleassignmentproperties): The properties of the role assignment.
* **type**: 'Microsoft.Billing/billingAccounts/billingRoleAssignments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/customers/policies@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [CustomerPolicyProperties](#customerpolicyproperties): The properties of a customer's policy.
* **type**: 'Microsoft.Billing/billingAccounts/customers/policies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/departments/billingRoleAssignments@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BillingRoleAssignmentProperties](#billingroleassignmentproperties): The properties of the role assignment.
* **type**: 'Microsoft.Billing/billingAccounts/departments/billingRoleAssignments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/enrollmentAccounts/billingRoleAssignments@2019-10-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2019-10-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BillingRoleAssignmentProperties](#billingroleassignmentproperties): The properties of the role assignment.
* **type**: 'Microsoft.Billing/billingAccounts/enrollmentAccounts/billingRoleAssignments' (ReadOnly, DeployTimeConstant): The resource type

## Function acceptTransfer (Microsoft.Billing/transfers@2019-10-01-preview)
* **Resource**: Microsoft.Billing/transfers
* **ApiVersion**: 2019-10-01-preview
* **Input**: [AcceptTransferRequest](#accepttransferrequest)
* **Output**: [RecipientTransferDetails](#recipienttransferdetails)

## Function declineTransfer (Microsoft.Billing/transfers@2019-10-01-preview)
* **Resource**: Microsoft.Billing/transfers
* **ApiVersion**: 2019-10-01-preview
* **Output**: [RecipientTransferDetails](#recipienttransferdetails)

## Function download (Microsoft.Billing/billingAccounts/billingProfiles/invoices/pricesheet@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoices/pricesheet
* **ApiVersion**: 2019-10-01-preview
* **Output**: [DownloadUrl](#downloadurl)

## Function download (Microsoft.Billing/billingAccounts/billingProfiles/pricesheet@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/pricesheet
* **ApiVersion**: 2019-10-01-preview
* **Output**: [DownloadUrl](#downloadurl)

## Function downloadDocuments (Microsoft.Billing/billingAccounts@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2019-10-01-preview
* **Input**: string[]
* **Output**: [DownloadUrl](#downloadurl)

## Function downloadDocuments (Microsoft.Billing/billingAccounts/billingSubscriptions@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingSubscriptions
* **ApiVersion**: 2019-10-01-preview
* **Input**: string[]
* **Output**: [DownloadUrl](#downloadurl)

## Function downloadDocuments (Microsoft.Billing/billingAccounts/billingProfiles@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles
* **ApiVersion**: 2019-10-01-preview
* **Input**: string[]
* **Output**: [DownloadUrl](#downloadurl)

## Function initiateTransfer (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections
* **ApiVersion**: 2019-10-01-preview
* **Input**: [InitiateTransferRequest](#initiatetransferrequest)
* **Output**: [TransferDetails](#transferdetails)

## Function initiateTransfer (Microsoft.Billing/billingAccounts/billingProfiles/customers@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/customers
* **ApiVersion**: 2019-10-01-preview
* **Input**: [InitiateTransferRequest](#initiatetransferrequest)
* **Output**: [TransferDetails](#transferdetails)

## Function listInvoiceSectionsWithCreateSubscriptionPermission (Microsoft.Billing/billingAccounts@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2019-10-01-preview
* **Output**: [InvoiceSectionListWithCreateSubPermissionResult](#invoicesectionlistwithcreatesubpermissionresult)

## Function transfer (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/billingSubscriptions@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/billingSubscriptions
* **ApiVersion**: 2019-10-01-preview
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [TransferBillingSubscriptionResult](#transferbillingsubscriptionresult)

## Function transfer (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products
* **ApiVersion**: 2019-10-01-preview
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [Product](#product)

## Function updateAutoRenew (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products
* **ApiVersion**: 2019-10-01-preview
* **Input**: [UpdateAutoRenewRequest](#updateautorenewrequest)
* **Output**: [UpdateAutoRenewOperation](#updateautorenewoperation)

## Function validateTransfer (Microsoft.Billing/transfers@2019-10-01-preview)
* **Resource**: Microsoft.Billing/transfers
* **ApiVersion**: 2019-10-01-preview
* **Input**: [AcceptTransferRequest](#accepttransferrequest)
* **Output**: [ValidateTransferListResponse](#validatetransferlistresponse)

## Function validateTransferEligibility (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/billingSubscriptions@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/billingSubscriptions
* **ApiVersion**: 2019-10-01-preview
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [ValidateSubscriptionTransferEligibilityResult](#validatesubscriptiontransfereligibilityresult)

## Function validateTransferEligibility (Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products@2019-10-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/billingProfiles/invoiceSections/products
* **ApiVersion**: 2019-10-01-preview
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [ValidateProductTransferEligibilityResult](#validateproducttransfereligibilityresult)

## AcceptTransferProperties
### Properties
* **productDetails**: [ProductDetails](#productdetails)[]: Request parameters to accept transfer.

## AcceptTransferRequest
### Properties
* **properties**: [AcceptTransferProperties](#accepttransferproperties): Request parameters to accept transfer.

## AcceptTransferRequest
### Properties
* **properties**: [AcceptTransferProperties](#accepttransferproperties): Request parameters to accept transfer.

## AddressDetails
### Properties
* **addressLine1**: string: Address line 1.
* **addressLine2**: string: Address line 2.
* **addressLine3**: string: Address line 3.
* **city**: string: Address city.
* **companyName**: string: Company name.
* **country**: string: Country code uses ISO2, 2-digit format.
* **firstName**: string: First name.
* **lastName**: string: Last name.
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
* **address**: [AddressDetails](#addressdetails): Billing address.
* **billingRelationshipType**: 'CSPPartner' | 'Direct' | 'IndirectCustomer' | 'IndirectPartner' | string (ReadOnly): Identifies which services and purchases are paid by a billing profile.
* **currency**: string (ReadOnly): The currency in which the charges for the billing profile are billed.
* **displayName**: string: The name of the billing profile.
* **enabledAzurePlans**: [AzurePlan](#azureplan)[]: Information about the enabled azure plans.
* **indirectRelationshipInfo**: [IndirectRelationshipInfo](#indirectrelationshipinfo) (ReadOnly): Identifies the billing profile that is linked to another billing profile in indirect purchase motion.
* **invoiceDay**: int (ReadOnly): The day of the month when the invoice for the billing profile is generated.
* **invoiceEmailOptIn**: bool: Flag controlling whether the invoices for the billing profile are sent through email.
* **invoiceSections**: [InvoiceSection](#invoicesection)[]: The invoice sections associated to the billing profile.
* **poNumber**: string: The purchase order name that will appear on the invoices generated for the billing profile.
* **spendingLimit**: 'Off' | 'On' | string (ReadOnly): The billing profile spending limit.
* **status**: 'Active' | 'Disabled' | 'Warned' | string (ReadOnly): The status of the billing profile.
* **statusReasonCode**: 'PastDue' | 'SpendingLimitExpired' | 'SpendingLimitReached' | string (ReadOnly): Reason for the specified billing profile status.
* **targetClouds**: 'USGov' | 'USNat' | 'USSec' | string[] (ReadOnly): Identifies the cloud environments that are associated with a billing profile. This is a system managed optional field and gets updated as the billing profile gets associated with accounts in various clouds.

## BillingRoleAssignmentProperties
### Properties
* **createdByPrincipalId**: string (ReadOnly): The principal Id of the user who created the role assignment.
* **createdByPrincipalTenantId**: string (ReadOnly): The tenant Id of the user who created the role assignment.
* **createdByUserEmailAddress**: string (ReadOnly): The email address of the user who created the role assignment. This is supported only for billing accounts with agreement type Enterprise Agreement.
* **createdOn**: string (ReadOnly): The date the role assignment was created.
* **name**: string (ReadOnly): The name of the role assignment.
* **principalId**: string: The principal id of the user to whom the role was assigned.
* **principalTenantId**: string: The principal tenant id of the user to whom the role was assigned.
* **roleDefinitionId**: string: The ID of the role definition.
* **scope**: string (ReadOnly): The scope at which the role was assigned.
* **userAuthenticationType**: string: The authentication type of the user, whether Organization or MSA, of the user to whom the role was assigned. This is supported only for billing accounts with agreement type Enterprise Agreement.
* **userEmailAddress**: string: The email address of the user to whom the role was assigned. This is supported only for billing accounts with agreement type Enterprise Agreement.

## CustomerPolicyProperties
### Properties
* **viewCharges**: 'Allowed' | 'NotAllowed' | string: The policy that controls whether the users in customer's organization can view charges at pay-as-you-go prices.

## DetailedTransferStatus
### Properties
* **errorDetails**: [Error](#error): Error details for transfer execution.
* **productId**: string (ReadOnly): The ID of the product that is transferred.
* **productType**: 'AzureReservation' | 'AzureSubscription' | string (ReadOnly): Type of product that is transferred.
* **transferStatus**: 'Completed' | 'Failed' | 'InProgress' | 'NotStarted' | string (ReadOnly): Transfer status.

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

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC when the download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## Error
### Properties
* **errorCode**: string (ReadOnly): Error code.
* **errorMessage**: string (ReadOnly): Error message.

## IndirectRelationshipInfo
### Properties
* **billingAccountName**: string: The billing account name of the partner or the customer for an indirect motion.
* **billingProfileName**: string: The billing profile name of the partner or the customer for an indirect motion.
* **displayName**: string: The display name of the partner or customer for an indirect motion.

## InitiateTransferProperties
### Properties
* **recipientEmailId**: string: The email ID of the recipient to whom the transfer request is sent.
* **resellerId**: string: Optional MPN ID of the reseller for transfer requests that are sent from a Microsoft Partner Agreement billing account.

## InitiateTransferRequest
### Properties
* **properties**: [InitiateTransferProperties](#initiatetransferproperties): Request parameters to initiate transfer.

## InitiateTransferRequest
### Properties
* **properties**: [InitiateTransferProperties](#initiatetransferproperties): Request parameters to initiate transfer.

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
* **state**: 'Active' | 'Restricted' | string (ReadOnly): Identifies the state of an invoice section.
* **targetCloud**: 'USGov' | 'USNat' | 'USSec' | string (ReadOnly): Identifies the cloud environments that are associated with an invoice section. This is a system managed optional field and gets updated as the invoice section gets associated with accounts in various clouds.

## InvoiceSectionWithCreateSubPermission
### Properties
* **billingProfileDisplayName**: string (ReadOnly): The name of the billing profile for the invoice section.
* **billingProfileId**: string (ReadOnly): The ID of the billing profile for the invoice section.
* **billingProfileSpendingLimit**: 'Off' | 'On' | string (ReadOnly): The billing profile spending limit.
* **billingProfileStatus**: 'Active' | 'Disabled' | 'Warned' | string (ReadOnly): The status of the billing profile.
* **billingProfileStatusReasonCode**: 'PastDue' | 'SpendingLimitExpired' | 'SpendingLimitReached' | string (ReadOnly): Reason for the specified billing profile status.
* **enabledAzurePlans**: [AzurePlan](#azureplan)[]: Enabled azure plans for the associated billing profile.
* **invoiceSectionDisplayName**: string (ReadOnly): The name of the invoice section.
* **invoiceSectionId**: string (ReadOnly): The ID of the invoice section.

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

## ProductDetails
### Properties
* **productId**: string: The ID of the product that is transferred.
* **productType**: 'AzureReservation' | 'AzureSubscription' | string: Type of the product that is transferred.

## ProductProperties
### Properties
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
* **parentProductId**: string (ReadOnly): Parent product Id.
* **productType**: string (ReadOnly): The description of the type of product.
* **productTypeId**: string (ReadOnly): The ID of the type of product.
* **purchaseDate**: string (ReadOnly): The date when the product was purchased.
* **quantity**: int (ReadOnly): The quantity purchased for the product.
* **reseller**: [Reseller](#reseller) (ReadOnly): Reseller for this product.
* **skuDescription**: string (ReadOnly): The sku description of the product.
* **skuId**: string (ReadOnly): The sku ID of the product.
* **status**: 'Active' | 'AutoRenew' | 'Cancelled' | 'Disabled' | 'Expired' | 'Expiring' | 'Inactive' | 'PastDue' | string: The current status of the product.
* **tenantId**: string (ReadOnly): The id of the tenant in which the product is used.

## RecipientTransferDetails
### Properties
* **properties**: [RecipientTransferProperties](#recipienttransferproperties): Details of the transfer.

## RecipientTransferDetails
### Properties
* **properties**: [RecipientTransferProperties](#recipienttransferproperties): Details of the transfer.

## RecipientTransferProperties
### Properties
* **allowedProductType**: 'AzureReservation' | 'DevTestAzureSubscription' | 'StandardAzureSubscription' | string[] (ReadOnly): Type of subscriptions that can be transferred.
* **canceledBy**: string (ReadOnly): The email ID of the user who canceled the transfer request.
* **creationTime**: string (ReadOnly): The time at which the transfer request was created.
* **detailedTransferStatus**: [DetailedTransferStatus](#detailedtransferstatus)[] (ReadOnly): Detailed transfer status.
* **expirationTime**: string (ReadOnly): The time at which the transfer request expires.
* **initiatorCustomerType**: string (ReadOnly): The type of customer who sent the transfer request.
* **initiatorEmailId**: string (ReadOnly): The email ID of the user who sent the transfer request.
* **lastModifiedTime**: string (ReadOnly): The time at which the transfer request was last modified.
* **recipientEmailId**: string (ReadOnly): The email ID of the user to whom the transfer request was sent.
* **resellerId**: string (ReadOnly): Optional MPN ID of the reseller for transfer requests that are sent from a Microsoft Partner Agreement billing account.
* **resellerName**: string (ReadOnly): Optional name of the reseller for transfer requests that are sent from Microsoft Partner Agreement billing account.
* **transferStatus**: 'Canceled' | 'Completed' | 'CompletedWithErrors' | 'Declined' | 'Failed' | 'InProgress' | 'Pending' | string (ReadOnly): Overall transfer status.

## Reseller
### Properties
* **description**: string (ReadOnly): The name of the reseller.
* **resellerId**: string (ReadOnly): The MPN ID of the reseller.

## TransferBillingSubscriptionRequestProperties
### Properties
* **destinationBillingProfileId**: string: The destination billing profile id.
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## TransferBillingSubscriptionRequestProperties
### Properties
* **destinationBillingProfileId**: string: The destination billing profile id.
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## TransferBillingSubscriptionResult
### Properties
* **properties**: [TransferBillingSubscriptionResultProperties](#transferbillingsubscriptionresultproperties): Properties of the transfer billing subscription operation result.

## TransferBillingSubscriptionResultProperties
### Properties
* **billingSubscriptionName**: string: The destination billing subscription id.

## TransferDetails
### Properties
* **properties**: [TransferProperties](#transferproperties): Details of the transfer.

## TransferDetails
### Properties
* **properties**: [TransferProperties](#transferproperties): Details of the transfer.

## TransferProductRequestProperties
### Properties
* **destinationBillingProfileId**: string: The destination billing profile id.
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## TransferProductRequestProperties
### Properties
* **destinationBillingProfileId**: string: The destination billing profile id.
* **destinationInvoiceSectionId**: string: The destination invoice section id.

## TransferProperties
### Properties
* **billingAccountId**: string (ReadOnly): The ID of the billing account to which the product is billed after the transfer request is completed.
* **billingProfileId**: string (ReadOnly): The ID of the billing profile to which the product will be billed after the transfer.
* **canceledBy**: string (ReadOnly): The email ID of the user who canceled the transfer request.
* **creationTime**: string (ReadOnly): The time at which the transfer request was created.
* **detailedTransferStatus**: [DetailedTransferStatus](#detailedtransferstatus)[] (ReadOnly): Detailed transfer status.
* **expirationTime**: string (ReadOnly): The time at which the transfer request expires.
* **initiatorCustomerType**: string (ReadOnly): The type of customer who sent the transfer request.
* **initiatorEmailId**: string (ReadOnly): The email ID of the user who sent the transfer request.
* **invoiceSectionId**: string (ReadOnly): The ID of the invoice section to which the product is billed after the transfer request is completed.
* **lastModifiedTime**: string (ReadOnly): The time at which the transfer request was last modified.
* **recipientEmailId**: string (ReadOnly): The email ID of the user to whom the transfer request was sent.
* **resellerId**: string (ReadOnly): Optional MPN ID of the reseller for transfer requests that are sent from a Microsoft Partner Agreement billing account.
* **resellerName**: string (ReadOnly): Optional name of the reseller for transfer requests that are sent from Microsoft Partner Agreement billing account.
* **transferStatus**: 'Canceled' | 'Completed' | 'CompletedWithErrors' | 'Declined' | 'Failed' | 'InProgress' | 'Pending' | string (ReadOnly): Overall transfer status.

## UpdateAutoRenewOperation
### Properties
* **properties**: [UpdateAutoRenewOperationProperties](#updateautorenewoperationproperties): Summary of update auto renew operation properties

## UpdateAutoRenewOperationProperties
### Properties
* **endDate**: string: The date at which the product will be canceled.

## UpdateAutoRenewRequest
### Properties
* **autoRenew**: 'false' | 'true' | string: The flag that determines the auto-renew settings for a product.

## ValidateProductTransferEligibilityError
### Properties
* **code**: 'CrossBillingAccountNotAllowed' | 'DestinationBillingProfilePastDue' | 'InsufficientPermissionOnDestination' | 'InsufficientPermissionOnSource' | 'InvalidSource' | 'NotAvailableForDestinationMarket' | 'OneTimePurchaseProductTransferNotAllowed' | 'ProductNotActive' | 'ProductTypeNotSupported' | string: Error code for the product transfer validation.
* **details**: string: Detailed error message explaining the error.
* **message**: string: The error message.

## ValidateProductTransferEligibilityResult
### Properties
* **errorDetails**: [ValidateProductTransferEligibilityError](#validateproducttransfereligibilityerror): Validation error details.
* **isTransferEligible**: bool (ReadOnly): Specifies whether the transfer is eligible or not.

## ValidateSubscriptionTransferEligibilityError
### Properties
* **code**: 'BillingAccountInactive' | 'CrossBillingAccountNotAllowed' | 'DestinationBillingProfileInactive' | 'DestinationBillingProfileNotFound' | 'DestinationBillingProfilePastDue' | 'DestinationInvoiceSectionInactive' | 'DestinationInvoiceSectionNotFound' | 'InsufficientPermissionOnDestination' | 'InsufficientPermissionOnSource' | 'InvalidDestination' | 'InvalidSource' | 'MarketplaceNotEnabledOnDestination' | 'NotAvailableForDestinationMarket' | 'ProductInactive' | 'ProductNotFound' | 'ProductTypeNotSupported' | 'SourceBillingProfilePastDue' | 'SourceInvoiceSectionInactive' | 'SubscriptionNotActive' | 'SubscriptionTypeNotSupported' | string: Error code for the product transfer validation.
* **details**: string: Detailed error message explaining the error.
* **message**: string: The error message.

## ValidateSubscriptionTransferEligibilityResult
### Properties
* **errorDetails**: [ValidateSubscriptionTransferEligibilityError](#validatesubscriptiontransfereligibilityerror): Validation error details.
* **isTransferEligible**: bool (ReadOnly): Specifies whether the subscription is eligible to be transferred.

## ValidateTransferListResponse
### Properties
* **value**: [ValidateTransferResponse](#validatetransferresponse)[] (ReadOnly): The list of transfer validation results.

## ValidateTransferResponse
### Properties
* **properties**: [ValidateTransferResponseProperties](#validatetransferresponseproperties): The properties of transfer validation response.

## ValidateTransferResponseProperties
### Properties
* **productId**: string (ReadOnly): The product id for which this result applies.
* **results**: [ValidationResultProperties](#validationresultproperties)[]: The array of validation results.
* **status**: string (ReadOnly): The status of validation

## ValidationResultProperties
### Properties
* **code**: string (ReadOnly): Result Code.
* **level**: string (ReadOnly): Result Level.
* **message**: string (ReadOnly): The validation message.

