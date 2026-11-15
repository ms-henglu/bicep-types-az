# Anyscale.Platform
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## anyscale.platform/agreements

Sign an agreement via PUT
```bicep
resource exampleResource 'Anyscale.Platform/agreements@2026-09-01' = {
  name: 'example'
  properties: {
  }
}
```

## anyscale.platform/clouds

Clouds_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds@2026-09-01' = {
  name: 'example'
  location: 'eastus'
  properties: {
    acrResourceId: '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Microsoft.ContainerRegistry/registries/anyscaleacr'
  }
  tags: {
    environment: 'production'
    team: 'ml-platform'
  }
}
```

## anyscale.platform/clouds/cloudresources

CloudResources_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/cloudResources@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  location: 'eastus'
  properties: {
    anyscaleOperatorIamIdentity: 'arn:aws:iam::123456789012:role/anyscale-operator'
    cloudStorageBucketEndpoint: 'https://anyscale-storage.s3.us-west-2.amazonaws.com'
    cloudStorageBucketName: 's3://anyscale-storage'
    cloudStorageBucketRegion: 'us-west-2'
    computeStack: 'K8S'
    provider: 'AWS'
    region: 'us-west-2'
  }
  tags: {
    environment: 'production'
    team: 'ml-platform'
  }
}
```

## anyscale.platform/clouds/computeconfigs

ComputeConfigs_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/computeConfigs@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    spec: {
      options: [
        {
          advancedInstanceConfig: '{}'
          cloudResourceNames: [
            '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/cloudResources/eastus-cloud-resource'
          ]
          flags: {
          }
          headNode: {
            name: 'head-node'
            advancedInstanceConfig: '{}'
            flags: {
            }
            instanceType: 'Standard_D8s_v5'
            labels: {
              'ray.io/node-type': 'head'
            }
            requiredLabels: {
              'node-pool': 'default'
            }
            requiredResources: {
              accelerator: ''
              cpu: 8
              cpuArchitecture: 'x86_64'
              gpu: 0
              memory: 32
              tpu: 0
            }
            resources: {
              cpu: 8
              customResources: {
              }
              gpu: 0
              memory: 32
              objectStoreMemory: 8
            }
          }
          workerNodes: [
            {
              name: 'gpu-worker'
              advancedInstanceConfig: '{}'
              flags: {
              }
              instanceType: 'Standard_NC24ads_A100_v4'
              labels: {
                'ray.io/node-type': 'worker'
              }
              marketType: 'ON_DEMAND'
              maxNodes: 10
              minNodes: 1
              requiredLabels: {
                'node-pool': 'gpu-pool'
              }
              requiredResources: {
                accelerator: 'A100'
                cpu: 24
                cpuArchitecture: 'x86_64'
                gpu: 1
                memory: 220
                tpu: 0
              }
              resources: {
                cpu: 24
                customResources: {
                }
                gpu: 1
                memory: 220
                objectStoreMemory: 50
              }
            }
          ]
          zones: [
            'eastus-1'
          ]
        }
      ]
    }
  }
}
```

## anyscale.platform/clouds/containerimages

ContainerImages_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/containerImages@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    containerImageUri: 'myacr.azurecr.io/anyscale/my-ray-image:latest'
  }
}
```

## anyscale.platform/clouds/projects

Projects_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/projects@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
  }
}
```

## anyscale.platform/clouds/projects/jobs

Jobs_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/projects/jobs@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    config: {
      computeConfig: {
        computeConfigName: '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/computeConfigs/my-compute-config'
        spec: {
          options: [
            {
              advancedInstanceConfig: '{}'
              cloudResourceNames: [
                '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/cloudResources/eastus-cloud-resource'
              ]
              flags: {
              }
              headNode: {
                name: 'head-node'
                advancedInstanceConfig: '{}'
                flags: {
                }
                instanceType: 'Standard_D8s_v5'
                labels: {
                  'ray.io/node-type': 'head'
                }
                requiredLabels: {
                  'node-pool': 'default'
                }
                requiredResources: {
                  accelerator: ''
                  cpu: 8
                  cpuArchitecture: 'x86_64'
                  gpu: 0
                  memory: 32
                  tpu: 0
                }
                resources: {
                  cpu: 8
                  customResources: {
                  }
                  gpu: 0
                  memory: 32
                  objectStoreMemory: 8
                }
              }
              workerNodes: [
                {
                  name: 'gpu-worker'
                  advancedInstanceConfig: '{}'
                  flags: {
                  }
                  instanceType: 'Standard_NC24ads_A100_v4'
                  labels: {
                    'ray.io/node-type': 'worker'
                  }
                  marketType: 'ON_DEMAND'
                  maxNodes: 10
                  minNodes: 1
                  requiredLabels: {
                    'node-pool': 'gpu-pool'
                  }
                  requiredResources: {
                    accelerator: 'A100'
                    cpu: 24
                    cpuArchitecture: 'x86_64'
                    gpu: 1
                    memory: 220
                    tpu: 0
                  }
                  resources: {
                    cpu: 24
                    customResources: {
                    }
                    gpu: 1
                    memory: 220
                    objectStoreMemory: 50
                  }
                }
              ]
              zones: [
                'eastus-1'
              ]
            }
          ]
        }
      }
      entrypoint: 'python train.py --epochs 10 --batch-size 32'
      envVars: {
        WANDB_PROJECT: 'anyscale-demo'
      }
      imageUri: 'anyscale/ray:2.44.0-py312-cu124'
      maxRetries: 3
      pipRequirements: [
        'torch==2.1.0'
        'transformers==4.36.0'
      ]
      pyModules: [
        'https://myaccount.blob.core.windows.net/my-container/my_module-0.1.0-py3-none-any.whl'
      ]
      timeout: 1380
      workingDir: 'https://myaccount.blob.core.windows.net/my-container/my-project'
    }
  }
}
```

