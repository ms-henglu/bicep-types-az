# Microsoft.Security @ 2020-07-01-preview

## Resource Microsoft.Security/sqlVulnerabilityAssessments/baselineRules@2020-07-01-preview
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2020-07-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **latestScan**: bool (WriteOnly): Take results from latest scan.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [RuleResultsProperties](#ruleresultsproperties) (ReadOnly): Rule results properties.
* **results**: string[][] (WriteOnly): Expected results to be inserted into the baseline.
Leave this field empty it LatestScan == true.
* **type**: 'Microsoft.Security/sqlVulnerabilityAssessments/baselineRules' (ReadOnly, DeployTimeConstant): The resource type

## Function baselineRules (Microsoft.Security/sqlVulnerabilityAssessments@2020-07-01-preview)
* **Resource**: Microsoft.Security/sqlVulnerabilityAssessments
* **ApiVersion**: 2020-07-01-preview
* **Input**: [RulesResultsInput](#rulesresultsinput)
* **Output**: [RulesResults](#rulesresults)

## RuleResults
### Properties
* **id**: string (ReadOnly): Resource Id
* **name**: string (ReadOnly): Resource name
* **properties**: [RuleResultsProperties](#ruleresultsproperties): Rule results properties.
* **type**: string (ReadOnly): Resource type

## RuleResultsProperties
### Properties
* **results**: string[][]: Expected results in the baseline.

## RulesResults
### Properties
* **value**: [RuleResults](#ruleresults)[]: List of rule results.

## RulesResultsInput
### Properties
* **latestScan**: bool: Take results from latest scan.
* **results**: [RulesResultsInputResults](#rulesresultsinputresults): Expected results to be inserted into the baseline.
Leave this field empty it LatestScan == true.

## RulesResultsInputResults
### Properties
### Additional Properties
* **Additional Properties Type**: string[][]

