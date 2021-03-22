# Microsoft.CertificateRegistration @ 2020-10-01

## Resource Microsoft.CertificateRegistration/certificateOrders@2020-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-01' (ReadOnly, DeployTimeConstant)
* **id**: string (ReadOnly, DeployTimeConstant)
* **kind**: string
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: [schemas:2_properties](#schemas2properties)
* **systemData**: [systemData](#systemdata)
* **tags**: [Dictionary<string,String>](#dictionarystringstring)
* **type**: 'Microsoft.CertificateRegistration/certificateOrders' (ReadOnly, DeployTimeConstant)

## Resource Microsoft.CertificateRegistration/certificateOrders/certificates@2020-10-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-10-01' (ReadOnly, DeployTimeConstant)
* **id**: string (ReadOnly, DeployTimeConstant)
* **kind**: string
* **location**: string (Required)
* **name**: string (Required, DeployTimeConstant)
* **properties**: [AppServiceCertificate](#appservicecertificate)
* **systemData**: [systemData](#systemdata)
* **tags**: [Dictionary<string,String>](#dictionarystringstring)
* **type**: 'Microsoft.CertificateRegistration/certificateOrders/certificates' (ReadOnly, DeployTimeConstant)

## schemas:2_properties
### Properties
* **appServiceCertificateNotRenewableReasons**: 'ExpirationNotInRenewalTimeRange' | 'RegistrationStatusNotSupportedForRenewal' | 'SubscriptionNotActive'[] (ReadOnly)
* **autoRenew**: bool
* **certificates**: [Dictionary<string,AppServiceCertificate>](#dictionarystringappservicecertificate)
* **csr**: string
* **distinguishedName**: string
* **domainVerificationToken**: string (ReadOnly)
* **expirationTime**: string (ReadOnly)
* **intermediate**: [CertificateDetails](#certificatedetails) (ReadOnly)
* **isPrivateKeyExternal**: bool (ReadOnly)
* **keySize**: int
* **lastCertificateIssuanceTime**: string (ReadOnly)
* **nextAutoRenewalTimeStamp**: string (ReadOnly)
* **productType**: 'StandardDomainValidatedSsl' | 'StandardDomainValidatedWildCardSsl' (Required)
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded' (ReadOnly)
* **root**: [CertificateDetails](#certificatedetails) (ReadOnly)
* **serialNumber**: string (ReadOnly)
* **signedCertificate**: [CertificateDetails](#certificatedetails) (ReadOnly)
* **status**: 'Canceled' | 'Denied' | 'Expired' | 'Issued' | 'NotSubmitted' | 'Pendingissuance' | 'PendingRekey' | 'Pendingrevocation' | 'Revoked' | 'Unused' (ReadOnly)
* **validityInYears**: int

## Dictionary<string,AppServiceCertificate>
### Properties
### Additional Properties
* **Additional Properties Type**: [AppServiceCertificate](#appservicecertificate)

## AppServiceCertificate
### Properties
* **keyVaultId**: string
* **keyVaultSecretName**: string
* **provisioningState**: 'AzureServiceUnauthorizedToAccessKeyVault' | 'CertificateOrderFailed' | 'ExternalPrivateKey' | 'Initialized' | 'KeyVaultDoesNotExist' | 'KeyVaultSecretDoesNotExist' | 'OperationNotPermittedOnKeyVault' | 'Succeeded' | 'Unknown' | 'UnknownError' | 'WaitingOnCertificateOrder' (ReadOnly)

## CertificateDetails
### Properties
* **issuer**: string (ReadOnly)
* **notAfter**: string (ReadOnly)
* **notBefore**: string (ReadOnly)
* **rawData**: string (ReadOnly)
* **serialNumber**: string (ReadOnly)
* **signatureAlgorithm**: string (ReadOnly)
* **subject**: string (ReadOnly)
* **thumbprint**: string (ReadOnly)
* **version**: int (ReadOnly)

## systemData
### Properties
* **createdAt**: string
* **createdBy**: string
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User'
* **lastModifiedAt**: string
* **lastModifiedBy**: string
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User'

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
