# Microsoft.CognitiveServices
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.cognitiveservices/accounts

Create a Foundry account with customer-owned AKS hosting
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts@2026-11-15-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.ManagedIdentity/userAssignedIdentities/account-control-plane': {
      }
    }
  }
  kind: 'AIServices'
  location: 'West US'
  properties: {
    agentHostingConfigurations: [
      {
        name: 'default'
        clusterResourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.ContainerService/managedClusters/cluster1'
        hostingManagementIdentityResourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.ManagedIdentity/userAssignedIdentities/account-control-plane'
        hostingType: 'ManagedCluster'
        storageAccountResourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/storage1'
        workloadIdentityResourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.ManagedIdentity/userAssignedIdentities/aks-workload'
      }
    ]
  }
  sku: {
    name: 'S0'
  }
}
```

Create Account
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts@2026-11-15-preview' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  kind: 'Emotion'
  location: 'West US'
  properties: {
    capabilitySettings: {
      blobStore: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount'
      documentStore: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDB/databaseAccounts/myCosmosAccount'
      vectorStore: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.Search/searchServices/mySearchService'
    }
    encryption: {
      keySource: 'Microsoft.KeyVault'
      keyVaultProperties: {
        keyName: 'KeyName'
        keyVaultUri: 'https://pltfrmscrts-use-pc-dev.vault.azure.net/'
        keyVersion: '891CF236-D241-4738-9462-D506AF493DFA'
      }
    }
    userOwnedStorage: [
      {
        resourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount'
      }
    ]
  }
  sku: {
    name: 'S0'
  }
}
```

Create Account Min
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts@2026-11-15-preview' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  kind: 'CognitiveServices'
  location: 'West US'
  properties: {
  }
  sku: {
    name: 'S0'
  }
}
```

Create an account with private CA trust
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts@2026-11-15-preview' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  kind: 'AIServices'
  location: 'eastus'
  properties: {
    allowProjectManagement: true
    customSubDomainName: 'myAccount'
    trustedCertificateSources: [
      {
        type: 'AzureKeyVault'
        certificateBundleReferences: [
          {
            secretName: 'corporate-ca-bundle'
            secretVersion: '11111111111111111111111111111111'
          }
          {
            secretName: 'partner-ca-bundle'
            secretVersion: '22222222222222222222222222222222'
          }
        ]
        resourceId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.KeyVault/vaults/myKeyVault'
      }
    ]
  }
  sku: {
    name: 'S0'
  }
}
```

## microsoft.cognitiveservices/accounts/adapterdeployments

CreateOrUpdateAdapterDeployment
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/adapterDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    sourceModelId: 'azureai://accounts/accountName/projects/projectName/models/modelName/versions/1'
    targetDeploymentName: 'managedComputeDeploymentName'
  }
}
```

## microsoft.cognitiveservices/accounts/arcdeployments

CreateOrUpdateArcDeployment
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/arcDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    extensionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.Kubernetes/connectedClusters/edge-cluster/providers/Microsoft.KubernetesConfiguration/extensions/inference-operator'
    model: {
      assetId: 'azureml://registries/azureml/models/Phi-3-mini-128k-instruct-generic-cpu/versions/3'
    }
    nodeSelector: {
      agentpool: 'cpu'
    }
    replicas: 2
    resources: {
      limits: {
        cpu: '8'
        memory: '16Gi'
      }
      requests: {
        cpu: '8'
        memory: '16Gi'
      }
    }
  }
  sku: {
    name: 'Arc'
  }
}
```

CreateOrUpdateArcDeploymentWithGpu
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/arcDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    extensionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.Kubernetes/connectedClusters/edge-cluster/providers/Microsoft.KubernetesConfiguration/extensions/inference-operator'
    model: {
      assetId: 'azureml://registries/azureml/models/Phi-3-mini-128k-instruct-cuda-gpu/versions/2'
    }
    nodeSelector: {
      agentpool: 'a100'
    }
    replicas: 2
    resources: {
      limits: {
        gpu: 5
      }
    }
  }
  sku: {
    name: 'Arc'
  }
}
```

CreateOrUpdateArcDeploymentWithVllm
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/arcDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    extensionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.Kubernetes/connectedClusters/edge-cluster/providers/Microsoft.KubernetesConfiguration/extensions/inference-operator'
    model: {
      assetId: 'azureml://registries/azure-foundrylocalonazurelocal/models/openai-gpt-oss-20b/versions/1'
    }
    nodeSelector: {
      agentpool: 'a100'
    }
    replicas: 2
    resources: {
      limits: {
        gpu: 5
      }
    }
  }
  sku: {
    name: 'Arc'
  }
}
```

