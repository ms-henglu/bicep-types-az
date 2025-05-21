# Microsoft.Media @ 2022-11-01

## Resource Microsoft.Media/mediaservices/liveEvents@2022-11-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {minLength: 1, maxLength: 32, pattern: "^[a-zA-Z0-9]+(-*[a-zA-Z0-9])*$"} (Required, DeployTimeConstant): The resource name
* **properties**: [LiveEventProperties](#liveeventproperties): The live event properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Media/mediaservices/liveEvents' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Media/mediaservices/liveEvents/liveOutputs@2022-11-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1, maxLength: 256, pattern: "^([a-zA-Z0-9])+(-*[a-zA-Z0-9])*$"} (Required, DeployTimeConstant): The resource name
* **properties**: [LiveOutputProperties](#liveoutputproperties): Live output properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: 'Microsoft.Media/mediaservices/liveEvents/liveOutputs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Media/mediaservices/liveEvents/liveOutputs/operationLocations@2022-11-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string {minLength: 1} (Required, DeployTimeConstant): The resource name
* **properties**: [LiveOutputProperties](#liveoutputproperties) (ReadOnly): Live output properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **type**: 'Microsoft.Media/mediaservices/liveEvents/liveOutputs/operationLocations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Media/mediaservices/liveEvents/operationLocations@2022-11-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): The geo-location where the resource lives
* **name**: string {minLength: 1} (Required, DeployTimeConstant): The resource name
* **properties**: [LiveEventProperties](#liveeventproperties) (ReadOnly): The live event properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags) (ReadOnly): Resource tags.
* **type**: 'Microsoft.Media/mediaservices/liveEvents/operationLocations' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Media/mediaservices/streamingEndpoints@2022-11-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string {minLength: 1, maxLength: 24, pattern: "^[a-zA-Z0-9]+(-*[a-zA-Z0-9])*$"} (Required, DeployTimeConstant): The resource name
* **properties**: [StreamingEndpointProperties](#streamingendpointproperties): The streaming endpoint properties.
* **sku**: [ArmStreamingEndpointCurrentSku](#armstreamingendpointcurrentsku): The streaming endpoint sku.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.Media/mediaservices/streamingEndpoints' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Media/mediaservices/streamingEndpoints/operationLocations@2022-11-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): The geo-location where the resource lives
* **name**: string {minLength: 1} (Required, DeployTimeConstant): The resource name
* **properties**: [StreamingEndpointProperties](#streamingendpointproperties) (ReadOnly): The streaming endpoint properties.
* **sku**: [ArmStreamingEndpointCurrentSku](#armstreamingendpointcurrentsku) (ReadOnly): The streaming endpoint sku.
* **systemData**: [SystemData](#systemdata) (ReadOnly): The system metadata relating to this resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags) (ReadOnly): Resource tags.
* **type**: 'Microsoft.Media/mediaservices/streamingEndpoints/operationLocations' (ReadOnly, DeployTimeConstant): The resource type

## Function allocate (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01

## Function getStatus (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01
* **Output**: [LiveEventGetStatusResult](#liveeventgetstatusresult)

## Function getStreamEvents (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01
* **Output**: [LiveEventGetStreamEventsResult](#liveeventgetstreameventsresult)

## Function getTrackIngestHeartbeats (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01
* **Output**: [LiveEventGetTrackIngestHeartbeatsResult](#liveeventgettrackingestheartbeatsresult)

## Function reset (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01

## Function scale (Microsoft.Media/mediaservices/streamingEndpoints@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/streamingEndpoints
* **ApiVersion**: 2022-11-01
* **Input**: [StreamingEntityScaleUnit](#streamingentityscaleunit)

## Function start (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01

## Function start (Microsoft.Media/mediaservices/streamingEndpoints@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/streamingEndpoints
* **ApiVersion**: 2022-11-01

## Function stop (Microsoft.Media/mediaservices/liveEvents@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/liveEvents
* **ApiVersion**: 2022-11-01
* **Input**: [LiveEventActionInput](#liveeventactioninput)

## Function stop (Microsoft.Media/mediaservices/streamingEndpoints@2022-11-01)
* **Resource**: Microsoft.Media/mediaservices/streamingEndpoints
* **ApiVersion**: 2022-11-01

## AkamaiAccessControl
### Properties
* **akamaiSignatureHeaderAuthenticationKeyList**: [AkamaiSignatureHeaderAuthenticationKey](#akamaisignatureheaderauthenticationkey)[]: authentication key list

## AkamaiSignatureHeaderAuthenticationKey
### Properties
* **base64Key**: string: authentication key
* **expiration**: string: The expiration time of the authentication key.
* **identifier**: string: identifier of the key

## ArmStreamingEndpointCurrentSku
### Properties
* **capacity**: int: The streaming endpoint sku capacity.
* **name**: string (ReadOnly): The streaming endpoint sku name.

## CrossSiteAccessPolicies
### Properties
* **clientAccessPolicy**: string: The content of clientaccesspolicy.xml used by Silverlight.
* **crossDomainPolicy**: string: The content of crossdomain.xml used by Silverlight.

## Hls
### Properties
* **fragmentsPerTsSegment**: int: The number of fragments in an HTTP Live Streaming (HLS) TS segment in the output of the live event. This value does not affect the packing ratio for HLS CMAF output.

## IPAccessControl
### Properties
* **allow**: [IPRange](#iprange)[]: The IP allow list.

## IPRange
### Properties
* **address**: string: The IP address.
* **name**: string: The friendly name for the IP address range.
* **subnetPrefixLength**: int: The subnet mask prefix length (see CIDR notation).

## LiveEventActionInput
### Properties
* **removeOutputsOnStop**: bool: The flag indicates whether live outputs are automatically deleted when live event is being stopped. Deleting live outputs do not delete the underlying assets.

## LiveEventEncoding
### Properties
* **encodingType**: 'None' | 'PassthroughBasic' | 'PassthroughStandard' | 'Premium1080p' | 'Standard' | string: Live event type. When encodingType is set to PassthroughBasic or PassthroughStandard, the service simply passes through the incoming video and audio layer(s) to the output. When encodingType is set to Standard or Premium1080p, a live encoder transcodes the incoming stream into multiple bitrates or layers. See https://go.microsoft.com/fwlink/?linkid=2095101 for more information. This property cannot be modified after the live event is created.
* **keyFrameInterval**: string: Use an ISO 8601 time value between 0.5 to 20 seconds to specify the output fragment length for the video and audio tracks of an encoding live event. For example, use PT2S to indicate 2 seconds. For the video track it also defines the key frame interval, or the length of a GoP (group of pictures).   If this value is not set for an encoding live event, the fragment duration defaults to 2 seconds. The value cannot be set for pass-through live events.
* **presetName**: string: The optional encoding preset name, used when encodingType is not None. This value is specified at creation time and cannot be updated. If the encodingType is set to Standard, then the default preset name is ‘Default720p’. Else if the encodingType is set to Premium1080p, the default preset is ‘Default1080p’.
* **stretchMode**: 'AutoFit' | 'AutoSize' | 'None' | string: Specifies how the input video will be resized to fit the desired output resolution(s). Default is None

## LiveEventEndpoint
### Properties
* **protocol**: string: The endpoint protocol.
* **url**: string: The endpoint URL.

## LiveEventGetStatusResult
### Properties
* **value**: [LiveEventStatus](#liveeventstatus)[]: The result of the get live event status.

## LiveEventGetStreamEventsResult
### Properties
* **value**: [LiveEventStreamEvent](#liveeventstreamevent)[]: The result of the get live event stream events.

## LiveEventGetTrackIngestHeartbeatsResult
### Properties
* **value**: [LiveEventTrackEvent](#liveeventtrackevent)[]: The result of the get live event track events.

## LiveEventIngestInterruption
### Properties
* **begin**: string: UTC time of interruption start, encoder disconnected.
* **duration**: string: Duration of interruption in ISO 8601 time. For example, use PT1H30M to indicate 1 hour and 30 minutes.
* **end**: string: UTC time of interruption end, encoder re-connected.
* **reason**: string: Interruption reason.

## LiveEventIngestion
### Properties
* **begin**: string: Ingestion begin time in UTC.
* **end**: string: Ingestion end time in UTC. Empty if it's not stopped yet.
* **endReason**: string: Reason why ingestion stops. Empty if it's not stopped yet. E.g) Service Stopped. No Ingestion.
* **ingestInterruptions**: [LiveEventIngestInterruption](#liveeventingestinterruption)[]: IngestInterruption entry list.
* **streamName**: string: Ingestion stream name.

## LiveEventInput
### Properties
* **accessControl**: [LiveEventInputAccessControl](#liveeventinputaccesscontrol): Access control for live event input.
* **accessToken**: string: A UUID in string form to uniquely identify the stream. This can be specified at creation time but cannot be updated. If omitted, the service will generate a unique value.
* **endpoints**: [LiveEventEndpoint](#liveeventendpoint)[]: The input endpoints for the live event.
* **keyFrameIntervalDuration**: string: ISO 8601 time duration of the key frame interval duration of the input. This value sets the EXT-X-TARGETDURATION property in the HLS output. For example, use PT2S to indicate 2 seconds. Leave the value empty for encoding live events.
* **streamingProtocol**: 'FragmentedMP4' | 'RTMP' | string (Required): The input protocol for the live event. This is specified at creation time and cannot be updated.
* **timedMetadataEndpoints**: [LiveEventTimedMetadataEndpoint](#liveeventtimedmetadataendpoint)[]: The metadata endpoints for the live event.

## LiveEventInputAccessControl
### Properties
* **ip**: [IPAccessControl](#ipaccesscontrol): The IP access control properties.

## LiveEventInputTrackSelection
### Properties
* **operation**: string: Comparing operation. This property is reserved for future use, any value set on this property will be ignored.
* **property**: string: Property name to select. This property is reserved for future use, any value set on this property will be ignored.
* **value**: string: Property value to select. This property is reserved for future use, any value set on this property will be ignored.

## LiveEventOutputTranscriptionTrack
### Properties
* **trackName**: string (Required): The output track name. This property is reserved for future use, any value set on this property will be ignored.

## LiveEventPreview
### Properties
* **accessControl**: [LiveEventPreviewAccessControl](#liveeventpreviewaccesscontrol): The access control for live event preview.
* **alternativeMediaId**: string: An alternative media identifier associated with the streaming locator created for the preview. This value is specified at creation time and cannot be updated. The identifier can be used in the CustomLicenseAcquisitionUrlTemplate or the CustomKeyAcquisitionUrlTemplate of the StreamingPolicy specified in the StreamingPolicyName field.
* **endpoints**: [LiveEventEndpoint](#liveeventendpoint)[]: The endpoints for preview. Do not share the preview URL with the live event audience.
* **previewLocator**: string: The identifier of the preview locator in Guid format. Specifying this at creation time allows the caller to know the preview locator url before the event is created. If omitted, the service will generate a random identifier. This value cannot be updated once the live event is created.
* **streamingPolicyName**: string: The name of streaming policy used for the live event preview. This value is specified at creation time and cannot be updated.

## LiveEventPreviewAccessControl
### Properties
* **ip**: [IPAccessControl](#ipaccesscontrol): The IP access control properties.

## LiveEventProperties
### Properties
* **created**: string (ReadOnly): The creation time for the live event
* **crossSiteAccessPolicies**: [CrossSiteAccessPolicies](#crosssiteaccesspolicies): Live event cross site access policies.
* **description**: string: A description for the live event.
* **encoding**: [LiveEventEncoding](#liveeventencoding): Encoding settings for the live event. It configures whether a live encoder is used for the live event and settings for the live encoder if it is used.
* **hostnamePrefix**: string: When useStaticHostname is set to true, the hostnamePrefix specifies the first part of the hostname assigned to the live event preview and ingest endpoints. The final hostname would be a combination of this prefix, the media service account name and a short code for the Azure Media Services data center.
* **input**: [LiveEventInput](#liveeventinput) (Required): Live event input settings. It defines how the live event receives input from a contribution encoder.
* **lastModified**: string (ReadOnly): The last modified time of the live event.
* **preview**: [LiveEventPreview](#liveeventpreview): Live event preview settings. Preview allows live event producers to preview the live streaming content without creating any live output.
* **provisioningState**: string (ReadOnly): The provisioning state of the live event.
* **resourceState**: 'Allocating' | 'Deleting' | 'Running' | 'StandBy' | 'Starting' | 'Stopped' | 'Stopping' | string (ReadOnly): The resource state of the live event. See https://go.microsoft.com/fwlink/?linkid=2139012 for more information.
* **streamOptions**: ('Default' | 'LowLatency' | 'LowLatencyV2' | string)[]: The options to use for the LiveEvent. This value is specified at creation time and cannot be updated. The valid values for the array entry values are 'Default' and 'LowLatency'.
* **transcriptions**: [LiveEventTranscription](#liveeventtranscription)[]: Live transcription settings for the live event. See https://go.microsoft.com/fwlink/?linkid=2133742 for more information about the live transcription feature.
* **useStaticHostname**: bool: Specifies whether a static hostname would be assigned to the live event preview and ingest endpoints. This value can only be updated if the live event is in Standby state

## LiveEventStatus
### Properties
* **healthDescriptions**: string[]: List of strings justifying the health status.
* **healthStatus**: 'Excellent' | 'Good' | 'Poor' | string: Health status of last 20 seconds.
* **ingestion**: [LiveEventIngestion](#liveeventingestion): Live event ingestion entry.
* **lastUpdatedTime**: string: Last updated UTC time of this status.
* **state**: 'Running' | 'Stopped' | string: Current state of the live event. See https://go.microsoft.com/fwlink/?linkid=2139012 for more information.
* **trackStatus**: [LiveEventTrackStatus](#liveeventtrackstatus)[]: Track entry list.

## LiveEventStreamEvent
### Properties
* **data**: [LiveEventStreamEventData](#liveeventstreameventdata): Event data based on event type.
* **eventLevel**: 'Critical' | 'Error' | 'Information' | 'Warning' | string: Event level.
* **eventTime**: string: The time event raised.
* **eventType**: 'StreamEvent/BeginIngest' | 'StreamEvent/ChunkDropped' | 'StreamEvent/Discontinuity' | 'StreamEvent/EndIngest' | 'StreamEvent/FirstChunkReceived' | 'StreamEvent/InvalidConnection' | 'StreamEvent/UnalignedKeyFrames' | 'StreamEvent/UnalignedPresentation' | string: The type of the stream event. Format: StreamEvent/{eventType}

## LiveEventStreamEventData
### Properties
* **bitrate**: int: Bitrate of the track.
* **currentFragmentTimestamp**: string: Current fragment timestamp in timescale.
* **discontinuityGap**: int: Length of the discontinuity gap in timescale.
* **duration**: string: Fragment duration.
* **fragmentDropReason**: string: Reason the fragment was dropped.
* **fragmentOneDuration**: string: Duration of first fragment used to make a comparison, in timescale.
* **fragmentOneTimestamp**: string: Timestamp of first fragment used to make a comparison, in timescale.
* **fragmentTwoDuration**: string: Duration of second fragment used to make a comparison, in timescale.
* **fragmentTwoTimestamp**: string: Timestamp of second fragment used to make a comparison, in timescale.
* **maxTime**: string: The larger timestamp of the two fragments compared.
* **maxTimeMediaType**: 'Audio' | 'Video' | string: The media type of the larger timestamp of two fragments compared.
* **mediaTimestamp**: string: Fragment timestamp in timescale.
* **mediaType**: 'audio' | 'video' | string: Type of the track.
* **minTime**: string: The smaller timestamp of the two fragments compared.
* **minTimeMediaType**: 'Audio' | 'Video' | string: The media type of the smaller timestamp of two fragments compared.
* **previousFragmentDuration**: string: Previous fragment duration in timescale.
* **previousFragmentTimestamp**: string: Previous fragment timestamp in timescale.
* **remoteIp**: string: Truncated IP of the encoder.
* **remotePort**: string: Port of the encoder.
* **resolution**: string: Width x Height for video, null otherwise.
* **resultCode**: string: Result code.
* **resultMessage**: string: Result message.
* **streamId**: string: Stream ID in the format "trackName_bitrate"
* **streamName**: string: Identifier of the stream or connection. Encoder or customer is responsible to add this ID in the ingest URL.
* **timescale**: string: Timescale in which timestamps are expressed.
* **timescaleOfMaxTime**: string: Timescale of the fragment with the larger timestamp.
* **timescaleOfMinTime**: string: Timescale of the fragment with the smaller timestamp.
* **trackId**: int: Track index.
* **trackName**: string: Name of the track.

## LiveEventTimedMetadataEndpoint
### Properties
* **url**: string: The metadata endpoint URL.

## LiveEventTrackEvent
### Properties
* **data**: [LiveEventTrackEventData](#liveeventtrackeventdata): Event data.
* **eventTime**: string: The time event raised.
* **eventType**: 'TrackEvent/IngestHeartbeat' | string: The type of the track event.

## LiveEventTrackEventData
### Properties
* **bitrate**: int: Bitrate of the track.
* **discontinuityCount**: int: Number of discontinuities detected in the last 20 seconds.
* **healthy**: bool: Indicates whether ingest is healthy.
* **incomingBitrate**: int: Calculated bitrate based on data chunks coming from encoder.
* **ingestDriftValue**: string: Indicates the speed of delay, in seconds-per-minute, of the incoming audio or video data during the last minute. The value is greater than zero if data is arriving to the live event slower than expected in the last minute; zero if data arrived with no delay; and "n/a" if no audio or video data was received. For example, if you have a contribution encoder sending in live content, and it is slowing down due to processing issues, or network latency, it may be only able to deliver a total of 58 seconds of audio or video in a one-minute period. This would be reported as two seconds-per-minute of drift. If the encoder is able to catch up and send all 60 seconds or more of data every minute, you will see this value reported as 0. If there was a disconnection or discontinuity from the encoder, this value may still display as 0, as it does not account for breaks in the data - only data that is delayed in timestamps.
* **lastFragmentArrivalTime**: string: The last timestamp in UTC that a fragment arrived at the ingest endpoint.
* **lastTimestamp**: string: Latest timestamp received for a track in last 20 seconds.
* **nonincreasingCount**: int: Number of data chunks with timestamps in the past that were received in last 20 seconds.
* **overlapCount**: int: Number of data chunks that had overlapped timestamps in last 20 seconds.
* **state**: string: State of the live event.
* **timescale**: string: Timescale in which timestamps are expressed.
* **trackName**: string: Name of the track.
* **trackType**: 'audio' | 'video' | string: Type of the track.
* **transcriptionLanguage**: string: The language code (in BCP-47 format) of the transcription language. For example, "de-de" indicates German (Germany). The value is empty for the video track heartbeats, or when live transcription is turned off.
* **transcriptionState**: string: This value is "On" for audio track heartbeats if live transcription is turned on, otherwise you will see an empty string. This state is only applicable to track type of "audio" for Live transcription. All other tracks will have an empty value.
* **unexpectedBitrate**: bool: If expected and actual bitrates differ by more than allowed limit in last 20 seconds.

## LiveEventTrackStatus
### Properties
* **expectedBitrate**: int: Expected bitrate for this track.
* **incomingBitrate**: int: Average incoming bitrate for last 20 seconds when live event is running.
* **ingestDrift**: string: Current ingest drift value in seconds for last 1 minute.
* **requestReceived**: int: Total number of timed metadata request received.
* **requestSucceeded**: int: Total number of successful timed metadata request received.
* **trackId**: string: Track Id.

## LiveEventTranscription
### Properties
* **inputTrackSelection**: [LiveEventInputTrackSelection](#liveeventinputtrackselection)[]: Provides a mechanism to select the audio track in the input live feed, to which speech-to-text transcription is applied. This property is reserved for future use, any value set on this property will be ignored.
* **language**: string: Specifies the language (locale) to be used for speech-to-text transcription – it should match the spoken language in the audio track. The value should be in BCP-47 format (e.g: 'en-US'). See https://go.microsoft.com/fwlink/?linkid=2133742 for more information about the live transcription feature and the list of supported languages.
* **outputTranscriptionTrack**: [LiveEventOutputTranscriptionTrack](#liveeventoutputtranscriptiontrack): Describes a transcription track in the output of a live event, generated using speech-to-text transcription. This property is reserved for future use, any value set on this property will be ignored.

## LiveOutputProperties
### Properties
* **archiveWindowLength**: string (Required): ISO 8601 time between 1 minute to 25 hours to indicate the maximum content length that can be archived in the asset for this live output. This also sets the maximum content length for the rewind window. For example, use PT1H30M to indicate 1 hour and 30 minutes of archive window.
* **assetName**: string (Required): The asset that the live output will write to.
* **created**: string (ReadOnly): The creation time the live output.
* **description**: string: The description of the live output.
* **hls**: [Hls](#hls): HTTP Live Streaming (HLS) packing setting for the live output.
* **lastModified**: string (ReadOnly): The time the live output was last modified.
* **manifestName**: string: The manifest file name. If not provided, the service will generate one automatically.
* **outputSnapTime**: int: The initial timestamp that the live output will start at, any content before this value will not be archived.
* **provisioningState**: string (ReadOnly): The provisioning state of the live output.
* **resourceState**: 'Creating' | 'Deleting' | 'Running' | string (ReadOnly): The resource state of the live output.
* **rewindWindowLength**: string: ISO 8601 time between 1 minute to the duration of archiveWindowLength to control seek-able window length during Live. The service won't use this property once LiveOutput stops. The archived VOD will have full content with original ArchiveWindowLength. For example, use PT1H30M to indicate 1 hour and 30 minutes of rewind window length. Service will use implicit default value 30m only if Live Event enables LL.

## StreamingEndpointAccessControl
### Properties
* **akamai**: [AkamaiAccessControl](#akamaiaccesscontrol): The access control of Akamai
* **ip**: [IPAccessControl](#ipaccesscontrol): The IP access control of the streaming endpoint.

## StreamingEndpointProperties
### Properties
* **accessControl**: [StreamingEndpointAccessControl](#streamingendpointaccesscontrol): The access control definition of the streaming endpoint.
* **availabilitySetName**: string: This feature is deprecated, do not set a value for this property.
* **cdnEnabled**: bool: The CDN enabled flag.
* **cdnProfile**: string: The CDN profile name.
* **cdnProvider**: string: The CDN provider name.
* **created**: string (ReadOnly): The exact time the streaming endpoint was created.
* **crossSiteAccessPolicies**: [CrossSiteAccessPolicies](#crosssiteaccesspolicies): The streaming endpoint access policies.
* **customHostNames**: string[]: The custom host names of the streaming endpoint
* **description**: string: The streaming endpoint description.
* **freeTrialEndTime**: string (ReadOnly): The free trial expiration time.
* **hostName**: string (ReadOnly): The streaming endpoint host name.
* **lastModified**: string (ReadOnly): The exact time the streaming endpoint was last modified.
* **maxCacheAge**: int: Max cache age
* **provisioningState**: string (ReadOnly): The provisioning state of the streaming endpoint.
* **resourceState**: 'Deleting' | 'Running' | 'Scaling' | 'Starting' | 'Stopped' | 'Stopping' | string (ReadOnly): The resource state of the streaming endpoint.
* **scaleUnits**: int (Required): The number of scale units. Use the Scale operation to adjust this value.

## StreamingEntityScaleUnit
### Properties
* **scaleUnit**: int: The scale unit number of the streaming endpoint.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

