# Microsoft.ContainerService
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.containerservice/fleets

Creates a Fleet resource with a long running operation.
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets@2025-03-01' = {
  name: 'example'
  location: 'East US'
  properties: {
    hubProfile: {
      agentProfile: {
        vmSize: 'Standard_DS1'
      }
      dnsPrefix: 'dnsprefix1'
    }
  }
  tags: {
    archv2: ''
    tier: 'production'
  }
}
```

Creates a Fleet resource with a long running operation. - generated by [MaximumSet] rule
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets@2025-03-01' = {
  name: 'example'
  identity: {
    type: 'None'
    userAssignedIdentities: {
      key126: {
      }
    }
  }
  location: 'East US'
  properties: {
    hubProfile: {
      agentProfile: {
        subnetId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgfleets/providers/Microsoft.Network/virtualNetwork/myvnet/subnets/mysubnet1'
        vmSize: 'Standard_DS1'
      }
      apiServerAccessProfile: {
        enablePrivateCluster: true
        enableVnetIntegration: true
        subnetId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgfleets/providers/Microsoft.Network/virtualNetwork/myvnet/subnets/mysubnet1'
      }
      dnsPrefix: 'dnsprefix1'
    }
  }
  tags: {
  }
}
```

## microsoft.containerservice/fleets/autoupgradeprofiles

Create an AutoUpgradeProfile.
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/autoUpgradeProfiles@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    channel: 'Stable'
  }
}
```

Create an AutoUpgradeProfile. - generated by [MaximumSet] rule
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/autoUpgradeProfiles@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    autoUpgradeProfileStatus: {
      lastTriggerError: {
      }
    }
    channel: 'Stable'
    disabled: true
    nodeImageSelection: {
      type: 'Latest'
    }
    updateStrategyId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgfleets/providers/Microsoft.ContainerService/fleets/fleet1/updateStrategies/strategy1'
  }
}
```

## microsoft.containerservice/fleets/members

Creates a FleetMember resource with a long running operation.
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/members@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    clusterResourceId: '/subscriptions/subid1/resourcegroups/rg1/providers/Microsoft.ContainerService/managedClusters/cluster-1'
  }
}
```

Creates a FleetMember resource with a long running operation. - generated by [MaximumSet] rule
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/members@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    clusterResourceId: '/subscriptions/subid1/resourcegroups/rg1/providers/Microsoft.ContainerService/managedClusters/cluster-1'
    group: 'fleet1'
  }
}
```

## microsoft.containerservice/fleets/updateruns

Create an UpdateRun.
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/updateRuns@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    managedClusterUpdate: {
      nodeImageSelection: {
        type: 'Latest'
      }
      upgrade: {
        type: 'Full'
        kubernetesVersion: '1.26.1'
      }
    }
    strategy: {
      stages: [
        {
          name: 'stage1'
          afterStageWaitInSeconds: 3600
          groups: [
            {
              name: 'group-a'
            }
          ]
        }
      ]
    }
    updateStrategyId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.ContainerService/fleets/myFleet/updateStrategies/strategy1'
  }
}
```

Create an UpdateRun. - generated by [MaximumSet] rule
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/updateRuns@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    autoUpgradeProfileId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgfleets/providers/Microsoft.ContainerService/fleets/fleet1/autoUpgradeProfiles/aup1'
    managedClusterUpdate: {
      nodeImageSelection: {
        type: 'Latest'
        customNodeImageVersions: [
          {
          }
        ]
      }
      upgrade: {
        type: 'Full'
        kubernetesVersion: '1.26.1'
      }
    }
    status: {
      nodeImageSelection: {
      }
      status: {
        error: {
        }
        state: 'NotStarted'
      }
    }
    strategy: {
      stages: [
        {
          name: 'stage1'
          afterStageWaitInSeconds: 3600
          groups: [
            {
              name: 'group-a'
            }
          ]
        }
      ]
    }
    updateStrategyId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.ContainerService/fleets/myFleet/updateStrategies/strategy1'
  }
}
```

## microsoft.containerservice/fleets/updatestrategies

Create a FleetUpdateStrategy.
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/updateStrategies@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    strategy: {
      stages: [
        {
          name: 'stage1'
          afterStageWaitInSeconds: 3600
          groups: [
            {
              name: 'group-a'
            }
          ]
        }
      ]
    }
  }
}
```

Create a FleetUpdateStrategy. - generated by [MaximumSet] rule
```bicep
resource exampleResource 'Microsoft.ContainerService/fleets/updateStrategies@2025-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    strategy: {
      stages: [
        {
          name: 'stage1'
          afterStageWaitInSeconds: 3600
          groups: [
            {
              name: 'group-a'
            }
          ]
        }
      ]
    }
  }
}
```