## microsoft.cognitiveservices/accounts/attachedaksclusters

CreateOrUpdateAttachedAksCluster
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/attachedAksClusters@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    capabilities: [
      'foundryNative'
      'kuberay'
    ]
    clusterResourceId: '/subscriptions/11111111-2222-3333-4444-555555555555/resourceGroups/rgaks/providers/Microsoft.ContainerService/managedClusters/myAks'
    extensionProfile: {
      configuration: {
        rayVersion: '2.52.0'
      }
      releaseTrain: 'stable'
      version: '1.0.0'
    }
  }
}
```

## microsoft.cognitiveservices/accounts/capabilityhosts

CreateOrUpdate Account CapabilityHost.
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/capabilityHosts@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    customerSubnet: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroups/providers/Microsoft.Network/virtualNetworks/myVnet/subnets/mySubnet'
    enablePublicHostingEnvironment: true
  }
}
```

## microsoft.cognitiveservices/accounts/commitmentplans

PutCommitmentPlan
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/commitmentPlans@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    autoRenew: true
    current: {
      tier: 'T1'
    }
    hostingModel: 'Web'
    planType: 'Speech2Text'
  }
}
```

## microsoft.cognitiveservices/accounts/computes

PutCompute
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/computes@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'None'
  }
  properties: {
    computeType: 'Cluster'
    location: 'eastus'
    pools: [
      {
        name: 'default'
        instanceType: 'Standard_DS3_v2'
        nodeCount: 2
        vmPriority: 'Regular'
      }
    ]
  }
}
```

PutContainerInstanceCompute
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/computes@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/rgcognitiveservices/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myIdentity': {
      }
    }
  }
  properties: {
    computeType: 'ContainerInstance'
    idleTimeBeforeShutdown: 'PT30M'
    imageLink: 'mcr.microsoft.com/azureml/curated/pytorch-gpu:latest'
    location: 'eastus'
    sshSettings: {
      adminEnabled: true
      sshPublicKey: 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQ...'
    }
    targetClusterId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/rgcognitiveservices/providers/Microsoft.CognitiveServices/accounts/myAccount/computes/myCluster'
  }
}
```

## microsoft.cognitiveservices/accounts/connections

CreateAccountConnection
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/connections@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authType: 'None'
    category: 'ContainerRegistry'
    expiryTime: '2024-03-15T14:30:00Z'
    target: '[target url]'
  }
}
```

## microsoft.cognitiveservices/accounts/costcontrols

Create or replace an account cost budget
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/costControls@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    amount: 1000
    category: 'Cost'
    filter: {
      and: [
        {
          additionalInfo: {
            name: 'project'
            operator: 'In'
            values: [
              'production'
            ]
          }
        }
        {
          additionalInfo: {
            name: 'agent'
            operator: 'In'
            values: [
              'customer-support'
              'order-assistant'
            ]
          }
        }
        {
          additionalInfo: {
            name: 'deployment'
            operator: 'In'
            values: [
              'customer-support-model'
            ]
          }
        }
      ]
    }
    grouping: [
      {
        name: 'agent'
        type: 'AdditionalInfoKey'
      }
    ]
    notifications: {
      usageAlert: {
        enabled: true
        eventGridConnectionId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/foundry-resource-group/providers/Microsoft.CognitiveServices/accounts/foundry-account/connections/budget-alerts'
        operator: 'GreaterThanOrEqualTo'
        threshold: 80
        thresholdType: 'Percentage'
      }
    }
    providerProperties: {
      actions: {
        stopRequests: {
          type: 'Block'
          operator: 'GreaterThanOrEqualTo'
          threshold: 100
          thresholdType: 'Percentage'
        }
      }
    }
    timeGrain: 'Monthly'
    timePeriod: {
      endDate: '2027-11-15T00:00:00Z'
      startDate: '2026-11-15T00:00:00Z'
    }
  }
}
```

## microsoft.cognitiveservices/accounts/defenderforaisettings

PutDefenderForAISetting
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/defenderForAISettings@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    state: 'Enabled'
  }
}
```

