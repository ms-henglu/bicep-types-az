# Microsoft.Billing @ 2018-11-01-preview

## Resource Microsoft.Billing/billingAccounts/billingProfiles@2018-11-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BillingProfileProperties](#billingprofileproperties): A billing profile.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/billingProfiles/policies@2018-11-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [PolicyProperties](#policyproperties): The properties of policy.
* **type**: 'Microsoft.Billing/billingAccounts/billingProfiles/policies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/invoiceSections@2018-11-01-preview
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties): The InvoiceSection.
* **type**: 'Microsoft.Billing/billingAccounts/invoiceSections' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Billing/billingAccounts/lineOfCredit@2018-11-01-preview
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-11-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [LineOfCreditProperties](#lineofcreditproperties): A line of credit.
* **type**: 'Microsoft.Billing/billingAccounts/lineOfCredit' (ReadOnly, DeployTimeConstant): The resource type

## Function acceptTransfer (Microsoft.Billing/transfers@2018-11-01-preview)
* **Resource**: Microsoft.Billing/transfers
* **ApiVersion**: 2018-11-01-preview
* **Input**: [AcceptTransferRequest](#accepttransferrequest)
* **Output**: [RecipientTransferDetails](#recipienttransferdetails)

## Function billingProfiles (Microsoft.Billing/billingAccounts@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2018-11-01-preview
* **Input**: [BillingProfileCreationParameters](#billingprofilecreationparameters)
* **Output**: [BillingProfile](#billingprofile)

## Function declineTransfer (Microsoft.Billing/transfers@2018-11-01-preview)
* **Resource**: Microsoft.Billing/transfers
* **ApiVersion**: 2018-11-01-preview
* **Output**: [RecipientTransferDetails](#recipienttransferdetails)

## Function download (Microsoft.Billing/billingAccounts/invoices/pricesheet@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoices/pricesheet
* **ApiVersion**: 2018-11-01-preview
* **Output**: [DownloadUrl](#downloadurl)

## Function initiateTransfer (Microsoft.Billing/billingAccounts/invoiceSections@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections
* **ApiVersion**: 2018-11-01-preview
* **Input**: [InitiateTransferRequest](#initiatetransferrequest)
* **Output**: [TransferDetails](#transferdetails)

## Function invoiceSections (Microsoft.Billing/billingAccounts@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts
* **ApiVersion**: 2018-11-01-preview
* **Input**: [InvoiceSectionCreationRequest](#invoicesectioncreationrequest)
* **Output**: [InvoiceSection](#invoicesection)

## Function transfer (Microsoft.Billing/billingAccounts/invoiceSections/billingSubscriptions@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections/billingSubscriptions
* **ApiVersion**: 2018-11-01-preview
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [TransferBillingSubscriptionResult](#transferbillingsubscriptionresult)

## Function transfer (Microsoft.Billing/billingAccounts/invoiceSections/products@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections/products
* **ApiVersion**: 2018-11-01-preview
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [ProductSummary](#productsummary)

## Function updateAutoRenew (Microsoft.Billing/billingAccounts/invoiceSections/products@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections/products
* **ApiVersion**: 2018-11-01-preview
* **Input**: [UpdateAutoRenewRequest](#updateautorenewrequest)
* **Output**: [UpdateAutoRenewOperationSummary](#updateautorenewoperationsummary)

## Function updateAutoRenew (Microsoft.Billing/billingAccounts/products@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/products
* **ApiVersion**: 2018-11-01-preview
* **Input**: [UpdateAutoRenewRequest](#updateautorenewrequest)
* **Output**: [UpdateAutoRenewOperationSummary](#updateautorenewoperationsummary)

## Function validateTransferEligibility (Microsoft.Billing/billingAccounts/invoiceSections/billingSubscriptions@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections/billingSubscriptions
* **ApiVersion**: 2018-11-01-preview
* **Input**: [TransferBillingSubscriptionRequestProperties](#transferbillingsubscriptionrequestproperties)
* **Output**: [ValidateSubscriptionTransferEligibilityResult](#validatesubscriptiontransfereligibilityresult)

## Function validateTransferEligibility (Microsoft.Billing/billingAccounts/invoiceSections/products@2018-11-01-preview)
* **Resource**: Microsoft.Billing/billingAccounts/invoiceSections/products
* **ApiVersion**: 2018-11-01-preview
* **Input**: [TransferProductRequestProperties](#transferproductrequestproperties)
* **Output**: [ValidateProductTransferEligibilityResult](#validateproducttransfereligibilityresult)

## AcceptTransferProperties
### Properties
* **productDetails**: [ProductDetails](#productdetails)[]: Request parameters to accept transfer.

## AcceptTransferRequest
### Properties
* **properties**: [AcceptTransferProperties](#accepttransferproperties): Request parameters to accept transfer.

## Address
### Properties
* **addressLine1**: string: Address Line1.
* **addressLine2**: string: Address Line2.
* **addressLine3**: string: Address Line3.
* **city**: string: Address City.
* **companyName**: string: Company Name.
* **country**: string: Country code uses ISO2, 2-digit format.
* **firstName**: string: First Name.
* **lastName**: string: Last Name.
* **postalCode**: string: Address Postal Code.
* **region**: string: Address Region.

## Amount
### Properties
* **currency**: string (ReadOnly): The currency for the amount value.
* **value**: int: Amount value.

## BillingProfile
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [BillingProfileProperties](#billingprofileproperties): A billing profile.
* **type**: string (ReadOnly): Resource type.

## BillingProfile
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [BillingProfileProperties](#billingprofileproperties): A billing profile.
* **type**: string (ReadOnly): Resource type.

## BillingProfileCreationParameters
### Properties
* **address**: [Address](#address): Billing address.
* **displayName**: string: The billing profile name.
* **enableAzureSKUs**: [EnabledAzureSKUs](#enabledazureskus)[]: Azure skus to enable for this billing profile..
* **invoiceEmailOptIn**: bool: If the billing profile is opted in to receive invoices via email.
* **poNumber**: string: Purchase order number.

## BillingProfileProperties
### Properties
* **address**: [Address](#address): Billing address.
* **currency**: string (ReadOnly): The currency associated with the billing profile.
* **displayName**: string: The billing profile name.
* **enabledAzureSKUs**: [EnabledAzureSKUs](#enabledazureskus)[]: Information about the product.
* **invoiceDay**: int (ReadOnly): Invoice day.
* **invoiceEmailOptIn**: bool (ReadOnly): If the billing profile is opted in to receive invoices via email.
* **invoiceSections**: [InvoiceSection](#invoicesection)[]: The invoice sections associated to the billing profile.
* **isClassic**: bool (ReadOnly): Is OMS bootstrapped billing profile.
* **poNumber**: string: Purchase order number.

## DetailedTransferStatus
### Properties
* **errorDetails**: [Error](#error): Error details for transfer execution.
* **productId**: string (ReadOnly): Id of product being transferred.
* **productType**: 'AzureReservation' | 'AzureSubscription' | string (ReadOnly): Type of product being transferred.
* **transferStatus**: 'Completed' | 'Failed' | 'InProgress' | 'NotStarted' | string (ReadOnly): Transfer status.

## DownloadUrl
### Properties
* **expiryTime**: string (ReadOnly): The time in UTC at which this download URL will expire.
* **url**: string (ReadOnly): The URL to the PDF file.

## EnabledAzureSKUs
### Properties
* **skuDescription**: string (ReadOnly): The sku description.
* **skuId**: string: The sku id.

## Error
### Properties
* **errorCode**: string (ReadOnly): Error code.
* **errorMessage**: string (ReadOnly): Error message.

## InitiateTransferProperties
### Properties
* **billingProfileId**: string: Target Usage context for devTest subscriptions.
* **recipientEmailId**: string: Email Id of recipient for transfer.

## InitiateTransferRequest
### Properties
* **properties**: [InitiateTransferProperties](#initiatetransferproperties): Request parameters to initiate transfer.

## InvoiceSection
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties): The InvoiceSection.
* **type**: string (ReadOnly): Resource type.

## InvoiceSection
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [InvoiceSectionProperties](#invoicesectionproperties): The InvoiceSection.
* **type**: string (ReadOnly): Resource type.

## InvoiceSectionCreationRequest
### Properties
* **billingProfileId**: string: The billing profile id.
* **displayName**: string: The name of the InvoiceSection.

## InvoiceSectionProperties
### Properties
* **billingProfiles**: [BillingProfile](#billingprofile)[]: The billing profiles associated to the billing account.
* **displayName**: string: The name of the InvoiceSection.

## LineOfCreditProperties
### Properties
* **creditLimit**: [Amount](#amount): The current credit limit.
* **reason**: string (ReadOnly): The reason for the line of credit status when not approved.
* **remainingBalance**: [Amount](#amount) (ReadOnly): Remaining balance.
* **status**: 'Approved' | 'Rejected' | string: The line of credit status.

## PolicyProperties
### Properties
* **marketplacePurchasesAllowed**: bool: The marketplacePurchasesAllowed flag.
* **reservationPurchasesAllowed**: bool: The reservationPurchasesAllowed flag.
* **subscriptionOwnerCanViewCharges**: bool: The subscriptionOwnerCanViewCharges flag.

## ProductDetails
### Properties
* **productId**: string: Id of product to be transferred.
* **productType**: 'AzureReservation' | 'AzureSubscription' | string: Type of the product to be transferred.

## ProductSummary
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [ProductSummaryProperties](#productsummaryproperties): The properties of the product summary.
* **type**: string (ReadOnly): Resource type.

## ProductSummaryProperties
### Properties
* **availabilityId**: string (ReadOnly): Availability Id.
* **billingFrequency**: 'Monthly' | 'OneTime' | 'UsageBased' | string: Billing frequency.
* **billingProfileId**: string (ReadOnly): Billing Profile id to which this product belongs.
* **billingProfileName**: string (ReadOnly): Billing Profile name to which this product belongs.
* **displayName**: string (ReadOnly): The display name of the product.
* **endDate**: string (ReadOnly): end date.
* **invoiceSectionId**: string (ReadOnly): Invoice section id to which this product belongs.
* **invoiceSectionName**: string (ReadOnly): Invoice section name to which this product belongs.
* **lastCharge**: [Amount](#amount) (ReadOnly): Last month charges.
* **lastChargeDate**: string (ReadOnly): The date of the last charge.
* **parentProductId**: string (ReadOnly): Parent Product Id.
* **productType**: string (ReadOnly): The type of product.
* **productTypeId**: string (ReadOnly): The product type id.
* **purchaseDate**: string (ReadOnly): The date of purchase.
* **quantity**: int (ReadOnly): The purchased product quantity.
* **skuDescription**: string (ReadOnly): Sku description.
* **skuId**: string (ReadOnly): Sku Id.
* **status**: 'Active' | 'AutoRenew' | 'Cancelled' | 'Disabled' | 'Expired' | 'Expiring' | 'Inactive' | 'PastDue' | string: Product status.

## RecipientTransferDetails
### Properties
* **properties**: [RecipientTransferProperties](#recipienttransferproperties): Details of the transfer.

## RecipientTransferDetails
### Properties
* **properties**: [RecipientTransferProperties](#recipienttransferproperties): Details of the transfer.

## RecipientTransferProperties
### Properties
* **allowedProductType**: 'AzureReservation' | 'DevTestAzureSubscription' | 'StandardAzureSubscription' | string[] (ReadOnly): Type of subscriptions that can be transferred.
* **canceledBy**: string (ReadOnly): Email Id who user canceled the transfer.
* **creationTime**: string (ReadOnly): Transfer creation time.
* **detailedTransferStatus**: [DetailedTransferStatus](#detailedtransferstatus)[] (ReadOnly): Detailed transfer status.
* **expirationTime**: string (ReadOnly): Transfer expiration time.
* **initiatorEmailId**: string (ReadOnly): Email Id of initiator of transfer.
* **lastModifiedTime**: string (ReadOnly): Transfer last modification time.
* **recipientEmailId**: string (ReadOnly): Email Id of recipient of transfer.
* **transferStatus**: 'Canceled' | 'Completed' | 'CompletedWithErrors' | 'Declined' | 'Failed' | 'InProgress' | 'Pending' | string (ReadOnly): Overall transfer status.

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
* **properties**: [TransferBillingSubscriptionResultProperties](#transferbillingsubscriptionresultproperties): Request parameters to transfer billing subscription.

## TransferBillingSubscriptionResultProperties
### Properties
* **billingSubscriptionName**: string: The destination billing subscription id.

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
* **billingAccountId**: string (ReadOnly): Target billing account Id.
* **canceledBy**: string (ReadOnly): Email Id who user canceled the transfer.
* **creationTime**: string (ReadOnly): Transfer creation time.
* **detailedTransferStatus**: [DetailedTransferStatus](#detailedtransferstatus)[] (ReadOnly): Detailed transfer status.
* **expirationTime**: string (ReadOnly): Transfer expiration time.
* **initiatorEmailId**: string (ReadOnly): Email Id of initiator of transfer.
* **invoiceSectionId**: string (ReadOnly): Target invoice section Id.
* **lastModifiedTime**: string (ReadOnly): Transfer last modification time.
* **recipientEmailId**: string (ReadOnly): Email Id of recipient of transfer.
* **transferStatus**: 'Canceled' | 'Completed' | 'CompletedWithErrors' | 'Declined' | 'Failed' | 'InProgress' | 'Pending' | string (ReadOnly): Overall transfer status.

## UpdateAutoRenewOperationSummary
### Properties
* **properties**: [UpdateAutoRenewOperationSummaryProperties](#updateautorenewoperationsummaryproperties): Summary of update auto renew operation summary properties

## UpdateAutoRenewOperationSummary
### Properties
* **properties**: [UpdateAutoRenewOperationSummaryProperties](#updateautorenewoperationsummaryproperties): Summary of update auto renew operation summary properties

## UpdateAutoRenewOperationSummaryProperties
### Properties
* **endDate**: string: The end date of this asset

## UpdateAutoRenewRequest
### Properties
* **autoRenew**: 'false' | 'true' | string: Request parameters to update auto renew policy a product.

## UpdateAutoRenewRequest
### Properties
* **autoRenew**: 'false' | 'true' | string: Request parameters to update auto renew policy a product.

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
* **code**: 'CrossBillingAccountNotAllowed' | 'DestinationBillingProfilePastDue' | 'InsufficientPermissionOnDestination' | 'InsufficientPermissionOnSource' | 'InvalidSource' | 'NotAvailableForDestinationMarket' | 'SubscriptionNotActive' | 'SubscriptionTypeNotSupported' | string: Error code for the product transfer validation.
* **details**: string: Detailed error message explaining the error.
* **message**: string: The error message.

## ValidateSubscriptionTransferEligibilityResult
### Properties
* **errorDetails**: [ValidateSubscriptionTransferEligibilityError](#validatesubscriptiontransfereligibilityerror): Validation error details.
* **isTransferEligible**: bool (ReadOnly): Specifies whether the transfer is eligible or not.

