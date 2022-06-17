# Microsoft.Consumption @ 2018-11-01-preview

## Function download (Microsoft.Consumption/billingAccounts/invoices/pricesheet@2018-11-01-preview)
* **Resource**: Microsoft.Consumption/billingAccounts/invoices/pricesheet
* **ApiVersion**: 2018-11-01-preview
* **Output**: [PricesheetDownloadResponse](#pricesheetdownloadresponse)

## Function download (Microsoft.Consumption/billingAccounts/billingProfiles/pricesheet@2018-11-01-preview)
* **Resource**: Microsoft.Consumption/billingAccounts/billingProfiles/pricesheet
* **ApiVersion**: 2018-11-01-preview
* **Output**: [PricesheetDownloadResponse](#pricesheetdownloadresponse)

## DownloadUrl
### Properties
* **downloadUrl**: string (ReadOnly): The URL to the PDF file.
* **expiryTime**: string (ReadOnly): The time in UTC at which this download URL will expire.

## PricesheetDownloadResponse
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [DownloadUrl](#downloadurl): A secure URL that can be used to download a an entity until the URL expires.
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): Resource tags.
* **type**: string (ReadOnly): Resource type.

## PricesheetDownloadResponse
### Properties
* **id**: string (ReadOnly): Resource Id.
* **name**: string (ReadOnly): Resource name.
* **properties**: [DownloadUrl](#downloadurl): A secure URL that can be used to download a an entity until the URL expires.
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): Resource tags.
* **type**: string (ReadOnly): Resource type.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

