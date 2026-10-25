# Microsoft.HorizonDb
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.horizondb/clusters

Create a HorizonDB cluster with customer-managed key data encryption
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters@2026-10-01-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/identity-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/primary-encryption-identity': {
      }
    }
  }
  location: 'eastus2'
  properties: {
    backup: {
      geoRedundancy: 'Disabled'
      retentionDays: 14
    }
    dataEncryption: {
      type: 'AzureKeyVault'
      primaryKeyUri: 'https://primary-key-vault.vault.azure.net/keys/horizondb-primary-key'
      primaryUserAssignedIdentityId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/identity-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/primary-encryption-identity'
    }
    postgreSqlVersion: '17'
  }
}
```

Create a PostgreSQL 18 HorizonDB cluster with minimum configuration and service defaults
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters@2026-10-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
    backup: {
      geoRedundancy: 'Disabled'
    }
    postgreSqlVersion: '18'
  }
}
```

Create or replace a HorizonDB cluster
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters@2026-10-01-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/identity-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/fabric-writer': {
      }
    }
  }
  location: 'eastus2'
  properties: {
    backup: {
      geoRedundancy: 'Enabled'
      retentionDays: 14
    }
    network: {
      publicAccess: 'Enabled'
    }
    postgreSqlVersion: '17'
  }
  tags: {
    environment: 'production'
  }
}
```

Restore a HorizonDB cluster across Azure regions from the latest available backup
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters@2026-10-01-preview' = {
  name: 'example'
  location: 'westus2'
  properties: {
    backup: {
      geoRedundancy: 'Enabled'
      retentionDays: 14
    }
    creationMode: 'PointInTimeRestore'
    creationSourceClusterLocation: 'eastus2'
    creationSourceClusterResourceId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/example-resource-group/providers/Microsoft.HorizonDb/clusters/source-cluster'
    network: {
      publicAccess: 'Disabled'
    }
    pointInTimeUtc: '2026-07-27T12:00:00Z'
  }
}
```

Restore a HorizonDB cluster to a point in time
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters@2026-10-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
    backup: {
      geoRedundancy: 'Enabled'
      retentionDays: 14
    }
    creationMode: 'PointInTimeRestore'
    creationSourceClusterResourceId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/example-resource-group/providers/Microsoft.HorizonDb/clusters/source-cluster'
    network: {
      publicAccess: 'Disabled'
    }
    pointInTimeUtc: '2026-07-27T12:00:00Z'
  }
}
```

## microsoft.horizondb/clusters/authentications

Disable Microsoft Entra authentication declaratively
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/authentications@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    state: 'Disabled'
  }
}
```

Enable Microsoft Entra authentication declaratively
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/authentications@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    state: 'Enabled'
  }
}
```

Enable password authentication and set the administrator login and password during initial setup
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/authentications@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    administratorLogin: 'adminlogin1'
    administratorLoginPassword: '********'
    state: 'Enabled'
  }
}
```

## microsoft.horizondb/clusters/changedatacapture

Enable the cluster change data capture capability
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/changeDataCapture@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    autoUpgradeExtension: true
    desiredState: 'Enabled'
  }
}
```

## microsoft.horizondb/clusters/changedatacaptureconfigurations

Enroll a database for Microsoft Fabric Mirroring
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/changeDataCaptureConfigurations@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    databaseName: 'sales'
    desiredState: 'Enabled'
    destinationResourceId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/example-resource-group/providers/Microsoft.HorizonDb/clusters/example-cluster/changeDataCaptureDestinations/fabric-mirroring'
    usageProfile: 'Mirroring'
  }
}
```

## microsoft.horizondb/clusters/changedatacapturedestinations

Create a Microsoft Fabric change data capture destination
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/changeDataCaptureDestinations@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    desiredState: 'Enabled'
    destination: {
      destinationType: 'Fabric'
      workspaceId: 'aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee'
      protocol: 'Native'
    }
  }
}
```

## microsoft.horizondb/clusters/changedatacapturedestinations/identityassignments

Create a change data capture identity assignment for a UAMI attached to the parent cluster
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/changeDataCaptureDestinations/identityAssignments@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    identityResourceId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/identity-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/fabric-writer'
  }
}
```

## microsoft.horizondb/clusters/microsoftentraadministrators

Create or replace a Microsoft Entra administrator for a HorizonDB cluster
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/microsoftEntraAdministrators@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    principalName: 'database.administrators@contoso.com'
    principalType: 'Group'
    tenantId: '22222222-2222-2222-2222-222222222222'
  }
}
```

## microsoft.horizondb/clusters/pools

Create a minimum provisioned HorizonDB pool
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/pools@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    computeModel: {
      type: 'Provisioned'
      computeGeneration: 3
      computeProcessor: 'AMD'
      vCores: 2
    }
    highAvailability: {
      mode: 'Disabled'
    }
    nodeCount: 1
    parameterGroup: {
      applyMethod: 'Immediate'
      parameterGroupResourceId: '/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/providers/Microsoft.HorizonDb/locations/eastus2/parameterGroups/default-postgresql-17-provisioned'
    }
    scheduledMaintenance: {
      maintenanceManagementType: 'System'
    }
  }
}
```

## microsoft.horizondb/clusters/pools/firewallrules

Create or replace a firewall rule on a HorizonDB pool
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/pools/firewallRules@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Allow access from the corporate network'
    endIpAddress: '10.0.0.254'
    startIpAddress: '10.0.0.1'
  }
}
```

## microsoft.horizondb/clusters/privateendpointconnections

Approve or reject a private endpoint connection
```bicep
resource exampleResource 'Microsoft.HorizonDb/clusters/privateEndpointConnections@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
      description: 'Approved for the production database network'
      status: 'Approved'
    }
  }
}
```

## microsoft.horizondb/parametergroups

Create or replace a HorizonDB parameter group for a PostgreSQL version
```bicep
resource exampleResource 'Microsoft.HorizonDb/parameterGroups@2026-10-01-preview' = {
  name: 'example'
  location: 'eastus2'
  properties: {
    description: 'Parameters for production transactional workloads'
    parameters: [
      {
        name: 'application_name'
        value: 'horizondb-production'
      }
      {
        name: 'autovacuum'
        value: 'off'
      }
      {
        name: 'wal_receiver_timeout'
        value: '45000'
      }
      {
        name: 'work_mem'
        value: '8192'
      }
      {
        name: 'xmlbinary'
        value: 'base64'
      }
    ]
    postgreSqlVersion: '17'
  }
  tags: {
    environment: 'production'
  }
}
```
