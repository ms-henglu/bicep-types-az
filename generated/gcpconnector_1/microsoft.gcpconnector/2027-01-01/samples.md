# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/cloudfunctions

CloudFunctions_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/cloudFunctions@2027-01-01' = {
  name: 'example'
  location: 'ruxlgqjhiwabrxe'
  properties: {
    gcpProjectId: 'lvknddutseiexgbnso'
    gcpProjectNumber: 'albxnjvctceguzkfklixjvftebdge'
    gcpProperties: {
      name: 'uscjdxkickzdyecwfxzayzhvxawngb'
      description: 'yasjyjlqecutjmtcpepijtkgjedl'
      buildConfig: {
        automaticUpdatePolicy: {
        }
        build: 'dpis'
        dockerRegistry: 'DOCKER_REGISTRY_UNSPECIFIED'
        dockerRepository: 'ohjnnylkceakbmnvyynkyvbcgf'
        entryPoint: 'rtxszynuudve'
        environmentVariables: {
        }
        onDeployUpdatePolicy: {
          runtimeVersion: 'irsvkfeynotqgo'
        }
        runtime: 'ojxmowc'
        serviceAccount: 'fgyqzwjhufylttkkbqihtneoznfa'
        source: {
          gitUri: 'ovmfadxg'
          repoSource: {
            branchName: 'oehyfwx'
            commitSha: 'hnztmlcmawhjvvvedivz'
            dir: 'vmblykuodhpjyhfzbrsmmtrrwjam'
            projectId: 'siturzeuqiozcqwvclzyiwvn'
            repoName: 'fhryhnaljn'
            tagName: 'pqvdyunyhvxa'
          }
          storageSource: {
            bucket: 'xfdvkjxrufslwpibgk'
            generation: 'vl'
            object: 'jgisckvupztkb'
          }
        }
        sourceProvenance: {
          gitUri: 'ampi'
          resolvedRepoSource: {
            branchName: 'oehyfwx'
            commitSha: 'hnztmlcmawhjvvvedivz'
            dir: 'vmblykuodhpjyhfzbrsmmtrrwjam'
            projectId: 'siturzeuqiozcqwvclzyiwvn'
            repoName: 'fhryhnaljn'
            tagName: 'pqvdyunyhvxa'
          }
          resolvedStorageSource: {
            bucket: 'xfdvkjxrufslwpibgk'
            generation: 'vl'
            object: 'jgisckvupztkb'
          }
        }
        sourceToken: 'hxjeqtapgngdmosibjxwicr'
        workerPool: 'wioasedvlolsemsnmntghwslltfooh'
      }
      createTime: 'wjcovhsvgbtndlpkbmjjsuvrity'
      environment: 'ENVIRONMENT_UNSPECIFIED'
      eventTrigger: {
        channel: 'hdvujtewrkuavxjvdkod'
        eventFilters: [
          {
            attribute: 'heupsmfcbevaqahmlpfy'
            operator: 'xxqc'
            value: 'z'
          }
        ]
        eventType: 'ezlbxihgafsgifozgwlqjozqfvpuw'
        pubsubTopic: 'osg'
        retryPolicy: 'RETRY_POLICY_UNSPECIFIED'
        service: 'rqheqe'
        serviceAccountEmail: 'wap'
        trigger: 'qmfupnhnyqg'
        triggerRegion: 'pn'
      }
      kmsKeyName: 'fnzpwbwfkxlmpfpovz'
      labels: {
      }
      satisfiesPzi: true
      satisfiesPzs: true
      serviceConfig: {
        allTrafficOnLatestRevision: true
        availableCpu: 'avnkucrffp'
        availableMemory: 'qdqfagiuiupltwhieofovp'
        environmentVariables: {
        }
        ingressSettings: 'INGRESS_SETTINGS_UNSPECIFIED'
        maxInstanceCount: 27
        maxInstanceRequestConcurrency: 2
        minInstanceCount: 16
        revision: 'dfsvwaxlny'
        secretEnvironmentVariables: [
          {
            key: 'srjwpdquj'
            projectId: 'bcjdhogjsnwlfjptaqvammv'
            secret: 'xioxtmabmyn'
            version: 'y'
          }
        ]
        secretVolumes: [
          {
            mountPath: 'zyuiah'
            projectId: 'peqqhllp'
            secret: 'y'
            versions: [
              {
                path: 'hjkiv'
                version: 'jurittjt'
              }
            ]
          }
        ]
        securityLevel: 'SECURITY_LEVEL_UNSPECIFIED'
        service: 'ks'
        serviceAccountEmail: 'iptnzhypffw'
        timeoutSeconds: 1
        uri: 'zwurmdfylaoikdxbgg'
        vpcConnector: 'zwejumufthidoqnoxdooxqhz'
        vpcConnectorEgressSettings: 'VPC_CONNECTOR_EGRESS_SETTINGS_UNSPECIFIED'
      }
      state: 'STATE_UNSPECIFIED'
      stateMessages: [
        {
          type: 'csafrjvenugbhhycqnmsefft'
          message: 'lmrfqluqyqynignrmoxn'
          severity: 'SEVERITY_UNSPECIFIED'
        }
      ]
      updateTime: 'ihzrhrxehwhyagyuewavm'
      url: 'utoacffswx'
    }
    gcpRegion: 'ghlhojlhwqlndzmoxsatt'
    gcpSourceSchema: 'svcpjljnuxa'
    gcpTags: {
    }
    publicCloudConnectorsResourceId: 'cmhqojxrqcyk'
    publicCloudResourceName: 'nhvcaitcp'
    resourceName: 'oysfjfjagrnffepxgcfhqopjalpmv'
  }
  tags: {
  }
}
```
