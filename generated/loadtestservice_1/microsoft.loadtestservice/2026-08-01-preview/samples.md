# Microsoft.LoadTestService
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.loadtestservice/playwrightworkspaces

PlaywrightWorkspaces_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.LoadTestService/playwrightWorkspaces@2026-08-01-preview' = {
  name: 'example'
  location: 'westus3'
  properties: {
    localAuth: 'Enabled'
    regionalAffinity: 'Enabled'
    reporting: 'Enabled'
    storageUri: 'https://examplestorageaccount.blob.core.windows.net'
    subnetId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/dummyrg/providers/Microsoft.Network/virtualNetworks/myVnet/subnets/mySubnet'
  }
  tags: {
    Team: 'Dev Exp'
  }
}
```
