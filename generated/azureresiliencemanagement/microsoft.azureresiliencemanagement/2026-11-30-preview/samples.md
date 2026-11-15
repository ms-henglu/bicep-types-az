# Microsoft.AzureResilienceManagement
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.azureresiliencemanagement/drills

Drills_Create_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/drills@2026-11-30-preview' = {
  name: 'example'
  identity: {
    type: 'None'
    userAssignedIdentities: {
    }
  }
  properties: {
    chaosResourceProperties: {
      chaosResourceIdentityForFaults: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
    }
    drillAssetProperties: {
      region: 'eastus'
      resourceGroup: 'customDrillResourceGroup'
      subscription: '4e88bed3-114f-443d-9975-28f64122ec5e'
    }
    drillType: 'DrillProperties'
    executionReadinessState: 'Ready'
    executionState: 'NotRunning'
    goalAssignmentProperties: {
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
    }
    healthModelMonitoringProperties: {
      healthModelId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourceGroups/contoso-health/providers/Microsoft.CloudHealth/healthmodels/contoso-payments-hm'
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
    }
    lastRunProperties: {
      lastRunAttestation: 'Success'
      lastRunState: 'NotStarted'
    }
    monitoringProperties: {
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
    }
    rbacSetupMode: 'AutomatedCustomRole'
    recoveryPlanProperties: {
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
    }
    sliMonitoringProperties: {
      identity: {
        type: 'UserAssigned'
        userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
      }
      slis: [
        {
          type: 'Availability'
          sliId: '/providers/Microsoft.Management/serviceGroups/sampleServiceGroupName/providers/Microsoft.Monitor/slis/checkout-availability'
        }
        {
          type: 'Latency'
          sliId: '/providers/Microsoft.Management/serviceGroups/sampleServiceGroupName/providers/Microsoft.Monitor/slis/checkout-latency'
        }
      ]
    }
    systemMetadata: {
      initialConfig: 'Pending'
    }
  }
}
```

## microsoft.azureresiliencemanagement/goalassignments

GoalAssignments_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/goalAssignments@2026-11-30-preview' = {
  name: 'example'
  properties: {
    regionalObjectives: {
      targetRecoveryPointObjective: 'PT15M'
      targetRecoveryTimeObjective: 'PT1H'
    }
    requireRegionalResiliency: true
    requireZonalResiliency: true
    serviceLevelResources: [
      {
        serviceLevelIndicatorResourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyVirtualMachine'
      }
    ]
  }
}
```

GoalAssignments_CreateOrUpdate_MinimumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/goalAssignments@2026-11-30-preview' = {
  name: 'example'
  properties: {
    requireZonalResiliency: true
  }
}
```

## microsoft.azureresiliencemanagement/recoveryplans

RecoveryPlans_CreateOrUpdate_CyberRecovery
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/recoveryPlans@2026-11-30-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/cyber-recovery-rg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/cyber-recovery-identity': {
      }
    }
  }
  properties: {
    planDescription: 'Cyber recovery plan'
    planType: 'CyberRecovery'
    recoveryGroupsSetting: {
      additionalGroups: [
        {
          properties: {
            description: 'Tier 1 applications'
            groupUniqueId: '5d3c2b1a-8e7f-4a6b-9c0d-1e2f3a4b5c6d'
            orderId: 1
            resiliencyGroupProperties: {
              recoveryConfigProfileAssociations: [
                {
                  recoveryConfigProfileId: '/providers/Microsoft.Management/serviceGroups/contoso-service-group/providers/Microsoft.AzureResilienceManagement/recoveryPlans/cyber-plan/recoveryConfigProfiles/azure-vm-default'
                  workloadType: 'AzureVm'
                }
              ]
              resiliencyType: 'CyberResiliency'
            }
          }
        }
      ]
      defaultGroup: {
        properties: {
          description: 'Foundation services'
          groupUniqueId: 'b7e2a1c4-9f3b-4e2d-8c6a-2f7e4d1b5a9f'
          orderId: 0
        }
      }
    }
    resiliencyPlanProperties: {
      resiliencyType: 'CyberResiliency'
      targetEnvironment: {
        targetLocations: [
          'eastus2'
        ]
        targetSubscriptionIds: [
          '12345678-1234-1234-1234-123456789012'
        ]
      }
    }
  }
}
```

