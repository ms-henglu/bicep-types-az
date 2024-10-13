# Microsoft.CertificateRegistration @ 2015-08-01

## Resource Microsoft.CertificateRegistration/certificateOrders@2015-08-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-08-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateOrderProperties](#certificateorderproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.CertificateRegistration/certificateOrders' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.CertificateRegistration/certificateOrders/certificates@2015-08-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-08-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateOrderCertificateProperties](#certificateordercertificateproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.CertificateRegistration/certificateOrders/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Function reissue (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Input**: [ReissueCertificateOrderRequest](#reissuecertificateorderrequest)
* **Output**: any

## Function renew (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Input**: [RenewCertificateOrderRequest](#renewcertificateorderrequest)
* **Output**: any

## Function resendEmail (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Output**: any

## Function retrieveCertificateActions (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Output**: [CertificateOrderAction](#certificateorderaction)[]

## Function retrieveEmailHistory (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Output**: [CertificateEmail](#certificateemail)[]

## Function verifyDomainOwnership (Microsoft.CertificateRegistration/certificateOrders@2015-08-01)
* **Resource**: Microsoft.CertificateRegistration/certificateOrders
* **ApiVersion**: 2015-08-01
* **Output**: any

## CertificateDetails
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [CertificateDetailsProperties](#certificatedetailsproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## CertificateDetailsProperties
### Properties
* **issuer**: string: Issuer
* **notAfter**: string: Valid to
* **notBefore**: string: Valid from
* **rawData**: string: Raw certificate data
* **serialNumber**: string: Serial Number
* **signatureAlgorithm**: string: Signature Algorithm
* **subject**: string: Subject
* **thumbprint**: string: Thumbprint
* **version**: int: Version

## CertificateEmail
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [CertificateEmailProperties](#certificateemailproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## CertificateEmailProperties
### Properties
* **emailId**: string: Email id
* **timeStamp**: string: Time stamp

## CertificateOrderAction
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [CertificateOrderActionProperties](#certificateorderactionproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## CertificateOrderActionProperties
### Properties
* **createdAt**: string: Time at which the certificate action was performed
* **type**: 'CertificateIssued' | 'CertificateOrderCanceled' | 'CertificateOrderCreated' | 'CertificateRevoked' | 'DomainValidationComplete' | 'FraudDetected' | 'OrgNameChange' | 'OrgValidationComplete' | 'SanDrop' (Required): Type

## CertificateOrderCertificate
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [CertificateOrderCertificateProperties](#certificateordercertificateproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## CertificateOrderCertificateProperties
### Properties
* **keyVaultId**: string: Key Vault Csm resource Id
* **keyVaultSecretName**: string: Key Vault secret name
* **provisioningState**: 'AzureServiceUnauthorizedToAccessKeyVault' | 'CertificateOrderFailed' | 'Initialized' | 'KeyVaultDoesNotExist' | 'KeyVaultSecretDoesNotExist' | 'OperationNotPermittedOnKeyVault' | 'Succeeded' | 'Unknown' | 'UnknownError' | 'WaitingOnCertificateOrder': Status of the Key Vault secret

## CertificateOrderProperties
### Properties
* **autoRenew**: bool: Auto renew
* **certificates**: [CertificateOrderPropertiesCertificates](#certificateorderpropertiescertificates): State of the Key Vault secret
* **csr**: string: Last CSR that was created for this order
* **distinguishedName**: string: Certificate distinguished name
* **domainVerificationToken**: string: Domain Verification Token
* **expirationTime**: string: Certificate expiration time
* **intermediate**: [CertificateDetails](#certificatedetails): Intermediate certificate
* **keySize**: int: Certificate Key Size
* **lastCertificateIssuanceTime**: string: Certificate last issuance time
* **productType**: 'StandardDomainValidatedSsl' | 'StandardDomainValidatedWildCardSsl': Certificate product type
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded': Status of certificate order
* **root**: [CertificateDetails](#certificatedetails): Root certificate
* **serialNumber**: string: Current serial number of the certificate
* **signedCertificate**: [CertificateDetails](#certificatedetails): Signed certificate
* **status**: 'Canceled' | 'Denied' | 'Expired' | 'Issued' | 'NotSubmitted' | 'PendingRekey' | 'Pendingissuance' | 'Pendingrevocation' | 'Revoked' | 'Unused': Current order status
* **validityInYears**: int: Duration in years (must be between 1 and 3)

## CertificateOrderPropertiesCertificates
### Properties
### Additional Properties
* **Additional Properties Type**: [CertificateOrderCertificate](#certificateordercertificate)

## ReissueCertificateOrderRequest
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [ReissueCertificateOrderRequestProperties](#reissuecertificateorderrequestproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## ReissueCertificateOrderRequestProperties
### Properties
* **delayExistingRevokeInHours**: int: Delay in hours to revoke existing certificate after the new certificate is issued
* **keySize**: int: Certificate Key Size

## RenewCertificateOrderRequest
### Properties
* **id**: string: Resource Id
* **kind**: string: Kind of resource
* **location**: string (Required): Resource Location
* **name**: string: Resource Name
* **properties**: [RenewCertificateOrderRequestProperties](#renewcertificateorderrequestproperties)
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: string: Resource type

## RenewCertificateOrderRequestProperties
### Properties
* **keySize**: int: Certificate Key Size

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

