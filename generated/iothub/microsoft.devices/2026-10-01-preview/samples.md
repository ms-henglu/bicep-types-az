# Microsoft.Devices
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.devices/iothubs

CreateOrReplace_IotHub
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs@2026-10-01-preview' = {
  name: 'example'
  etag: 'AAAAAAFD6M4='
  location: 'centraluseuap'
  properties: {
    cloudToDevice: {
      defaultTtlAsIso8601: 'PT1H'
      feedback: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
      maxDeliveryCount: 10
    }
    enableDataResidency: true
    enableFileUploadNotifications: false
    eventHubEndpoints: {
      events: {
        partitionCount: 2
        retentionTimeInDays: 1
      }
    }
    features: 'None'
    ipFilterRules: [
    ]
    ipVersion: 'ipv4ipv6'
    messagingEndpoints: {
      fileNotifications: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
    }
    minTlsVersion: '1.2'
    networkRuleSets: {
      applyToBuiltInEventHubEndpoint: true
      defaultAction: 'Deny'
      ipRules: [
        {
          action: 'Allow'
          filterName: 'rule1'
          ipMask: '131.117.159.53'
        }
        {
          action: 'Allow'
          filterName: 'rule2'
          ipMask: '157.55.59.128/25'
        }
      ]
    }
    rootCertificate: {
      enableRootCertificateV2: true
    }
    routing: {
      endpoints: {
        eventHubs: [
        ]
        serviceBusQueues: [
        ]
        serviceBusTopics: [
        ]
        storageContainers: [
        ]
      }
      fallbackRoute: {
        name: '$fallback'
        condition: 'true'
        endpointNames: [
          'events'
        ]
        isEnabled: true
        source: 'DeviceMessages'
      }
      routes: [
        {
          name: 'Routeid'
          condition: 'true'
          dataSchema: 'aio-sr://aiosaalkopkedev/62a24af1d7db61cd44b2ad6b6c3f4ab7312be447f89ff3401d18357d0d05ce3a:1'
          endpointNames: [
            'events'
          ]
          isEnabled: true
          source: 'DeviceMessages'
        }
      ]
    }
    storageEndpoints: {
      '$default': {
        connectionString: ''
        containerName: ''
        sasTtlAsIso8601: 'PT1H'
      }
    }
  }
  sku: {
    name: 'S1'
    capacity: 1
  }
  tags: {
  }
}
```

CreateOrReplace_IoTHub_With_MqttV5
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs@2026-10-01-preview' = {
  name: 'example'
  etag: 'AAAAAAFD6M4='
  location: 'centraluseuap'
  properties: {
    cloudToDevice: {
      defaultTtlAsIso8601: 'PT1H'
      feedback: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
      maxDeliveryCount: 10
    }
    connectionProfile: 'MqttV5'
    enableDataResidency: true
    enableFileUploadNotifications: false
    eventHubEndpoints: {
      events: {
        partitionCount: 2
        retentionTimeInDays: 1
      }
    }
    features: 'None'
    ipFilterRules: [
    ]
    ipVersion: 'ipv4ipv6'
    messagingEndpoints: {
      fileNotifications: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
    }
    minTlsVersion: '1.2'
    mqttV5Settings: {
      topicGroups: [
        {
          topicGroupId: 'myTopicGroup'
          topicTemplates: [
            'mytopics/telemetry/temperature/*'
            'mytopics/telemetry/humidity/*'
          ]
        }
      ]
    }
    networkRuleSets: {
      applyToBuiltInEventHubEndpoint: true
      defaultAction: 'Deny'
      ipRules: [
        {
          action: 'Allow'
          filterName: 'rule1'
          ipMask: '131.117.159.53'
        }
        {
          action: 'Allow'
          filterName: 'rule2'
          ipMask: '157.55.59.128/25'
        }
      ]
    }
    rootCertificate: {
      enableRootCertificateV2: true
    }
    routing: {
      endpoints: {
        eventHubs: [
        ]
        serviceBusQueues: [
        ]
        serviceBusTopics: [
        ]
        storageContainers: [
        ]
      }
      fallbackRoute: {
        name: '$fallback'
        condition: 'true'
        endpointNames: [
          'events'
        ]
        isEnabled: true
        source: 'DeviceMessages'
      }
      routes: [
      ]
    }
    storageEndpoints: {
      '$default': {
        connectionString: ''
        containerName: ''
        sasTtlAsIso8601: 'PT1H'
      }
    }
  }
  sku: {
    name: 'S1'
    capacity: 1
  }
  tags: {
  }
}
```

