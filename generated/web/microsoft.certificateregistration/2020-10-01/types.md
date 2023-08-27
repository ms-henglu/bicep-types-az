# Microsoft.CertificateRegistration @ 2020-10-01

## Resource Microsoft.CertificateRegistration/certificateOrders@2020-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServiceCertificateOrderProperties](#appservicecertificateorderproperties): AppServiceCertificateOrder resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.CertificateRegistration/certificateOrders' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.CertificateRegistration/certificateOrders/certificates@2020-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServiceCertificate](#appservicecertificate): Core resource properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.CertificateRegistration/certificateOrders/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Function reissue (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Input**: [ReissueCertificateOrderRequest](#reissuecertificateorderrequest)

## Function renew (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Input**: [RenewCertificateOrderRequest](#renewcertificateorderrequest)

## Function resendEmail (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01

## Function resendRequestEmails (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Input**: [NameIdentifier](#nameidentifier)

## Function retrieveCertificateActions (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Output**: [CertificateOrderAction](#certificateorderaction)[]

## Function retrieveEmailHistory (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Output**: [CertificateEmail](#certificateemail)[]

## Function retrieveSiteSeal (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01
* **Input**: [SiteSealRequest](#sitesealrequest)
* **Output**: [SiteSeal](#siteseal)

## Function verifyDomainOwnership (Microsoft.CertificateRegistration/certificateOrders@2020-10-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2020-10-01

## AppServiceCertificate
### Properties
* **keyVaultId**: string: Key Vault resource Id.
* **keyVaultSecretName**: string: Key Vault secret name.
* **provisioningState**: 'AzureServiceUnauthorizedToAccessKeyVault' | 'CertificateOrderFailed' | 'ExternalPrivateKey' | 'Initialized' | 'KeyVaultDoesNotExist' | 'KeyVaultSecretDoesNotExist' | 'OperationNotPermittedOnKeyVault' | 'Succeeded' | 'Unknown' | 'UnknownError' | 'WaitingOnCertificateOrder' (ReadOnly): Status of the Key Vault secret.

## AppServiceCertificateOrderProperties
### Properties
* **appServiceCertificateNotRenewableReasons**: 'ExpirationNotInRenewalTimeRange' | 'RegistrationStatusNotSupportedForRenewal' | 'SubscriptionNotActive' | string[] (ReadOnly): Reasons why App Service Certificate is not renewable at the current moment.
* **autoRenew**: bool: <code>true</code> if the certificate should be automatically renewed when it expires; otherwise, <code>false</code>.
* **certificates**: [AppServiceCertificateOrderPropertiesCertificates](#appservicecertificateorderpropertiescertificates): State of the Key Vault secret.
* **csr**: string: Last CSR that was created for this order.
* **distinguishedName**: string: Certificate distinguished name.
* **domainVerificationToken**: string (ReadOnly): Domain verification token.
* **expirationTime**: string (ReadOnly): Certificate expiration time.
* **intermediate**: [CertificateDetails](#certificatedetails) (ReadOnly): Intermediate certificate.
* **isPrivateKeyExternal**: bool (ReadOnly): <code>true</code> if private key is external; otherwise, <code>false</code>.
* **keySize**: int: Certificate key size.
* **lastCertificateIssuanceTime**: string (ReadOnly): Certificate last issuance time.
* **nextAutoRenewalTimeStamp**: string (ReadOnly): Time stamp when the certificate would be auto renewed next
* **productType**: 'StandardDomainValidatedSsl' | 'StandardDomainValidatedWildCardSsl' (Required): Certificate product type.
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded' (ReadOnly): Status of certificate order.
* **root**: [CertificateDetails](#certificatedetails) (ReadOnly): Root certificate.
* **serialNumber**: string (ReadOnly): Current serial number of the certificate.
* **signedCertificate**: [CertificateDetails](#certificatedetails) (ReadOnly): Signed certificate.
* **status**: 'Canceled' | 'Denied' | 'Expired' | 'Issued' | 'NotSubmitted' | 'PendingRekey' | 'Pendingissuance' | 'Pendingrevocation' | 'Revoked' | 'Unused' (ReadOnly): Current order status.
* **validityInYears**: int: Duration in years (must be between 1 and 3).

## AppServiceCertificateOrderPropertiesCertificates
### Properties
### Additional Properties
* **Additional Properties Type**: [AppServiceCertificate](#appservicecertificate)

## CertificateDetails
### Properties
* **issuer**: string (ReadOnly): Certificate Issuer.
* **notAfter**: string (ReadOnly): Date Certificate is valid to.
* **notBefore**: string (ReadOnly): Date Certificate is valid from.
* **rawData**: string (ReadOnly): Raw certificate data.
* **serialNumber**: string (ReadOnly): Certificate Serial Number.
* **signatureAlgorithm**: string (ReadOnly): Certificate Signature algorithm.
* **subject**: string (ReadOnly): Certificate Subject.
* **thumbprint**: string (ReadOnly): Certificate Thumbprint.
* **version**: int (ReadOnly): Certificate Version.

## CertificateEmail
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [CertificateEmailProperties](#certificateemailproperties): CertificateEmail resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: string (ReadOnly): Resource type.

## CertificateEmailProperties
### Properties
* **emailId**: string: Email id.
* **timeStamp**: string: Time stamp.

## CertificateOrderAction
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [CertificateOrderActionProperties](#certificateorderactionproperties): CertificateOrderAction resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: string (ReadOnly): Resource type.

## CertificateOrderActionProperties
### Properties
* **actionType**: 'CertificateExpirationWarning' | 'CertificateExpired' | 'CertificateIssued' | 'CertificateOrderCanceled' | 'CertificateOrderCreated' | 'CertificateRevoked' | 'DomainValidationComplete' | 'FraudCleared' | 'FraudDetected' | 'FraudDocumentationRequired' | 'OrgNameChange' | 'OrgValidationComplete' | 'SanDrop' | 'Unknown' (ReadOnly): Action type.
* **createdAt**: string (ReadOnly): Time at which the certificate action was performed.

## NameIdentifier
### Properties
* **name**: string: Name of the object.

## ReissueCertificateOrderRequest
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [ReissueCertificateOrderRequestProperties](#reissuecertificateorderrequestproperties): ReissueCertificateOrderRequest resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: string (ReadOnly): Resource type.

## ReissueCertificateOrderRequestProperties
### Properties
* **csr**: string: Csr to be used for re-key operation.
* **delayExistingRevokeInHours**: int: Delay in hours to revoke existing certificate after the new certificate is issued.
* **isPrivateKeyExternal**: bool: Should we change the ASC type (from managed private key to external private key and vice versa).
* **keySize**: int: Certificate Key Size.

## RenewCertificateOrderRequest
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [RenewCertificateOrderRequestProperties](#renewcertificateorderrequestproperties): RenewCertificateOrderRequest resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: string (ReadOnly): Resource type.

## RenewCertificateOrderRequestProperties
### Properties
* **csr**: string: Csr to be used for re-key operation.
* **isPrivateKeyExternal**: bool: Should we change the ASC type (from managed private key to external private key and vice versa).
* **keySize**: int: Certificate Key Size.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SiteSeal
### Properties
* **html**: string (Required): HTML snippet

## SiteSealRequest
### Properties
* **lightTheme**: bool: If <code>true</code> use the light color theme for site seal; otherwise, use the default color theme.
* **locale**: string: Locale of site seal.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

