# Microsoft.ServiceNetworking
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.servicenetworking/trafficcontrollers

Put Traffic Controller
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers@2026-03-01' = {
  name: 'example'
  location: 'NorthCentralUS'
  tags: {
    key1: 'value1'
  }
}
```

## microsoft.servicenetworking/trafficcontrollers/associations

Put Association
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/associations@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  location: 'NorthCentralUS'
  properties: {
    associationType: 'subnets'
    subnet: {
      id: '/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/vnet-tc/subnets/tc-subnet'
    }
  }
}
```

## microsoft.servicenetworking/trafficcontrollers/frontends

Put Frontend
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/frontends@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  location: 'NorthCentralUS'
  properties: {
    publicNetworkAccess: 'Enabled'
  }
}
```

Put Private Frontend
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/frontends@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  location: 'NorthCentralUS'
  properties: {
    association: {
      id: '/subscriptions/subid/resourceGroups/rg1/providers/Microsoft.ServiceNetworking/trafficControllers/tc1/associations/as1'
    }
    publicNetworkAccess: 'Disabled'
  }
}
```

## microsoft.servicenetworking/trafficcontrollers/privateendpointconnections

Update Private Endpoint Connection
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/privateEndpointConnections@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  properties: {
    privateLinkServiceConnectionState: {
      description: 'Approved by admin'
      status: 'Approved'
    }
  }
}
```

## microsoft.servicenetworking/trafficcontrollers/securitypolicies

Put IpAccessRules SecurityPolicy
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/securityPolicies@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  location: 'NorthCentralUS'
  properties: {
    ipAccessRulesPolicy: {
      rules: [
      ]
    }
  }
}
```

Put WAF SecurityPolicy
```bicep
resource exampleResource 'Microsoft.ServiceNetworking/trafficControllers/securityPolicies@2026-03-01' = {
  parent: parentResource 
  name: 'example'
  location: 'NorthCentralUS'
  properties: {
    wafPolicy: {
      id: '/subscriptions/subid/resourcegroups/rg1/providers/Microsoft.Network/applicationGatewayWebApplicationFirewallPolicies/wp-0'
    }
  }
}
```