IotHubResource_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs@2026-10-01-preview' = {
  name: 'example'
  etag: 'AAAAAAFD6M4='
  identity: {
    type: 'SystemAssigned'
  }
  location: 'centraluseuap'
  properties: {
    cloudToDevice: {
      defaultTtlAsIso8601: 'PT1H'
      feedback: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
      maxDeliveryCount: 10
    }
    enableDataResidency: true
    enableFileUploadNotifications: false
    eventHubEndpoints: {
      events: {
        partitionCount: 2
        retentionTimeInDays: 1
      }
    }
    features: 'None'
    ipFilterRules: [
    ]
    ipVersion: 'ipv4ipv6'
    messagingEndpoints: {
      fileNotifications: {
        lockDurationAsIso8601: 'PT1M'
        maxDeliveryCount: 10
        ttlAsIso8601: 'PT1H'
      }
    }
    minTlsVersion: '1.2'
    networkRuleSets: {
      applyToBuiltInEventHubEndpoint: true
      defaultAction: 'Deny'
      ipRules: [
        {
          action: 'Allow'
          filterName: 'rule1'
          ipMask: '131.117.159.53'
        }
        {
          action: 'Allow'
          filterName: 'rule2'
          ipMask: '157.55.59.128/25'
        }
      ]
    }
    rootCertificate: {
      enableRootCertificateV2: true
    }
    routing: {
      endpoints: {
        eventHubs: [
        ]
        eventStreams: [
          {
            name: 'eventstreamendpoint1'
            authenticationType: 'identityBased'
            endpointUri: 'sb://eventstreamcustomsourceehns.azure.servicebus.net'
            entityPath: 'eventstreamcustomsourceeh'
            eventStreamId: '22222222-2222-2222-2222-222222222222'
            messagePayloadFormat: 'DOObservationV1'
            sourceId: '33333333-3333-3333-3333-333333333333'
            workspaceId: '11111111-1111-1111-1111-111111111111'
          }
        ]
        serviceBusQueues: [
        ]
        serviceBusTopics: [
        ]
        storageContainers: [
        ]
      }
      fallbackRoute: {
        name: '$fallback'
        condition: 'true'
        endpointNames: [
          'events'
        ]
        isEnabled: true
        source: 'DeviceMessages'
      }
      routes: [
      ]
    }
    storageEndpoints: {
      '$default': {
        connectionString: ''
        containerName: ''
        sasTtlAsIso8601: 'PT1H'
      }
    }
  }
  sku: {
    name: 'S1'
    capacity: 1
  }
  tags: {
  }
}
```

## microsoft.devices/iothubs/certificates

Certificates_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs/certificates@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    certificate: '############################################'
  }
}
```

CreateOrReplace_Certificates_With_CertificateAuthorityResourceId
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs/certificates@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    certificate: '############################################'
  }
}
```

## microsoft.devices/iothubs/eventhubendpoints/consumergroups

IotHubResource_CreateEventHubConsumerGroup
```bicep
resource exampleResource 'Microsoft.Devices/IotHubs/eventHubEndpoints/ConsumerGroups@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    name: 'test'
  }
}
```

## microsoft.devices/iothubs/privateendpointconnections

PrivateEndpointConnection_Update
```bicep
resource exampleResource 'Microsoft.Devices/iotHubs/privateEndpointConnections@2026-10-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
      description: 'Approved by johndoe@contoso.com'
      status: 'Approved'
    }
  }
}
```