## anyscale.platform/clouds/projects/services

Services_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/projects/services@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    deploymentConfig: {
      description: 'Production model serving endpoint'
      applications: [
        {
          name: 'my-serve-app'
          importPath: 'serve_app:app'
        }
      ]
      autoCompleteRollout: true
      canaryPercent: 0
      computeConfig: {
        computeConfigName: '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/computeConfigs/my-compute-config'
        spec: {
          options: [
            {
              advancedInstanceConfig: '{}'
              cloudResourceNames: [
                '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/cloudResources/eastus-cloud-resource'
              ]
              flags: {
              }
              headNode: {
                name: 'head-node'
                advancedInstanceConfig: '{}'
                flags: {
                }
                instanceType: 'Standard_D8s_v5'
                labels: {
                  'ray.io/node-type': 'head'
                }
                requiredLabels: {
                  'node-pool': 'default'
                }
                requiredResources: {
                  accelerator: ''
                  cpu: 8
                  cpuArchitecture: 'x86_64'
                  gpu: 0
                  memory: 32
                  tpu: 0
                }
                resources: {
                  cpu: 8
                  customResources: {
                  }
                  gpu: 0
                  memory: 32
                  objectStoreMemory: 8
                }
              }
              workerNodes: [
                {
                  name: 'gpu-worker'
                  advancedInstanceConfig: '{}'
                  flags: {
                  }
                  instanceType: 'Standard_NC24ads_A100_v4'
                  labels: {
                    'ray.io/node-type': 'worker'
                  }
                  marketType: 'ON_DEMAND'
                  maxNodes: 10
                  minNodes: 1
                  requiredLabels: {
                    'node-pool': 'gpu-pool'
                  }
                  requiredResources: {
                    accelerator: 'A100'
                    cpu: 24
                    cpuArchitecture: 'x86_64'
                    gpu: 1
                    memory: 220
                    tpu: 0
                  }
                  resources: {
                    cpu: 24
                    customResources: {
                    }
                    gpu: 1
                    memory: 220
                    objectStoreMemory: 50
                  }
                }
              ]
              zones: [
                'eastus-1'
              ]
            }
          ]
        }
      }
      connectionIds: [
        'connection-01'
      ]
      envVars: {
        MODEL_NAME: 'my-model'
      }
      grpcConfig: {
      }
      httpConfig: {
      }
      imageUri: 'anyscale/ray:2.44.0-py312-cu124'
      maxSurgePercent: 25
      maxUptimeTimeoutSec: 0
      rayGcsExternalStorageConfig: {
        address: 'redis://my-redis-host:6379'
      }
      rolloutStrategy: 'Rollout'
      tracingConfig: {
        enabled: true
        samplingRatio: 1
      }
      trafficPercent: 100
      version: 'v1'
    }
  }
}
```

## anyscale.platform/clouds/projects/workspaces

Workspaces_CreateOrUpdate
```bicep
resource exampleResource 'Anyscale.Platform/clouds/projects/workspaces@2026-09-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    computeConfig: {
      computeConfigName: '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/computeConfigs/my-compute-config'
      spec: {
        options: [
          {
            advancedInstanceConfig: '{}'
            cloudResourceNames: [
              '/subscriptions/14AB8053-986C-414E-96B3-11D82B8B478D/resourceGroups/rganyscale/providers/Anyscale.Platform/clouds/testcloud/cloudResources/eastus-cloud-resource'
            ]
            flags: {
            }
            headNode: {
              name: 'head-node'
              advancedInstanceConfig: '{}'
              flags: {
              }
              instanceType: 'Standard_D8s_v5'
              labels: {
                'ray.io/node-type': 'head'
              }
              requiredLabels: {
                'node-pool': 'default'
              }
              requiredResources: {
                accelerator: ''
                cpu: 8
                cpuArchitecture: 'x86_64'
                gpu: 0
                memory: 32
                tpu: 0
              }
              resources: {
                cpu: 8
                customResources: {
                }
                gpu: 0
                memory: 32
                objectStoreMemory: 8
              }
            }
            workerNodes: [
              {
                name: 'gpu-worker'
                advancedInstanceConfig: '{}'
                flags: {
                }
                instanceType: 'Standard_NC24ads_A100_v4'
                labels: {
                  'ray.io/node-type': 'worker'
                }
                marketType: 'ON_DEMAND'
                maxNodes: 10
                minNodes: 1
                requiredLabels: {
                  'node-pool': 'gpu-pool'
                }
                requiredResources: {
                  accelerator: 'A100'
                  cpu: 24
                  cpuArchitecture: 'x86_64'
                  gpu: 1
                  memory: 220
                  tpu: 0
                }
                resources: {
                  cpu: 24
                  customResources: {
                  }
                  gpu: 1
                  memory: 220
                  objectStoreMemory: 50
                }
              }
            ]
            zones: [
              'eastus-1'
            ]
          }
        ]
      }
    }
    idleTerminationMinutes: 30
    imageUri: 'anyscale/ray:2.44.0-py312-cu124'
  }
}
```
