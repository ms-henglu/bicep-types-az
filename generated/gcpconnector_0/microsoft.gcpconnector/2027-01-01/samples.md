# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/bigquerydatasets

BigQueryDatasets_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/bigQueryDatasets@2027-01-01' = {
  name: 'example'
  location: 'ljgjmtocpdgzmm'
  properties: {
    gcpProjectId: 'lvknddutseiexgbnso'
    gcpProjectNumber: 'dwwjpxudgxrmxnhshqgowpgf'
    gcpProperties: {
      type: 'DEFAULT'
      description: 'This is a test BigQuery dataset'
      access: [
        {
          role: 'OWNER'
          userByEmail: 'user@example.com'
        }
        {
          groupByEmail: 'team@example.com'
          role: 'READER'
        }
        {
          role: 'WRITER'
          specialGroup: 'projectWriters'
        }
      ]
      creationTime: '1632150000000'
      datasetReference: {
        datasetId: 'test-dataset'
        projectId: 'test-project'
      }
      defaultCollation: 'und:ci'
      defaultEncryptionConfiguration: {
        kmsKeyName: 'projects/test-project/locations/us/keyRings/test-keyring/cryptoKeys/test-key'
      }
      defaultPartitionExpirationMs: '259200000'
      defaultRoundingMode: 'ROUND_HALF_EVEN'
      defaultTableExpirationMs: '604800000'
      etag: 'abc123def456'
      friendlyName: 'Test Dataset'
      id: 'test-project:test-dataset'
      isCaseInsensitive: true
      kind: 'bigquery#dataset'
      labels: {
        department: 'engineering'
        environment: 'test'
      }
      lastModifiedTime: '1642150000000'
      linkedDatasetMetadata: {
        status: 'SYNCED'
      }
      linkedDatasetSource: {
        sourceDataset: {
          datasetId: 'source-dataset'
          projectId: 'source-project'
        }
      }
      location: 'US'
      maxTimeTravelHours: '168'
      resourceTags: {
        environment: 'development'
        project: 'testproject'
      }
      satisfiesPzi: false
      satisfiesPzs: true
      selfLink: 'https://bigquery.googleapis.com/bigquery/v2/projects/test-project/datasets/test-dataset'
      storageBillingModel: 'LOGICAL'
      tags: [
        {
          key: 'tag-key/name'
          value: 'tag-value'
        }
      ]
    }
    gcpRegion: 'hrrgxzyebg'
    gcpSourceSchema: 'ewziyhomey'
    gcpTags: {
    }
    publicCloudConnectorsResourceId: 'dhkwede'
    publicCloudResourceName: 'loypjtufnnsu'
    resourceName: 'cctuwniqhjgjyiwatf'
  }
  tags: {
  }
}
```
