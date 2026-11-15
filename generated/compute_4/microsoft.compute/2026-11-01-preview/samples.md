# Microsoft.Compute
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.compute/workloadspaces

Create a production workload space
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces@2026-11-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
  }
  tags: {
    environment: 'Production'
  }
}
```

## microsoft.compute/workloadspaces/capabilities

Enable the Agent Sandbox capability
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/capabilities@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'AgentSandbox'
  properties: {
    versionPolicy: 'ServiceManaged'
  }
}
```

Enable the Pod Snapshot Restore capability with the default version policy
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/capabilities@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'PodSnapshotRestore'
  properties: {
  }
}
```

## microsoft.compute/workloadspaces/runtimebindings

Attach a referenced Kubernetes runtime binding
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/runtimeBindings@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'Kubernetes'
  properties: {
    provisioningMode: 'Referenced'
    resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/aks-rg/providers/Microsoft.ContainerService/managedClusters/aks-prod'
  }
}
```

Create a managed Kubernetes runtime binding
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/runtimeBindings@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'Kubernetes'
  properties: {
    managedProfile: {
      offering: 'Automatic'
    }
    provisioningMode: 'Managed'
  }
}
```

Create a managed serverless container runtime binding
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/runtimeBindings@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'ServerlessContainers'
  properties: {
    managedProfile: {
      provider: 'ACI'
    }
    networkProfile: {
      egressMode: 'ServiceManaged'
    }
    provisioningMode: 'Managed'
  }
}
```

## microsoft.compute/workloadspaces/runtimelinks

Create a runtime link between Kubernetes and serverless containers
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/runtimeLinks@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    capacityProfile: {
      maximumNodes: 100
      minimumNodes: 1
    }
    executionBindingResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg-workload/providers/Microsoft.Compute/workloadSpaces/managed-agents-prod/runtimeBindings/serverless-default'
    orchestratorBindingResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg-workload/providers/Microsoft.Compute/workloadSpaces/managed-agents-prod/runtimeBindings/kubernetes-default'
  }
}
```

Create a runtime link without capacity intent
```bicep
resource exampleResource 'Microsoft.Compute/workloadSpaces/runtimeLinks@2026-11-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    executionBindingResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg-workload/providers/Microsoft.Compute/workloadSpaces/managed-agents-prod/runtimeBindings/serverless-default'
    orchestratorBindingResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg-workload/providers/Microsoft.Compute/workloadSpaces/managed-agents-prod/runtimeBindings/kubernetes-default'
  }
}
```
