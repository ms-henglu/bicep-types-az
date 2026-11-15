# Kore.AgentPlatform
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## kore.agentplatform/organizations

Organizations_Create
```bicep
resource exampleResource 'Kore.AgentPlatform/organizations@2026-07-01-preview' = {
  name: 'example'
  location: 'eastus2euap'
  properties: {
    companyDetails: {
      businessType: 'Technology'
      companyName: 'Contoso Ltd.'
      country: 'US'
      domain: 'contoso.com'
      numberOfEmployees: 500
    }
    partnerProperties: {
      billingEmail: 'billing@contoso.com'
      defaultWorkspace: {
        name: 'my first workspace'
        marketplaceDetails: [
          {
            offerDetails: {
              offerId: 'kore-ai-platform'
              planId: 'business-monthly'
              planName: 'Business Monthly'
              publisherId: 'kore-ai'
              termId: '1m'
              termUnit: 'P1M'
            }
            subscriptionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/contoso-rg/providers/Microsoft.SaaS/resources/kore-ai-saas'
            subscriptionStatus: 'Subscribed'
          }
        ]
        product: 'aiforwork'
      }
      organizationName: 'Contoso AI Platform'
      ownerEmail: 'admin@contoso.com'
    }
    user: {
      emailAddress: 'jane.doe@contoso.com'
      firstName: 'Jane'
      lastName: 'Doe'
      phoneNumber: '+1-425-555-0100'
      upn: 'jane.doe@contoso.onmicrosoft.com'
    }
  }
  tags: {
    environment: 'production'
  }
}
```

Organizations_Create_MaximumSet_Gen
```bicep
resource exampleResource 'Kore.AgentPlatform/organizations@2026-07-01-preview' = {
  name: 'example'
  location: 'eastus2euap'
  properties: {
    companyDetails: {
      businessType: 'Technology'
      companyName: 'Contoso Ltd.'
      country: 'US'
      domain: 'contoso.com'
      numberOfEmployees: 500
      officeAddress: '1 Microsoft Way, Redmond, WA 98052'
    }
    partnerProperties: {
      billingEmail: 'billing@contoso.com'
      defaultWorkspace: {
        name: 'my first workspace'
        marketplaceDetails: [
          {
            offerDetails: {
              offerId: 'kore-ai-platform'
              planId: 'business-monthly'
              planName: 'Business Monthly'
              publisherId: 'kore-ai'
              termId: '1m'
              termUnit: 'P1M'
            }
            subscriptionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/contoso-rg/providers/Microsoft.SaaS/resources/kore-ai-saas'
            subscriptionStatus: 'Subscribed'
          }
        ]
        product: 'aiforwork'
      }
      organizationName: 'Contoso AI Platform'
      ownerEmail: 'admin@contoso.com'
    }
    singleSignOn: {
      type: 'Saml'
      aadDomains: [
        'contoso.com'
      ]
      enterpriseAppId: '00000000-0000-0000-0000-000000000000'
      state: 'Enable'
      url: 'https://sso.kore.ai/contoso'
    }
    user: {
      address: '1 Microsoft Way, Redmond, WA 98052'
      alternateEmail: 'jane.alternate@contoso.com'
      emailAddress: 'jane.doe@contoso.com'
      firstName: 'Jane'
      lastName: 'Doe'
      phoneNumber: '+1-425-555-0100'
      upn: 'jane.doe@contoso.onmicrosoft.com'
    }
  }
  tags: {
    environment: 'production'
  }
}
```

## kore.agentplatform/organizations/workspaces

Workspaces_CreateOrUpdate
```bicep
resource exampleResource 'Kore.AgentPlatform/organizations/workspaces@2026-07-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    marketplaceDetails: [
      {
        offerDetails: {
          offerId: 'kore-ai-platform'
          planId: 'business-monthly'
          planName: 'Business Monthly'
          publisherId: 'kore-ai'
          termId: '1m'
          termUnit: 'P1M'
        }
        subscriptionId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/contoso-rg/providers/Microsoft.SaaS/resources/kore-ai-saas'
        subscriptionStatus: 'Subscribed'
      }
    ]
    partnerProperties: {
      name: 'Contoso Production'
      ownerEmail: 'owner@contoso.com'
    }
    product: 'aiforwork'
  }
}
```