## microsoft.cognitiveservices/accounts/deployments

PutDeployment
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/deployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    deploymentState: 'Running'
    model: {
      name: 'ada'
      format: 'OpenAI'
      version: '1'
    }
    serviceTier: 'Priority'
  }
  sku: {
    name: 'Standard'
    capacity: 1
  }
}
```

PutDeploymentWithSpeculativeDecoding
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/deployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    deploymentState: 'Running'
    model: {
      name: 'FW-Qwen3-14B'
      format: 'Fireworks'
      version: '1'
    }
    serviceTier: 'Default'
    speculativeDecoding: {
      draftModel: {
        name: 'testDraftModel'
        format: 'FireworksCustom'
        source: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/resourceGroupName/providers/Microsoft.CognitiveServices/accounts/accountName/projects/projectName'
        version: '1'
      }
      draftTokenCount: 4
    }
  }
  sku: {
    name: 'GlobalProvisionedManaged'
    capacity: 80
  }
}
```

## microsoft.cognitiveservices/accounts/encryptionscopes

PutEncryptionScope
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/encryptionScopes@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    keySource: 'Microsoft.KeyVault'
    keyVaultProperties: {
      identityClientId: '00000000-0000-0000-0000-000000000000'
      keyName: 'DevKeyWestUS2'
      keyVaultUri: 'https://devkvwestus2.vault.azure.net/'
      keyVersion: '9f85549d7bf14ff4bf178c10d3bdca95'
    }
    state: 'Enabled'
  }
}
```

## microsoft.cognitiveservices/accounts/managedcomputedeployments

CreateOrUpdateManagedComputeDeployment
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/managedComputeDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    acceleratorType: 'H100_80GB'
    deploymentTemplate: 'azureml://registries/azureml-openai-oss/deploymenttemplates/gpt-oss-120b-short-context/versions/1'
    gatedModelAccess: {
      connectionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.CognitiveServices/accounts/accountName/projects/my-project/connections/my-hf-connection'
    }
    model: 'azureml://registries/azureml-openai-oss/models/gpt-oss-120b/versions/4'
    versionUpgradeOption: 'OnceNewDefaultVersionAvailable'
  }
  sku: {
    name: 'GlobalManagedCompute'
    capacity: 1
  }
}
```

CreateOrUpdateVmManagedComputeDeployment
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/managedComputeDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    computeId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.CognitiveServices/accounts/accountName/computes/my-h100-pool'
    deploymentTemplate: 'projects/my-project/deploymentTemplates/gpt-oss-120b-vllm-tuned/versions/2'
    gatedModelAccess: {
      connectionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.CognitiveServices/accounts/accountName/projects/my-project/connections/my-hf-connection'
    }
    model: 'azureml://registries/azureml-openai-oss/models/gpt-oss-120b/versions/4'
    priority: 'High'
  }
  sku: {
    name: 'VmManagedCompute'
    capacity: 2
  }
}
```

## microsoft.cognitiveservices/accounts/managednetworks

Put ManagedNetworkSettings
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/managedNetworks@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    managedNetwork: {
      firewallSku: 'Standard'
      isolationMode: 'AllowOnlyApprovedOutbound'
      outboundRules: {
        rule_name_1: {
          type: 'FQDN'
          category: 'UserDefined'
          destination: 'destination_endpoint'
        }
      }
    }
  }
}
```

## microsoft.cognitiveservices/accounts/managednetworks/outboundrules

CreateOrUpdate OutboundRule
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/managedNetworks/outboundRules@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    type: 'FQDN'
    category: 'UserDefined'
    destination: 'destination_endpoint'
    status: 'Active'
  }
}
```

## microsoft.cognitiveservices/accounts/privateendpointconnections

PutPrivateEndpointConnection
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/privateEndpointConnections@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
      description: 'Auto-Approved'
      status: 'Approved'
    }
  }
}
```

## microsoft.cognitiveservices/accounts/projects

