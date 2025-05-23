# Microsoft.StreamAnalytics
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.streamanalytics/streamingjobs

Create a complete streaming job (a streaming job with a transformation, at least 1 input and at least 1 output)
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs@2017-04-01-preview' = {
  name: 'example'
  location: 'West US'
  properties: {
    compatibilityLevel: '1.0'
    dataLocale: 'en-US'
    eventsLateArrivalMaxDelayInSeconds: 5
    eventsOutOfOrderMaxDelayInSeconds: 0
    eventsOutOfOrderPolicy: 'Drop'
    functions: [
    ]
    inputs: [
      {
        name: 'inputtest'
        properties: {
          type: 'Stream'
          datasource: {
            type: 'Microsoft.Storage/Blob'
            properties: {
              container: 'containerName'
              pathPattern: ''
              storageAccounts: [
                {
                  accountKey: 'yourAccountKey=='
                  accountName: 'yourAccountName'
                }
              ]
            }
          }
          serialization: {
            type: 'Json'
            properties: {
              encoding: 'UTF8'
            }
          }
        }
      }
    ]
    outputErrorPolicy: 'Drop'
    outputs: [
      {
        name: 'outputtest'
        properties: {
          datasource: {
            type: 'Microsoft.Sql/Server/Database'
            properties: {
              database: 'databaseName'
              password: 'userPassword'
              server: 'serverName'
              table: 'tableName'
              user: '<user>'
            }
          }
        }
      }
    ]
    sku: {
      name: 'Standard'
    }
    transformation: {
      name: 'transformationtest'
      properties: {
        query: 'Select Id, Name from inputtest'
        streamingUnits: 1
      }
    }
  }
  tags: {
    key1: 'value1'
    key3: 'value3'
    randomKey: 'randomValue'
  }
}
```

Create a streaming job shell (a streaming job with no inputs, outputs, transformation, or functions)
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs@2017-04-01-preview' = {
  name: 'example'
  location: 'West US'
  properties: {
    compatibilityLevel: '1.0'
    dataLocale: 'en-US'
    eventsLateArrivalMaxDelayInSeconds: 16
    eventsOutOfOrderMaxDelayInSeconds: 5
    eventsOutOfOrderPolicy: 'Drop'
    functions: [
    ]
    inputs: [
    ]
    outputErrorPolicy: 'Drop'
    outputs: [
    ]
    sku: {
      name: 'Standard'
    }
  }
  tags: {
    key1: 'value1'
    key3: 'value3'
    randomKey: 'randomValue'
  }
}
```

## microsoft.streamanalytics/streamingjobs/functions

Create a CLRUdf function
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/functions@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Scalar'
    properties: {
      binding: {
        type: 'Microsoft.StreamAnalytics/CLRUdf'
        properties: {
          method: 'SquareFunction'
          class: 'ASAEdgeUDFDemo.Class1'
          dllPath: 'ASAEdgeApplication2_CodeBehind'
        }
      }
      inputs: [
        {
          dataType: 'nvarchar(max)'
        }
      ]
      output: {
        dataType: 'nvarchar(max)'
      }
    }
  }
}
```

Create a JavaScript function
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/functions@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Scalar'
    properties: {
      binding: {
        type: 'Microsoft.StreamAnalytics/JavascriptUdf'
        properties: {
          script: 'function (x, y) { return x + y; }'
        }
      }
      inputs: [
        {
          dataType: 'Any'
        }
      ]
      output: {
        dataType: 'Any'
      }
    }
  }
}
```

Create an Azure ML function
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/functions@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Scalar'
    properties: {
      binding: {
        type: 'Microsoft.MachineLearning/WebService'
        properties: {
          apiKey: 'someApiKey=='
          batchSize: 1000
          endpoint: 'someAzureMLEndpointURL'
          inputs: {
            name: 'input1'
            columnNames: [
              {
                name: 'tweet'
                dataType: 'string'
                mapTo: 0
              }
            ]
          }
          outputs: [
            {
              name: 'Sentiment'
              dataType: 'string'
            }
          ]
        }
      }
      inputs: [
        {
          dataType: 'nvarchar(max)'
        }
      ]
      output: {
        dataType: 'nvarchar(max)'
      }
    }
  }
}
```

Create an Azure ML Service function
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/functions@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Scalar'
    properties: {
      binding: {
        type: 'Microsoft.MachineLearningServices'
        properties: {
          apiKey: 'someApiKey=='
          batchSize: 1000
          endpoint: 'someAzureMLEndpointURL'
          inputs: [
            {
              name: 'data'
              dataType: 'array'
              mapTo: 0
            }
          ]
          numberOfParallelRequests: 1
          outputs: [
            {
              name: 'Sentiment'
              dataType: 'string'
            }
          ]
        }
      }
      inputs: [
        {
          dataType: 'nvarchar(max)'
        }
      ]
      output: {
        dataType: 'nvarchar(max)'
      }
    }
  }
}
```

