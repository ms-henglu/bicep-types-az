# Microsoft.NetworkSecurity
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.networksecurity/neuroshields

Create or update NeuroShield resource
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields@2026-10-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
    description: 'Test NeuroShield resource'
    responseMode: 'Manual'
    severityThreshold: 'Medium'
  }
  tags: {
    env: 'test'
  }
}
```

Create or update NeuroShield with omitted optional properties
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields@2026-10-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
    responseMode: 'Manual'
  }
}
```

## microsoft.networksecurity/neuroshields/protectedresources

Create or update protected resource with a system-assigned target identity
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields/protectedResources@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    targetIdentity: {
      type: 'SystemAssigned'
      principalId: '11111111-1111-1111-1111-111111111111'
      tenantId: '22222222-2222-2222-2222-222222222222'
    }
    targetResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myComputeRg/providers/Microsoft.Compute/virtualMachines/vm-01'
  }
}
```

Create or update protected resource with a user-assigned target identity
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields/protectedResources@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    targetIdentity: {
      type: 'UserAssigned'
      userAssignedIdentities: {
        '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myIdentityRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/neuronIdentity': {
          clientId: '22222222-2222-2222-2222-222222222222'
          principalId: '11111111-1111-1111-1111-111111111111'
        }
      }
    }
    targetResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myComputeRg/providers/Microsoft.Compute/virtualMachines/vm-01'
  }
}
```

Create or update protected resource with explicit None identity
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields/protectedResources@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    targetIdentity: {
      type: 'None'
    }
    targetResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myComputeRg/providers/Microsoft.Compute/virtualMachines/vm-01'
  }
}
```

Create or update protected resource without an identity
```bicep
resource exampleResource 'Microsoft.NetworkSecurity/neuroShields/protectedResources@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    targetResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myComputeRg/providers/Microsoft.Compute/virtualMachines/vm-01'
  }
}
```
