# Microsoft.GcpConnector
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.gcpconnector/containerclusters

ContainerClusters_CreateOrReplace
```bicep
resource exampleResource 'Microsoft.GcpConnector/containerClusters@2027-01-01' = {
  name: 'example'
  properties: {
    gcpProjectId: 'lvknddutseiexgbnso'
    gcpProjectNumber: 'dulaageahihlvokvhlquc'
    gcpProperties: {
      name: 'example-gke-cluster'
      description: 'Example GKE cluster for testing'
      addonsConfig: {
        horizontalPodAutoscaling: {
          disabled: false
        }
        httpLoadBalancing: {
          disabled: false
        }
        networkPolicyConfig: {
          disabled: false
        }
      }
      autopilot: {
        enabled: false
      }
      clusterIpv4Cidr: '10.0.0.0/14'
      conditions: [
        {
          code: 'RUNNING'
          message: 'Cluster is healthy'
        }
      ]
      createTime: '2023-06-19T10:00:00.000Z'
      currentMasterVersion: '1.27.3-gke.100'
      currentNodeCount: 3
      currentNodeVersion: '1.27.3-gke.100'
      enableKubernetesAlpha: false
      enableTpu: false
      endpoint: '203.0.113.100'
      etag: 'BwXhqQY-KuY='
      id: 'example-gke-cluster-12345'
      initialClusterVersion: '1.27.3-gke.100'
      initialNodeCount: 3
      ipAllocationPolicy: {
        clusterIpv4CidrBlock: '10.0.0.0/14'
        clusterSecondaryRangeName: 'gke-cluster-pods'
        servicesIpv4CidrBlock: '10.4.0.0/19'
        servicesSecondaryRangeName: 'gke-cluster-services'
        useIpAliases: true
      }
      labelFingerprint: 'abc123def456'
      legacyAbac: {
        enabled: false
        provider: 'gcp'
      }
      location: 'us-central1'
      locations: [
        'us-central1-a'
        'us-central1-b'
        'us-central1-c'
      ]
      loggingService: 'logging.googleapis.com/kubernetes'
      masterAuth: {
        clusterCaCertificate: 'LS0tLS1CRUdJTi=='
      }
      masterAuthorizedNetworksConfig: {
        cidrBlocks: [
          {
            cidrBlock: '203.0.113.0/24'
            displayName: 'Office Network'
          }
        ]
        enabled: true
      }
      monitoringService: 'monitoring.googleapis.com/kubernetes'
      network: 'projects/example-project/global/networks/default'
      networkPolicy: {
        enabled: true
        provider: 'CALICO'
      }
      nodeConfig: {
        diskSizeGb: 100
        imageType: 'COS_CONTAINERD'
        labels: {
          env: 'production'
        }
        machineType: 'e2-medium'
        metadata: {
          'disable-legacy-endpoints': 'true'
        }
        oauthScopes: [
          'https://www.googleapis.com/auth/cloud-platform'
        ]
        preemptible: false
        serviceAccount: 'default'
        tags: [
          'gke-node'
        ]
      }
      nodeIpv4CidrSize: 24
      resourceLabels: {
        environment: 'production'
        team: 'platform'
      }
      selfLink: 'https://container.googleapis.com/v1/projects/example-project/zones/us-central1/clusters/example-gke-cluster'
      servicesIpv4Cidr: '10.4.0.0/19'
      status: 'RUNNING'
      statusMessage: 'Cluster is running'
      subnetwork: 'projects/example-project/regions/us-central1/subnetworks/default'
      zone: 'us-central1'
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
