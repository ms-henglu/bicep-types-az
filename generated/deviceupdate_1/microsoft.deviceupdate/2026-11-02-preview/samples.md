# Microsoft.DeviceUpdate
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.deviceupdate/updateinstances

Creates or updates an Update Instance
```bicep
resource exampleResource 'Microsoft.DeviceUpdate/updateInstances@2026-11-02-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/test-rg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/contoso-mi': {
      }
    }
  }
  location: 'eastus2'
  properties: {
  }
  tags: {
    env: 'prod'
  }
}
```