## microsoft.streamanalytics/streamingjobs/inputs

Create a reference blob input with CSV serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/inputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Reference'
    datasource: {
      type: 'Microsoft.Storage/Blob'
      properties: {
        container: 'state'
        dateFormat: 'yyyy/MM/dd'
        pathPattern: '{date}/{time}'
        storageAccounts: [
          {
            accountKey: 'someAccountKey=='
            accountName: 'someAccountName'
          }
        ]
        timeFormat: 'HH'
      }
    }
    serialization: {
      type: 'Csv'
      properties: {
        encoding: 'UTF8'
        fieldDelimiter: ','
      }
    }
  }
}
```

Create a stream blob input with CSV serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/inputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Stream'
    datasource: {
      type: 'Microsoft.Storage/Blob'
      properties: {
        container: 'state'
        dateFormat: 'yyyy/MM/dd'
        pathPattern: '{date}/{time}'
        sourcePartitionCount: 16
        storageAccounts: [
          {
            accountKey: 'someAccountKey=='
            accountName: 'someAccountName'
          }
        ]
        timeFormat: 'HH'
      }
    }
    serialization: {
      type: 'Csv'
      properties: {
        encoding: 'UTF8'
        fieldDelimiter: ','
      }
    }
  }
}
```

Create a stream Event Hub input with JSON serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/inputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Stream'
    datasource: {
      type: 'Microsoft.ServiceBus/EventHub'
      properties: {
        consumerGroupName: 'sdkconsumergroup'
        eventHubName: 'sdkeventhub'
        serviceBusNamespace: 'sdktest'
        sharedAccessPolicyKey: 'someSharedAccessPolicyKey=='
        sharedAccessPolicyName: 'RootManageSharedAccessKey'
      }
    }
    serialization: {
      type: 'Json'
      properties: {
        encoding: 'UTF8'
      }
    }
  }
}
```

Create a stream IoT Hub input with Avro serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/inputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'Stream'
    datasource: {
      type: 'Microsoft.Devices/IotHubs'
      properties: {
        consumerGroupName: 'sdkconsumergroup'
        endpoint: 'messages/events'
        iotHubNamespace: 'iothub'
        sharedAccessPolicyKey: 'sharedAccessPolicyKey='
        sharedAccessPolicyName: 'owner'
      }
    }
    serialization: {
      type: 'Avro'
    }
  }
}
```

## microsoft.streamanalytics/streamingjobs/outputs

Create a blob output with CSV serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Storage/Blob'
      properties: {
        container: 'state'
        dateFormat: 'yyyy/MM/dd'
        pathPattern: '{date}/{time}'
        storageAccounts: [
          {
            accountKey: 'accountKey=='
            accountName: 'someAccountName'
          }
        ]
        timeFormat: 'HH'
      }
    }
    serialization: {
      type: 'Csv'
      properties: {
        encoding: 'UTF8'
        fieldDelimiter: ','
      }
    }
  }
}
```

Create a Delta Lake output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Storage/Blob'
      properties: {
        container: 'deltaoutput'
        dateFormat: {
        }
        pathPattern: {
        }
        storageAccounts: [
          {
            accountKey: 'accountKey=='
            accountName: 'someAccountName'
          }
        ]
        timeFormat: {
        }
      }
    }
    serialization: {
      type: 'Delta'
      properties: {
        deltaTablePath: '/folder1/table1'
        partitionColumns: [
          'column1'
        ]
      }
    }
  }
}
```

