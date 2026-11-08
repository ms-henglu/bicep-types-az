# Microsoft.App
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.app/agents

Agents_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.App/agents@2026-07-01' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'East US'
  properties: {
    actionConfiguration: {
      accessLevel: 'High'
      identity: '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/actionIdentity'
      mode: 'Review'
    }
    agentIdentity: {
      initialSponsorGroupId: '99999999-aaaa-bbbb-cccc-dddddddddddd'
    }
    defaultModel: {
      name: 'gpt-5'
      provider: 'MicrosoftFoundry'
    }
    knowledgeGraphConfiguration: {
      identity: '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/testIdentity'
      managedResources: [
        '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.Storage/storageAccounts/teststorage'
      ]
    }
    logConfiguration: {
      applicationInsightsConfiguration: {
        appId: '87654321-4321-4321-4321-210987654321'
        connectionString: 'InstrumentationKey=87654321-4321-4321-4321-210987654321;IngestionEndpoint=https://eastus-0.in.applicationinsights.azure.com/'
      }
    }
  }
  tags: {
    environment: 'production'
    team: 'platform'
  }
}
```

Agents_CreateOrUpdate_FullNetworkConfiguration
```bicep
resource exampleResource 'Microsoft.App/agents@2026-07-01' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'eastus'
  properties: {
    sandboxConfiguration: {
      egress: {
        allowHttpMcpServerNetworkAccess: false
        allowedCodeRepositories: [
          'Github'
          'GithubEnterprise'
          'AzureDevOps'
          'GitLab'
        ]
        allowedHosts: [
          'api.contoso.com'
          '*.example.com'
        ]
        allowedRegistries: [
          'pypi'
          'npmjs'
          'nuget-org'
          'ubuntu'
        ]
        httpProxy: {
          httpUrl: 'http://proxy.contoso.internal:3128'
          httpsUrl: 'http://proxy.contoso.internal:3128'
          noProxy: [
            '.contoso.internal'
            '10.0.0.4'
          ]
        }
        mode: 'AzureVNet'
      }
      packages: [
        {
          name: 'numpy'
          packageManager: 'pip'
          version: '1.26.0'
        }
        {
          name: 'lodash'
          packageManager: 'npm'
        }
        {
          name: 'dotnet-ef'
          packageManager: 'nuget'
          version: '9.0.0'
        }
      ]
    }
    vnetConfiguration: {
      subnetResourceId: '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.Network/virtualNetworks/agentVnet/subnets/agentSubnet'
    }
  }
}
```

Agents_CreateOrUpdate_Vnet
```bicep
resource exampleResource 'Microsoft.App/agents@2026-07-01' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'eastus'
  properties: {
    sandboxConfiguration: {
      egress: {
        mode: 'AzureVNet'
      }
    }
    vnetConfiguration: {
      subnetResourceId: '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.Network/virtualNetworks/agentVnet/subnets/agentSubnet'
    }
  }
}
```

## microsoft.app/agents/connectors

AgentsConnectors_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.App/agents/connectors@2026-07-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    dataConnectorType: 'Kusto'
    endpoint: 'https://newcluster.eastus.kusto.windows.net'
    extendedProperties: {
      AuthType: 'Custom'
      CustomHeader: {
        DD_API_KEY: 'value 1'
        DD_APPLICATION_KEY: 'value 2'
      }
    }
    identity: '/subscriptions/8efdecc5-919e-44eb-b179-915dca89ebf9/resourceGroups/examplerg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/kustoIdentity'
  }
}
```
