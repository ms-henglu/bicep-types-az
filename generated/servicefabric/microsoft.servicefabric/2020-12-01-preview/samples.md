# Microsoft.ServiceFabric
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.servicefabric/clusters

Put a cluster with maximum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters@2020-12-01-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    addOnFeatures: [
      'RepairManager'
      'DnsService'
      'BackupRestoreService'
      'ResourceMonitorService'
    ]
    applicationTypeVersionsCleanupPolicy: {
      maxUnusedVersionsToKeep: 2
    }
    azureActiveDirectory: {
      clientApplication: 'd151ad89-4bce-4ae8-b3d1-1dc79679fa75'
      clusterApplication: '5886372e-7bf4-4878-a497-8098aba608ae'
      tenantId: '6abcc6a0-8666-43f1-87b8-172cf86a9f9c'
    }
    certificateCommonNames: {
      commonNames: [
        {
          certificateCommonName: 'abc.com'
          certificateIssuerThumbprint: '12599211F8F14C90AFA9532AD79A6F2CA1C00622'
        }
      ]
      x509StoreName: 'My'
    }
    clientCertificateCommonNames: [
      {
        certificateCommonName: 'abc.com'
        certificateIssuerThumbprint: '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'
        isAdmin: true
      }
    ]
    clientCertificateThumbprints: [
      {
        certificateThumbprint: '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'
        isAdmin: true
      }
    ]
    clusterCodeVersion: '7.0.470.9590'
    diagnosticsStorageAccountConfig: {
      blobEndpoint: 'https://diag.blob.core.windows.net/'
      protectedAccountKeyName: 'StorageAccountKey1'
      queueEndpoint: 'https://diag.queue.core.windows.net/'
      storageAccountName: 'diag'
      tableEndpoint: 'https://diag.table.core.windows.net/'
    }
    eventStoreServiceEnabled: true
    fabricSettings: [
      {
        name: 'UpgradeService'
        parameters: [
          {
            name: 'AppPollIntervalInSeconds'
            value: '60'
          }
        ]
      }
    ]
    managementEndpoint: 'https://myCluster.eastus.cloudapp.azure.com:19080'
    nodeTypes: [
      {
        name: 'nt1vm'
        applicationPorts: {
          endPort: 30000
          startPort: 20000
        }
        clientConnectionEndpointPort: 19000
        durabilityLevel: 'Bronze'
        ephemeralPorts: {
          endPort: 64000
          startPort: 49000
        }
        httpGatewayEndpointPort: 19007
        isPrimary: true
        vmInstanceCount: 5
      }
    ]
    reliabilityLevel: 'Silver'
    reverseProxyCertificateCommonNames: {
      commonNames: [
        {
          certificateCommonName: 'abc.com'
          certificateIssuerThumbprint: '12599211F8F14C90AFA9532AD79A6F2CA1C00622'
        }
      ]
      x509StoreName: 'My'
    }
    upgradeDescription: {
      deltaHealthPolicy: {
        applicationDeltaHealthPolicies: {
          'fabric:/myApp1': {
            defaultServiceTypeDeltaHealthPolicy: {
              maxPercentDeltaUnhealthyServices: 0
            }
            serviceTypeDeltaHealthPolicies: {
              myServiceType1: {
                maxPercentDeltaUnhealthyServices: 0
              }
            }
          }
        }
        maxPercentDeltaUnhealthyApplications: 0
        maxPercentDeltaUnhealthyNodes: 0
        maxPercentUpgradeDomainDeltaUnhealthyNodes: 0
      }
      forceRestart: false
      healthCheckRetryTimeout: '00:05:00'
      healthCheckStableDuration: '00:00:30'
      healthCheckWaitDuration: '00:00:30'
      healthPolicy: {
        applicationHealthPolicies: {
          'fabric:/myApp1': {
            defaultServiceTypeHealthPolicy: {
              maxPercentUnhealthyServices: 0
            }
            serviceTypeHealthPolicies: {
              myServiceType1: {
                maxPercentUnhealthyServices: 100
              }
            }
          }
        }
        maxPercentUnhealthyApplications: 0
        maxPercentUnhealthyNodes: 0
      }
      upgradeDomainTimeout: '00:15:00'
      upgradeReplicaSetCheckTimeout: '00:10:00'
      upgradeTimeout: '01:00:00'
    }
    upgradeMode: 'Manual'
    vmImage: 'Windows'
  }
  tags: {
  }
}
```

Put a cluster with minimum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters@2020-12-01-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    diagnosticsStorageAccountConfig: {
      blobEndpoint: 'https://diag.blob.core.windows.net/'
      protectedAccountKeyName: 'StorageAccountKey1'
      queueEndpoint: 'https://diag.queue.core.windows.net/'
      storageAccountName: 'diag'
      tableEndpoint: 'https://diag.table.core.windows.net/'
    }
    fabricSettings: [
      {
        name: 'UpgradeService'
        parameters: [
          {
            name: 'AppPollIntervalInSeconds'
            value: '60'
          }
        ]
      }
    ]
    managementEndpoint: 'http://myCluster.eastus.cloudapp.azure.com:19080'
    nodeTypes: [
      {
        name: 'nt1vm'
        applicationPorts: {
          endPort: 30000
          startPort: 20000
        }
        clientConnectionEndpointPort: 19000
        durabilityLevel: 'Bronze'
        ephemeralPorts: {
          endPort: 64000
          startPort: 49000
        }
        httpGatewayEndpointPort: 19007
        isPrimary: true
        vmInstanceCount: 5
      }
    ]
    reliabilityLevel: 'Silver'
    upgradeMode: 'Automatic'
  }
  tags: {
  }
}
```

