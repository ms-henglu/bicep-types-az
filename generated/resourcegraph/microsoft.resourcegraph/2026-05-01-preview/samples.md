# Microsoft.ResourceGraph
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.resourcegraph/offerings

Create an offering
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings@2026-05-01-preview' = {
  name: 'example'
  properties: {
    contactEmails: [
      'insights-team@contoso.com'
    ]
    displayName: 'Contoso Insights'
    documentationLink: 'https://aka.ms/contoso-insights'
    lifecycleState: 'Preview'
    organizationName: 'Contoso'
    scenarioDescription: 'Network topology insights across Contoso subscriptions.'
    serviceTreeId: '11111111-2222-3333-4444-555555555555'
    tier: 'Shared'
  }
}
```

## microsoft.resourcegraph/offerings/ontologies

Create or update an ontology covered by approved supply
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings/ontologies@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    autoOnboard: true
    displayName: 'Network Topology'
    edgeTypeRefs: [
      {
        relationshipType: 'Microsoft.Network/attachedTo'
        sourceNodeType: 'microsoft.network/networkinterfaces'
        targetNodeType: 'microsoft.network/virtualnetworks'
      }
    ]
    nodeTypeRefs: [
      {
        alias: 'vnet'
        resourceType: 'microsoft.network/virtualnetworks'
      }
      {
        alias: 'nic'
        resourceType: 'microsoft.network/networkinterfaces'
      }
    ]
  }
}
```

Declare a node-only ontology using default onboarding settings
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings/ontologies@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    nodeTypeRefs: [
      {
        resourceType: 'Microsoft.Compute/virtualMachines'
      }
    ]
  }
}
```

## microsoft.resourcegraph/offerings/ontologies/locations/activation

Activate an ontology in one region
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings/ontologies/locations/activation@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    ontologySnapshot: {
      edgeTypeRefs: [
        {
          relationshipType: 'Microsoft.Network/attachedTo'
          sourceNodeType: 'microsoft.network/networkinterfaces'
          targetNodeType: 'microsoft.network/virtualnetworks'
        }
      ]
      nodeTypeRefs: [
        {
          alias: 'vnet'
          resourceType: 'microsoft.network/virtualnetworks'
        }
        {
          alias: 'nic'
          resourceType: 'microsoft.network/networkinterfaces'
        }
      ]
    }
  }
}
```

## microsoft.resourcegraph/offerings/queryendpoints

Create a query endpoint over an approved ontology
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings/queryEndpoints@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    displayName: 'Topology Explorer'
    enginePreference: 'Pacific'
    estimatedQueriesPerDay: 250000
    ontologyRef: '/subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.ResourceGraph/offerings/contoso-insights/ontologies/network-topology'
    peakQueriesPerMinute: 900
  }
}
```

## microsoft.resourcegraph/offerings/queryendpoints/locations/activation

Activate a query endpoint in one region
```bicep
resource exampleResource 'Microsoft.ResourceGraph/offerings/queryEndpoints/locations/activation@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
}
```
