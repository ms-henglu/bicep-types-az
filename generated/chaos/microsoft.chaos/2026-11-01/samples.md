# Microsoft.Chaos
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.chaos/experiments

Create/update a Experiment in a resource group.
```bicep
resource exampleResource 'Microsoft.Chaos/experiments@2026-11-01' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'eastus2euap'
  properties: {
    customerDataStorage: {
      blobContainerName: 'azurechaosstudioexperiments'
      storageAccountResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/exampleRG/providers/Microsoft.Storage/storageAccounts/exampleStorage'
    }
    selectors: [
      {
        type: 'List'
        id: 'selector1'
        targets: [
          {
            type: 'ChaosTarget'
            id: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Compute/virtualMachines/exampleVM/providers/Microsoft.Chaos/targets/Microsoft-VirtualMachine'
          }
        ]
      }
    ]
    steps: [
      {
        name: 'step1'
        branches: [
          {
            name: 'branch1'
            actions: [
              {
                name: 'urn:csci:microsoft:virtualMachine:shutdown/1.0'
                type: 'continuous'
                duration: 'PT10M'
                parameters: [
                  {
                    key: 'abruptShutdown'
                    value: 'false'
                  }
                ]
                selectorId: 'selector1'
              }
            ]
          }
        ]
      }
    ]
  }
  tags: {
    key2138: 'fjaeecgnvqd'
    key7131: 'ryohwcoiccwsnewjigfmijz'
  }
}
```

## microsoft.chaos/targets

Create/update a Target that extends a virtual machine resource.
```bicep
resource exampleResource 'Microsoft.Chaos/targets@2026-11-01' = {
  name: 'example'
  properties: {
  }
}
```

## microsoft.chaos/targets/capabilities

Create/update a Capability that extends a virtual machine Target resource.
```bicep
resource exampleResource 'Microsoft.Chaos/targets/capabilities@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
  }
}
```

## microsoft.chaos/workspaces

Create a workspace only when absent, or return 412 when it already exists
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  location: 'westus2'
  properties: {
    scopes: [
      '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG'
    ]
  }
}
```

Create or update a Microsoft-managed Workspace with empty encryption settings
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  location: 'westus2'
  properties: {
    encryption: {
    }
    scopes: [
      '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG'
    ]
  }
}
```

Create or update a Microsoft-managed Workspace without encryption settings
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  location: 'westus2'
  properties: {
    scopes: [
      '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG'
    ]
  }
}
```

Create or update a Workspace with a customer-managed key
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  location: 'westus2'
  properties: {
    encryption: {
      customerManagedKeyEncryption: {
        keyEncryptionKeyUrl: 'https://contoso-vault.vault.azure.net/keys/workspace-key'
        keyVaultResourceId: '/subscriptions/11111111-1111-1111-1111-111111111111/resourceGroups/customer-keys/providers/Microsoft.KeyVault/vaults/contoso-vault'
      }
    }
    scopes: [
      '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG'
    ]
  }
}
```

Create/update a workspace in a resource group.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/exampleResourceGroup/providers/Microsoft.ManagedIdentity/userAssignedIdentities/exampleIdentity': {
      }
    }
  }
  location: 'westus2'
  properties: {
    scopes: [
      '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/exampleResourceGroup'
    ]
  }
  tags: {
    department: 'engineering'
    environment: 'production'
    project: 'chaos-testing'
  }
}
```

Update a workspace only when present, or return 412 when it does not exist
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces@2026-11-01' = {
  name: 'example'
  location: 'westus2'
  properties: {
    scopes: [
      '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG'
    ]
  }
}
```

## microsoft.chaos/workspaces/connections

Create or update a connection.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/connections@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    kind: 'AksExtension'
    principalId: '00000000-0000-0000-0000-000000000000'
    targetResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/exampleRG/providers/Microsoft.ContainerService/managedClusters/exampleCluster'
    tenantId: '00000000-0000-0000-0000-000000000000'
  }
}
```

## microsoft.chaos/workspaces/scenarios

Create a scenario from a built-in scenario template version.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Simulates a datacenter/availability zone failure by shutting down VMSS instances and standalone VMs in the target zone. Zone failures account for ~25% of all cloud incidents — this scenario validates your application\'s cross-zone resilience.'
    createdFrom: '/providers/Microsoft.Chaos/scenarioTemplates/ComputeZoneDown/versions/1.2'
  }
}
```

Create a scenario only when absent, or return 412 when it already exists
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    actions: [
      {
        name: 'restart'
        actionId: 'microsoft-compute-shutdown/2.0'
        duration: 'PT5M'
        selectors: [
          {
            name: 'logicalZone'
            value: '1'
          }
          {
            name: 'location'
            value: 'eastus'
          }
        ]
      }
    ]
    parameters: [
    ]
  }
}
```

Create or update a scenario that continues past suppressed action failures.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Probes dependencies best-effort, then runs a critical shutdown whose failure must stop the run.'
    actions: [
      {
        name: 'dependencyProbe'
        description: 'Best-effort dependency probe. Inherits the scenario-level Continue behavior, so a failure here does not fail the run.'
        actionId: 'urn:csci:microsoft:agent:networkDisconnect/1.0.0'
        duration: 'PT5M'
      }
      {
        name: 'criticalShutdown'
        description: 'Critical shutdown. Overrides the scenario default so that a failure stops the run.'
        actionId: 'urn:csci:microsoft:compute:shutdown/1.0.0'
        duration: 'PT10M'
        failureBehavior: 'Stop'
        runAfter: {
          behavior: 'All'
          items: [
            {
              name: 'dependencyProbe'
              type: 'Action'
              onActionLifecycle: 'AnyTerminal'
            }
          ]
        }
      }
    ]
    failureBehavior: 'Continue'
  }
}
```