Create a Foundry project with tool controls
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  location: 'westus'
  properties: {
    displayName: 'My project'
    toolControls: {
      allowedTools: [
        {
          type: 'code_interpreter'
        }
        {
          type: 'mcp'
          serverUrl: 'https://*.contoso.com/mcp'
        }
      ]
      defaultAction: 'Deny'
    }
  }
}
```

Create Project
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'West US'
  properties: {
    description: 'Description of this project'
    capabilitySettings: {
      documentStore: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDB/databaseAccounts/myProjectCosmosAccount'
      vectorStore: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/myResourceGroup/providers/Microsoft.Search/searchServices/myProjectSearchService'
    }
    displayName: 'p1'
  }
}
```

Create Project Min
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'West US'
  properties: {
  }
}
```

## microsoft.cognitiveservices/accounts/projects/applications

Create or Update Account Agent Application.
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/applications@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Sample agent application for customer support'
    displayName: 'Customer Support Agent'
    tags: {
      environment: 'production'
      team: 'ai-platform'
    }
  }
}
```

## microsoft.cognitiveservices/accounts/projects/applications/agentdeployments

Create or Update Agent Deployment.
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/applications/agentDeployments@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    agents: [
      {
        agentId: 'agent-123'
        agentName: 'support-agent'
        agentVersion: '1.0.0'
      }
    ]
    deploymentType: 'Managed'
    displayName: 'Production Deployment'
    protocols: [
      {
        version: '1.0'
        protocol: 'Agent'
      }
    ]
    state: 'Starting'
  }
}
```

## microsoft.cognitiveservices/accounts/projects/capabilityhosts

CreateOrUpdate Project CapabilityHost.
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/capabilityHosts@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    aiServicesConnections: [
      'aoai_connection'
    ]
    storageConnections: [
      'blob_connection'
    ]
    threadStorageConnections: [
      'aca_connection'
    ]
    vectorStoreConnections: [
      'acs_connection'
    ]
  }
}
```

## microsoft.cognitiveservices/accounts/projects/connections

CreateProjectConnection
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/connections@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    authType: 'None'
    category: 'ContainerRegistry'
    expiryTime: '2024-03-15T14:30:00Z'
    target: '[target url]'
  }
}
```

## microsoft.cognitiveservices/accounts/projects/costcontrols

Create or replace a project token budget
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/costControls@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    amount: 1000000
    category: 'Tokens'
    filter: {
      additionalInfo: {
        name: 'tokenType'
        operator: 'In'
        values: [
          'input'
          'output'
        ]
      }
    }
    notifications: {
      usageAlert: {
        enabled: true
        eventGridConnectionId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/foundry-resource-group/providers/Microsoft.CognitiveServices/accounts/foundry-account/connections/budget-alerts'
        operator: 'GreaterThanOrEqualTo'
        threshold: 80
        thresholdType: 'Percentage'
      }
    }
    providerProperties: {
      actions: {
        stopRequests: {
          type: 'Block'
          operator: 'GreaterThanOrEqualTo'
          threshold: 100
          thresholdType: 'Percentage'
        }
      }
    }
    timeGrain: 'Daily'
    timePeriod: {
      endDate: '2027-11-15T00:00:00Z'
      startDate: '2026-11-15T00:00:00Z'
    }
  }
}
```

## microsoft.cognitiveservices/accounts/projects/workbenches

PutWorkbench
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/workbenches@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/rgcognitiveservices/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myIdentity': {
      }
    }
  }
  properties: {
    datasetId: 'dataset-12345'
    gpuCount: 1
    idleTimeBeforeShutdown: 'PT30M'
    imageLink: 'mcr.microsoft.com/azureml/curated/pytorch-gpu:latest'
    instanceType: 'Singularity.ND12_H100_v5-n1'
    sshSettings: {
      adminEnabled: true
      sshPublicKey: 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQ...'
    }
    targetClusterId: '/subscriptions/11111111-1111-1111-1111-111111111111/resourceGroups/vc-rg/providers/Microsoft.MachineLearningServices/virtualClusters/test-vc'
  }
}
```

PutWorkbenchPending
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/projects/workbenches@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    imageLink: 'mcr.microsoft.com/azureml/curated/pytorch-gpu:latest'
    targetClusterId: '/subscriptions/00000000-1111-2222-3333-444444444444/resourceGroups/rgcognitiveservices/providers/Microsoft.CognitiveServices/accounts/myAccount/computes/myCluster'
  }
}
```

