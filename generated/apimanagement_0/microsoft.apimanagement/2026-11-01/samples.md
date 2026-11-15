# Microsoft.ApiManagement
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.apimanagement/aigateways

Create an AI Gateway
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways@2026-11-01' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'westus2'
  properties: {
    backend: {
      subnet: {
        id: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.Network/virtualNetworks/example-vnet/subnets/example-subnet'
      }
    }
    publicNetworkAccess: 'Enabled'
  }
  sku: {
    name: 'Standard'
  }
  tags: {
    environment: 'development'
  }
}
```

## microsoft.apimanagement/aigateways/apikeys

Create an AI Gateway API key
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/apiKeys@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    displayName: 'Application key'
  }
}
```

## microsoft.apimanagement/aigateways/privateendpointconnections

Approve or reject a private endpoint connection for an AI Gateway
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/privateEndpointConnections@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
      description: 'Approved by administrator.'
      status: 'Approved'
    }
  }
}
```

## microsoft.apimanagement/aigateways/workspaces/aliases

Create an AI Gateway alias with automatic model selection and failover
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/aliases@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Chat alias with automatic model selection and failover'
    aliasName: 'chat-router'
    autoModelSelection: {
      allowedRequestOverrides: [
        'model'
        'objective'
        'filterModelsForToolCompatibility'
      ]
      objective: 'Balanced'
    }
    backendModels: [
      {
        priority: 0
        resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.ApiManagement/aigateways/example-gateway/workspaces/default/modelProviders/foundry-provider/models/gpt-4o'
        selectorModelName: 'gpt-4o'
        weight: 1
      }
      {
        priority: 0
        resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.ApiManagement/aigateways/example-gateway/workspaces/default/modelProviders/foundry-provider/models/gpt-4o-mini'
        selectorModelName: 'gpt-4o-mini'
        weight: 1
      }
    ]
    failures: [
      {
        excludeFor: 'PT30S'
        retryAttempts: 1
        when: '@cel(response != null && response.status_code in [429, 500, 503])'
      }
    ]
    maxRetryAttempts: 2
    selectionOrder: [
      'autoModelSelection'
      'priority'
    ]
  }
}
```

Create or update an AI Gateway Alias
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/aliases@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Stable chat model alias'
    aliasName: 'chat'
    backendModels: [
      {
        priority: 0
        resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.ApiManagement/aigateways/example-gateway/workspaces/default/modelProviders/foundry-provider/models/gpt-4o'
        weight: 1
      }
    ]
    policies: [
      {
        type: 'costLimit'
        amount: 10
        counterKey: [
          'identity'
        ]
        id: 'daily-budget'
        period: 'day'
        scope: 'resource'
      }
    ]
    selectionOrder: [
      'priority'
    ]
  }
}
```

## microsoft.apimanagement/aigateways/workspaces/modelproviders

Create a custom model provider with API key authentication
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/modelProviders@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authentication: {
      headers: [
        {
          name: 'api-key'
          value: '{api-key}'
        }
      ]
    }
    custom: {
      endpoint: {
        url: 'https://api.contoso.com/v1'
      }
    }
    displayName: 'Custom provider'
    modelProviderType: 'Custom'
  }
}
```

Create a Foundry model provider
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/modelProviders@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authentication: {
      managedIdentity: {
        resource: 'https://cognitiveservices.azure.com'
      }
    }
    displayName: 'Foundry provider'
    foundry: {
      endpoint: {
        url: 'https://example-foundry.services.ai.azure.com'
      }
      resourceIds: [
        '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.CognitiveServices/accounts/example-account'
      ]
    }
    modelProviderType: 'Foundry'
  }
}
```

## microsoft.apimanagement/aigateways/workspaces/modelproviders/models

Create an AI Gateway model
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/modelProviders/models@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Primary chat model'
    deployment: {
      modelName: 'gpt-4o'
      modelVersion: '2024-11-20'
      resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.CognitiveServices/accounts/example-account/deployments/gpt-4o'
    }
    displayName: 'GPT-4o'
    policies: [
      {
        type: 'tokenLimit'
        count: 100000
        counterKey: [
          'identity'
        ]
        period: 'day'
      }
    ]
    supportedEndpoints: [
      'chatCompletions'
      'responses'
    ]
  }
}
```

## microsoft.apimanagement/aigateways/workspaces/telemetryexporters