## microsoft.servicefabric/clusters/applications

Put an application with maximum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applications@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    maximumNodes: 3
    metrics: [
      {
        name: 'metric1'
        maximumCapacity: 3
        reservationCapacity: 1
        totalApplicationCapacity: 5
      }
    ]
    minimumNodes: 1
    parameters: {
      param1: 'value1'
    }
    removeApplicationCapacity: false
    typeName: 'myAppType'
    typeVersion: '1.0'
    upgradePolicy: {
      applicationHealthPolicy: {
        considerWarningAsError: true
        defaultServiceTypeHealthPolicy: {
          maxPercentUnhealthyPartitionsPerService: 0
          maxPercentUnhealthyReplicasPerPartition: 0
          maxPercentUnhealthyServices: 0
        }
        maxPercentUnhealthyDeployedApplications: 0
      }
      forceRestart: false
      rollingUpgradeMonitoringPolicy: {
        failureAction: 'Rollback'
        healthCheckRetryTimeout: '00:10:00'
        healthCheckStableDuration: '00:05:00'
        healthCheckWaitDuration: '00:02:00'
        upgradeDomainTimeout: '1.06:00:00'
        upgradeTimeout: '01:00:00'
      }
      upgradeMode: 'Monitored'
      upgradeReplicaSetCheckTimeout: '01:00:00'
    }
  }
}
```

Put an application with minimum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applications@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    removeApplicationCapacity: false
    typeName: 'myAppType'
    typeVersion: '1.0'
  }
}
```

## microsoft.servicefabric/clusters/applications/services

Put a service with maximum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applications/services@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    correlationScheme: [
      {
        scheme: 'Affinity'
        serviceName: 'fabric:/app1/app1~svc1'
      }
    ]
    defaultMoveCost: 'Medium'
    instanceCount: 5
    partitionDescription: {
      partitionScheme: 'Singleton'
    }
    placementConstraints: 'NodeType==frontend'
    serviceDnsName: 'my.service.dns'
    serviceKind: 'Stateless'
    serviceLoadMetrics: [
      {
        name: 'metric1'
        weight: 'Low'
      }
    ]
    servicePackageActivationMode: 'SharedProcess'
    servicePlacementPolicies: [
    ]
    serviceTypeName: 'myServiceType'
  }
}
```

Put a service with minimum parameters
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applications/services@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    instanceCount: 1
    partitionDescription: {
      partitionScheme: 'Singleton'
    }
    serviceKind: 'Stateless'
    serviceTypeName: 'myServiceType'
  }
}
```

## microsoft.servicefabric/clusters/applicationtypes

Put an application type
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applicationTypes@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
}
```

## microsoft.servicefabric/clusters/applicationtypes/versions

Put an application type version
```bicep
resource exampleResource 'Microsoft.ServiceFabric/clusters/applicationTypes/versions@2020-12-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    appPackageUrl: 'http://fakelink.test.com/MyAppType'
  }
}
```