## microsoft.cognitiveservices/accounts/raibindings

Bind an Azure OpenAI deployment to an ACS policy
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiBindings@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    boundResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource-group/providers/Microsoft.CognitiveServices/accounts/aoai-account/deployments/chat-prod'
    targetPolicyName: 'agent-guard'
  }
}
```

Update a RAI binding target conditionally across subscriptions
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiBindings@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    boundResourceId: '/subscriptions/11111111-1111-1111-1111-111111111111/resourceGroups/target-resource-group/providers/Microsoft.CognitiveServices/accounts/aoai-account/deployments/chat-canary'
    targetPolicyName: 'agent-guard-v2'
  }
}
```

## microsoft.cognitiveservices/accounts/raiblocklists

PutRaiBlocklist
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiBlocklists@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Basic blocklist description'
  }
}
```

## microsoft.cognitiveservices/accounts/raiblocklists/raiblocklistitems

PutRaiBlocklistItem
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiBlocklists/raiBlocklistItems@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    isRegex: false
    pattern: 'Pattern To Block'
  }
}
```

## microsoft.cognitiveservices/accounts/raipolicies

Create an ACS policy with optional annotations and an egress companion
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    format: 'ACS'
    acs: {
      agent_control_specification_version: '0.4.0-alpha.1'
      annotators: {
        risk: {
          type: 'llm'
          api_version: '2024-10-21'
          deployment: 'judge'
          endpoint: 'https://synthetic-judge.openai.azure.com/'
          provider: 'azure_openai'
          result_schema: 'acs.judge.observation/v2'
          system_prompt: 'Classify the complete subject for harmful intent. Score from 0 to 10: 0 is benign, 5 is ambiguous or potentially harmful, and 10 is clear harmful intent. Use label clear for scores below 4, review for scores from 4 to below 7, and high_risk for scores of 7 or higher. Report observations only; Rego decides the action.'
          timeout_ms: 10000
        }
      }
      intervention_points: {
        agent_shutdown: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.summary'
          policy_target_kind: 'agent_summary'
        }
        agent_startup: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.agent_init'
          policy_target_kind: 'agent_init'
        }
        input: {
          annotations: {
            risk: {
              from: '$target.content'
            }
          }
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.input'
          policy_target_kind: 'user_input'
        }
        output: {
          annotations: {
            risk: {
              from: '$target.content'
            }
          }
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.output'
          policy_target_kind: 'assistant_output'
        }
        post_model_call: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.response'
          policy_target_kind: 'model_response'
        }
        post_tool_call: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.tool_result.value'
          policy_target_kind: 'tool_result'
        }
        pre_model_call: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.messages'
          policy_target_kind: 'messages'
        }
        pre_tool_call: {
          policy: {
            id: 'agent-guard'
          }
          policy_target: '$snap.tool_call.args'
          policy_target_kind: 'tool_args'
        }
      }
      metadata: {
        description: 'Illustrative annotation authoring; supported annotators and configuration depend on the evaluation host.'
      }
      policies: {
        'agent-guard': {
          type: 'rego'
          query: 'data.agent_guard.verdict'
        }
      }
    }
    acsRegos: [
      {
        regoName: 'agent-guard'
      }
    ]
    egressPolicy: {
      defaultAction: 'Deny'
      mode: 'Audit'
      rules: [
        {
          name: 'allow-docs'
          action: {
            actionType: 'Allow'
          }
          match: {
            path: '/azure/*'
            host: 'learn.microsoft.com'
          }
          ruleType: 'Fqdn'
        }
        {
          name: 'label-api'
          action: {
            actionType: 'Transform'
            headers: [
              {
                name: 'X-Workload-Class'
                operation: 'Set'
                value: 'public-demo'
              }
            ]
          }
          match: {
            path: '/v1/*'
            host: 'api.contoso.com'
          }
          ruleType: 'Fqdn'
        }
      ]
    }
    mode: 'Asynchronous_filter'
  }
}
```

Create an ACS policy with optional policy dependencies
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    format: 'ACS'
    acs: {
      agent_control_specification_version: '0.4.0-alpha.1'
      annotators: {
      }
      intervention_points: {
        input: {
          policy: {
            aacs_moderation: {
              harm_configs: [
                {
                  category: 'PromptInjection'
                }
              ]
              subject_format: 'text'
            }
            id: 'input-guard'
          }
          policy_target: '$snap.input'
          policy_target_kind: 'user_input'
        }
        post_tool_call: {
          policy: {
            id: 'tool-guard'
          }
          policy_target: '$snap.tool_result.value'
          policy_target_kind: 'tool_result'
          tool_name_from: '$snap.tool_call.name'
        }
        pre_tool_call: {
          policy: {
            id: 'tool-guard'
          }
          policy_target: '$snap.tool_call.args'
          policy_target_kind: 'tool_args'
          tool_name_from: '$snap.tool_call.name'
        }
      }
      metadata: {
        name: 'agent-guard'
      }
      policies: {
        'input-guard': {
          type: 'rego'
          query: 'data.input_guard.verdict'
        }
        'tool-guard': {
          type: 'rego'
          query: 'data.tool_guard.verdict'
        }
      }
      tools: {
        web_search: {
          type: 'retrieval'
          description: 'Search approved public documentation'
          allowed_domains: [
            'learn.microsoft.com'
          ]
          clearance: 'public'
          id: 'web_search'
          security_labels: [
            'network_egress'
            'untrusted_content'
          ]
        }
        wire_transfer: {
          type: 'financial_action'
          clearance: 'confidential'
          id: 'wire_transfer'
          security_labels: [
            'financial_write'
          ]
        }
      }
    }
    acsRegos: [
      {
        regoName: 'input-guard'
      }
      {
        regoName: 'tool-guard'
      }
    ]
    customBlocklists: [
      {
        blocking: true
        blocklistName: 'blocked-terms'
        source: 'Prompt'
      }
    ]
    customExternalSafetyProviders: [
      {
        blocking: true
        externalSafetyProviderName: 'contoso-safety-provider'
        managedIdentityResourceId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/safety-provider-identity'
        source: 'Prompt'
      }
    ]
    mode: 'Asynchronous_filter'
  }
}
```

