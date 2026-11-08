# Microsoft.AAD
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.aad/domainservices

Create Domain Service
```bicep
resource exampleResource 'Microsoft.AAD/domainServices@2026-08-31-preview' = {
  name: 'example'
  properties: {
    domainName: 'TestDomainService.com'
    domainSecuritySettings: {
      ntlmV1: 'Enabled'
      syncNtlmPasswords: 'Enabled'
      syncOnPremSamAccountName: 'Enabled'
      tlsV1: 'Disabled'
    }
    filteredSync: 'Enabled'
    initialFilteredSyncGroupIds: [
      'c2d4b743-7a4c-4f7a-95d6-5a6f6d72657c'
      'f95a5bbc-8c42-4a41-a57c-3a24c7f55d2f'
    ]
    ldapsSettings: {
      externalAccess: 'Enabled'
      ldaps: 'Enabled'
      pfxCertificate: 'MIIDPDCCAiSgAwIBAgIQQUI9P6tq2p9OFIJa7DLNvTANBgkqhkiG9w0BAQsFADAgMR4w...'
      pfxCertificatePassword: '<pfxCertificatePassword>'
    }
    notificationSettings: {
      additionalRecipients: [
        'jicha@microsoft.com'
        'caalmont@microsoft.com'
      ]
      notifyDcAdmins: 'Enabled'
      notifyGlobalAdmins: 'Enabled'
    }
    replicaSets: [
      {
        location: 'West US'
        subnetId: '/subscriptions/1639790a-76a2-4ac4-98d9-8562f5dfcb4d/resourceGroups/TestNetworkResourceGroup/providers/Microsoft.Network/virtualNetworks/TestVnetWUS/subnets/TestSubnetWUS'
      }
    ]
  }
}
```

## microsoft.aad/domainservices/oucontainer

Create OuContainer
```bicep
resource exampleResource 'Microsoft.AAD/domainServices/ouContainer@2026-08-31-preview' = {
  parent: parentResource 
  name: 'example'
  accountName: 'AccountName1'
  password: '<password>'
  spn: 'Spn1'
}
```
