# Microsoft.PlatformValidation
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.platformvalidation/cloudvalidations

CloudValidations_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.PlatformValidation/cloudValidations@2026-08-01-preview' = {
  name: 'example'
  location: 'southcentralus'
  properties: {
    description: 'Cloud validation that groups platform validation execution plans for the target subscription.'
  }
  tags: {
    environment: 'production'
  }
}
```

## microsoft.platformvalidation/cloudvalidations/validationexecutionplans

ValidationExecutionPlans_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.PlatformValidation/cloudValidations/validationExecutionPlans@2026-08-01-preview' = {
  parent: parentResource 
  name: 'example'
  location: 'southcentralus'
  properties: {
    description: 'Runs all public Linux-compatible AzCertify catalog tests against the Contoso Linux image.'
    planConfigurationJson: '{"apiVersion":"microsoft.PlatformValidation/validationExecutionPlan.v0","kind":"ValidationExecutionPlan","metadata":{"name":"contoso-linux-cert"},"parameters":{"certificationPackageReference":{"osType":"Linux","vmGenerationType":"V1","architectureType":"X64","recommendedVMSizes":["Standard_D4s_v3"],"storageProfile":{"osDiskImage":{"sourceVhdUri":"https://contoso.blob.core.windows.net/vhds/img.vhd?<sas>"},"dataDiskImages":[]},"additionalProperties":{}}},"authoring":{"steps":[{"name":"os-disk-size","type":"test","testRef":"/providers/Microsoft.PlatformValidation/validationTests/os-disk-size/versions/1.0.0"},{"name":"data-disk-size","type":"test","testRef":"/providers/Microsoft.PlatformValidation/validationTests/data-disk-size/versions/1.0.0"},{"name":"malware-defender","type":"test","testRef":"/providers/Microsoft.PlatformValidation/validationTests/malware-defender/versions/1.0.0"},{"name":"malware-esrp","type":"test","testRef":"/providers/Microsoft.PlatformValidation/validationTests/malware-esrp/versions/1.0.0"},{"name":"linux-quality-validation","type":"test","testRef":"/providers/Microsoft.PlatformValidation/validationTests/linux-quality-validation/versions/1.0.0","inputs":{"concurrency":1,"testSuite":[{"testNames":["smoke_test","validate_netvsc_reload"]}]}}]}}'
  }
  tags: {
    'owner-team': 'azure-platform-validation'
  }
}
```

## microsoft.platformvalidation/cloudvalidations/validationexecutionplans/executionplanruns

ExecutionPlanRuns_CreateOrUpdate_MaximumSet
```bicep
resource exampleResource 'Microsoft.PlatformValidation/cloudValidations/validationExecutionPlans/executionPlanRuns@2026-08-01-preview' = {
  parent: parentResource 
  name: 'example'
  properties: {
    description: 'Run the Contoso Linux image certification plan.'
  }
}
```