Create an ACS policy without a tool catalog
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    format: 'ACS'
    acs: {
      agent_control_specification_version: '0.4.0-alpha.1'
      intervention_points: {
        input: {
          policy: {
            id: 'input-guard'
          }
          policy_target: '$snap.input'
          policy_target_kind: 'user_input'
        }
      }
      policies: {
        'input-guard': {
          type: 'rego'
          query: 'data.input_guard.verdict'
        }
      }
    }
    acsRegos: [
      {
        regoName: 'input-guard'
      }
    ]
  }
}
```

PutRaiPolicy
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    basePolicyName: 'Microsoft.Default'
    contentFilters: [
      {
        name: 'Hate'
        blocking: false
        enabled: false
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Hate'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Sexual'
        blocking: true
        enabled: true
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Sexual'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Selfharm'
        blocking: true
        enabled: true
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Selfharm'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Violence'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Prompt'
      }
      {
        name: 'Violence'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Jailbreak'
        blocking: true
        enabled: true
        source: 'Prompt'
      }
      {
        name: 'Protected Material Text'
        blocking: true
        enabled: true
        source: 'Completion'
      }
      {
        name: 'Protected Material Code'
        blocking: true
        enabled: true
        source: 'Completion'
      }
      {
        name: 'Profanity'
        blocking: true
        enabled: true
        source: 'Prompt'
      }
    ]
    mode: 'Asynchronous_filter'
  }
}
```

