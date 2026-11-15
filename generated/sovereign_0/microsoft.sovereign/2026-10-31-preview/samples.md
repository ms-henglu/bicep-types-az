# Microsoft.Sovereign
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.sovereign/sovereignviews

SovereignViewOperations_Create
```bicep
resource exampleResource 'Microsoft.Sovereign/sovereignViews@2026-10-31-preview' = {
  name: 'example'
  identity: {
    type: 'SystemAssigned'
  }
  location: 'northeurope'
  properties: {
    dimensionSettings: {
      dataResidency: {
        parameters: {
          allowedLocations: [
            'northeurope'
            'swedencentral'
          ]
        }
        resourceEvaluationScope: 'Residency360'
      }
    }
    isWorkload: true
    policyInitiatives: [
      {
        dimension: 'EncryptionAtRest'
        policyAssignmentIds: [
          '/subscriptions/22b62f96-c8d5-4131-97f8-f820a5a3c55f/providers/Microsoft.Authorization/policyAssignments/ExamplePolicyAssignment'
        ]
        policyInitiativeId: '/subscriptions/22b62f96-c8d5-4131-97f8-f820a5a3c55f/providers/Microsoft.Authorization/policySetDefinitions/ExamplePolicySet'
        policyVersion: '1.0.0'
      }
      {
        dimension: 'BusinessContinuity'
        policyAssignmentIds: [
          '/subscriptions/22b62f96-c8d5-4131-97f8-f820a5a3c55f/providers/Microsoft.Authorization/policyAssignments/ExampleBusinessContinuityPolicyAssignment'
        ]
        policyInitiativeId: '/subscriptions/22b62f96-c8d5-4131-97f8-f820a5a3c55f/providers/Microsoft.Authorization/policySetDefinitions/ExampleBusinessContinuityPolicySet'
        policyVersion: '1.0.0'
      }
    ]
    regulatoryDocumentName: 'SovereignControlBaseline'
    scope: {
      managementGroups: [
        {
          name: 'ExampleManagementGroup'
          id: '/providers/Microsoft.Management/managementGroups/ExampleManagementGroup'
        }
      ]
      subscriptions: [
        {
          name: 'ExampleSubscription1'
          id: '22b62f96-c8d5-4131-97f8-f820a5a3c55f'
        }
        {
          name: 'ExampleSubscription2'
          id: '9a7a1a5f-4e73-4a2a-8b4f-3e9e5b2c6d10'
        }
      ]
    }
  }
  tags: {
    tag1: 'MCFS'
  }
}
```
