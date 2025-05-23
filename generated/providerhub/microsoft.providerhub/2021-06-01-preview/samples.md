# Microsoft.ProviderHub
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.providerhub/providerregistrations

ProviderRegistrations_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations@2021-06-01-preview' = {
  name: 'example'
  properties: {
    capabilities: [
      {
        effect: 'Allow'
        quotaId: 'CSP_2015-05-01'
      }
      {
        effect: 'Allow'
        quotaId: 'CSP_MG_2017-12-01'
      }
    ]
    management: {
      incidentContactEmail: 'helpme@contoso.com'
      incidentRoutingService: 'Contoso Resource Provider'
      incidentRoutingTeam: 'Contoso Triage'
    }
    providerType: 'Internal'
    providerVersion: '2.0'
  }
}
```

## microsoft.providerhub/providerregistrations/customrollouts

CustomRollouts_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/customRollouts@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    specification: {
      canary: {
        regions: [
          'brazilus'
        ]
      }
    }
  }
}
```

## microsoft.providerhub/providerregistrations/defaultrollouts

DefaultRollouts_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/defaultRollouts@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    specification: {
      canary: {
        skipRegions: [
          'eastus2euap'
        ]
      }
      expeditedRollout: {
        enabled: true
      }
      restOfTheWorldGroupTwo: {
        waitDuration: 'PT4H'
      }
    }
  }
}
```

## microsoft.providerhub/providerregistrations/notificationregistrations

NotificationRegistrations_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/notificationRegistrations@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    includedEvents: [
      '*/write'
      'Microsoft.Contoso/employees/delete'
    ]
    messageScope: 'RegisteredSubscriptions'
    notificationEndpoints: [
      {
        locations: [
          ''
          'East US'
        ]
        notificationDestination: '/subscriptions/ac6bcfb5-3dc1-491f-95a6-646b89bf3e88/resourceGroups/mgmtexp-eastus/providers/Microsoft.EventHub/namespaces/unitedstates-mgmtexpint/eventhubs/armlinkednotifications'
      }
      {
        locations: [
          'North Europe'
        ]
        notificationDestination: '/subscriptions/ac6bcfb5-3dc1-491f-95a6-646b89bf3e88/resourceGroups/mgmtexp-northeurope/providers/Microsoft.EventHub/namespaces/europe-mgmtexpint/eventhubs/armlinkednotifications'
      }
    ]
    notificationMode: 'EventHub'
  }
}
```

## microsoft.providerhub/providerregistrations/resourcetyperegistrations

ResourceTypeRegistrations_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    endpoints: [
      {
        apiVersions: [
          '2020-06-01-preview'
        ]
        locations: [
          'West US'
          'East US'
          'North Europe'
        ]
        requiredFeatures: [
          '<feature flag>'
        ]
      }
    ]
    management: {
      incidentContactEmail: 'helpme@contoso.com'
      incidentRoutingService: ''
      incidentRoutingTeam: ''
      manifestOwners: [
        'SPARTA-PlatformServiceAdministrator'
      ]
      resourceAccessPolicy: 'NotSpecified'
    }
    openApiConfiguration: {
      validation: {
        allowNoncompliantCollectionResponse: true
      }
    }
    regionality: 'Regional'
    resourceConcurrencyControlOptions: {
      patch: {
        policy: 'SynchronizeBeginExtension'
      }
      post: {
        policy: 'SynchronizeBeginExtension'
      }
      put: {
        policy: 'SynchronizeBeginExtension'
      }
    }
    resourceGraphConfiguration: {
      apiVersion: '2019-01-01'
      enabled: true
    }
    routingType: 'Default'
    swaggerSpecifications: [
      {
        apiVersions: [
          '2020-06-01-preview'
        ]
        swaggerSpecFolderUri: 'https://github.com/Azure/azure-rest-api-specs/blob/feature/azure/contoso/specification/contoso/resource-manager/Microsoft.SampleRP/'
      }
    ]
  }
}
```

## microsoft.providerhub/providerregistrations/resourcetyperegistrations/resourcetyperegistrations/resourcetyperegistrations/resourcetyperegistrations/skus

Skus_CreateOrUpdateNestedResourceTypeThird
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    skuSettings: [
      {
        name: 'freeSku'
        kind: 'Standard'
        tier: 'Tier1'
      }
      {
        name: 'premiumSku'
        costs: [
          {
            meterId: 'xxx'
          }
        ]
        kind: 'Premium'
        tier: 'Tier2'
      }
    ]
  }
}
```

## microsoft.providerhub/providerregistrations/resourcetyperegistrations/resourcetyperegistrations/resourcetyperegistrations/skus

Skus_CreateOrUpdateNestedResourceTypeSecond
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    skuSettings: [
      {
        name: 'freeSku'
        kind: 'Standard'
        tier: 'Tier1'
      }
      {
        name: 'premiumSku'
        costs: [
          {
            meterId: 'xxx'
          }
        ]
        kind: 'Premium'
        tier: 'Tier2'
      }
    ]
  }
}
```

## microsoft.providerhub/providerregistrations/resourcetyperegistrations/resourcetyperegistrations/skus

Skus_CreateOrUpdateNestedResourceTypeFirst
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/resourcetypeRegistrations/skus@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    skuSettings: [
      {
        name: 'freeSku'
        kind: 'Standard'
        tier: 'Tier1'
      }
      {
        name: 'premiumSku'
        costs: [
          {
            meterId: 'xxx'
          }
        ]
        kind: 'Premium'
        tier: 'Tier2'
      }
    ]
  }
}
```

## microsoft.providerhub/providerregistrations/resourcetyperegistrations/skus

Skus_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.ProviderHub/providerRegistrations/resourcetypeRegistrations/skus@2021-06-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    skuSettings: [
      {
        name: 'freeSku'
        kind: 'Standard'
        tier: 'Tier1'
      }
      {
        name: 'premiumSku'
        costs: [
          {
            meterId: 'xxx'
          }
        ]
        kind: 'Premium'
        tier: 'Tier2'
      }
    ]
  }
}
```
