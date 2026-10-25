# Microsoft.Security
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.security/serviceentitlementsettings

Creates or updates a service entitlement setting
```bicep
resource exampleResource 'Microsoft.Security/serviceEntitlementSettings@2026-09-16-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    isDefault: true
  }
  tags: {
    environment: 'test'
  }
}
```

Creates or updates a service entitlement setting without optional tags
```bicep
resource exampleResource 'Microsoft.Security/serviceEntitlementSettings@2026-09-16-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    isDefault: true
  }
}
```