PutRaiPolicyWithEgress
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    basePolicyName: 'Microsoft.Default'
    contentFilters: [
    ]
    egressPolicy: {
      description: 'Corporate baseline egress policy for sandboxed agents'
      defaultAction: 'Deny'
      mode: 'Enforced'
      rules: [
        {
          name: 'allow-openai'
          description: 'Allow traffic to OpenAI API'
          action: {
            actionType: 'Allow'
          }
          match: {
            host: '*.openai.com'
          }
          ruleType: 'Fqdn'
        }
        {
          name: 'inject-auth-for-internal'
          description: 'Inject managed identity token for internal services'
          action: {
            actionType: 'Transform'
            headers: [
              {
                name: 'Authorization'
                operation: 'Set'
                valueRef: {
                  managedIdentityRef: {
                    format: 'Bearer {value}'
                    resource: 'https://internal.contoso.com/.default'
                  }
                }
              }
            ]
          }
          match: {
            host: '*.internal.contoso.com'
          }
          ruleType: 'Fqdn'
        }
        {
          name: 'rewrite-legacy-api'
          description: 'Rewrite legacy API hostname to new internal endpoint'
          action: {
            actionType: 'Rewrite'
            headers: [
              {
                name: 'X-Forwarded-Host'
                operation: 'Set'
                value: 'legacy-api.contoso.com'
              }
            ]
            rewrite: {
              path: '/v2/'
              host: 'api-v2.internal.contoso.com'
              scheme: 'https'
            }
          }
          match: {
            path: '/v1/*'
            host: 'legacy-api.contoso.com'
          }
          ruleType: 'Fqdn'
        }
      ]
    }
  }
}
```

Replace an ACS policy conditionally
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiPolicies@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    format: 'ACS'
    acs: {
      agent_control_specification_version: '0.4.0-alpha.1'
      intervention_points: {
        input: {
          policy: {
            aacs_moderation: {
              harm_configs: [
                {
                  category: 'Hate'
                  harm_config_id: 'Hate_Text_MultiSev'
                }
                {
                  category: 'PromptInjection'
                }
              ]
              subject_format: 'text'
            }
            id: 'input-guard'
          }
          policy_target: '$snap.input'
          policy_target_kind: 'user_input'
        }
        post_tool_call: {
          policy: {
            id: 'tool-guard'
          }
          policy_target: '$snap.tool_result.value'
          policy_target_kind: 'tool_result'
          tool_name_from: '$snap.tool_call.name'
        }
        pre_tool_call: {
          policy: {
            id: 'tool-guard'
          }
          policy_target: '$snap.tool_call.args'
          policy_target_kind: 'tool_args'
          tool_name_from: '$snap.tool_call.name'
        }
      }
      policies: {
        'input-guard': {
          type: 'rego'
          query: 'data.input_guard.verdict'
        }
        'tool-guard': {
          type: 'rego'
          query: 'data.tool_guard.verdict'
        }
      }
      tools: {
        web_search: {
          type: 'retrieval'
          description: 'Search approved public documentation and approved partner sites'
          allowed_domains: [
            'learn.microsoft.com'
            'support.microsoft.com'
          ]
          clearance: 'public'
          id: 'web_search'
          security_labels: [
            'network_egress'
            'untrusted_content'
          ]
        }
        wire_transfer: {
          type: 'financial_action'
          clearance: 'confidential'
          id: 'wire_transfer'
          security_labels: [
            'financial_write'
          ]
        }
      }
    }
    acsRegos: [
      {
        regoName: 'input-guard'
      }
      {
        regoName: 'tool-guard'
      }
    ]
    customBlocklists: [
    ]
    customExternalSafetyProviders: [
    ]
  }
}
```

## microsoft.cognitiveservices/accounts/rairegos

Create a reusable Rego artifact
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiRegos@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    encoding: 'None'
    rego: 'package input_guard\n\nimport rego.v1\n\ndefault verdict := {"decision": "allow"}\n\nverdict := {"decision": "deny", "reason": "prompt_injection_detected"} if {\n  input.snapshot.moderation.harm.PromptInjection.detected\n}'
  }
  tags: {
    environment: 'production'
  }
}
```

Replace a reusable Rego artifact conditionally
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiRegos@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    encoding: 'None'
    rego: 'package input_guard\n\nimport rego.v1\n\ndefault verdict := {"decision": "allow"}\n\nblocking_signal if {\n  input.snapshot.moderation.harm.PromptInjection.detected\n}\n\nblocking_signal if {\n  input.snapshot.moderation.harm.Hate.severity >= 4\n}\n\nverdict := {"decision": "deny", "reason": "unsafe_input"} if {\n  blocking_signal\n}'
  }
}
```

## microsoft.cognitiveservices/accounts/raitoollabels

