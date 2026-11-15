# Microsoft.EdgeOperator
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.edgeoperator/systemconfiguration

SystemConfiguration_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.EdgeOperator/systemConfiguration@2026-06-01-preview' = {
  name: 'example'
  properties: {
    connectionIntent: 'Connected'
    deviceResourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/rg-aldo/providers/Microsoft.Edge/disconnectedOperations/demo-resource'
    dnsForwarderIpAddress: '10.0.0.1'
    stampId: '3af55315-1caf-4251-ad6a-6b461729328d'
  }
}
```
