# Microsoft.Web @ 2016-09-01

## Resource Microsoft.Web/hostingEnvironments@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServiceEnvironment](#appserviceenvironment): Core resource properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.Web/hostingEnvironments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/hostingEnvironments/multiRolePools@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [WorkerPool](#workerpool): Core resource properties
* **sku**: [SkuDescription](#skudescription): Description of a SKU for a scalable resource.
* **type**: 'Microsoft.Web/hostingEnvironments/multiRolePools' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/hostingEnvironments/workerPools@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [WorkerPool](#workerpool): Core resource properties
* **sku**: [SkuDescription](#skudescription): Description of a SKU for a scalable resource.
* **type**: 'Microsoft.Web/hostingEnvironments/workerPools' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/serverfarms@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppServicePlanProperties](#appserviceplanproperties): AppServicePlan resource specific properties
* **sku**: [SkuDescription](#skudescription): Description of a SKU for a scalable resource.
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.Web/serverfarms' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/serverfarms/virtualNetworkConnections/gateways@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string: Kind of resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VnetGatewayProperties](#vnetgatewayproperties): VnetGateway resource specific properties
* **type**: 'Microsoft.Web/serverfarms/virtualNetworkConnections/gateways' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Web/serverfarms/virtualNetworkConnections/routes@2016-09-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-09-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: string (WriteOnly): Kind of resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VnetRouteProperties](#vnetrouteproperties) (WriteOnly): VnetRoute resource specific properties
* **type**: 'Microsoft.Web/serverfarms/virtualNetworkConnections/routes' (ReadOnly, DeployTimeConstant): The resource type

## Function listKeys (Microsoft.Web/serverfarms/hybridConnectionNamespaces/relays@2016-09-01)
* **Resource**: Microsoft.Web/serverfarms/hybridConnectionNamespaces/relays
* **ApiVersion**: 2016-09-01
* **Output**: [HybridConnectionKey](#hybridconnectionkey)

## Function resume (Microsoft.Web/hostingEnvironments@2016-09-01)
* **Resource**: Microsoft.Web/hostingEnvironments
* **ApiVersion**: 2016-09-01
* **Output**: [WebAppCollection](#webappcollection)

## Function suspend (Microsoft.Web/hostingEnvironments@2016-09-01)
* **Resource**: Microsoft.Web/hostingEnvironments
* **ApiVersion**: 2016-09-01
* **Output**: [WebAppCollection](#webappcollection)

## ApiDefinitionInfo
### Properties
* **url**: string: The URL of the API definition.

## AppServiceEnvironment
### Properties
* **allowedMultiSizes**: string (ReadOnly): List of comma separated strings describing which VM sizes are allowed for front-ends.
* **allowedWorkerSizes**: string (ReadOnly): List of comma separated strings describing which VM sizes are allowed for workers.
* **apiManagementAccountId**: string: API Management Account associated with the App Service Environment.
* **clusterSettings**: [NameValuePair](#namevaluepair)[]: Custom settings for changing the behavior of the App Service Environment.
* **databaseEdition**: string (ReadOnly): Edition of the metadata database for the App Service Environment, e.g. "Standard".
* **databaseServiceObjective**: string (ReadOnly): Service objective of the metadata database for the App Service Environment, e.g. "S0".
* **defaultFrontEndScaleFactor**: int (ReadOnly): Default Scale Factor for FrontEnds.
* **dnsSuffix**: string: DNS suffix of the App Service Environment.
* **dynamicCacheEnabled**: bool: True/false indicating whether the App Service Environment is suspended. The environment can be suspended e.g. when the management endpoint is no longer available
(most likely because NSG blocked the incoming traffic).
* **environmentCapacities**: [StampCapacity](#stampcapacity)[] (ReadOnly): Current total, used, and available worker capacities.
* **environmentIsHealthy**: bool (ReadOnly): True/false indicating whether the App Service Environment is healthy.
* **environmentStatus**: string (ReadOnly): Detailed message about with results of the last check of the App Service Environment.
* **frontEndScaleFactor**: int: Scale factor for front-ends.
* **internalLoadBalancingMode**: 'None' | 'Publishing' | 'Web': Specifies which endpoints to serve internally in the Virtual Network for the App Service Environment.
* **ipsslAddressCount**: int: Number of IP SSL addresses reserved for the App Service Environment.
* **lastAction**: string (ReadOnly): Last deployment action on the App Service Environment.
* **lastActionResult**: string (ReadOnly): Result of the last deployment action on the App Service Environment.
* **location**: string (Required): Location of the App Service Environment, e.g. "West US".
* **maximumNumberOfMachines**: int (ReadOnly): Maximum number of VMs in the App Service Environment.
* **multiRoleCount**: int: Number of front-end instances.
* **multiSize**: string: Front-end VM size, e.g. "Medium", "Large".
* **name**: string (Required): Name of the App Service Environment.
* **networkAccessControlList**: [NetworkAccessControlEntry](#networkaccesscontrolentry)[]: Access control list for controlling traffic to the App Service Environment.
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded' (ReadOnly): Provisioning state of the App Service Environment.
* **resourceGroup**: string (ReadOnly): Resource group of the App Service Environment.
* **status**: 'Deleting' | 'Preparing' | 'Ready' | 'Scaling' (ReadOnly): Current status of the App Service Environment.
* **subscriptionId**: string (ReadOnly): Subscription of the App Service Environment.
* **suspended**: bool: <code>true</code> if the App Service Environment is suspended; otherwise, <code>false</code>. The environment can be suspended, e.g. when the management endpoint is no longer available
 (most likely because NSG blocked the incoming traffic).
* **upgradeDomains**: int (ReadOnly): Number of upgrade domains of the App Service Environment.
* **userWhitelistedIpRanges**: string[]: User added ip ranges to whitelist on ASE db
* **vipMappings**: [VirtualIPMapping](#virtualipmapping)[] (ReadOnly): Description of IP SSL mapping for the App Service Environment.
* **virtualNetwork**: [VirtualNetworkProfile](#virtualnetworkprofile) (Required): Description of the Virtual Network.
* **vnetName**: string: Name of the Virtual Network for the App Service Environment.
* **vnetResourceGroupName**: string: Resource group of the Virtual Network.
* **vnetSubnetName**: string: Subnet of the Virtual Network.
* **workerPools**: [WorkerPool](#workerpool)[] (Required): Description of worker pools with worker size IDs, VM sizes, and number of workers in each pool.

## AppServicePlanProperties
### Properties
* **adminSiteName**: string: App Service plan administration site.
* **geoRegion**: string (ReadOnly): Geographical location for the App Service plan.
* **hostingEnvironmentProfile**: [HostingEnvironmentProfile](#hostingenvironmentprofile): Specification for the App Service Environment to use for the App Service plan.
* **isSpot**: bool: If <code>true</code>, this App Service Plan owns spot instances.
* **maximumNumberOfWorkers**: int (ReadOnly): Maximum number of instances that can be assigned to this App Service plan.
* **name**: string (Required): Name for the App Service plan.
* **numberOfSites**: int (ReadOnly): Number of apps assigned to this App Service plan.
* **perSiteScaling**: bool: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.
If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.
* **provisioningState**: 'Canceled' | 'Deleting' | 'Failed' | 'InProgress' | 'Succeeded' (ReadOnly): Provisioning state of the App Service Environment.
* **reserved**: bool: If Linux app service plan <code>true</code>, <code>false</code> otherwise.
* **resourceGroup**: string (ReadOnly): Resource group of the App Service plan.
* **spotExpirationTime**: string: The time when the server farm expires. Valid only if it is a spot server farm.
* **status**: 'Creating' | 'Pending' | 'Ready' (ReadOnly): App Service plan status.
* **subscription**: string (ReadOnly): App Service plan subscription.
* **targetWorkerCount**: int: Scaling worker count.
* **targetWorkerSizeId**: int: Scaling worker size ID.
* **workerTierName**: string: Target worker tier assigned to the App Service plan.

## AutoHealActions
### Properties
* **actionType**: 'CustomAction' | 'LogEvent' | 'Recycle': Predefined action to be taken.
* **customAction**: [AutoHealCustomAction](#autohealcustomaction): Custom action to be taken.
* **minProcessExecutionTime**: string: Minimum time the process must execute
before taking the action

## AutoHealCustomAction
### Properties
* **exe**: string: Executable to be run.
* **parameters**: string: Parameters for the executable.

## AutoHealRules
### Properties
* **actions**: [AutoHealActions](#autohealactions): Actions to be executed when a rule is triggered.
* **triggers**: [AutoHealTriggers](#autohealtriggers): Conditions that describe when to execute the auto-heal actions.

## AutoHealTriggers
### Properties
* **privateBytesInKB**: int: A rule based on private bytes.
* **requests**: [RequestsBasedTrigger](#requestsbasedtrigger): A rule based on total requests.
* **slowRequests**: [SlowRequestsBasedTrigger](#slowrequestsbasedtrigger): A rule based on request execution time.
* **statusCodes**: [StatusCodesBasedTrigger](#statuscodesbasedtrigger)[]: A rule based on status codes.

## Capability
### Properties
* **name**: string: Name of the SKU capability.
* **reason**: string: Reason of the SKU capability.
* **value**: string: Value of the SKU capability.

## CloningInfo
### Properties
* **appSettingsOverrides**: [CloningInfoAppSettingsOverrides](#cloninginfoappsettingsoverrides): Application setting overrides for cloned app. If specified, these settings override the settings cloned 
from source app. Otherwise, application settings from source app are retained.
* **cloneCustomHostNames**: bool: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.
* **cloneSourceControl**: bool: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.
* **configureLoadBalancing**: bool: <code>true</code> to configure load balancing for source and destination app.
* **correlationId**: string: Correlation ID of cloning operation. This ID ties multiple cloning operations
together to use the same snapshot.
* **hostingEnvironment**: string: App Service Environment.
* **ignoreQuotas**: bool: <code>true</code> if quotas should be ignored; otherwise, <code>false</code>.
* **overwrite**: bool: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.
* **sourceWebAppId**: string (Required): ARM resource ID of the source app. App resource ID is of the form 
/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and 
/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.
* **trafficManagerProfileId**: string: ARM resource ID of the Traffic Manager profile to use, if it exists. Traffic Manager resource ID is of the form 
/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
* **trafficManagerProfileName**: string: Name of Traffic Manager profile to create. This is only needed if Traffic Manager profile does not already exist.

## CloningInfoAppSettingsOverrides
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConnStringInfo
### Properties
* **connectionString**: string: Connection string value.
* **name**: string: Name of connection string.
* **type**: 'ApiHub' | 'Custom' | 'DocDb' | 'EventHub' | 'MySql' | 'NotificationHub' | 'PostgreSQL' | 'RedisCache' | 'SQLAzure' | 'SQLServer' | 'ServiceBus': Type of database.

## CorsSettings
### Properties
* **allowedOrigins**: string[]: Gets or sets the list of origins that should be allowed to make cross-origin
calls (for example: http://example.com:12345). Use "*" to allow all.

## Experiments
### Properties
* **rampUpRules**: [RampUpRule](#rampuprule)[]: List of ramp-up rules.

## HandlerMapping
### Properties
* **arguments**: string: Command-line arguments to be passed to the script processor.
* **extension**: string: Requests with this extension will be handled using the specified FastCGI application.
* **scriptProcessor**: string: The absolute path to the FastCGI application.

## HostingEnvironmentProfile
### Properties
* **id**: string: Resource ID of the App Service Environment.
* **name**: string (ReadOnly): Name of the App Service Environment.
* **type**: string (ReadOnly): Resource type of the App Service Environment.

## HostNameSslState
### Properties
* **hostType**: 'Repository' | 'Standard': Indicates whether the hostname is a standard or repository hostname.
* **name**: string: Hostname.
* **sslState**: 'Disabled' | 'IpBasedEnabled' | 'SniEnabled': SSL type.
* **thumbprint**: string: SSL certificate thumbprint.
* **toUpdate**: bool: Set to <code>true</code> to update existing hostname.
* **virtualIP**: string: Virtual IP address assigned to the hostname if IP based SSL is enabled.

## HybridConnectionKey
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [HybridConnectionKeyProperties](#hybridconnectionkeyproperties): HybridConnectionKey resource specific properties
* **type**: string (ReadOnly): Resource type.

## HybridConnectionKeyProperties
### Properties
* **sendKeyName**: string (ReadOnly): The name of the send key.
* **sendKeyValue**: string (ReadOnly): The value of the send key.

## IpSecurityRestriction
### Properties
* **ipAddress**: string (Required): IP address the security restriction is valid for.
* **subnetMask**: string: Subnet mask for the range of IP addresses the restriction is valid for.

## ManagedServiceIdentity
### Properties
* **principalId**: string (ReadOnly): Principal Id of managed service identity.
* **tenantId**: string (ReadOnly): Tenant of managed service identity.
* **type**: 'SystemAssigned' | string: Type of managed service identity.

## NameValuePair
### Properties
* **name**: string: Pair name.
* **value**: string: Pair value.

## NetworkAccessControlEntry
### Properties
* **action**: 'Deny' | 'Permit': Action object.
* **description**: string: Description of network access control entry.
* **order**: int: Order of precedence.
* **remoteSubnet**: string: Remote subnet.

## PushSettings
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [PushSettingsProperties](#pushsettingsproperties): PushSettings resource specific properties
* **type**: string (ReadOnly): Resource type.

## PushSettingsProperties
### Properties
* **dynamicTagsJson**: string: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.
* **isPushEnabled**: bool (Required): Gets or sets a flag indicating whether the Push endpoint is enabled.
* **tagsRequiringAuth**: string: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.
Tags can consist of alphanumeric characters and the following:
'_', '@', '#', '.', ':', '-'. 
Validation should be performed at the PushRequestHandler.
* **tagWhitelistJson**: string: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.

## RampUpRule
### Properties
* **actionHostName**: string: Hostname of a slot to which the traffic will be redirected if decided to. E.g. myapp-stage.azurewebsites.net.
* **changeDecisionCallbackUrl**: string: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified. See TiPCallback site extension for the scaffold and contracts.
https://www.siteextensions.net/packages/TiPCallback/
* **changeIntervalInMinutes**: int: Specifies interval in minutes to reevaluate ReroutePercentage.
* **changeStep**: int: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches 
<code>MinReroutePercentage</code> or <code>MaxReroutePercentage</code>. Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.
Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.
* **maxReroutePercentage**: int: Specifies upper boundary below which ReroutePercentage will stay.
* **minReroutePercentage**: int: Specifies lower boundary above which ReroutePercentage will stay.
* **name**: string: Name of the routing rule. The recommended name would be to point to the slot which will receive the traffic in the experiment.
* **reroutePercentage**: int: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.

## RequestsBasedTrigger
### Properties
* **count**: int: Request Count.
* **timeInterval**: string: Time interval.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Site
### Properties
* **id**: string (ReadOnly): Resource Id.
* **identity**: [ManagedServiceIdentity](#managedserviceidentity): Managed service identity.
* **kind**: string: Kind of resource.
* **location**: string (Required): Resource Location.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [SiteProperties](#siteproperties): Site resource specific properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: string (ReadOnly): Resource type.

## SiteConfig
### Properties
* **alwaysOn**: bool: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.
* **apiDefinition**: [ApiDefinitionInfo](#apidefinitioninfo): Information about the formal API definition for the app.
* **appCommandLine**: string: App command line to launch.
* **appSettings**: [NameValuePair](#namevaluepair)[]: Application settings.
* **autoHealEnabled**: bool: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.
* **autoHealRules**: [AutoHealRules](#autohealrules): Auto Heal rules.
* **autoSwapSlotName**: string: Auto-swap slot name.
* **connectionStrings**: [ConnStringInfo](#connstringinfo)[]: Connection strings.
* **cors**: [CorsSettings](#corssettings): Cross-Origin Resource Sharing (CORS) settings.
* **defaultDocuments**: string[]: Default documents.
* **detailedErrorLoggingEnabled**: bool: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.
* **documentRoot**: string: Document root.
* **experiments**: [Experiments](#experiments): This is work around for polymorphic types.
* **handlerMappings**: [HandlerMapping](#handlermapping)[]: Handler mappings.
* **http20Enabled**: bool: Http20Enabled: configures a web site to allow clients to connect over http2.0
* **httpLoggingEnabled**: bool: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.
* **ipSecurityRestrictions**: [IpSecurityRestriction](#ipsecurityrestriction)[]: IP security restrictions.
* **javaContainer**: string: Java container.
* **javaContainerVersion**: string: Java container version.
* **javaVersion**: string: Java version.
* **limits**: [SiteLimits](#sitelimits): Site limits.
* **linuxFxVersion**: string: Linux App Framework and version
* **loadBalancing**: 'LeastRequests' | 'LeastResponseTime' | 'RequestHash' | 'WeightedRoundRobin' | 'WeightedTotalTraffic': Site load balancing.
* **localMySqlEnabled**: bool: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.
* **logsDirectorySizeLimit**: int: HTTP logs directory size limit.
* **machineKey**: [SiteMachineKey](#sitemachinekey) (ReadOnly): Site MachineKey.
* **managedPipelineMode**: 'Classic' | 'Integrated': Managed pipeline mode.
* **minTlsVersion**: '1.0' | '1.1' | '1.2' | string: MinTlsVersion: configures the minimum version of TLS required for SSL requests
* **netFrameworkVersion**: string: .NET Framework version.
* **nodeVersion**: string: Version of Node.js.
* **numberOfWorkers**: int: Number of workers.
* **phpVersion**: string: Version of PHP.
* **publishingUsername**: string: Publishing user name.
* **push**: [PushSettings](#pushsettings): Push endpoint settings.
* **pythonVersion**: string: Version of Python.
* **remoteDebuggingEnabled**: bool: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.
* **remoteDebuggingVersion**: string: Remote debugging version.
* **requestTracingEnabled**: bool: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.
* **requestTracingExpirationTime**: string: Request tracing expiration time.
* **scmType**: 'BitbucketGit' | 'BitbucketHg' | 'CodePlexGit' | 'CodePlexHg' | 'Dropbox' | 'ExternalGit' | 'ExternalHg' | 'GitHub' | 'LocalGit' | 'None' | 'OneDrive' | 'Tfs' | 'VSO' | string: SCM type.
* **tracingOptions**: string: Tracing options.
* **use32BitWorkerProcess**: bool: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.
* **virtualApplications**: [VirtualApplication](#virtualapplication)[]: Virtual applications.
* **vnetName**: string: Virtual Network name.
* **webSocketsEnabled**: bool: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.

## SiteLimits
### Properties
* **maxDiskSizeInMb**: int: Maximum allowed disk size usage in MB.
* **maxMemoryInMb**: int: Maximum allowed memory usage in MB.
* **maxPercentageCpu**: int: Maximum allowed CPU usage percentage.

## SiteMachineKey
### Properties
* **decryption**: string: Algorithm used for decryption.
* **decryptionKey**: string: Decryption key.
* **validation**: string: MachineKey validation.
* **validationKey**: string: Validation key.

## SiteProperties
### Properties
* **availabilityState**: 'DisasterRecoveryMode' | 'Limited' | 'Normal' (ReadOnly): Management information availability state for the app.
* **clientAffinityEnabled**: bool: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance. Default is <code>true</code>.
* **clientCertEnabled**: bool: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>. Default is <code>false</code>.
* **cloningInfo**: [CloningInfo](#cloninginfo) (WriteOnly): If specified during app creation, the app is cloned from a source app.
* **containerSize**: int: Size of the function container.
* **dailyMemoryTimeQuota**: int: Maximum allowed daily memory-time quota (applicable on dynamic apps only).
* **defaultHostName**: string (ReadOnly): Default hostname of the app. Read-only.
* **enabled**: bool: <code>true</code> if the app is enabled; otherwise, <code>false</code>. Setting this value to false disables the app (takes the app offline).
* **enabledHostNames**: string[] (ReadOnly): Enabled hostnames for the app.Hostnames need to be assigned (see HostNames) AND enabled. Otherwise,
the app is not served on those hostnames.
* **hostingEnvironmentProfile**: [HostingEnvironmentProfile](#hostingenvironmentprofile): App Service Environment to use for the app.
* **hostNames**: string[] (ReadOnly): Hostnames associated with the app.
* **hostNamesDisabled**: bool: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.
 If <code>true</code>, the app is only accessible via API management process.
* **hostNameSslStates**: [HostNameSslState](#hostnamesslstate)[]: Hostname SSL states are used to manage the SSL bindings for app's hostnames.
* **httpsOnly**: bool: HttpsOnly: configures a web site to accept only https requests. Issues redirect for
http requests
* **isDefaultContainer**: bool (ReadOnly): <code>true</code> if the app is a default container; otherwise, <code>false</code>.
* **lastModifiedTimeUtc**: string (ReadOnly): Last time the app was modified, in UTC. Read-only.
* **maxNumberOfWorkers**: int (ReadOnly): Maximum number of workers.
This only applies to Functions container.
* **outboundIpAddresses**: string (ReadOnly): List of IP addresses that the app uses for outbound connections (e.g. database access). Includes VIPs from tenants that site can be hosted with current settings. Read-only.
* **possibleOutboundIpAddresses**: string (ReadOnly): List of IP addresses that the app uses for outbound connections (e.g. database access). Includes VIPs from all tenants. Read-only.
* **repositorySiteName**: string (ReadOnly): Name of the repository site.
* **reserved**: bool: <code>true</code> if reserved; otherwise, <code>false</code>.
* **resourceGroup**: string (ReadOnly): Name of the resource group the app belongs to. Read-only.
* **scmSiteAlsoStopped**: bool: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>. The default is <code>false</code>.
* **serverFarmId**: string: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".
* **siteConfig**: [SiteConfig](#siteconfig): Configuration of the app.
* **slotSwapStatus**: [SlotSwapStatus](#slotswapstatus) (ReadOnly): Status of the last deployment slot swap operation.
* **snapshotInfo**: [SnapshotRecoveryRequest](#snapshotrecoveryrequest) (WriteOnly): If specified during app creation, the app is created from a previous snapshot.
* **state**: string (ReadOnly): Current state of the app.
* **suspendedTill**: string (ReadOnly): App suspended till in case memory-time quota is exceeded.
* **targetSwapSlot**: string (ReadOnly): Specifies which deployment slot this app will swap into. Read-only.
* **trafficManagerHostNames**: string[] (ReadOnly): Azure Traffic Manager hostnames associated with the app. Read-only.
* **usageState**: 'Exceeded' | 'Normal' (ReadOnly): State indicating whether the app has exceeded its quota usage. Read-only.

## SkuCapacity
### Properties
* **default**: int: Default number of workers for this App Service plan SKU.
* **maximum**: int: Maximum number of workers for this App Service plan SKU.
* **minimum**: int: Minimum number of workers for this App Service plan SKU.
* **scaleType**: string: Available scale configurations for an App Service plan.

## SkuDescription
### Properties
* **capabilities**: [Capability](#capability)[]: Capabilities of the SKU, e.g., is traffic manager enabled?
* **capacity**: int: Current number of instances assigned to the resource.
* **family**: string: Family code of the resource SKU.
* **locations**: string[]: Locations of the SKU.
* **name**: string: Name of the resource SKU.
* **size**: string: Size specifier of the resource SKU.
* **skuCapacity**: [SkuCapacity](#skucapacity): Min, max, and default scale values of the SKU.
* **tier**: string: Service tier of the resource SKU.

## SlotSwapStatus
### Properties
* **destinationSlotName**: string (ReadOnly): The destination slot of the last swap operation.
* **sourceSlotName**: string (ReadOnly): The source slot of the last swap operation.
* **timestampUtc**: string (ReadOnly): The time the last successful slot swap completed.

## SlowRequestsBasedTrigger
### Properties
* **count**: int: Request Count.
* **timeInterval**: string: Time interval.
* **timeTaken**: string: Time taken.

## SnapshotRecoveryRequest
### Properties
* **id**: string (ReadOnly): Resource Id.
* **kind**: string: Kind of resource.
* **name**: string (ReadOnly): Resource Name.
* **properties**: [SnapshotRecoveryRequestProperties](#snapshotrecoveryrequestproperties): SnapshotRecoveryRequest resource specific properties
* **type**: string (ReadOnly): Resource type.

## SnapshotRecoveryRequestProperties
### Properties
* **ignoreConflictingHostNames**: bool: If true, custom hostname conflicts will be ignored when recovering to a target web app.
This setting is only necessary when RecoverConfiguration is enabled.
* **overwrite**: bool (Required): If <code>true</code> the recovery operation can overwrite source app; otherwise, <code>false</code>.
* **recoverConfiguration**: bool: If true, site configuration, in addition to content, will be reverted.
* **recoveryTarget**: [SnapshotRecoveryTarget](#snapshotrecoverytarget): Specifies the web app that snapshot contents will be written to.
* **snapshotTime**: string: Point in time in which the app recovery should be attempted, formatted as a DateTime string.

## SnapshotRecoveryTarget
### Properties
* **id**: string: ARM resource ID of the target app. 
/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and 
/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.
* **location**: string: Geographical location of the target web app, e.g. SouthEastAsia, SouthCentralUS

## StampCapacity
### Properties
* **availableCapacity**: int: Available capacity (# of machines, bytes of storage etc...).
* **computeMode**: 'Dedicated' | 'Dynamic' | 'Shared': Shared/dedicated workers.
* **excludeFromCapacityAllocation**: bool: If <code>true</code>, it includes basic apps.
Basic apps are not used for capacity allocation.
* **isApplicableForAllComputeModes**: bool: <code>true</code> if capacity is applicable for all apps; otherwise, <code>false</code>.
* **name**: string: Name of the stamp.
* **siteMode**: string: Shared or Dedicated.
* **totalCapacity**: int: Total capacity (# of machines, bytes of storage etc...).
* **unit**: string: Name of the unit.
* **workerSize**: 'D1' | 'D2' | 'D3' | 'Default' | 'Large' | 'Medium' | 'Small': Size of the machines.
* **workerSizeId**: int: Size ID of machines: 
0 - Small
1 - Medium
2 - Large

## StatusCodesBasedTrigger
### Properties
* **count**: int: Request Count.
* **status**: int: HTTP status code.
* **subStatus**: int: Request Sub Status.
* **timeInterval**: string: Time interval.
* **win32Status**: int: Win32 error code.

## VirtualApplication
### Properties
* **physicalPath**: string: Physical path.
* **preloadEnabled**: bool: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.
* **virtualDirectories**: [VirtualDirectory](#virtualdirectory)[]: Virtual directories for virtual application.
* **virtualPath**: string: Virtual path.

## VirtualDirectory
### Properties
* **physicalPath**: string: Physical path.
* **virtualPath**: string: Path to virtual application.

## VirtualIPMapping
### Properties
* **internalHttpPort**: int: Internal HTTP port.
* **internalHttpsPort**: int: Internal HTTPS port.
* **inUse**: bool: Is virtual IP mapping in use.
* **virtualIP**: string: Virtual IP address.

## VirtualNetworkProfile
### Properties
* **id**: string: Resource id of the Virtual Network.
* **name**: string (ReadOnly): Name of the Virtual Network (read-only).
* **subnet**: string: Subnet within the Virtual Network.
* **type**: string (ReadOnly): Resource type of the Virtual Network (read-only).

## VnetGatewayProperties
### Properties
* **vnetName**: string: The Virtual Network name.
* **vpnPackageUri**: string (Required, WriteOnly): The URI where the VPN package can be downloaded.

## VnetRouteProperties
### Properties
* **endAddress**: string: The ending address for this route. If the start address is specified in CIDR notation, this must be omitted.
* **name**: string: The name of this route. This is only returned by the server and does not need to be set by the client.
* **routeType**: 'DEFAULT' | 'INHERITED' | 'STATIC' | string: The type of route this is:
DEFAULT - By default, every app has routes to the local address ranges specified by RFC1918
INHERITED - Routes inherited from the real Virtual Network routes
STATIC - Static route set on the app only

These values will be used for syncing an app's routes with those from a Virtual Network.
* **startAddress**: string: The starting address for this route. This may also include a CIDR notation, in which case the end address must not be specified.

## WebAppCollection
### Properties
* **nextLink**: string (ReadOnly): Link to next page of resources.
* **value**: [Site](#site)[] (Required): Collection of resources.

## WebAppCollection
### Properties
* **nextLink**: string (ReadOnly): Link to next page of resources.
* **value**: [Site](#site)[] (Required): Collection of resources.

## WorkerPool
### Properties
* **computeMode**: 'Dedicated' | 'Dynamic' | 'Shared': Shared or dedicated app hosting.
* **instanceNames**: string[] (ReadOnly): Names of all instances in the worker pool (read only).
* **workerCount**: int: Number of instances in the worker pool.
* **workerSize**: string: VM size of the worker pool instances.
* **workerSizeId**: int: Worker size ID for referencing this worker pool.

