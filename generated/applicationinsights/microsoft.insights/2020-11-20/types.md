# Microsoft.Insights @ 2020-11-20

## Resource Microsoft.Insights/workbooktemplates@2020-11-20
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2020-11-20' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [WorkbookTemplateProperties](#workbooktemplateproperties): Properties that contain a workbook template.
* **tags**: [Dictionary<string,String>](#dictionarystringstring): Resource tags
* **type**: 'Microsoft.Insights/workbooktemplates' (ReadOnly, DeployTimeConstant): The resource type

## WorkbookTemplateProperties
### Properties
* **author**: string: Information about the author of the workbook template.
* **galleries**: [WorkbookTemplateGallery](#workbooktemplategallery)[] (Required): Workbook galleries supported by the template.
* **localized**: [Dictionary<string,IList<WorkbookTemplateLocalizedGallery>>](#dictionarystringilistworkbooktemplatelocalizedgallery): Key value pair of localized gallery. Each key is the locale code of languages supported by the Azure portal.
* **priority**: int: Priority of the template. Determines which template to open when a workbook gallery is opened in viewer mode.
* **templateData**: any (Required): Valid JSON object containing workbook template payload.

## WorkbookTemplateGallery
### Properties
* **category**: string: Category for the gallery.
* **name**: string: Name of the workbook template in the gallery.
* **order**: int: Order of the template within the gallery.
* **resourceType**: string: Azure resource type supported by the gallery.
* **type**: string: Type of workbook supported by the workbook template.

## Dictionary<string,IList<WorkbookTemplateLocalizedGallery>>
### Properties
### Additional Properties
* **Additional Properties Type**: [WorkbookTemplateLocalizedGallery](#workbooktemplatelocalizedgallery)[]

## WorkbookTemplateLocalizedGallery
### Properties
* **galleries**: [WorkbookTemplateGallery](#workbooktemplategallery)[]: Workbook galleries supported by the template.
* **templateData**: any: Valid JSON object containing workbook template payload.

## Dictionary<string,String>
### Properties
### Additional Properties
* **Additional Properties Type**: string