RecoveryPlans_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/recoveryPlans@2026-11-30-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1': {
      }
    }
  }
  properties: {
    planDescription: 'Sample Plan'
    planState: 'UnderEdit'
    planType: 'Regional'
    recoveryGroupsSetting: {
      additionalGroups: [
        {
          properties: {
            description: 'sample recoverygroup'
            groupUniqueId: 'b7e2a1c4-9f3b-4e2d-8c6a-2f7e4d1b5a9f'
            orderId: 1
            postActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
            preActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
          }
        }
        {
          properties: {
            description: 'sample recoverygroup'
            groupUniqueId: 'b7e2a1c4-9f3b-4e2d-8c6a-2f7e4d1b5a9f'
            orderId: 1
            postActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
            preActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
          }
        }
        {
          properties: {
            description: 'sample recoverygroup'
            groupUniqueId: 'b7e2a1c4-9f3b-4e2d-8c6a-2f7e4d1b5a9f'
            orderId: 1
            postActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
            preActions: [
              {
                name: 'sample-group-action'
                type: 'CustomRunbook'
                actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
                associatedIdentity: {
                  type: 'UserAssigned'
                  userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
                }
                parameters: {
                  key7795: 'uvapupcbbdgow'
                }
                timeoutInMinutes: 29
              }
            ]
          }
        }
      ]
      defaultGroup: {
        properties: {
          description: 'sample recoverygroup'
          groupUniqueId: 'b7e2a1c4-9f3b-4e2d-8c6a-2f7e4d1b5a9f'
          orderId: 0
          postActions: [
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
          ]
          preActions: [
            {
              name: 'sample-group-action'
              type: 'CustomRunbook'
              description: 'sample group action instructions'
              actionResourceId: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.Automation/automationAccounts/sampleAccount/runbooks/sameplRunbooks1'
              associatedIdentity: {
                type: 'UserAssigned'
                userAssignedIdentity: '/subscriptions/4e88bed3-114f-443d-9975-28f64122ec5e/resourcegroups/resourceGroup1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/uami1'
              }
              parameters: {
                key7795: 'uvapupcbbdgow'
              }
              timeoutInMinutes: 29
            }
          ]
        }
      }
    }
  }
}
```

## microsoft.azureresiliencemanagement/recoveryplans/recoveryconfigprofiles

RecoveryConfigProfiles_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/recoveryPlans/recoveryConfigProfiles@2026-11-30-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    recoveryPointPolicy: {
      type: 'Latest'
      backupType: [
        'Snapshot'
      ]
      endTime: '2026-09-28T04:00:00Z'
      recoveryPointHealthStatus: 'HealthyAndUnknown'
      startTime: '2026-09-27T04:00:00Z'
    }
    targetScope: {
      location: 'eastus2'
      subscriptionId: '12345678-1234-1234-1234-123456789012'
    }
    workloadConfig: {
      recoveryType: 'CreateNewVM'
      resourceGroup: {
        armResourceType: 'Microsoft.Resources/resourceGroups'
        provisioningMode: 'Existing'
        resourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/cyber-recovery-rg'
      }
      storageAccount: {
        armResourceType: 'Microsoft.Storage/storageAccounts'
        provisioningMode: 'Existing'
        resourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/cyber-recovery-rg/providers/Microsoft.Storage/storageAccounts/cyberrecoverystorage'
      }
      subnet: {
        armResourceType: 'Microsoft.Network/virtualNetworks/subnets'
        dependsOn: [
          'targetVirtualNetwork'
        ]
        provisioningMode: 'Existing'
        resourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/cyber-recovery-rg/providers/Microsoft.Network/virtualNetworks/cyber-recovery-vnet/subnets/default'
      }
      targetNamePrefix: 'cr-'
      virtualNetwork: {
        armResourceType: 'Microsoft.Network/virtualNetworks'
        provisioningMode: 'Existing'
        resourceId: '/subscriptions/12345678-1234-1234-1234-123456789012/resourceGroups/cyber-recovery-rg/providers/Microsoft.Network/virtualNetworks/cyber-recovery-vnet'
      }
      workloadType: 'AzureVm'
      zones: [
        '1'
        '2'
      ]
    }
  }
}
```

## microsoft.azureresiliencemanagement/usageplans

UsagePlans_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/usagePlans@2026-11-30-preview' = {
  name: 'example'
  location: 'global'
  properties: {
    planType: 'Standard'
  }
  tags: {
    environment: 'production'
  }
}
```

## microsoft.azureresiliencemanagement/usageplans/enrollments

Enrollments_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.AzureResilienceManagement/usagePlans/enrollments@2026-11-30-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    serviceGroupId: '/providers/Microsoft.Management/serviceGroups/sg1'
  }
}
```
