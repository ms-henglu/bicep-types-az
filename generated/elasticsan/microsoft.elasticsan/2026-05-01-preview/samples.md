# Microsoft.ElasticSan
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.elasticsan/elasticsans

ElasticSans_V1_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans@2026-05-01-preview' = {
  name: 'example'
  location: 'France Central'
  properties: {
    autoScaleProperties: {
      scaleUpProperties: {
        autoScalePolicyEnforcement: 'None'
        capacityUnitScaleUpLimitTiB: 17
        increaseCapacityUnitByTiB: 4
        unusedSizeTiB: 24
      }
    }
    availabilityZones: [
      '1'
    ]
    baseSizeTiB: 5
    extendedCapacitySizeTiB: 25
    publicNetworkAccess: 'Enabled'
    sku: {
      name: 'Premium_LRS'
      tier: 'Premium'
    }
    version: 'V1'
  }
  tags: {
    key9316: 'ihndtieqibtob'
  }
}
```

ElasticSans_V1_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans@2026-05-01-preview' = {
  name: 'example'
  location: 'France Central'
  properties: {
    baseSizeTiB: 15
    extendedCapacitySizeTiB: 27
    sku: {
      name: 'Premium_LRS'
    }
  }
}
```

ElasticSans_V2_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans@2026-05-01-preview' = {
  name: 'example'
  location: 'France Central'
  properties: {
    autoScaleProperties: {
      scaleUpProperties: {
        autoScalePolicyEnforcement: 'None'
        capacityUnitScaleUpLimitTiB: 17
        increaseCapacityUnitByTiB: 4
        unusedSizeTiB: 24
      }
    }
    availabilityZones: [
      '1'
    ]
    publicNetworkAccess: 'Enabled'
    sku: {
      name: 'ElasticSAN_LRS'
    }
    totalIops: 22
    totalMBps: 4
    totalSizeTiB: 27
    version: 'V2'
  }
  tags: {
    key9316: 'ihndtieqibtob'
  }
}
```

ElasticSans_V2_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans@2026-05-01-preview' = {
  name: 'example'
  location: 'France Central'
  properties: {
    sku: {
      name: 'ElasticSAN_LRS'
    }
    totalIops: 22
    totalMBps: 4
    totalSizeTiB: 27
    version: 'V2'
  }
}
```

## microsoft.elasticsan/elasticsans/privateendpointconnections

PrivateEndpointConnections_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/privateEndpointConnections@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    groupIds: [
      'jdwrzpemdjrpiwzvy'
    ]
    privateEndpoint: {
    }
    privateLinkServiceConnectionState: {
      description: 'dxl'
      actionsRequired: 'jhjdpwvyzipggtn'
      status: 'Pending'
    }
  }
}
```

PrivateEndpointConnections_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/privateEndpointConnections@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
    }
  }
}
```

## microsoft.elasticsan/elasticsans/volumegroups

VolumeGroups_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'None'
    userAssignedIdentities: {
      key2350: {
      }
    }
  }
  properties: {
    deleteRetentionPolicy: {
      policyState: 'Enabled'
      retentionPeriodDays: 14
    }
    encryption: 'EncryptionAtRestWithPlatformKey'
    encryptionInTransit: true
    encryptionProperties: {
      identity: {
        userAssignedIdentity: 'vgbeephfgecgg'
      }
      keyVaultProperties: {
        keyName: 'rommjwp'
        keyVaultUri: 'https://microsoft.com/at'
        keyVersion: 'ulmxxgzgsuhalwesmhfslq'
      }
    }
    enforceDataIntegrityCheckForIscsi: true
    networkAcls: {
      virtualNetworkRules: [
        {
          action: 'Allow'
          id: 'fhhawhc'
        }
      ]
    }
    protocolType: 'Iscsi'
  }
}
```

VolumeGroups_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
}
```

VolumeGroups_GeneralPurpose_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'None'
    userAssignedIdentities: {
      key2350: {
      }
    }
  }
  properties: {
    deleteRetentionPolicy: {
      policyState: 'Enabled'
      retentionPeriodDays: 14
    }
    encryption: 'EncryptionAtRestWithPlatformKey'
    encryptionInTransit: true
    encryptionProperties: {
      identity: {
        userAssignedIdentity: 'vgbeephfgecgg'
      }
      keyVaultProperties: {
        keyName: 'rommjwp'
        keyVaultUri: 'https://microsoft.com/at'
        keyVersion: 'ulmxxgzgsuhalwesmhfslq'
      }
    }
    enforceDataIntegrityCheckForIscsi: true
    networkAcls: {
      virtualNetworkRules: [
        {
          action: 'Allow'
          id: 'fhhawhc'
        }
      ]
    }
    protocolType: 'Iscsi'
    qualityOfService: 'GeneralPurpose'
  }
}
```

VolumeGroups_GeneralPurpose_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    protocolType: 'Iscsi'
    qualityOfService: 'GeneralPurpose'
  }
}
```

VolumeGroups_PerformanceCritical_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'None'
    userAssignedIdentities: {
      key2350: {
      }
    }
  }
  properties: {
    encryption: 'EncryptionAtRestWithPlatformKey'
    encryptionProperties: {
      identity: {
        userAssignedIdentity: 'vgbeephfgecgg'
      }
      keyVaultProperties: {
        keyName: 'rommjwp'
        keyVaultUri: 'https://microsoft.com/at'
        keyVersion: 'ulmxxgzgsuhalwesmhfslq'
      }
    }
    protocolType: 'DirectAttach'
    qualityOfService: 'PerformanceCritical'
    reservedIops: 10000
    reservedMBps: 800
  }
}
```

VolumeGroups_PerformanceCritical_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    protocolType: 'DirectAttach'
    qualityOfService: 'PerformanceCritical'
    reservedIops: 10000
    reservedMBps: 800
  }
}
```

## microsoft.elasticsan/elasticsans/volumegroups/snapshots

VolumeSnapshots_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups/snapshots@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    creationData: {
      sourceId: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ElasticSan/elasticSans/{elasticSanName}/volumegroups/{volumeGroupName}/volumes/{volumeName}'
    }
  }
}
```

VolumeSnapshots_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups/snapshots@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    creationData: {
      sourceId: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ElasticSan/elasticSans/{elasticSanName}/volumegroups/{volumeGroupName}/volumes/{volumeName}'
    }
  }
}
```

## microsoft.elasticsan/elasticsans/volumegroups/volumes

Volumes_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups/volumes@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    creationData: {
      createSource: 'None'
      sourceId: 'mdonegivjquite'
    }
    managedBy: [
      {
        clientId: 'pclpkrpkpmvcsegcubrakcoodrubo'
        resourceIds: [
          '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.SomeProvider/someResource/myResource'
        ]
        version: 1
      }
    ]
    sizeGiB: 23
  }
}
```

Volumes_Create_MinimumSet_Gen
```bicep
resource exampleResource 'Microsoft.ElasticSan/elasticSans/volumegroups/volumes@2026-05-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    sizeGiB: 9
  }
}
```