Create an Application Insights telemetry exporter
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/telemetryExporters@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    applicationInsights: {
      connectionString: '{connection-string}'
      resourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/example-rg/providers/Microsoft.Insights/components/example-insights'
    }
    payloadCapture: false
    telemetryExporterType: 'ApplicationInsights'
  }
}
```

Create an OpenTelemetry exporter with header authentication
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/telemetryExporters@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authentication: {
      headers: [
        {
          name: 'Authorization'
          value: '******'
        }
      ]
    }
    openTelemetry: {
      tracesEndpoint: {
        url: 'https://collector.example.com/v1/traces'
      }
    }
    payloadCapture: false
    telemetryExporterType: 'OpenTelemetry'
  }
}
```

Create or update an AI Gateway TelemetryExporter
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/telemetryExporters@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authentication: {
      managedIdentity: {
        clientId: '11111111-1111-1111-1111-111111111111'
        resource: 'https://monitor.azure.com/'
      }
    }
    openTelemetry: {
      logsEndpoint: {
        url: 'https://collector.example.com/v1/logs'
      }
      metricsEndpoint: {
        url: 'https://collector.example.com/v1/metrics'
      }
      tracesEndpoint: {
        url: 'https://collector.example.com/v1/traces'
      }
    }
    payloadCapture: false
    telemetry: {
      attributes: [
        {
          signals: [
            'logs'
            'traces'
            'metrics'
          ]
          source: {
            kind: 'claims'
            value: 'oid'
          }
        }
      ]
    }
    telemetryExporterType: 'OpenTelemetry'
  }
}
```

## microsoft.apimanagement/aigateways/workspaces/toolservers

Create a connector tool server
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/toolServers@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    displayName: 'Connector tools'
    toolServerType: 'connector'
  }
}
```

Create an MCP tool server
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/toolServers@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    displayName: 'Weather tools'
    endpoints: [
      {
        authentication: {
          headers: [
            {
              name: 'x-api-key'
              value: 'fake-example-key'
            }
          ]
        }
        id: 'endpoint-1'
        kind: 'mcp'
        mcp: {
          endpoint: {
            url: 'https://example.invalid/mcp'
          }
          transport: 'streamableHttp'
        }
        mode: 'failClosed'
        namespace: 'weather'
      }
      {
        authentication: {
          oauth2: {
            authorizationEndpoint: {
              url: 'https://example.invalid/oauth/authorize'
            }
            authorizationParameters: [
              {
                name: 'prompt'
                value: 'consent'
              }
            ]
            clientId: 'example-client'
            grantType: 'authorizationCode'
            scopes: [
              'tools.read'
            ]
            tokenEndpoint: {
              url: 'https://example.invalid/oauth/token'
            }
            tokenParameters: [
              {
                name: 'audience'
                value: 'https://example.invalid/forecast'
              }
            ]
          }
        }
        id: 'endpoint-2'
        kind: 'mcp'
        mcp: {
          endpoint: {
            url: 'https://example.invalid/forecast/mcp'
          }
          transport: 'streamableHttp'
        }
        mode: 'failClosed'
        namespace: 'forecast'
      }
    ]
    toolServerType: 'mcp'
  }
}
```

Create an OpenAPI tool server with inline and URL document sources
```bicep
resource exampleResource 'Microsoft.ApiManagement/aigateways/workspaces/toolServers@2026-11-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    displayName: 'OpenAPI tools'
    endpoints: [
      {
        authentication: {
          headers: [
            {
              name: 'x-api-key'
              value: '{api-key}'
            }
          ]
        }
        id: 'inline-endpoint'
        kind: 'openApi'
        mode: 'failClosed'
        namespace: 'weather'
        openApi: {
          specSource: {
            type: 'inline'
            contentBase64: 'eyJvcGVuYXBpIjoiMy4wLjMiLCJpbmZvIjp7InRpdGxlIjoiRXhhbXBsZSB3ZWF0aGVyIHRvb2xzIiwidmVyc2lvbiI6IjEuMC4wIn0sInNlcnZlcnMiOlt7InVybCI6Imh0dHBzOi8vYXBpLmNvbnRvc28uY29tIn1dLCJwYXRocyI6eyIvd2VhdGhlciI6eyJnZXQiOnsib3BlcmF0aW9uSWQiOiJnZXRXZWF0aGVyIiwicmVzcG9uc2VzIjp7IjIwMCI6eyJkZXNjcmlwdGlvbiI6IlN1Y2Nlc3MifX19fX19'
          }
        }
      }
      {
        id: 'url-endpoint'
        kind: 'openApi'
        mode: 'failOpen'
        namespace: 'forecast'
        openApi: {
          specSource: {
            type: 'url'
            url: 'https://api.contoso.com/openapi.json'
          }
        }
      }
    ]
    toolServerType: 'openApi'
  }
}
```
