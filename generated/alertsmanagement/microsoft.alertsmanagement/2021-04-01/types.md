# microsoft.alertsManagement @ 2021-04-01

## Resource microsoft.alertsManagement/smartDetectorAlertRules@2021-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AlertRuleProperties](#alertruleproperties): The alert rule properties.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): The resource tags.
* **type**: 'microsoft.alertsManagement/smartDetectorAlertRules' (ReadOnly, DeployTimeConstant): The resource type

## AlertRuleProperties
### Properties
* **actionGroups**: [ActionGroupsInformation](#actiongroupsinformation) (Required): The Action Groups information, used by the alert rule.
* **description**: string: The alert rule description.
* **detector**: [Detector](#detector) (Required): The detector information. By default this is not populated, unless it's specified in expandDetector
* **frequency**: string (Required): The alert rule frequency in ISO8601 format. The time granularity must be in minutes and minimum value is 1 minute, depending on the detector.
* **scope**: string[] (Required): The alert rule resources scope.
* **severity**: 'Sev0' | 'Sev1' | 'Sev2' | 'Sev3' | 'Sev4' (Required): The alert rule severity.
* **state**: 'Disabled' | 'Enabled' (Required): The alert rule state.
* **throttling**: [ThrottlingInformation](#throttlinginformation): Optional throttling information for the alert rule.

## ActionGroupsInformation
### Properties
* **customEmailSubject**: string: An optional custom email subject to use in email notifications.
* **customWebhookPayload**: string: An optional custom web-hook payload to use in web-hook notifications.
* **groupIds**: string[] (Required): The Action Group resource IDs.

## Detector
### Properties
* **description**: string (ReadOnly): The Smart Detector description.
* **id**: string (Required): The detector id.
* **imagePaths**: string[] (ReadOnly): The Smart Detector image path. By default this is not populated, unless it's specified in expandDetector
* **name**: string (ReadOnly): The Smart Detector name.
* **parameterDefinitions**: [DetectorParameterDefinition](#detectorparameterdefinition)[] (ReadOnly): The Smart Detector parameters definitions.'
* **parameters**: [Dictionary<string,Object>](#dictionarystringobject): The detector's parameters.'
* **supportedCadences**: int[] (ReadOnly): The Smart Detector supported cadences.
* **supportedResourceTypes**: string[] (ReadOnly): The Smart Detector supported resource types.

## DetectorParameterDefinition
### Properties
* **description**: string: The detector parameter description.
* **displayName**: string: The detector parameter display name.
* **isMandatory**: bool: A value indicating whether this detector parameter is mandatory.
* **name**: string: The detector parameter name.
* **type**: 'Boolean' | 'DateTime' | 'Double' | 'Integer' | 'String': The detector parameter type.

## Dictionary<string,Object>
### Properties
### Additional Properties
* **Additional Properties Type**: any

## ThrottlingInformation
### Properties
* **duration**: string: The required duration (in ISO8601 format) to wait before notifying on the alert rule again. The time granularity must be in minutes and minimum value is 0 minutes

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
