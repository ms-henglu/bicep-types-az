# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/storagebuckets

StorageBuckets_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/storageBuckets@2027-01-01' = {
  name: 'example'
  location: 'ljgjmtocpdgzmm'
  properties: {
    gcpProjectId: 'lvknddutseiexgbnso'
    gcpProjectNumber: 'dwwjpxudgxrmxnhshqgowpgf'
    gcpProperties: {
      name: 'awktcngnenppsdynpkjvfjoprom'
      acl: [
        {
          bucket: 'pvjywpilhzzxfpgsmvdltueky'
          domain: 'ft'
          email: 'nbjncjpmpaxci'
          entity: 'vwedgmfnxrxpihgoqtvwievnme'
          entityId: 'ltmojyovixgrngq'
          etag: 'ssboocjadoaqqiztsmomc'
          id: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.GcpConnector/{resource}/{resourceName}'
          kind: 'fzozeilqpugvykgqmesy'
          projectTeam: {
            projectNumber: 'rnyt'
            team: 'cutadapksshgilrelfsfow'
          }
          role: 'qyxcmgfikoyhzfmepdiqiejsvfvou'
          selfLink: 'rgqokdrvgtkxr'
        }
      ]
      autoclass: {
        enabled: true
        terminalStorageClass: 'jhxyfpxvedfbbogsj'
        terminalStorageClassUpdateTime: '2025-06-19T19:45:45.743Z'
        toggleTime: '2025-06-19T19:45:45.744Z'
      }
      billing: {
        requesterPays: true
      }
      cors: [
        {
          method: [
            'rdd'
          ]
          maxAgeSeconds: 13
          origin: [
            'ueiraolxywbspcfc'
          ]
          responseHeader: [
            'gtdsrleun'
          ]
        }
      ]
      customPlacementConfig: {
        dataLocations: [
          'ufflpbweskcex'
        ]
      }
      defaultEventBasedHold: true
      defaultObjectAcl: [
        {
          bucket: 'xmejktkjjpjun'
          domain: 'jr'
          email: 'ywmwb'
          entity: 'lihwojxlmqazispl'
          entityId: 'i'
          etag: 'mfwitplvdjdxthpgbfquz'
          generation: 'ifjdkmguszzad'
          id: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.GcpConnector/{resource}/{resourceName}'
          kind: 'gsrviyepewo'
          object: 'tpstdaoquhzwzpf'
          projectTeam: {
            projectNumber: 'yavvdopwcthxt'
            team: 'cxkkqbbgvnymrgoyyefshzypis'
          }
          role: 'khegwhzqfxio'
          selfLink: 'atyhpocsopsdkdaqwfgegqh'
        }
      ]
      encryption: {
        defaultKmsKeyName: 'cwjrpkkvicmqhaktlkkegaxoimbl'
      }
      etag: 'stlaffdeqcgozxfdkike'
      generation: 'gnrbmzjilnovtqlxf'
      hierarchicalNamespace: {
        enabled: true
      }
      iamConfiguration: {
        bucketPolicyOnly: {
          enabled: true
          lockedTime: '2025-06-19T19:45:45.744Z'
        }
        publicAccessPrevention: 'plzdsidgrxkyyzzmadcnnfr'
        uniformBucketLevelAccess: {
          enabled: true
          lockedTime: '2025-06-19T19:45:45.744Z'
        }
      }
      id: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.GcpConnector/{resource}/{resourceName}'
      kind: 'ogwmh'
      labels: {
      }
      lifecycle: {
        rule: [
          {
            action: {
              type: 'bbampgxyru'
              storageClass: 'v'
            }
            condition: {
              age: 21
              createdBefore: '2025-06-19'
              customTimeBefore: '2025-06-19'
              daysSinceCustomTime: 27
              daysSinceNoncurrentTime: 24
              isLive: true
              matchesPattern: 'cjolbnss'
              matchesPrefix: [
                'wycnjrq'
              ]
              matchesStorageClass: [
                'lzgdbxsutzxzbqtiuhgbizzt'
              ]
              matchesSuffix: [
                'mmwaemw'
              ]
              noncurrentTimeBefore: '2025-06-19'
              numNewerVersions: 25
            }
          }
        ]
      }
      location: 'clxigdeubkjekrtqnajjqgazftatq'
      locationType: 'jnwkfmf'
      logging: {
        logBucket: 'qtadmbrorsssxgbfqch'
        logObjectPrefix: 'kh'
      }
      metageneration: 'nyerfkvzr'
      objectRetention: {
        mode: 'ojqnmehdbczbaon'
      }
      owner: {
        entity: 't'
        entityId: 'bmxpfpvgwlyugmzsmdjh'
      }
      projectNumber: 'xplnnfasf'
      retentionPolicy: {
        effectiveTime: '2025-06-19T19:45:45.744Z'
        isLocked: true
        retentionPeriod: 'z'
      }
      rpo: 'dqnd'
      satisfiesPZS: true
      selfLink: 'nzjfmjmxstnkhndhywicnlsl'
      softDeletePolicy: {
        effectiveTime: '2025-06-19T19:45:45.745Z'
        retentionDurationSeconds: 'jmxkdnnvfulaejzrmmojwmir'
      }
      storageClass: 'beiajnmktvxaiavq'
      timeCreated: '2025-06-19T19:45:45.745Z'
      updated: '2025-06-19T19:45:45.745Z'
      versioning: {
        enabled: true
      }
      website: {
        mainPageSuffix: 'uipglkaydrsxk'
        notFoundPage: 'znhagqekhbdqpiys'
      }
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
