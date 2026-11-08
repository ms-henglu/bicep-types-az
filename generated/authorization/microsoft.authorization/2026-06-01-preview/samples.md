# Microsoft.Authorization
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.authorization/privilegedresourcefavorites

Add a favorite (idempotent PUT)
```bicep
resource exampleResource 'Microsoft.Authorization/privilegedResourceFavorites@2026-06-01-preview' = {
  name: 'example'
  properties: {
    resourceId: '/subscriptions/11111111-2222-3333-4444-555555555555/resourceGroups/my-rg/providers/Microsoft.Compute/virtualMachines/my-vm'
  }
}
```