PutRaiToolLabel
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raiToolLabels@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    accountScope: {
      labelValues: {
        confidentiality: 'low'
      }
    }
    projectScopes: [
      {
        labelValues: {
          confidentiality: 'low'
        }
        project: 'test-project'
      }
      {
        labelValues: {
          confidentiality: 'low'
        }
        project: 'sample-project'
      }
    ]
    toolConnectionName: 'Web_Search'
  }
}
```

## microsoft.cognitiveservices/accounts/raitopics

PutRaiTopic
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/raitopics@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'This is a sample topic.'
    sampleBlobUrl: 'https://example.blob.core.windows.net/sampleblob'
    topicName: 'raiTopicName'
  }
}
```

## microsoft.cognitiveservices/accounts/testraiexternalsafetyprovider

TestRaiExternalSafetyProvider
```bicep
resource exampleResource 'Microsoft.CognitiveServices/accounts/testRaiExternalSafetyProvider@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    keyVaultUri: 'https://contoso-vault.vault.azure.net/'
    managedIdentity: 'f3b9c2e7-4aad-4b1f-9d9c-9e9b1e9b1f9b'
    mode: 'sync'
    providerId: '00000000-0000-0000-0000-000000000000'
    providerName: 'safetyProviderName'
    secretName: 'safety-provider-secret'
    url: 'https://example-safety-provider.contoso.com/webhook'
  }
}
```

## microsoft.cognitiveservices/commitmentplans

Create Commitment Plan
```bicep
resource exampleResource 'Microsoft.CognitiveServices/commitmentPlans@2026-11-15-preview' = {
  name: 'example'
  kind: 'SpeechServices'
  location: 'West US'
  properties: {
    autoRenew: true
    current: {
      tier: 'T1'
    }
    hostingModel: 'Web'
    planType: 'STT'
  }
  sku: {
    name: 'S0'
  }
}
```

## microsoft.cognitiveservices/commitmentplans/accountassociations

PutCommitmentPlan
```bicep
resource exampleResource 'Microsoft.CognitiveServices/commitmentPlans/accountAssociations@2026-11-15-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    accountId: '/subscriptions/subscriptionId/resourceGroups/resourceGroupName/providers/Microsoft.CognitiveServices/accounts/accountName'
  }
}
```

## microsoft.cognitiveservices/quotatiers

Update the quota tier resource for a subscription
```bicep
resource exampleResource 'Microsoft.CognitiveServices/quotaTiers@2026-11-15-preview' = {
  name: 'example'
  properties: {
    tierUpgradePolicy: 'NoAutoUpgrade'
  }
}
```

## microsoft.cognitiveservices/raiexternalsafetyproviders

PutRaiExternalSafetyProvider
```bicep
resource exampleResource 'Microsoft.CognitiveServices/raiExternalSafetyProviders@2026-11-15-preview' = {
  name: 'example'
  properties: {
    keyVaultUri: 'https://example.vault.azure.net'
    managedIdentity: '00000000-0000-0000-0000-000000000000'
    mode: 'sync'
    providerId: '00000000-0000-0000-0000-000000000000'
    providerName: 'safetyProviderName'
    secretName: 'mySecretName'
    url: 'https://example.webhook.endpoint'
  }
}
```

## microsoft.cognitiveservices/raipolicy

PutRaiPolicy
```bicep
resource exampleResource 'Microsoft.CognitiveServices/raiPolicy@2026-11-15-preview' = {
  name: 'example'
  properties: {
    basePolicyName: 'Microsoft.Default'
    contentFilters: [
      {
        name: 'Hate'
        blocking: false
        enabled: false
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Hate'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Sexual'
        blocking: true
        enabled: true
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Sexual'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Selfharm'
        blocking: true
        enabled: true
        severityThreshold: 'High'
        source: 'Prompt'
      }
      {
        name: 'Selfharm'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Violence'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Prompt'
      }
      {
        name: 'Violence'
        blocking: true
        enabled: true
        severityThreshold: 'Medium'
        source: 'Completion'
      }
      {
        name: 'Jailbreak'
        blocking: true
        enabled: true
        source: 'Prompt'
      }
      {
        name: 'Protected Material Text'
        blocking: true
        enabled: true
        source: 'Completion'
      }
      {
        name: 'Protected Material Code'
        blocking: true
        enabled: true
        source: 'Completion'
      }
      {
        name: 'Profanity'
        blocking: true
        enabled: true
        source: 'Prompt'
      }
    ]
    mode: 'Asynchronous_filter'
  }
}
```