Create a DocumentDB output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Storage/DocumentDB'
      properties: {
        accountId: 'someAccountId'
        accountKey: 'accountKey=='
        collectionNamePattern: 'collection'
        database: 'db01'
        documentId: 'documentId'
        partitionKey: 'key'
      }
    }
  }
}
```

Create a Power BI output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'PowerBI'
      properties: {
        authenticationMode: 'ConnectionString'
        dataset: 'someDataset'
        groupId: 'ac40305e-3e8d-43ac-8161-c33799f43e95'
        groupName: 'MyPowerBIGroup'
        refreshToken: 'someRefreshToken=='
        table: 'someTable'
        tokenUserDisplayName: 'Bob Smith'
        tokenUserPrincipalName: 'bobsmith@contoso.com'
      }
    }
  }
}
```

Create a Service Bus Queue output with Avro serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.ServiceBus/Queue'
      properties: {
        propertyColumns: [
          'column1'
          'column2'
        ]
        queueName: 'sdkqueue'
        serviceBusNamespace: 'sdktest'
        sharedAccessPolicyKey: 'sharedAccessPolicyKey='
        sharedAccessPolicyName: 'RootManageSharedAccessKey'
      }
    }
    serialization: {
      type: 'Avro'
    }
  }
}
```

Create a Service Bus Topic output with CSV serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.ServiceBus/Topic'
      properties: {
        propertyColumns: [
          'column1'
          'column2'
        ]
        serviceBusNamespace: 'sdktest'
        sharedAccessPolicyKey: 'sharedAccessPolicyKey='
        sharedAccessPolicyName: 'RootManageSharedAccessKey'
        topicName: 'sdktopic'
      }
    }
    serialization: {
      type: 'Csv'
      properties: {
        encoding: 'UTF8'
        fieldDelimiter: ','
      }
    }
  }
}
```

Create an Azure Data Lake Store output with JSON serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.DataLake/Accounts'
      properties: {
        accountName: 'someaccount'
        dateFormat: 'yyyy/MM/dd'
        filePathPrefix: '{date}/{time}'
        refreshToken: 'someRefreshToken=='
        tenantId: 'cea4e98b-c798-49e7-8c40-4a2b3beb47dd'
        timeFormat: 'HH'
        tokenUserDisplayName: 'Bob Smith'
        tokenUserPrincipalName: 'bobsmith@contoso.com'
      }
    }
    serialization: {
      type: 'Json'
      properties: {
        format: 'Array'
        encoding: 'UTF8'
      }
    }
  }
}
```

Create an Azure Data Warehouse output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Sql/Server/DataWarehouse'
      properties: {
        database: 'zhayaSQLpool'
        password: 'password123'
        server: 'asatestserver'
        table: 'test2'
        user: 'tolladmin'
      }
    }
  }
}
```

Create an Azure Function output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.AzureFunction'
      properties: {
        apiKey: {
        }
        functionAppName: 'functionappforasaautomation'
        functionName: 'HttpTrigger2'
        maxBatchCount: 100
        maxBatchSize: 256
      }
    }
  }
}
```

Create an Azure SQL database output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Sql/Server/Database'
      properties: {
        database: 'someDatabase'
        password: 'somePassword'
        server: 'someServer'
        table: 'someTable'
        user: '<user>'
      }
    }
  }
}
```

Create an Azure Table output
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.Storage/Table'
      properties: {
        accountKey: 'accountKey=='
        accountName: 'someAccountName'
        batchSize: 25
        columnsToRemove: [
          'column1'
          'column2'
        ]
        partitionKey: 'partitionKey'
        rowKey: 'rowKey'
        table: 'samples'
      }
    }
  }
}
```

Create an Event Hub output with JSON serialization
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/outputs@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    datasource: {
      type: 'Microsoft.ServiceBus/EventHub'
      properties: {
        eventHubName: 'sdkeventhub'
        partitionKey: 'partitionKey'
        serviceBusNamespace: 'sdktest'
        sharedAccessPolicyKey: 'sharedAccessPolicyKey='
        sharedAccessPolicyName: 'RootManageSharedAccessKey'
      }
    }
    serialization: {
      type: 'Json'
      properties: {
        format: 'Array'
        encoding: 'UTF8'
      }
    }
  }
}
```

## microsoft.streamanalytics/streamingjobs/transformations

Create a transformation
```bicep
resource exampleResource 'Microsoft.StreamAnalytics/streamingjobs/transformations@2017-04-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    query: 'Select Id, Name from inputtest'
    streamingUnits: 6
  }
}
```
