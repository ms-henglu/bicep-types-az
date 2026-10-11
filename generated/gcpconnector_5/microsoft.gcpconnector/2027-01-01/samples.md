# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/sqladmininstances

SQLAdminInstances_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/sqlAdminInstances@2027-01-01' = {
  name: 'example'
  location: 'global'
  properties: {
    gcpProjectId: 'test-project'
    gcpProjectNumber: '123456789'
    gcpProperties: {
      name: 'test-sql-instance'
      backendType: 'SECOND_GEN'
      connectionName: 'test-project:us-central1:test-sql-instance'
      createTime: '2025-06-19T19:45:45.743Z'
      databaseVersion: 'MYSQL_8_0'
      etag: 'abc123def456'
      gceZone: 'us-central1-a'
      instanceType: 'CLOUD_SQL_INSTANCE'
      ipAddresses: [
        {
          type: 'PRIMARY'
          ipAddress: '10.0.0.1'
        }
      ]
      kind: 'sql#instance'
      project: 'test-project'
      region: 'us-central1'
      satisfiesPzs: false
      selfLink: 'https://sqladmin.googleapis.com/sql/v1beta4/projects/test-project/instances/test-sql-instance'
      settings: {
        activationPolicy: 'ALWAYS'
        availabilityType: 'ZONAL'
        backupConfiguration: {
          enabled: true
          pointInTimeRecoveryEnabled: true
          startTime: '02:00'
          transactionLogRetentionDays: 7
        }
        dataDiskSizeGb: '20'
        dataDiskType: 'PD_SSD'
        ipConfiguration: {
          authorizedNetworks: [
            {
              name: 'test-network'
              value: '0.0.0.0/0'
            }
          ]
          ipv4Enabled: true
          requireSsl: false
        }
        pricingPlan: 'PER_USE'
        replicationType: 'SYNCHRONOUS'
        storageAutoResize: true
        storageAutoResizeLimit: '100'
        tier: 'db-n1-standard-1'
      }
      state: 'RUNNABLE'
    }
    gcpRegion: 'us-central1'
    gcpSourceSchema: 'sql#instance'
    gcpTags: {
      environment: 'test'
      project: 'test-project'
    }
    publicCloudConnectorsResourceId: 'test-connector-id'
    publicCloudResourceName: 'test-sql-instance'
    resourceName: 'test-sql-instance'
  }
  tags: {
    environment: 'test'
    project: 'test-project'
  }
}
```
