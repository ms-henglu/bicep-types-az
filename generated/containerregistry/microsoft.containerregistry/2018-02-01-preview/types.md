# Microsoft.ContainerRegistry @ 2018-02-01-preview

## Resource Microsoft.ContainerRegistry/registries/builds@2018-02-01-preview (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildProperties](#buildproperties) (ReadOnly): The properties of a build.
* **type**: 'Microsoft.ContainerRegistry/registries/builds' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/buildTasks@2018-02-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location of the resource. This cannot be changed after the resource is created.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildTaskProperties](#buildtaskproperties): The properties of a build task.
* **tags**: [ResourceTags](#resourcetags): The tags of the resource.
* **type**: 'Microsoft.ContainerRegistry/registries/buildTasks' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.ContainerRegistry/registries/buildTasks/steps@2018-02-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2018-02-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildStepProperties](#buildstepproperties): The properties of a build step.
* **type**: 'Microsoft.ContainerRegistry/registries/buildTasks/steps' (ReadOnly, DeployTimeConstant): The resource type

## Function cancel (Microsoft.ContainerRegistry/registries/builds@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries/builds
* **ApiVersion**: 2018-02-01-preview

## Function getBuildSourceUploadUrl (Microsoft.ContainerRegistry/registries@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries
* **ApiVersion**: 2018-02-01-preview
* **Output**: [SourceUploadDefinition](#sourceuploaddefinition)

## Function getLogLink (Microsoft.ContainerRegistry/registries/builds@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries/builds
* **ApiVersion**: 2018-02-01-preview
* **Output**: [BuildGetLogResult](#buildgetlogresult)

## Function listBuildArguments (Microsoft.ContainerRegistry/registries/buildTasks/steps@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries/buildTasks/steps
* **ApiVersion**: 2018-02-01-preview
* **Output**: [BuildArgumentList](#buildargumentlist)

## Function listSourceRepositoryProperties (Microsoft.ContainerRegistry/registries/buildTasks@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries/buildTasks
* **ApiVersion**: 2018-02-01-preview
* **Output**: [SourceRepositoryProperties](#sourcerepositoryproperties)

## Function queueBuild (Microsoft.ContainerRegistry/registries@2018-02-01-preview)
* **Resource**: Microsoft.ContainerRegistry/registries
* **ApiVersion**: 2018-02-01-preview
* **Input**: [QueueBuildRequest](#queuebuildrequest)
* **Output**: [Build](#build)

## BaseImageDependency
### Properties
* **digest**: string: The sha256-based digest of the image manifest.
* **registry**: string: The registry login server.
* **repository**: string: The repository name.
* **tag**: string: The tag name.
* **type**: 'BuildTime' | 'RunTime' | string: The type of the base image dependency.

## Build
### Properties
* **id**: string (ReadOnly): The resource ID.
* **name**: string (ReadOnly): The name of the resource.
* **properties**: [BuildProperties](#buildproperties): The properties of a build.
* **type**: string (ReadOnly): The type of the resource.

## BuildArgument
### Properties
* **isSecret**: bool: Flag to indicate whether the argument represents a secret and want to be removed from build logs.
* **name**: string (Required): The name of the argument.
* **type**: 'DockerBuildArgument' | string (Required): The type of the argument.
* **value**: string (Required): The value of the argument.

## BuildArgumentList
### Properties
* **nextLink**: string: The URI that can be used to request the next set of paged results.
* **value**: [BuildArgument](#buildargument)[]: The collection value.

## BuildGetLogResult
### Properties
* **logLink**: string: The link to logs for a azure container registry build.

## BuildProperties
### Properties
* **buildId**: string: The unique identifier for the build.
* **buildTask**: string: The build task with which the build was started.
* **buildType**: 'AutoBuild' | 'QuickBuild' | string: The type of build.
* **createTime**: string: The time the build was created.
* **finishTime**: string: The time the build finished.
* **gitCommitTrigger**: [GitCommitTrigger](#gitcommittrigger): The git commit trigger that caused the build.
* **imageUpdateTrigger**: [ImageUpdateTrigger](#imageupdatetrigger): The image update trigger that caused the build.
* **isArchiveEnabled**: bool: The value that indicates whether archiving is enabled or not.
* **lastUpdatedTime**: string: The last updated time for the build.
* **outputImages**: [ImageDescriptor](#imagedescriptor)[]: The list of all images that were generated from the build.
* **platform**: [PlatformProperties](#platformproperties): The platform properties against which the build will happen.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string: The provisioning state of a build.
* **startTime**: string: The time the build started.
* **status**: 'Canceled' | 'Error' | 'Failed' | 'Queued' | 'Running' | 'Started' | 'Succeeded' | 'Timeout' | string: The current status of the build.

## BuildStepProperties
* **Discriminator**: type

### Base Properties
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): The provisioning state of the build step.
### DockerBuildStep
#### Properties
* **baseImageDependencies**: [BaseImageDependency](#baseimagedependency)[] (ReadOnly): List of base image dependencies for a step.
* **baseImageTrigger**: 'All' | 'None' | 'Runtime' | string: The type of the auto trigger for base image dependency updates.
* **branch**: string: The repository branch name.
* **buildArguments**: [BuildArgument](#buildargument)[]: The custom arguments for building this build step.
* **contextPath**: string: The relative context path for a docker build in the source.
* **dockerFilePath**: string: The Docker file path relative to the source control root.
* **imageNames**: string[]: The fully qualified image names including the repository and tag.
* **isPushEnabled**: bool: The value of this property indicates whether the image built should be pushed to the registry or not.
* **noCache**: bool: The value of this property indicates whether the image cache is enabled or not.
* **type**: 'Docker' (Required): The type of the step.


## BuildTaskProperties
### Properties
* **alias**: string (Required): The alternative updatable name for a build task.
* **creationDate**: string (ReadOnly): The creation date of build task.
* **platform**: [PlatformProperties](#platformproperties) (Required): The platform properties against which the build has to happen.
* **provisioningState**: 'Canceled' | 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): The provisioning state of the build task.
* **sourceRepository**: [SourceRepositoryProperties](#sourcerepositoryproperties) (Required): The properties that describes the source(code) for the build task.
* **status**: 'Disabled' | 'Enabled' | string: The current status of build task.
* **timeout**: int: Build timeout in seconds.

## GitCommitTrigger
### Properties
* **branchName**: string: The branch name in the repository.
* **commitId**: string: The unique ID that identifies a commit.
* **id**: string: The unique ID of the trigger.
* **providerType**: string: The source control provider type.
* **repositoryUrl**: string: The repository URL.

## ImageDescriptor
### Properties
* **digest**: string: The sha256-based digest of the image manifest.
* **registry**: string: The registry login server.
* **repository**: string: The repository name.
* **tag**: string: The tag name.

## ImageUpdateTrigger
### Properties
* **id**: string: The unique ID of the trigger.
* **images**: [ImageDescriptor](#imagedescriptor)[]: The list of image updates that caused the build.
* **timestamp**: string: The timestamp when the image update happened.

## PlatformProperties
### Properties
* **cpu**: int: The CPU configuration in terms of number of cores required for the build.
* **osType**: 'Linux' | 'Windows' | string (Required): The operating system type required for the build.

## QueueBuildRequest
* **Discriminator**: type

### Base Properties
### BuildTaskBuildRequest
#### Properties
* **buildTaskName**: string (Required): The name of build task against which build has to be queued.
* **type**: 'BuildTask' (Required): The type of the build request.

### QuickBuildRequest
#### Properties
* **buildArguments**: [BuildArgument](#buildargument)[]: The collection of build arguments to be used.
* **dockerFilePath**: string (Required): The Docker file path relative to the source location.
* **imageNames**: string[]: The fully qualified image names including the repository and tag.
* **isPushEnabled**: bool: The value of this property indicates whether the image built should be pushed to the registry or not.
* **noCache**: bool: The value of this property indicates whether the image cache is enabled or not.
* **platform**: [PlatformProperties](#platformproperties) (Required): The platform properties against which the build will happen.
* **sourceLocation**: string (Required): The URL(absolute or relative) of the source that needs to be built. For Docker build, it can be an URL to a tar or github repository as supported by Docker.
If it is relative URL, the relative path should be obtained from calling getSourceUploadUrl API.
* **timeout**: int: Build timeout in seconds.
* **type**: 'QuickBuild' (Required): The type of the build request.


## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## SourceControlAuthInfo
### Properties
* **expiresIn**: int: Time in seconds that the token remains valid
* **refreshToken**: string: The refresh token used to refresh the access token.
* **scope**: string: The scope of the access token.
* **token**: string (Required): The access token used to access the source control provider.
* **tokenType**: 'OAuth' | 'PAT' | string: The type of Auth token.

## SourceRepositoryProperties
### Properties
* **isCommitTriggerEnabled**: bool: The value of this property indicates whether the source control commit trigger is enabled or not.
* **repositoryUrl**: string (Required): The full URL to the source code repository
* **sourceControlAuthProperties**: [SourceControlAuthInfo](#sourcecontrolauthinfo): The authorization properties for accessing the source code repository.
* **sourceControlType**: 'Github' | 'VisualStudioTeamService' | string (Required): The type of source control service.

## SourceRepositoryProperties
### Properties
* **isCommitTriggerEnabled**: bool: The value of this property indicates whether the source control commit trigger is enabled or not.
* **repositoryUrl**: string (Required): The full URL to the source code repository
* **sourceControlAuthProperties**: [SourceControlAuthInfo](#sourcecontrolauthinfo): The authorization properties for accessing the source code repository.
* **sourceControlType**: 'Github' | 'VisualStudioTeamService' | string (Required): The type of source control service.

## SourceUploadDefinition
### Properties
* **relativePath**: string: The relative path to the source. This is used to submit the subsequent queue build request.
* **uploadUrl**: string: The URL where the client can upload the source.

