# Microsoft.Compute
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.compute/locations/bulkcreate

BulkCreate_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Compute/locations/bulkCreate@2026-09-06-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  properties: {
    capacity: 2
    capacityType: 'VM'
    computeProfile: {
      computeApiVersion: '2024-11-01'
      virtualMachineProfile: {
        networkProfile: {
          networkApiVersion: '2020-11-01'
          networkInterfaceConfigurations: [
            {
              name: 'bulkvm-nic'
              properties: {
                deleteOption: 'Delete'
                ipConfigurations: [
                  {
                    name: 'bulkvm-ipconfig'
                    properties: {
                      primary: true
                      subnet: {
                        id: '/subscriptions/1FBA3C66-5C9C-4391-B72F-9F52735FC9F2/resourceGroups/rgBulkactions/providers/Microsoft.Network/virtualNetworks/bulkvnet/subnets/default'
                      }
                    }
                  }
                ]
                primary: true
              }
            }
          ]
        }
        osProfile: {
          adminUsername: 'azureuser'
          computerName: 'bulkvm'
          linuxConfiguration: {
            disablePasswordAuthentication: true
            ssh: {
              publicKeys: [
                {
                  path: '/home/azureuser/.ssh/authorized_keys'
                  keyData: 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDExampleKeyReplaceWithYourOwn azureuser@bulklaunch'
                }
              ]
            }
          }
        }
        storageProfile: {
          imageReference: {
            offer: '0001-com-ubuntu-server-jammy'
            publisher: 'Canonical'
            sku: '22_04-lts-gen2'
            version: 'latest'
          }
          osDisk: {
            caching: 'ReadWrite'
            createOption: 'FromImage'
            deleteOption: 'Delete'
            managedDisk: {
              storageAccountType: 'Premium_LRS'
            }
            osType: 'Linux'
          }
        }
      }
    }
    executionParameters: {
      retryPolicy: {
        onFailureAction: 'Delete'
        retryWindowInMinutes: 30
      }
    }
    minCapacity: 1
    partialFulfillmentPolicy: {
      mode: 'Enabled'
    }
    priorityProfile: {
      type: 'Spot'
      allocationStrategy: 'LowestPrice'
      evictionPolicy: 'Delete'
      maxPricePerVM: 0.2
    }
    vmSizesProfile: [
      {
        name: 'Standard_D2s_v5'
        rank: 1
      }
      {
        name: 'Standard_D4s_v5'
        rank: 2
      }
    ]
    zoneAllocationPolicy: {
      distributionStrategy: 'BestEffortBalanced'
      zonePreferences: [
        {
          rank: 1
          zone: '1'
        }
        {
          rank: 2
          zone: '2'
        }
      ]
    }
  }
  tags: {
    env: 'prod'
    workload: 'batch-render'
  }
  zones: [
    '1'
    '2'
  ]
}
```

## microsoft.compute/locations/bulkcreatecustom

BulkCreateCustom_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Compute/locations/bulkCreateCustom@2026-09-06-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  properties: {
    capacity: 2
    capacityType: 'VM'
    computeProfile: {
      computeApiVersion: '2024-11-01'
      virtualMachineProfile: {
        networkProfile: {
          networkApiVersion: '2020-11-01'
          networkInterfaceConfigurations: [
            {
              name: 'bulkvm-nic'
              properties: {
                deleteOption: 'Delete'
                ipConfigurations: [
                  {
                    name: 'bulkvm-ipconfig'
                    properties: {
                      primary: true
                      subnet: {
                        id: '/subscriptions/1FBA3C66-5C9C-4391-B72F-9F52735FC9F2/resourceGroups/rgBulkactions/providers/Microsoft.Network/virtualNetworks/bulkvnet/subnets/default'
                      }
                    }
                  }
                ]
                primary: true
              }
            }
          ]
        }
        osProfile: {
          adminUsername: 'azureuser'
          computerName: 'bulkvm'
          linuxConfiguration: {
            disablePasswordAuthentication: true
            ssh: {
              publicKeys: [
                {
                  path: '/home/azureuser/.ssh/authorized_keys'
                  keyData: 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDExampleKeyReplaceWithYourOwn azureuser@bulklaunch'
                }
              ]
            }
          }
        }
        storageProfile: {
          imageReference: {
            offer: '0001-com-ubuntu-server-jammy'
            publisher: 'Canonical'
            sku: '22_04-lts-gen2'
            version: 'latest'
          }
          osDisk: {
            caching: 'ReadWrite'
            createOption: 'FromImage'
            deleteOption: 'Delete'
            managedDisk: {
              storageAccountType: 'Premium_LRS'
            }
            osType: 'Linux'
          }
        }
      }
    }
    executionParameters: {
      retryPolicy: {
        onFailureAction: 'Delete'
        retryWindowInMinutes: 30
      }
    }
    minCapacity: 1
    overridesProfile: {
      overrides: [
        {
          tags: {
            env: 'prod'
            workload: 'payments'
          }
          virtualMachineName: 'bulkvm-payments-0'
        }
        {
          tags: {
            workload: 'batch'
          }
        }
      ]
      virtualMachineNamePrefix: 'bulkvm'
    }
    partialFulfillmentPolicy: {
      mode: 'Enabled'
    }
    priorityProfile: {
      type: 'Spot'
      allocationStrategy: 'LowestPrice'
      evictionPolicy: 'Delete'
      maxPricePerVM: 0.2
    }
    vmSizesProfile: [
      {
        name: 'Standard_D2s_v5'
        rank: 1
      }
      {
        name: 'Standard_D4s_v5'
        override: {
          virtualMachineProfile: {
            storageProfile: {
              imageReference: {
                offer: '0001-com-ubuntu-server-jammy'
                publisher: 'Canonical'
                sku: '22_04-lts-arm64'
                version: 'latest'
              }
            }
          }
        }
        rank: 2
      }
    ]
    zoneAllocationPolicy: {
      distributionStrategy: 'BestEffortBalanced'
      zonePreferences: [
        {
          rank: 1
          zone: '1'
        }
        {
          rank: 2
          zone: '2'
        }
      ]
    }
  }
  tags: {
    env: 'prod'
    workload: 'batch-render'
  }
  zones: [
    '1'
    '2'
  ]
}
```

