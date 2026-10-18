# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/computeinstances

ComputeInstances_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/computeInstances@2027-01-01' = {
  name: 'example'
  properties: {
    gcpProjectId: 'lvknddutseiexgbnso'
    gcpProjectNumber: 'dulaageahihlvokvhlquc'
    gcpProperties: {
      name: 'Replace this value with a string matching RegExp [a-z](?:[-a-z0-9]{0,61}[a-z0-9])?'
      description: 'yc'
      advancedMachineFeatures: {
        enableNestedVirtualization: true
        enableUefiNetworking: true
        threadsPerCore: 1
        visibleCoreCount: 1
      }
      canIpForward: true
      confidentialInstanceConfig: {
        enableConfidentialCompute: true
      }
      cpuPlatform: 'dduztttfaimzsarzcyylxixk'
      creationTimestamp: 'cz'
      deletionProtection: true
      disks: [
        {
          type: 'PERSISTENT'
          architecture: 'ARCHITECTURE_UNSPECIFIED'
          autoDelete: true
          boot: true
          deviceName: 'oxeqfqqmrqsrhn'
          diskEncryptionKey: {
            kmsKeyName: 'kyyysqczjtxnfnkek'
            kmsKeyServiceAccount: 'yrjfsczfqrav'
            rawKey: 'unchvnkqc'
            rsaEncryptedKey: 'romzhrkszbuirnbyzwrikywigou'
            sha256: 'tawtkork'
          }
          diskSizeGb: 'mtnvcixodrgjyzzyyyqsyywtyrmcbu'
          forceAttach: true
          guestOsFeatures: [
            {
              type: 'FEATURE_TYPE_UNSPECIFIED'
            }
          ]
          index: 14
          initializeParams: {
            description: 'vnlejkhtgtmiijmmcveehfnbrbfhu'
            architecture: 'ARCHITECTURE_UNSPECIFIED'
            diskName: 'ypenpobbehfxgjhemiqmw'
            diskSizeGb: 'qsupmjgujbluqjwrsznbtxxymcnqdz'
            diskType: 'kulgkicjncysnldaffasbckbvdwlo'
            enableConfidentialCompute: true
            labels: {
            }
            licenses: [
              'fdapfiupaohdoxgkxeftj'
            ]
            onUpdateAction: 'RECREATE_DISK'
            provisionedIops: 'lyszlswinaaabgfajwdhtahu'
            provisionedThroughput: 'ktjsyslmcameit'
            replicaZones: [
              'epyshsvpmouzluuhrsqnx'
            ]
            resourceManagerTags: {
            }
            resourcePolicies: [
              'lozrvq'
            ]
            sourceImage: 'dvgwuoabworyolevrut'
            sourceImageEncryptionKey: {
              kmsKeyName: 'kyyysqczjtxnfnkek'
              kmsKeyServiceAccount: 'yrjfsczfqrav'
              rawKey: 'unchvnkqc'
              rsaEncryptedKey: 'romzhrkszbuirnbyzwrikywigou'
              sha256: 'tawtkork'
            }
            sourceSnapshot: 'jhirlroivwizyibqsfarjl'
            sourceSnapshotEncryptionKey: {
              kmsKeyName: 'kyyysqczjtxnfnkek'
              kmsKeyServiceAccount: 'yrjfsczfqrav'
              rawKey: 'unchvnkqc'
              rsaEncryptedKey: 'romzhrkszbuirnbyzwrikywigou'
              sha256: 'tawtkork'
            }
          }
          interface: 'NVME'
          kind: 'ajqxtlsaqcxbhzgpuijd'
          licenses: [
            'txzwrhdogsj'
          ]
          mode: 'READ_ONLY'
          savedState: 'DISK_SAVED_STATE_UNSPECIFIED'
          shieldedInstanceInitialState: {
            dbs: [
              {
                content: 'Y29udGVudDE='
                fileType: 'BIN'
              }
            ]
            dbxs: [
              {
                content: 'Y29udGVudDE='
                fileType: 'BIN'
              }
            ]
            keks: [
              {
                content: 'Y29udGVudDE='
                fileType: 'BIN'
              }
            ]
            pk: {
              content: 'Y29udGVudDE='
              fileType: 'BIN'
            }
          }
          source: 'myrtfxnszzkwwpfwlqhfyghorzmb'
        }
      ]
      displayDevice: {
        enableDisplay: true
      }
      fingerprint: 'ZmluZ2VycHJpbnQx'
      guestAccelerators: [
        {
          acceleratorCount: 3
          acceleratorType: 'svnnusfwowayaxhkp'
        }
      ]
      hostname: 'ztwzgzceuiiyxqkdptvroaiyyv'
      id: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.GcpConnector/{resource}/{resourceName}'
      instanceEncryptionKey: {
        kmsKeyName: 'kyyysqczjtxnfnkek'
        kmsKeyServiceAccount: 'yrjfsczfqrav'
        rawKey: 'unchvnkqc'
        rsaEncryptedKey: 'romzhrkszbuirnbyzwrikywigou'
        sha256: 'tawtkork'
      }
      keyRevocationActionType: 'KEY_REVOCATION_ACTION_TYPE_UNSPECIFIED'
      kind: 'r'
      labelFingerprint: 'bGFiZWxGaW5nZXJwcmludDE='
      labels: {
      }
      lastStartTimestamp: 'jrxmqtsdgngcvoktyj'
      lastStopTimestamp: 'igjjlsdkdppvh'
      lastSuspendedTimestamp: 'x'
      machineType: 'omcfqiakyyyvgyzjeped'
      metadata: {
        fingerprint: 'ZmluZ2VycHJpbnQx'
        items: [
          {
            key: 'Replace this value with a string matching RegExp [a-zA-Z0-9-_]{1,128}'
            value: 'vnwkrouueqawaflxax'
          }
        ]
        kind: 'ugcmmldazobywmupsglhqiepmwmt'
      }
      minCpuPlatform: 'qybquxkdgtjsedy'
      networkInterfaces: [
        {
          name: 'vxyrwcaeasxuasdvozymlzuivp'
          accessConfigs: [
            {
              name: 'u'
              type: 'DIRECT_IPV6'
              externalIpv6: 'gxo'
              externalIpv6PrefixLength: 23
              kind: 'qkyyhovvkwrameouoooye'
              natIP: 'avpbnmmpzoprsidmzjfrkfystemqel'
              networkTier: 'FIXED_STANDARD'
              publicPtrDomainName: 'dnhhibwhczbzuvjamxcftpvv'
              securityPolicy: 'drt'
              setPublicPtr: true
            }
          ]
          aliasIpRanges: [
            {
              ipCidrRange: 'p'
              subnetworkRangeName: 'mrlrrfgwcw'
            }
          ]
          fingerprint: 'ZmluZ2VycHJpbnQx'
          internalIpv6PrefixLength: 22
          ipv6AccessConfigs: [
            {
              name: 'u'
              type: 'DIRECT_IPV6'
              externalIpv6: 'gxo'
              externalIpv6PrefixLength: 23
              kind: 'qkyyhovvkwrameouoooye'
              natIP: 'avpbnmmpzoprsidmzjfrkfystemqel'
              networkTier: 'FIXED_STANDARD'
              publicPtrDomainName: 'dnhhibwhczbzuvjamxcftpvv'
              securityPolicy: 'drt'
              setPublicPtr: true
            }
          ]
          ipv6AccessType: 'EXTERNAL'
          ipv6Address: 'tm'
          kind: 'gzdmkbaihs'
          network: 'oxtpgeoqvqhxcmaavo'
          networkAttachment: 'xxrufcbnnhnlgpl'
          networkIP: 'lbjr'
          nicType: 'GVNIC'
          queueCount: 22
          stackType: 'IPV4_IPV6'
          subnetwork: 'zbbxfjxagehhyym'
        }
      ]
      networkPerformanceConfig: {
        totalEgressBandwidthTier: 'DEFAULT'
      }
      params: {
        resourceManagerTags: {
        }
      }
      privateIpv6GoogleAccess: 'ENABLE_BIDIRECTIONAL_ACCESS_TO_GOOGLE'
      reservationAffinity: {
        consumeReservationType: 'ANY_RESERVATION'
        key: 'ekojht'
        values: [
          'mllpgblygzjqvji'
        ]
      }
      resourcePolicies: [
        'pzgbzqazylftsdynvlmuydocmuvg'
      ]
      resourceStatus: {
        physicalHost: 'f'
        upcomingMaintenance: {
          type: 'SCHEDULED'
          canReschedule: true
          latestWindowStartTime: 'mfhvqncirhxrwwevxqgfci'
          maintenanceStatus: 'ONGOING'
          windowEndTime: 'oxynofnrgnpvjgpp'
          windowStartTime: 'wnmuqzqdjfpkhlbadumth'
        }
      }
      satisfiesPzi: true
      satisfiesPzs: true
      scheduling: {
        automaticRestart: true
        instanceTerminationAction: 'DELETE'
        localSsdRecoveryTimeout: {
          nanos: 18
          seconds: 'ttqhbujcqtdhtsfonkwkc'
        }
        locationHint: 'rgyydzkhhfygjsygdbuueayyhlyf'
        minNodeCpus: 5
        nodeAffinities: [
          {
            key: 'hxkkjttbuvgddt'
            operator: 'IN'
            values: [
              'xanku'
            ]
          }
        ]
        onHostMaintenance: 'MIGRATE'
        preemptible: true
        provisioningModel: 'SPOT'
      }
      selfLink: 'huzisfuqmmfgrhktnxngixkhpsnuk'
      serviceAccounts: [
        {
          email: 'ayxmdlzhytnadwwdqxxnyf'
          scopes: [
            'hq'
          ]
        }
      ]
      shieldedInstanceConfig: {
        enableIntegrityMonitoring: true
        enableSecureBoot: true
        enableVtpm: true
      }
      shieldedInstanceIntegrityPolicy: {
        updateAutoLearnPolicy: true
      }
      sourceMachineImage: 'tpsbbhxnefylubmyxn'
      sourceMachineImageEncryptionKey: {
        kmsKeyName: 'kyyysqczjtxnfnkek'
        kmsKeyServiceAccount: 'yrjfsczfqrav'
        rawKey: 'unchvnkqc'
        rsaEncryptedKey: 'romzhrkszbuirnbyzwrikywigou'
        sha256: 'tawtkork'
      }
      startRestricted: true
      status: 'DEPROVISIONING'
      statusMessage: 'tojkjtnsjbjezqsyazjqxvh'
      tags: {
        fingerprint: 'ZmluZ2VycHJpbnQx'
        items: [
          'aijdeyuoymw'
        ]
      }
      zone: 'uyfhfmyzimegdgfhkjlh'
    }
    gcpRegion: 'xrxjlshmnbbw'
    gcpSourceSchema: 'asgbfmepnkauoizxpxt'
    gcpTags: {
    }
    publicCloudConnectorsResourceId: 'siilqwhsmldrvezs'
    publicCloudResourceName: 'yxjfmhqt'
    resourceName: 'nnczpspvaz'
  }
}
```
