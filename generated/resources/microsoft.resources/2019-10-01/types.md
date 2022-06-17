# Microsoft.Resources @ 2019-10-01

## Resource Microsoft.Resources/deployments@2019-10-01
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2019-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The location to store the deployment data.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DeploymentPropertiesOrDeploymentPropertiesExtended](#deploymentpropertiesordeploymentpropertiesextended) (Required): The deployment properties.
* **tags**: [DeploymentTags](#deploymenttags): Deployment tags
* **type**: 'Microsoft.Resources/deployments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Resources/resourceGroups@2019-10-01
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2019-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the resource group. It cannot be changed after the resource group has been created. It must be one of the supported Azure locations.
* **managedBy**: string: The ID of the resource that manages this resource group.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ResourceGroupProperties](#resourcegroupproperties): The resource group properties.
* **tags**: [ResourceGroupTags](#resourcegrouptags): The tags attached to the resource group.
* **type**: 'Microsoft.Resources/resourceGroups' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Resources/tags@2019-10-01
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2019-10-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [Tags](#tags) (Required): The set of tags.
* **type**: 'Microsoft.Resources/tags' (ReadOnly, DeployTimeConstant): The resource type

## Function exportTemplate (Microsoft.Resources/deployments@2019-10-01)
* **Resource**: Microsoft.Resources/deployments
* **ApiVersion**: 2019-10-01
* **Output**: [DeploymentExportResult](#deploymentexportresult)

## Function validate (Microsoft.Resources/deployments@2019-10-01)
* **Resource**: Microsoft.Resources/deployments
* **ApiVersion**: 2019-10-01
* **Input**: [Deployment](#deployment)
* **Output**: [DeploymentValidateResult](#deploymentvalidateresult)

## Function whatIf (Microsoft.Resources/deployments@2019-10-01)
* **Resource**: Microsoft.Resources/deployments
* **ApiVersion**: 2019-10-01
* **Input**: [ScopedDeploymentWhatIf](#scopeddeploymentwhatif)
* **Output**: [WhatIfOperationResult](#whatifoperationresult)

## Alias
### Properties
* **defaultPath**: string: The default path for an alias.
* **defaultPattern**: [AliasPattern](#aliaspattern): The default pattern for an alias.
* **name**: string: The alias name.
* **paths**: [AliasPath](#aliaspath)[]: The paths for an alias.
* **type**: 'Mask' | 'NotSpecified' | 'PlainText': The type of the alias.

## AliasPath
### Properties
* **apiVersions**: string[]: The API versions.
* **path**: string: The path of an alias.
* **pattern**: [AliasPattern](#aliaspattern): The pattern for an alias path.

## AliasPattern
### Properties
* **phrase**: string: The alias pattern phrase.
* **type**: 'Extract' | 'NotSpecified': The type of alias pattern
* **variable**: string: The alias pattern variable.

## BasicDependency
### Properties
* **id**: string: The ID of the dependency.
* **resourceName**: string: The dependency resource name.
* **resourceType**: string: The dependency resource type.

## DebugSetting
### Properties
* **detailLevel**: string: Specifies the type of information to log for debugging. The permitted values are none, requestContent, responseContent, or both requestContent and responseContent separated by a comma. The default is none. When setting this value, carefully consider the type of information you are passing in during deployment. By logging information about the request or response, you could potentially expose sensitive data that is retrieved through the deployment operations.

## Dependency
### Properties
* **dependsOn**: [BasicDependency](#basicdependency)[]: The list of dependencies.
* **id**: string: The ID of the dependency.
* **resourceName**: string: The dependency resource name.
* **resourceType**: string: The dependency resource type.

## Deployment
### Properties
* **location**: string: The location to store the deployment data.
* **properties**: [DeploymentProperties](#deploymentproperties) (Required): The deployment properties.
* **tags**: [DeploymentTags](#deploymenttags): Deployment tags

## DeploymentExportResult
### Properties
* **template**: any: The template content.

## DeploymentProperties
### Properties
* **debugSetting**: [DebugSetting](#debugsetting): The debug setting of the deployment.
* **mode**: 'Complete' | 'Incremental' (Required): The mode that is used to deploy resources. This value can be either Incremental or Complete. In Incremental mode, resources are deployed without deleting existing resources that are not included in the template. In Complete mode, resources are deployed and existing resources in the resource group that are not included in the template are deleted. Be careful when using Complete mode as you may unintentionally delete resources.
* **onErrorDeployment**: [OnErrorDeployment](#onerrordeployment): The deployment on error behavior.
* **parameters**: any: Name and value pairs that define the deployment parameters for the template. You use this element when you want to provide the parameter values directly in the request rather than link to an existing parameter file. Use either the parametersLink property or the parameters property, but not both. It can be a JObject or a well formed JSON string.
* **parametersLink**: [ParametersLink](#parameterslink): The URI of parameters file. You use this element to link to an existing parameters file. Use either the parametersLink property or the parameters property, but not both.
* **template**: any: The template content. You use this element when you want to pass the template syntax directly in the request rather than link to an existing template. It can be a JObject or well-formed JSON string. Use either the templateLink property or the template property, but not both.
* **templateLink**: [TemplateLink](#templatelink): The URI of the template. Use either the templateLink property or the template property, but not both.

## DeploymentPropertiesExtended
### Properties
* **correlationId**: string (ReadOnly): The correlation ID of the deployment.
* **debugSetting**: [DebugSetting](#debugsetting) (ReadOnly): The debug setting of the deployment.
* **dependencies**: [Dependency](#dependency)[] (ReadOnly): The list of deployment dependencies.
* **duration**: string (ReadOnly): The duration of the template deployment.
* **error**: [ErrorResponse](#errorresponse) (ReadOnly): The deployment error.
* **mode**: 'Complete' | 'Incremental' (ReadOnly): The deployment mode. Possible values are Incremental and Complete.
* **onErrorDeployment**: [OnErrorDeploymentExtended](#onerrordeploymentextended) (ReadOnly): The deployment on error behavior.
* **outputResources**: [ResourceReference](#resourcereference)[] (ReadOnly): Array of provisioned resources.
* **outputs**: any (ReadOnly): Key/value pairs that represent deployment output.
* **parameters**: any (ReadOnly): Deployment parameters.
* **parametersLink**: [ParametersLink](#parameterslink) (ReadOnly): The URI referencing the parameters.
* **providers**: [Provider](#provider)[] (ReadOnly): The list of resource providers needed for the deployment.
* **provisioningState**: string (ReadOnly): The state of the provisioning.
* **templateHash**: string (ReadOnly): The hash produced for the template.
* **templateLink**: [TemplateLink](#templatelink) (ReadOnly): The URI referencing the template.
* **timestamp**: string (ReadOnly): The timestamp of the template deployment.
* **validatedResources**: [ResourceReference](#resourcereference)[] (ReadOnly): Array of validated resources.

## DeploymentPropertiesOrDeploymentPropertiesExtended
### Properties
* **correlationId**: string (ReadOnly): The correlation ID of the deployment.
* **debugSetting**: [DebugSetting](#debugsetting): The debug setting of the deployment.
* **dependencies**: [Dependency](#dependency)[] (ReadOnly): The list of deployment dependencies.
* **duration**: string (ReadOnly): The duration of the template deployment.
* **error**: [ErrorResponse](#errorresponse) (ReadOnly): The deployment error.
* **mode**: 'Complete' | 'Incremental' (Required): The mode that is used to deploy resources. This value can be either Incremental or Complete. In Incremental mode, resources are deployed without deleting existing resources that are not included in the template. In Complete mode, resources are deployed and existing resources in the resource group that are not included in the template are deleted. Be careful when using Complete mode as you may unintentionally delete resources.
* **onErrorDeployment**: [OnErrorDeploymentOrOnErrorDeploymentExtended](#onerrordeploymentoronerrordeploymentextended): The deployment on error behavior.
* **outputResources**: [ResourceReference](#resourcereference)[] (ReadOnly): Array of provisioned resources.
* **outputs**: any (ReadOnly): Key/value pairs that represent deployment output.
* **parameters**: any: Name and value pairs that define the deployment parameters for the template. You use this element when you want to provide the parameter values directly in the request rather than link to an existing parameter file. Use either the parametersLink property or the parameters property, but not both. It can be a JObject or a well formed JSON string.
* **parametersLink**: [ParametersLink](#parameterslink): The URI of parameters file. You use this element to link to an existing parameters file. Use either the parametersLink property or the parameters property, but not both.
* **providers**: [Provider](#provider)[] (ReadOnly): The list of resource providers needed for the deployment.
* **provisioningState**: string (ReadOnly): The state of the provisioning.
* **template**: any (WriteOnly): The template content. You use this element when you want to pass the template syntax directly in the request rather than link to an existing template. It can be a JObject or well-formed JSON string. Use either the templateLink property or the template property, but not both.
* **templateHash**: string (ReadOnly): The hash produced for the template.
* **templateLink**: [TemplateLink](#templatelink): The URI of the template. Use either the templateLink property or the template property, but not both.
* **timestamp**: string (ReadOnly): The timestamp of the template deployment.
* **validatedResources**: [ResourceReference](#resourcereference)[] (ReadOnly): Array of validated resources.

## DeploymentTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DeploymentTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DeploymentValidateResult
### Properties
* **error**: [ErrorResponse](#errorresponse) (ReadOnly): The deployment validation error.
* **properties**: [DeploymentPropertiesExtended](#deploymentpropertiesextended): The template deployment properties.

## DeploymentWhatIfProperties
### Properties
* **debugSetting**: [DebugSetting](#debugsetting): The debug setting of the deployment.
* **mode**: 'Complete' | 'Incremental' (Required): The mode that is used to deploy resources. This value can be either Incremental or Complete. In Incremental mode, resources are deployed without deleting existing resources that are not included in the template. In Complete mode, resources are deployed and existing resources in the resource group that are not included in the template are deleted. Be careful when using Complete mode as you may unintentionally delete resources.
* **onErrorDeployment**: [OnErrorDeployment](#onerrordeployment): The deployment on error behavior.
* **parameters**: any: Name and value pairs that define the deployment parameters for the template. You use this element when you want to provide the parameter values directly in the request rather than link to an existing parameter file. Use either the parametersLink property or the parameters property, but not both. It can be a JObject or a well formed JSON string.
* **parametersLink**: [ParametersLink](#parameterslink): The URI of parameters file. You use this element to link to an existing parameters file. Use either the parametersLink property or the parameters property, but not both.
* **template**: any: The template content. You use this element when you want to pass the template syntax directly in the request rather than link to an existing template. It can be a JObject or well-formed JSON string. Use either the templateLink property or the template property, but not both.
* **templateLink**: [TemplateLink](#templatelink): The URI of the template. Use either the templateLink property or the template property, but not both.
* **whatIfSettings**: [DeploymentWhatIfSettings](#deploymentwhatifsettings): Optional What-If operation settings.

## DeploymentWhatIfSettings
### Properties
* **resultFormat**: 'FullResourcePayloads' | 'ResourceIdOnly': The format of the What-If results

## ErrorAdditionalInfo
### Properties
* **info**: any (ReadOnly): The additional info.
* **type**: string (ReadOnly): The additional info type.

## ErrorResponse
### Properties
* **additionalInfo**: [ErrorAdditionalInfo](#erroradditionalinfo)[] (ReadOnly): The error additional info.
* **code**: string (ReadOnly): The error code.
* **details**: [ErrorResponse](#errorresponse)[] (ReadOnly): The error details.
* **message**: string (ReadOnly): The error message.
* **target**: string (ReadOnly): The error target.

## OnErrorDeployment
### Properties
* **deploymentName**: string: The deployment to be used on error case.
* **type**: 'LastSuccessful' | 'SpecificDeployment': The deployment on error behavior type. Possible values are LastSuccessful and SpecificDeployment.

## OnErrorDeploymentExtended
### Properties
* **deploymentName**: string: The deployment to be used on error case.
* **provisioningState**: string (ReadOnly): The state of the provisioning for the on error deployment.
* **type**: 'LastSuccessful' | 'SpecificDeployment': The deployment on error behavior type. Possible values are LastSuccessful and SpecificDeployment.

## OnErrorDeploymentOrOnErrorDeploymentExtended
### Properties
* **deploymentName**: string: The deployment to be used on error case.
* **provisioningState**: string (ReadOnly): The state of the provisioning for the on error deployment.
* **type**: 'LastSuccessful' | 'SpecificDeployment': The deployment on error behavior type. Possible values are LastSuccessful and SpecificDeployment.

## ParametersLink
### Properties
* **contentVersion**: string: If included, must match the ContentVersion in the template.
* **uri**: string (Required): The URI of the parameters file.

## Provider
### Properties
* **id**: string (ReadOnly): The provider ID.
* **namespace**: string: The namespace of the resource provider.
* **registrationPolicy**: string (ReadOnly): The registration policy of the resource provider.
* **registrationState**: string (ReadOnly): The registration state of the resource provider.
* **resourceTypes**: [ProviderResourceType](#providerresourcetype)[] (ReadOnly): The collection of provider resource types.

## ProviderResourceType
### Properties
* **aliases**: [Alias](#alias)[]: The aliases that are supported by this resource type.
* **apiVersions**: string[]: The API version.
* **capabilities**: string: The additional capabilities offered by this resource type.
* **locations**: string[]: The collection of locations where this resource type can be created.
* **properties**: [ProviderResourceTypeProperties](#providerresourcetypeproperties): The properties.
* **resourceType**: string: The resource type.
* **zoneMappings**: [ZoneMapping](#zonemapping)[]

## ProviderResourceTypeProperties
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceGroupProperties
### Properties
* **provisioningState**: string (ReadOnly): The provisioning state.

## ResourceGroupTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceReference
### Properties
* **id**: string (ReadOnly): The fully qualified resource Id.

## ScopedDeploymentWhatIf
### Properties
* **location**: string (Required): The location to store the deployment data.
* **properties**: [DeploymentWhatIfProperties](#deploymentwhatifproperties) (Required): The deployment properties.

## Tags
### Properties
* **tags**: [Tags](#tags): Dictionary of <string>

## Tags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TemplateLink
### Properties
* **contentVersion**: string: If included, must match the ContentVersion in the template.
* **uri**: string (Required): The URI of the template to deploy.

## WhatIfChange
### Properties
* **after**: any: The predicted snapshot of the resource after the deployment is executed.
* **before**: any: The snapshot of the resource before the deployment is executed.
* **changeType**: 'Create' | 'Delete' | 'Deploy' | 'Ignore' | 'Modify' | 'NoChange' (Required): Type of change that will be made to the resource when the deployment is executed.
* **delta**: [WhatIfPropertyChange](#whatifpropertychange)[]: The predicted changes to resource properties.
* **resourceId**: string (Required): Resource ID

## WhatIfOperationProperties
### Properties
* **changes**: [WhatIfChange](#whatifchange)[]: List of resource changes predicted by What-If operation.

## WhatIfOperationResult
### Properties
* **error**: [ErrorResponse](#errorresponse): Error when What-If operation fails.
* **properties**: [WhatIfOperationProperties](#whatifoperationproperties): What-If operation properties.
* **status**: string: Status of the What-If operation.

## WhatIfPropertyChange
### Properties
* **after**: any: The value of the property after the deployment is executed.
* **before**: any: The value of the property before the deployment is executed.
* **children**: [WhatIfPropertyChange](#whatifpropertychange)[]: Nested property changes.
* **path**: string (Required): The path of the property.
* **propertyChangeType**: 'Array' | 'Create' | 'Delete' | 'Modify' (Required): The type of property change.

## ZoneMapping
### Properties
* **location**: string: The location of the zone mapping.
* **zones**: string[]