## microsoft.compute/scheduledactions

01 - Create a new recurring scheduled action
```bicep
resource exampleResource 'Microsoft.Compute/scheduledActions@2026-09-06-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    actionType: 'Start'
    notificationSettings: [
    ]
    resourceType: 'VirtualMachine'
    schedule: {
      requestedWeekDays: [
        'Monday'
        'Tuesday'
        'Wednesday'
        'Thursday'
        'Friday'
      ]
      scheduledTime: '07:00:00'
      timeZone: 'America/Los_Angeles'
    }
    startTime: '2026-09-15T07:00:00-07:00'
  }
}
```

02 - Create a recurring scheduled action with comprehensive settings
```bicep
resource exampleResource 'Microsoft.Compute/scheduledActions@2026-09-06-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    actionType: 'Start'
    disabled: false
    endTime: '2027-09-01T19:00:00-07:00'
    notificationSettings: [
      {
        type: 'Email'
        destination: 'admin@contoso.com'
        disabled: true
        language: 'en-us'
      }
    ]
    resourceType: 'VirtualMachine'
    schedule: {
      requestedDaysOfTheMonth: [
        1
        15
      ]
      requestedMonths: [
        'All'
      ]
      requestedWeekDays: [
        'All'
      ]
      scheduledTime: '19:00:00'
      timeZone: 'America/Los_Angeles'
    }
    startTime: '2026-09-01T19:00:00-07:00'
  }
  tags: {
    environment: 'production'
  }
}
```
