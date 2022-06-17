# Microsoft.Web @ 2016-03-01

## Resource Microsoft.Web/certificates@2016-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateProperties](#certificateproperties): Certificate resource specific properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.Web/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/publishingUsers@2016-03-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2016-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **name**: 'web' (Required, DeployTimeConstant): The resource name
* **properties**: [UserProperties](#userproperties): User resource specific properties
* **type**: 'Microsoft.Web/publishingUsers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/sourcecontrols@2016-03-01
* **Valid Scope(s)**: Tenant
### Properties
* **apiVersion**: '2016-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SourceControlProperties](#sourcecontrolproperties): SourceControl resource specific properties
* **type**: 'Microsoft.Web/sourcecontrols' (ReadOnly, DeployTimeConstant): The resource type

## Function execute (Microsoft.Web/sites/diagnostics/analyses@2016-03-01)
* **Resource**: Microsoft.Web/sites/diagnostics/analyses
* **ApiVersion**: 2016-03-01
* **Output**: [DiagnosticAnalysis](#diagnosticanalysis)

## Function execute (Microsoft.Web/sites/diagnostics/detectors@2016-03-01)
* **Resource**: Microsoft.Web/sites/diagnostics/detectors
* **ApiVersion**: 2016-03-01
* **Output**: [DiagnosticDetectorResponse](#diagnosticdetectorresponse)

## Function execute (Microsoft.Web/sites/slots/diagnostics/analyses@2016-03-01)
* **Resource**: Microsoft.Web/sites/slots/diagnostics/analyses
* **ApiVersion**: 2016-03-01
* **Output**: [DiagnosticAnalysis](#diagnosticanalysis)

## Function execute (Microsoft.Web/sites/slots/diagnostics/detectors@2016-03-01)
* **Resource**: Microsoft.Web/sites/slots/diagnostics/detectors
* **ApiVersion**: 2016-03-01
* **Output**: [DiagnosticDetectorResponse](#diagnosticdetectorresponse)

## AbnormalTimePeriod
### Properties
* **endTime**: string: End time of the downtime
* **events**: [DetectorAbnormalTimePeriod](#detectorabnormaltimeperiod)[]: List of Possible Cause of downtime
* **solutions**: [Solution](#solution)[]: List of proposed solutions
* **startTime**: string: Start time of the downtime

## AnalysisData
### Properties
* **data**: [NameValuePair](#namevaluepair)[][]: Additional Source Data
* **detectorDefinition**: [DetectorDefinition](#detectordefinition): Detector Definition
* **detectorMetaData**: [ResponseMetaData](#responsemetadata): Detector Meta Data
* **metrics**: [DiagnosticMetricSet](#diagnosticmetricset)[]: Source Metrics
* **source**: string: Name of the Detector

## CertificateProperties
### Properties
* **cerBlob**: any (ReadOnly): Raw bytes of .cer file
* **expirationDate**: string (ReadOnly): Certificate expiration date.
* **friendlyName**: string (ReadOnly): Friendly name of the certificate.
* **geoRegion**: string (ReadOnly): Region of the certificate.
* **hostingEnvironmentProfile**: [HostingEnvironmentProfile](#hostingenvironmentprofile) (ReadOnly): Specification for the App Service Environment to use for the certificate.
* **hostNames**: string[]: Host names the certificate applies to.
* **issueDate**: string (ReadOnly): Certificate issue Date.
* **issuer**: string (ReadOnly): Certificate issuer.
* **keyVaultId**: string: Key Vault Csm resource Id.
* **keyVaultSecretName**: string: Key Vault secret name.
* **keyVaultSecretStatus**: 'AzureServiceUnauthorizedToAccessKeyVault' | 'CertificateOrderFailed' | 'ExternalPrivateKey' | 'Initialized' | 'KeyVaultDoesNotExist' | 'KeyVaultSecretDoesNotExist' | 'OperationNotPermittedOnKeyVault' | 'Succeeded' | 'Unknown' | 'UnknownError' | 'WaitingOnCertificateOrder' (ReadOnly): Status of the Key Vault secret.
* **password**: string (Required, WriteOnly): Certificate password.
* **pfxBlob**: any: Pfx blob.
* **publicKeyHash**: string (ReadOnly): Public key hash.
* **selfLink**: string (ReadOnly): Self link.
* **serverFarmId**: string: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".
* **siteName**: string (ReadOnly): App name.
* **subjectName**: string (ReadOnly): Subject name of the certificate.
* **thumbprint**: string (ReadOnly): Certificate thumbprint.
* **valid**: bool (ReadOnly): Is the certificate valid?.

## DataSource
### Properties
* **dataSourceUri**: [NameValuePair](#namevaluepair)[]: Datasource Uri Links
* **instructions**: string[]: Instructions if any for the data source

## DetectorAbnormalTimePeriod
### Properties
* **endTime**: string: End time of the correlated event
* **message**: string: Message describing the event
* **metaData**: [NameValuePair](#namevaluepair)[][]: Downtime metadata
* **priority**: int: Represents the rank of the Detector
* **solutions**: [Solution](#solution)[]: List of proposed solutions
* **source**: string: Represents the name of the Detector
* **startTime**: string: Start time of the correlated event
* **type**: 'AppCrash' | 'AppDeployment' | 'AseDeployment' | 'Other' | 'PlatformIssue' | 'RuntimeIssueDetected' | 'ServiceIncident' | 'UserIssue': Represents the type of the Detector

## DetectorDefinition
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [DetectorDefinitionProperties](#detectordefinitionproperties): DetectorDefinition resource specific properties
* **type**: string (ReadOnly): Resource type.

## DetectorDefinitionProperties
### Properties
* **description**: string (ReadOnly): Description of the detector
* **displayName**: string (ReadOnly): Display name of the detector
* **isEnabled**: bool (ReadOnly): Flag representing whether detector is enabled or not.
* **rank**: int (ReadOnly): Detector Rank

## DiagnosticAnalysis
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [DiagnosticAnalysisProperties](#diagnosticanalysisproperties): DiagnosticAnalysis resource specific properties
* **type**: string (ReadOnly): Resource type.

## DiagnosticAnalysis
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [DiagnosticAnalysisProperties](#diagnosticanalysisproperties): DiagnosticAnalysis resource specific properties
* **type**: string (ReadOnly): Resource type.

## DiagnosticAnalysisProperties
### Properties
* **abnormalTimePeriods**: [AbnormalTimePeriod](#abnormaltimeperiod)[]: List of time periods.
* **endTime**: string: End time of the period
* **nonCorrelatedDetectors**: [DetectorDefinition](#detectordefinition)[]: Data by each detector for detectors that did not corelate
* **payload**: [AnalysisData](#analysisdata)[]: Data by each detector
* **startTime**: string: Start time of the period

## DiagnosticDetectorResponse
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [DiagnosticDetectorResponseProperties](#diagnosticdetectorresponseproperties): DiagnosticDetectorResponse resource specific properties
* **type**: string (ReadOnly): Resource type.

## DiagnosticDetectorResponse
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [DiagnosticDetectorResponseProperties](#diagnosticdetectorresponseproperties): DiagnosticDetectorResponse resource specific properties
* **type**: string (ReadOnly): Resource type.

## DiagnosticDetectorResponseProperties
### Properties
* **abnormalTimePeriods**: [DetectorAbnormalTimePeriod](#detectorabnormaltimeperiod)[]: List of Correlated events found by the detector
* **data**: [NameValuePair](#namevaluepair)[][]: Additional Data that detector wants to send.
* **detectorDefinition**: [DetectorDefinition](#detectordefinition): Detector's definition
* **endTime**: string: End time of the period
* **issueDetected**: bool: Flag representing Issue was detected.
* **metrics**: [DiagnosticMetricSet](#diagnosticmetricset)[]: Metrics provided by the detector
* **responseMetaData**: [ResponseMetaData](#responsemetadata): Meta Data
* **startTime**: string: Start time of the period

## DiagnosticMetricSample
### Properties
* **isAggregated**: bool: Whether the values are aggregates across all workers or not
* **maximum**: int: Maximum of the metric sampled during the time period
* **minimum**: int: Minimum of the metric sampled during the time period
* **roleInstance**: string: Role Instance. Null if this counter is not per instance 
This is returned and should be whichever instance name we desire to be returned
i.e. CPU and Memory return RDWORKERNAME (LargeDed..._IN_0) 
where RDWORKERNAME is Machine name below and RoleInstance name in parenthesis
* **timestamp**: string: Time at which metric is measured
* **total**: int: Total value of the metric. If multiple measurements are made this will have sum of all.

## DiagnosticMetricSet
### Properties
* **endTime**: string: End time of the period
* **name**: string: Name of the metric
* **startTime**: string: Start time of the period
* **timeGrain**: string: Presented time grain. Supported grains at the moment are PT1M, PT1H, P1D
* **unit**: string: Metric's unit
* **values**: [DiagnosticMetricSample](#diagnosticmetricsample)[]: Collection of metric values for the selected period based on the {Microsoft.Web.Hosting.Administration.DiagnosticMetricSet.TimeGrain}

## HostingEnvironmentProfile
### Properties
* **id**: string: Resource ID of the App Service Environment.
* **name**: string (ReadOnly): Name of the App Service Environment.
* **type**: string (ReadOnly): Resource type of the App Service Environment.

## NameValuePair
### Properties
* **name**: string: Pair name.
* **value**: string: Pair value.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResponseMetaData
### Properties
* **dataSource**: [DataSource](#datasource): Source of the Data

## Solution
### Properties
* **data**: [NameValuePair](#namevaluepair)[][]: Solution Data.
* **description**: string: Description of the solution
* **displayName**: string: Display Name of the solution
* **id**: int: Solution Id.
* **metadata**: [NameValuePair](#namevaluepair)[][]: Solution Metadata.
* **order**: int: Order of the solution.
* **type**: 'BestPractices' | 'DeepInvestigation' | 'QuickSolution': Type of Solution

## SourceControlProperties
### Properties
* **expirationTime**: string: OAuth token expiration.
* **name**: string: Name or source control type.
* **refreshToken**: string: OAuth refresh token.
* **token**: string: OAuth access token.
* **tokenSecret**: string: OAuth access token secret.

## UserProperties
### Properties
* **name**: string: Username
* **publishingPassword**: string: Password used for publishing.
* **publishingPasswordHash**: string: Password hash used for publishing.
* **publishingPasswordHashSalt**: string: Password hash salt used for publishing.
* **publishingUserName**: string (Required): Username used for publishing.

