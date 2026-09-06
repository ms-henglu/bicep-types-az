# Microsoft.RedHatOpenShift
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.redhatopenshift/hcpopenshiftclusters

HcpOpenShiftClusters_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.RedHatOpenShift/hcpOpenShiftClusters@2024-06-10-preview' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/rgopenapi/providers/Microsoft.ManagedIdentity/userAssignedIdentities/serviceMI': {
      }
    }
  }
  location: 'ayecbdqonsqfowbq'
  properties: {
    api: {
      authorizedCidrs: [
        '192.168.1.0/24'
        '10.0.0.0/16'
      ]
      visibility: 'Public'
    }
    autoscaling: {
      maxNodeProvisionTimeSeconds: 0
      maxNodesTotal: 0
      maxPodGracePeriodSeconds: 0
      podPriorityThreshold: 1
    }
    clusterImageRegistry: {
      state: 'Enabled'
    }
    console: {
    }
    dns: {
      baseDomainPrefix: 'jcldjrtyebhrlxs'
    }
    etcd: {
      dataEncryption: {
        customerManaged: {
          encryptionType: 'KMS'
          kms: {
            activeKey: {
              name: 'my-cool-key'
              vaultName: 'my-cool-vault'
              version: '8e73e7d1fd7d4a87b730f676fc77d3a6'
            }
          }
        }
        keyManagementMode: 'CustomerManaged'
      }
    }
    network: {
      hostPrefix: 21
      machineCidr: '10.0.0.0/16'
      networkType: 'OVNKubernetes'
      podCidr: '10.128.0.0/14'
      serviceCidr: '172.30.0.0/16'
    }
    nodeDrainTimeoutMinutes: 20
    platform: {
      managedResourceGroup: 'nhyhywrxupo'
      networkSecurityGroupId: '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/resourceGroupName/providers/Microsoft.Network/networkSecurityGroups/nsg-example'
      operatorsAuthentication: {
        userAssignedIdentities: {
          controlPlaneOperators: {
          }
          dataPlaneOperators: {
          }
          serviceManagedIdentity: '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/rgopenapi/providers/Microsoft.ManagedIdentity/userAssignedIdentities/serviceMI'
        }
      }
      outboundType: 'LoadBalancer'
      subnetId: '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/resourceGroupName/providers/Microsoft.Network/virtualNetworks/hcp-network-example/subnets/example-subnet'
    }
    version: {
      channelGroup: 'stable'
      id: '4.12'
    }
  }
  tags: {
    key4181: 'leaswtidajsjtgmqawhdl'
  }
}
```

## microsoft.redhatopenshift/hcpopenshiftclusters/externalauths

ExternalAuths_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.RedHatOpenShift/hcpOpenShiftClusters/externalAuths@2024-06-10-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    claim: {
      mappings: {
        groups: {
          claim: 'icvcoadhpyprqygxyvqhewaycjdtzrwjzbjgmyralburdaolouyvkymfpetymlcwpqsoteryaatoapieizbsnttmkkxsrhyaacnucznujhgmxkmnmgtcjntjsmuabplpoyxberrjdikkkqqiqfnlvwngpbfajzhxzdgqicoconqtrrstzzumdurgfsheypcm'
          prefix: 'kjlxhbjdvwarcwdu'
        }
        username: {
          claim: 'utlmketyrdxmwijowjzbuqyawuoqrlriryuknigayeviriulgjvuwvxjrsrhpmvavyyxzapgkfeyedcklnoddeviibefgvubvecffqgdhntammtlwjsjemhsqhafmmorskpuwbtjgkoggxq'
          prefix: 'ojmwi'
          prefixPolicy: 'mdbghfytgejdqobfllqmajtc'
        }
      }
      validationRules: [
        {
          type: 'RequiredClaim'
          requiredClaim: {
            claim: 'ciapdmvrnfitudpx'
            requiredValue: 'mqzzjiozgxfgflhdrnwawpke'
          }
        }
      ]
    }
    clients: [
      {
        type: 'Confidential'
        clientId: 'vobxtzobefgl'
        component: {
          name: 'my-cool-component'
          authClientNamespace: 'my-cool-namespace'
        }
        extraScopes: [
          'ejmvezdxvoozyiickteiqnvpxqciep'
        ]
      }
    ]
    issuer: {
      audiences: [
        'audience1'
        'audience2'
        'audience3'
        'audience4'
        'audience5'
      ]
      ca: 'lrakpuqodeqscdauefb'
      url: 'https://microsoft.com/a'
    }
  }
}
```

## microsoft.redhatopenshift/hcpopenshiftclusters/nodepools

NodePools_CreateOrUpdate
```bicep
resource exampleResource 'Microsoft.RedHatOpenShift/hcpOpenShiftClusters/nodePools@2024-06-10-preview' = {
  parent: parentResource 
  name: 'example'
  location: 'mqewzbuvnyxnwbmir'
  properties: {
    autoRepair: true
    autoScaling: {
      max: 29
      min: 6
    }
    labels: [
      {
        key: 'release'
        value: '4.12'
      }
    ]
    nodeDrainTimeoutMinutes: 20
    platform: {
      availabilityZone: 'australiaeast-az1'
      enableEncryptionAtHost: true
      osDisk: {
        diskStorageAccountType: 'Premium_LRS'
        encryptionSetId: '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/resourceGroupName/providers/Microsoft.Compute/diskEncryptionSets/hcp-disk-encryption-set-example'
        sizeGiB: 64
      }
      subnetId: '/subscriptions/FDEA43EA-0230-4A7D-BDEE-F3AFF2183B1D/resourceGroups/resourceGroupName/providers/Microsoft.Network/virtualNetworks/hcp-network-example/subnets/example-subnet'
      vmSize: 'Standard_D2s_v3'
    }
    replicas: 18
    taints: [
      {
        effect: 'NoSchedule'
        key: 'iveofwsptzsxepyfirlfypshvkgzkpfdwrpreacacbcifrzpvmgmovnpmkeqxgvamtbwqfewlrnlcqcmbnqhdgvosyxazqxwtlcviveerkvdrveayeyvasngwjmrsnhyvmayzrndwahvuoocvbqjuscmybctzhrhbotipnrwhnkhejgiuanmidrdjetccddupjtvvztlbwlgdxgdwlhxdlluvcduh'
        value: 'x'
      }
    ]
    version: {
      channelGroup: 'stable'
      id: '4.12'
    }
  }
  tags: {
    key: 'value'
  }
}
```
