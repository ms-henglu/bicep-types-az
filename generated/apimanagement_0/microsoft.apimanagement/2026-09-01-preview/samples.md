# Microsoft.ApiManagement
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.apimanagement/aigateways

Create an AI Gateway
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways@2026-09-01-preview' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'westus2'
  properties: {
    backend: {
      subnet: {
        id: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.Network/virtualNetworks/example-vnet/subnets/example-subnet'
      }
    }
  }
  sku: {
    name: 'AIGateway'
  }
  tags: {
    environment: 'development'
  }
}
```
