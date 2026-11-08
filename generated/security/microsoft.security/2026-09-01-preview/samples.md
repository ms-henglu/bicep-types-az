# Microsoft.Security
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.security/serviceentitlements

Creates or updates a service entitlement
```bicep
resource exampleResource 'Microsoft.Security/serviceEntitlements@2026-09-01-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    serviceType: 'Perception'
    state: 'Enabled'
  }
  tags: {
    environment: 'test'
  }
}
```
