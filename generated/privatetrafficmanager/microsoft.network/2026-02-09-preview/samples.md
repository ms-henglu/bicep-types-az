# Microsoft.Network
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.network/privatetrafficmanagerprofiles

Profiles_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/privateTrafficManagerProfiles@2026-02-09-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    customTopologyMapMode: 'Disabled'
    dnsConfig: {
      recordType: 'A'
      ttl: 10
    }
    endpoints: [
      {
        name: 'eelctkkre'
        alwaysServe: 'Enabled'
        endpointStatus: 'Enabled'
        healthPolicyId: '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/privateTrafficManagerProfiles/myProfile/healthPolicies/myHealthPolicy'
        kind: 'Endpoint'
        monitoringTarget: '10.0.0.1'
        priority: 10
        target: '10.0.0.1'
        weight: 100
      }
    ]
    profileStatus: 'Enabled'
    topologyMapId: '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/topologyMaps/myTopologyMap'
    trafficRoutingMethod: 'Priority'
  }
  tags: {
    environment: 'production'
  }
}
```

## microsoft.network/privatetrafficmanagerprofiles/endpoints

Endpoints_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/privateTrafficManagerProfiles/endpoints@2026-02-09-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    alwaysServe: 'Enabled'
    endpointStatus: 'Enabled'
    healthPolicyId: '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/privateTrafficManagerProfiles/myProfile/healthPolicies/myHealthPolicy'
    kind: 'Endpoint'
    monitoringTarget: '10.0.0.1'
    priority: 10
    target: '10.0.0.1'
    weight: 100
  }
}
```

## microsoft.network/privatetrafficmanagerprofiles/healthpolicies

HealthPolicies_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/privateTrafficManagerProfiles/healthPolicies@2026-02-09-preview' = {
  parent: parentResource 
  name: 'example'
  kind: 'Probe'
  properties: {
    probeConfig: {
      path: '/health'
      intervalInSeconds: 30
      port: 443
      timeoutInSeconds: 10
      toleratedNumberOfFailures: 3
      protocol: 'HTTPS'
    }
  }
}
```

## microsoft.network/privatetrafficmanagerprofiles/probinggateways

ProfileProbingGateways_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/privateTrafficManagerProfiles/probingGateways@2026-02-09-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    probingGatewayId: '/subscriptions/A1B2C3D4-E5F6-7890-ABCD-1234567890EF/resourceGroups/rgProbingInfra/providers/Microsoft.Network/probingGateways/pgw-westus-001'
  }
}
```

## microsoft.network/topologymaps

TopologyMaps_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/topologyMaps@2026-02-09-preview' = {
  name: 'example'
  location: 'eastus'
  properties: {
    catchAllSiteName: 'mySite'
    sites: [
      {
        name: 'mySite'
        properties: {
          probingGatewayIds: [
            '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/probingGateways/myProbingGateway'
          ]
          virtualNetworkIds: [
            '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/virtualNetworks/myVirtualNetwork'
          ]
        }
      }
    ]
  }
  tags: {
    environment: 'production'
  }
}
```

## microsoft.network/topologymaps/sites

Sites_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.Network/topologyMaps/sites@2026-02-09-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    probingGatewayIds: [
      '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/probingGateways/myProbingGateway'
    ]
    virtualNetworkIds: [
      '/subscriptions/10B6D88D-ADF4-4281-B3D0-B5A6702DEEDA/resourceGroups/rgprivateTrafficManager/providers/Microsoft.Network/virtualNetworks/myVirtualNetwork'
    ]
  }
}
```