Create or update a scenario.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Induces an outage of all discovered VM and VMSS instances in the target zone with an option to invoke custom scripted actions using Automation Runbooks. Additionally, it forces failover of discovered Redis instances to simulate backend zonal outage.'
    actions: [
      {
        name: 'vmssZoneDown'
        description: 'Force shutdown VMSS instances in target zone'
        actionId: 'microsoft-compute-shutdown/2.0'
        duration: '%%{parameters.duration}%%'
        parameters: [
        ]
        selectors: [
          {
            name: 'logicalZone'
            value: '%%{parameters.logicalZone}%%'
          }
          {
            name: 'location'
            value: '%%{parameters.location}%%'
          }
        ]
      }
      {
        name: 'vmZoneDown'
        description: 'Force shutdown VM instances in target zone'
        actionId: 'microsoft-compute-shutdown/2.0'
        duration: '%%{parameters.duration}%%'
        parameters: [
        ]
        selectors: [
          {
            name: 'logicalZone'
            value: '%%{parameters.logicalZone}%%'
          }
          {
            name: 'location'
            value: '%%{parameters.location}%%'
          }
        ]
      }
      {
        name: 'redisFailover'
        description: 'Force failover of Redis instances to simulate backend zonal outage'
        actionId: 'urn:csci:microsoft:azureClusteredCacheForRedis:Reboot/1.0.0'
        duration: 'PT5M'
        parameters: [
          {
            key: 'RebootType'
            value: 'PrimaryNode'
          }
        ]
      }
      {
        name: 'custom-runbook-1'
        description: 'Custom Runbook 1'
        actionId: 'urn:csci:microsoft:Automation:StartRunbook/1.0.0'
        duration: 'PT30M'
        externalResource: {
          resourceId: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Automation/automationAccounts/exampleAutomationAccount/runbooks/exampleRunbook'
        }
        parameters: [
          {
            key: 'RunbookParameters'
            value: '%%{parameters.customRunbook1ParametersJson}%%'
          }
        ]
      }
    ]
    parameters: [
      {
        name: 'logicalZone'
        type: 'string'
        description: 'Logical availability-zone label to test in each target subscription, for example 1.'
        required: true
      }
      {
        name: 'location'
        type: 'string'
        description: 'Azure location name in which to test the logical zone, for example eastus.'
        required: true
      }
      {
        name: 'duration'
        type: 'string'
        description: 'The duration of the outage scenario.'
        default: 'PT15M'
        required: false
      }
      {
        name: 'customRunbook1ResourceId'
        type: 'string'
        description: 'Optional custom runbook 1 resource ID. If not provided, this action will be skipped.'
        required: false
      }
      {
        name: 'customRunbook1ParametersJson'
        type: 'string'
        description: 'Optional custom runbook 1 parameters in JSON format.'
        default: '{}'
        required: false
      }
    ]
  }
}
```

Update a scenario only when present, or return 412 when it does not exist
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    actions: [
      {
        name: 'restart'
        actionId: 'microsoft-compute-shutdown/2.0'
        duration: 'PT5M'
        selectors: [
          {
            name: 'logicalZone'
            value: '1'
          }
          {
            name: 'location'
            value: 'eastus'
          }
        ]
      }
    ]
    parameters: [
    ]
  }
}
```

## microsoft.chaos/workspaces/scenarios/configurations

Create a scenario configuration only when absent, or return 412 when it already exists
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios/configurations@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    scenarioId: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Chaos/workspaces/exampleWorkspace/scenarios/exampleScenario'
  }
}
```

Create or update a scenario configuration with physical zone targeting.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios/configurations@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    parameters: [
      {
        key: 'duration'
        value: 'PT10M'
      }
    ]
    resourceTargeting: {
      exclude: {
        resources: [
          '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Compute/virtualMachines/protectedVM'
        ]
      }
      include: {
        physicalZones: [
          'westus2-az1'
        ]
      }
    }
    scenarioId: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Chaos/workspaces/exampleWorkspace/scenarios/12345678-1234-1234-1234-123456789012'
  }
}
```

Create or update a scenario configuration.
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios/configurations@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    parameters: [
      {
        key: 'duration'
        value: 'PT10M'
      }
      {
        key: 'targetResourceIds'
        value: '["/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Compute/virtualMachines/vm1","/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Compute/virtualMachines/vm2"]'
      }
    ]
    resourceTargeting: {
      exclude: {
        resources: [
          '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Compute/virtualMachines/protectedVM'
        ]
        tags: [
          {
            key: 'environment'
            value: 'production'
          }
        ]
        types: [
          'Microsoft.Compute/virtualMachineScaleSets'
        ]
      }
      include: {
        locations: [
          'eastus'
        ]
        zones: [
          '1'
        ]
      }
    }
    scenarioId: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Chaos/workspaces/exampleWorkspace/scenarios/12345678-1234-1234-1234-123456789012'
  }
}
```

Update a scenario configuration only when present, or return 412 when it does not exist
```bicep
resource exampleResource 'Microsoft.Chaos/workspaces/scenarios/configurations@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    scenarioId: '/subscriptions/6b052e15-03d3-4f17-b2e1-be7f07588291/resourceGroups/exampleRG/providers/Microsoft.Chaos/workspaces/exampleWorkspace/scenarios/exampleScenario'
  }
}
```
