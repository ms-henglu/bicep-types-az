# Microsoft.BotService @ 2021-03-01

## Resource Microsoft.BotService/botServices@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: Entity Tag
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'azurebot' | 'bot' | 'designer' | 'function' | 'sdk': Required. Gets or sets the Kind of the resource.
* **location**: string: Specifies the location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BotProperties](#botproperties): The parameters to provide for the Bot.
* **sku**: [Sku](#sku): The SKU of the cognitive services account.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Contains resource tags defined as key/value pairs.
* **type**: 'Microsoft.BotService/botServices' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.BotService/botServices/channels@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: Entity Tag
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'azurebot' | 'bot' | 'designer' | 'function' | 'sdk': Required. Gets or sets the Kind of the resource.
* **location**: string: Specifies the location of the resource.
* **name**: 'AlexaChannel' | 'DirectLineChannel' | 'DirectLineSpeechChannel' | 'EmailChannel' | 'FacebookChannel' | 'KikChannel' | 'LineChannel' | 'MsTeamsChannel' | 'SkypeChannel' | 'SlackChannel' | 'SmsChannel' | 'TelegramChannel' | 'WebChatChannel' (Required, DeployTimeConstant): The resource name
* **properties**: [Channel](#channel): Channel definition
* **sku**: [Sku](#sku): The SKU of the cognitive services account.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Contains resource tags defined as key/value pairs.
* **type**: 'Microsoft.BotService/botServices/channels' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.BotService/botServices/connections@2021-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **etag**: string: Entity Tag
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **kind**: 'azurebot' | 'bot' | 'designer' | 'function' | 'sdk': Required. Gets or sets the Kind of the resource.
* **location**: string: Specifies the location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ConnectionSettingProperties](#connectionsettingproperties): Properties for a Connection Setting Item
* **sku**: [Sku](#sku): The SKU of the cognitive services account.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Contains resource tags defined as key/value pairs.
* **type**: 'Microsoft.BotService/botServices/connections' (ReadOnly, DeployTimeConstant): The resource type

## BotProperties
### Properties
* **cmekKeyVaultUrl**: string: The CMK Url
* **configuredChannels**: string[] (ReadOnly): Collection of channels for which the bot is configured
* **description**: string: The description of the bot
* **developerAppInsightKey**: string: The Application Insights key
* **developerAppInsightsApiKey**: string: The Application Insights Api Key
* **developerAppInsightsApplicationId**: string: The Application Insights App Id
* **displayName**: string (Required): The Name of the bot
* **enabledChannels**: string[] (ReadOnly): Collection of channels for which the bot is enabled
* **endpoint**: string (Required): The bot's endpoint
* **endpointVersion**: string (ReadOnly): The bot's endpoint version
* **iconUrl**: string: The Icon Url of the bot
* **isCmekEnabled**: bool: Whether Cmek is enabled
* **luisAppIds**: string[]: Collection of LUIS App Ids
* **luisKey**: string: The LUIS Key
* **msaAppId**: string (Required): Microsoft App Id for the bot

## Sku
### Properties
* **name**: 'F0' | 'S1' (Required): The sku name.
* **tier**: 'Free' | 'Standard' (ReadOnly): Gets the sku tier. This is based on the SKU name.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Channel
* **Discriminator**: channelName
### Base Properties
### AlexaChannel
#### Properties
* **channelName**: 'AlexaChannel' (Required): Alexa channel definition
* **properties**: [AlexaChannelProperties](#alexachannelproperties): The parameters to provide for the Alexa channel.

### DirectLineChannel
#### Properties
* **channelName**: 'DirectLineChannel' (Required): Direct Line channel definition
* **properties**: [DirectLineChannelProperties](#directlinechannelproperties): The parameters to provide for the Direct Line channel.

### DirectLineSpeechChannel
#### Properties
* **channelName**: 'DirectLineSpeechChannel' (Required): DirectLine Speech channel definition
* **properties**: [DirectLineSpeechChannelProperties](#directlinespeechchannelproperties): The parameters to provide for the DirectLine Speech channel.

### EmailChannel
#### Properties
* **channelName**: 'EmailChannel' (Required): Email channel definition
* **properties**: [EmailChannelProperties](#emailchannelproperties): The parameters to provide for the Email channel.

### FacebookChannel
#### Properties
* **channelName**: 'FacebookChannel' (Required): Facebook channel definition
* **properties**: [FacebookChannelProperties](#facebookchannelproperties): The parameters to provide for the Facebook channel.

### KikChannel
#### Properties
* **channelName**: 'KikChannel' (Required): Kik channel definition
* **properties**: [KikChannelProperties](#kikchannelproperties): The parameters to provide for the Kik channel.

### LineChannel
#### Properties
* **channelName**: 'LineChannel' (Required): Line channel definition
* **properties**: [LineChannelProperties](#linechannelproperties): The parameters to provide for the Line channel.

### MsTeamsChannel
#### Properties
* **channelName**: 'MsTeamsChannel' (Required): Microsoft Teams channel definition
* **properties**: [MsTeamsChannelProperties](#msteamschannelproperties): The parameters to provide for the Microsoft Teams channel.

### SkypeChannel
#### Properties
* **channelName**: 'SkypeChannel' (Required): Skype channel definition
* **properties**: [SkypeChannelProperties](#skypechannelproperties): The parameters to provide for the Microsoft Teams channel.

### SlackChannel
#### Properties
* **channelName**: 'SlackChannel' (Required): Slack channel definition
* **properties**: [SlackChannelProperties](#slackchannelproperties): The parameters to provide for the Slack channel.

### SmsChannel
#### Properties
* **channelName**: 'SmsChannel' (Required): Sms channel definition
* **properties**: [SmsChannelProperties](#smschannelproperties): The parameters to provide for the Sms channel.

### TelegramChannel
#### Properties
* **channelName**: 'TelegramChannel' (Required): Telegram channel definition
* **properties**: [TelegramChannelProperties](#telegramchannelproperties): The parameters to provide for the Telegram channel.

### WebChatChannel
#### Properties
* **channelName**: 'WebChatChannel' (Required): Web Chat channel definition
* **properties**: [WebChatChannelProperties](#webchatchannelproperties): The parameters to provide for the Web Chat channel.


## AlexaChannel
### Properties
* **channelName**: 'AlexaChannel' (Required): Alexa channel definition
* **properties**: [AlexaChannelProperties](#alexachannelproperties): The parameters to provide for the Alexa channel.

## AlexaChannelProperties
### Properties
* **alexaSkillId**: string (Required): The Alexa skill Id
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **serviceEndpointUri**: string (ReadOnly): Full Uri used to configured the skill in Alexa
* **urlFragment**: string (ReadOnly): Url fragment used in part of the Uri configured in Alexa

## DirectLineChannel
### Properties
* **channelName**: 'DirectLineChannel' (Required): Direct Line channel definition
* **properties**: [DirectLineChannelProperties](#directlinechannelproperties): The parameters to provide for the Direct Line channel.

## DirectLineChannelProperties
### Properties
* **sites**: [DirectLineSite](#directlinesite)[]: The list of Direct Line sites

## DirectLineSite
### Properties
* **isEnabled**: bool (Required): Whether this site is enabled for DirectLine channel.
* **isSecureSiteEnabled**: bool: Whether this site is enabled for authentication with Bot Framework.
* **isV1Enabled**: bool (Required): Whether this site is enabled for Bot Framework V1 protocol.
* **isV3Enabled**: bool (Required): Whether this site is enabled for Bot Framework V1 protocol.
* **key**: string (ReadOnly): Primary key. Value only returned through POST to the action Channel List API, otherwise empty.
* **key2**: string (ReadOnly): Secondary key. Value only returned through POST to the action Channel List API, otherwise empty.
* **siteId**: string (ReadOnly): Site Id
* **siteName**: string (Required): Site name
* **trustedOrigins**: string[]: List of Trusted Origin URLs for this site. This field is applicable only if isSecureSiteEnabled is True.

## DirectLineSpeechChannel
### Properties
* **channelName**: 'DirectLineSpeechChannel' (Required): DirectLine Speech channel definition
* **properties**: [DirectLineSpeechChannelProperties](#directlinespeechchannelproperties): The parameters to provide for the DirectLine Speech channel.

## DirectLineSpeechChannelProperties
### Properties
* **cognitiveServicesSubscriptionId**: string (Required): The cognitive service subscription ID to use with this channel registration.
* **customSpeechModelId**: string: Custom voice deployment id (optional).
* **customVoiceDeploymentId**: string: Custom speech model id (optional).
* **isDefaultBotForCogSvcAccount**: bool: Make this a default bot for chosen cognitive service account.
* **isEnabled**: bool: Whether this channel is enabled or not.

## EmailChannel
### Properties
* **channelName**: 'EmailChannel' (Required): Email channel definition
* **properties**: [EmailChannelProperties](#emailchannelproperties): The parameters to provide for the Email channel.

## EmailChannelProperties
### Properties
* **emailAddress**: string (Required): The email address
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **password**: string: The password for the email address. Value only returned through POST to the action Channel List API, otherwise empty.

## FacebookChannel
### Properties
* **channelName**: 'FacebookChannel' (Required): Facebook channel definition
* **properties**: [FacebookChannelProperties](#facebookchannelproperties): The parameters to provide for the Facebook channel.

## FacebookChannelProperties
### Properties
* **appId**: string (Required): Facebook application id
* **appSecret**: string: Facebook application secret. Value only returned through POST to the action Channel List API, otherwise empty.
* **callbackUrl**: string (ReadOnly): Callback Url
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **pages**: [FacebookPage](#facebookpage)[]: The list of Facebook pages
* **verifyToken**: string (ReadOnly): Verify token. Value only returned through POST to the action Channel List API, otherwise empty.

## FacebookPage
### Properties
* **accessToken**: string: Facebook application access token. Value only returned through POST to the action Channel List API, otherwise empty.
* **id**: string (Required): Page id

## KikChannel
### Properties
* **channelName**: 'KikChannel' (Required): Kik channel definition
* **properties**: [KikChannelProperties](#kikchannelproperties): The parameters to provide for the Kik channel.

## KikChannelProperties
### Properties
* **apiKey**: string: Kik API key. Value only returned through POST to the action Channel List API, otherwise empty.
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **isValidated**: bool: Whether this channel is validated for the bot
* **userName**: string (Required): The Kik user name

## LineChannel
### Properties
* **channelName**: 'LineChannel' (Required): Line channel definition
* **properties**: [LineChannelProperties](#linechannelproperties): The parameters to provide for the Line channel.

## LineChannelProperties
### Properties
* **callbackUrl**: string (ReadOnly): Callback Url to enter in line registration.
* **isValidated**: bool (ReadOnly): Whether this channel is validated for the bot
* **lineRegistrations**: [LineRegistration](#lineregistration)[] (Required): The list of line channel registrations

## LineRegistration
### Properties
* **channelAccessToken**: string: Access token for the line channel registration
* **channelSecret**: string: Secret for the line channel registration
* **generatedId**: string (ReadOnly): Id generated for the line channel registration

## MsTeamsChannel
### Properties
* **channelName**: 'MsTeamsChannel' (Required): Microsoft Teams channel definition
* **properties**: [MsTeamsChannelProperties](#msteamschannelproperties): The parameters to provide for the Microsoft Teams channel.

## MsTeamsChannelProperties
### Properties
* **callingWebHook**: string: Webhook for Microsoft Teams channel calls
* **enableCalling**: bool: Enable calling for Microsoft Teams channel
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot

## SkypeChannel
### Properties
* **channelName**: 'SkypeChannel' (Required): Skype channel definition
* **properties**: [SkypeChannelProperties](#skypechannelproperties): The parameters to provide for the Microsoft Teams channel.

## SkypeChannelProperties
### Properties
* **callingWebHook**: string: Calling web hook for Skype channel
* **enableCalling**: bool: Enable calling for Skype channel
* **enableGroups**: bool: Enable groups for Skype channel
* **enableMediaCards**: bool: Enable media cards for Skype channel
* **enableMessaging**: bool: Enable messaging for Skype channel
* **enableScreenSharing**: bool: Enable screen sharing for Skype channel
* **enableVideo**: bool: Enable video for Skype channel
* **groupsMode**: string: Group mode for Skype channel
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot

## SlackChannel
### Properties
* **channelName**: 'SlackChannel' (Required): Slack channel definition
* **properties**: [SlackChannelProperties](#slackchannelproperties): The parameters to provide for the Slack channel.

## SlackChannelProperties
### Properties
* **clientId**: string: The Slack client id
* **clientSecret**: string: The Slack client secret. Value only returned through POST to the action Channel List API, otherwise empty.
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **isValidated**: bool (ReadOnly): Whether this channel is validated for the bot
* **landingPageUrl**: string: The Slack landing page Url
* **lastSubmissionId**: string (ReadOnly): The Sms auth token
* **redirectAction**: string (ReadOnly): The Slack redirect action
* **registerBeforeOAuthFlow**: bool (ReadOnly): Whether to register the settings before OAuth validation is performed. Recommended to True.
* **signingSecret**: string: The Slack signing secret.
* **verificationToken**: string: The Slack verification token. Value only returned through POST to the action Channel List API, otherwise empty.

## SmsChannel
### Properties
* **channelName**: 'SmsChannel' (Required): Sms channel definition
* **properties**: [SmsChannelProperties](#smschannelproperties): The parameters to provide for the Sms channel.

## SmsChannelProperties
### Properties
* **accountSID**: string (Required): The Sms account SID. Value only returned through POST to the action Channel List API, otherwise empty.
* **authToken**: string: The Sms auth token. Value only returned through POST to the action Channel List API, otherwise empty.
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **isValidated**: bool: Whether this channel is validated for the bot
* **phone**: string (Required): The Sms phone

## TelegramChannel
### Properties
* **channelName**: 'TelegramChannel' (Required): Telegram channel definition
* **properties**: [TelegramChannelProperties](#telegramchannelproperties): The parameters to provide for the Telegram channel.

## TelegramChannelProperties
### Properties
* **accessToken**: string: The Telegram access token. Value only returned through POST to the action Channel List API, otherwise empty.
* **isEnabled**: bool (Required): Whether this channel is enabled for the bot
* **isValidated**: bool: Whether this channel is validated for the bot

## WebChatChannel
### Properties
* **channelName**: 'WebChatChannel' (Required): Web Chat channel definition
* **properties**: [WebChatChannelProperties](#webchatchannelproperties): The parameters to provide for the Web Chat channel.

## WebChatChannelProperties
### Properties
* **sites**: [WebChatSite](#webchatsite)[]: The list of Web Chat sites
* **webChatEmbedCode**: string (ReadOnly): Web chat control embed code

## WebChatSite
### Properties
* **enablePreview**: bool (Required): Whether this site is enabled for preview versions of Webchat
* **isEnabled**: bool (Required): Whether this site is enabled for DirectLine channel
* **key**: string (ReadOnly): Primary key. Value only returned through POST to the action Channel List API, otherwise empty.
* **key2**: string (ReadOnly): Secondary key. Value only returned through POST to the action Channel List API, otherwise empty.
* **siteId**: string (ReadOnly): Site Id
* **siteName**: string (Required): Site name

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ConnectionSettingProperties
### Properties
* **clientId**: string: Client Id associated with the Connection Setting.
* **clientSecret**: string: Client Secret associated with the Connection Setting
* **parameters**: [ConnectionSettingParameter](#connectionsettingparameter)[]: Service Provider Parameters associated with the Connection Setting
* **scopes**: string: Scopes associated with the Connection Setting
* **serviceProviderDisplayName**: string: Service Provider Display Name associated with the Connection Setting
* **serviceProviderId**: string: Service Provider Id associated with the Connection Setting
* **settingId**: string (ReadOnly): Setting Id set by the service for the Connection Setting.

## ConnectionSettingParameter
### Properties
* **key**: string: Key for the Connection Setting Parameter.
* **value**: string: Value associated with the Connection Setting Parameter.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
