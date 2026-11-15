# Microsoft.Security
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.security/batchpricings

Update pricing batch - partial success
```bicep
resource exampleResource 'Microsoft.Security/batchPricings@2026-07-01' = {
  name: 'example'
  properties: {
    plansConfigurations: [
      {
        planName: 'VirtualMachines'
        properties: {
          pricingTier: 'Standard'
          subPlan: 'P2'
          extensions: [
            {
              name: 'AgentlessVmScanning'
              isEnabled: 'True'
            }
          ]
        }
      }
      {
        planName: 'SqlServers'
        properties: {
          pricingTier: 'Standard'
          extensions: [
            {
              name: 'InvalidExtension'
              isEnabled: 'True'
            }
          ]
        }
      }
      {
        planName: 'CloudPosture'
        properties: {
          pricingTier: 'Standard'
          securityOperatorResourceId: '/providers/Microsoft.Management/managementGroups/ContosoGroup/providers/Microsoft.Security/securityOperators/ContosoOperator'
          extensions: [
            {
              name: 'AgentlessDiscoveryForKubernetes'
              isEnabled: 'True'
            }
          ]
        }
      }
    ]
  }
}
```

Update pricing batch - success
```bicep
resource exampleResource 'Microsoft.Security/batchPricings@2026-07-01' = {
  name: 'example'
  properties: {
    plansConfigurations: [
      {
        planName: 'VirtualMachines'
        properties: {
          pricingTier: 'Standard'
          subPlan: 'P2'
          extensions: [
            {
              name: 'AgentlessVmScanning'
              isEnabled: 'True'
            }
            {
              name: 'FileIntegrityMonitoring'
              additionalExtensionProperties: {
                detectionType: 'WindowsFiles'
                workspace: '/subscriptions/20ff7fc3-e762-44dd-bd96-b71116dcdc23/resourceGroups/myRg/providers/Microsoft.OperationalInsights/workspaces/myWorkspace'
              }
              isEnabled: 'True'
            }
          ]
        }
      }
      {
        planName: 'StorageAccounts'
        properties: {
          pricingTier: 'Standard'
          subPlan: 'DefenderForStorageV2'
          extensions: [
            {
              name: 'OnUploadMalwareScanning'
              additionalExtensionProperties: {
                capGBPerMonth: '5000'
              }
              isEnabled: 'True'
            }
            {
              name: 'SensitiveDataDiscovery'
              isEnabled: 'True'
            }
          ]
        }
      }
      {
        planName: 'CloudPosture'
        properties: {
          pricingTier: 'Standard'
          securityOperatorResourceId: '/providers/Microsoft.Management/managementGroups/ContosoGroup/providers/Microsoft.Security/securityOperators/ContosoOperator'
          extensions: [
            {
              name: 'AgentlessDiscoveryForKubernetes'
              isEnabled: 'True'
            }
            {
              name: 'ContainerRegistriesVulnerabilityAssessments'
              isEnabled: 'True'
            }
            {
              name: 'EntraPermissionsManagement'
              isEnabled: 'True'
            }
          ]
        }
      }
    ]
  }
}
```

## microsoft.security/pricings

Update pricing on resource (example for Containers plan)
```bicep
resource exampleResource 'Microsoft.Security/pricings@2026-07-01' = {
  name: 'example'
  properties: {
    pricingTier: 'Standard'
    extensions: [
      {
        name: 'ContainerRegistriesVulnerabilityAssessments'
        isEnabled: 'True'
      }
      {
        name: 'ContainerSensor'
        isEnabled: 'True'
      }
      {
        name: 'AgentlessDiscoveryForKubernetes'
        isEnabled: 'True'
      }
      {
        name: 'AgentlessVmScanning'
        additionalExtensionProperties: {
          ExclusionTags: '[]'
        }
        isEnabled: 'True'
      }
      {
        name: 'ContainerIntegrityContribution'
        isEnabled: 'True'
      }
    ]
  }
}
```

Update pricing on resource (example for VirtualMachines plan)
```bicep
resource exampleResource 'Microsoft.Security/pricings@2026-07-01' = {
  name: 'example'
  properties: {
    pricingTier: 'Standard'
    subPlan: 'P1'
  }
}
```

Update pricing on subscription (example for CloudPosture plan)
```bicep
resource exampleResource 'Microsoft.Security/pricings@2026-07-01' = {
  name: 'example'
  properties: {
    pricingTier: 'Standard'
  }
}
```

Update pricing on subscription (example for CloudPosture plan) - partial success
```bicep
resource exampleResource 'Microsoft.Security/pricings@2026-07-01' = {
  name: 'example'
  properties: {
    pricingTier: 'Standard'
  }
}
```

Update pricing on subscription (example for VirtualMachines plan)
```bicep
resource exampleResource 'Microsoft.Security/pricings@2026-07-01' = {
  name: 'example'
  properties: {
    enforce: 'True'
    pricingTier: 'Standard'
    subPlan: 'P2'
  }
}
```
