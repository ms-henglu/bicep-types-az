# Microsoft.VirtualMachineImages
  
> [!NOTE]
> The code samples in this document are generated from API usage examples contributed by Resource Providers in their [Azure Rest API specifications](https://github.com/Azure/azure-rest-api-specs). Any issues should be reported and addressed in the source.


## microsoft.virtualmachineimages/imagetemplates

Create an Image Template for Linux.
```bicep
resource exampleResource 'Microsoft.VirtualMachineImages/imageTemplates@2020-02-14' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/rg1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/identity_1': {
      }
    }
  }
  location: 'westus'
  properties: {
    customize: [
      {
        name: 'Shell Customizer Example'
        type: 'Shell'
        scriptUri: 'https://example.com/path/to/script.sh'
      }
    ]
    distribute: [
      {
        type: 'ManagedImage'
        artifactTags: {
          tagName: 'value'
        }
        imageId: '/subscriptions/{subscription-id}/resourceGroups/rg1/providers/Microsoft.Compute/images/image_it_1'
        location: '1_location'
        runOutputName: 'image_it_pir_1'
      }
    ]
    source: {
      type: 'ManagedImage'
      imageId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/images/source_image'
    }
    vmProfile: {
      osDiskSizeGB: 64
      vmSize: 'Standard_D2s_v3'
      vnetConfig: {
        subnetId: '/subscriptions/{subscription-id}/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name'
      }
    }
  }
  tags: {
    imagetemplate_tag1: 'IT_T1'
    imagetemplate_tag2: 'IT_T2'
  }
}
```

Create an Image Template for Windows.
```bicep
resource exampleResource 'Microsoft.VirtualMachineImages/imageTemplates@2020-02-14' = {
  name: 'example'
  identity: {
    type: 'UserAssigned'
    userAssignedIdentities: {
      '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/rg1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/identity_1': {
      }
    }
  }
  location: 'westus'
  properties: {
    customize: [
      {
        name: 'PowerShell (inline) Customizer Example'
        type: 'PowerShell'
        inline: [
          'Powershell command-1'
          'Powershell command-2'
          'Powershell command-3'
        ]
      }
      {
        name: 'PowerShell (inline) Customizer Elevated user Example'
        type: 'PowerShell'
        inline: [
          'Powershell command-1'
          'Powershell command-2'
          'Powershell command-3'
        ]
        runElevated: true
      }
      {
        name: 'PowerShell (inline) Customizer Elevated Local System user Example'
        type: 'PowerShell'
        inline: [
          'Powershell command-1'
          'Powershell command-2'
          'Powershell command-3'
        ]
        runAsSystem: true
        runElevated: true
      }
      {
        name: 'PowerShell (script) Customizer Example'
        type: 'PowerShell'
        scriptUri: 'https://example.com/path/to/script.ps1'
        validExitCodes: [
          0
          1
        ]
      }
      {
        name: 'PowerShell (script) Customizer Elevated Local System user Example'
        type: 'PowerShell'
        runElevated: true
        scriptUri: 'https://example.com/path/to/script.ps1'
        validExitCodes: [
          0
          1
        ]
      }
      {
        name: 'PowerShell (script) Customizer Elevated Local System user Example'
        type: 'PowerShell'
        runAsSystem: true
        runElevated: true
        scriptUri: 'https://example.com/path/to/script.ps1'
        validExitCodes: [
          0
          1
        ]
      }
      {
        name: 'Restart Customizer Example'
        type: 'WindowsRestart'
        restartCheckCommand: 'powershell -command "& {Write-Output \'restarted.\'}"'
        restartCommand: 'shutdown /f /r /t 0 /c "packer restart"'
        restartTimeout: '10m'
      }
      {
        name: 'Windows Update Customizer Example'
        type: 'WindowsUpdate'
        filters: [
          '$_.BrowseOnly'
        ]
        searchCriteria: 'BrowseOnly=0 and IsInstalled=0'
        updateLimit: 100
      }
    ]
    distribute: [
      {
        type: 'ManagedImage'
        artifactTags: {
          tagName: 'value'
        }
        imageId: '/subscriptions/{subscription-id}/resourceGroups/rg1/providers/Microsoft.Compute/images/image_it_1'
        location: '1_location'
        runOutputName: 'image_it_pir_1'
      }
    ]
    source: {
      type: 'ManagedImage'
      imageId: '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/images/source_image'
    }
    vmProfile: {
      osDiskSizeGB: 64
      vmSize: 'Standard_D2s_v3'
      vnetConfig: {
        subnetId: '/subscriptions/{subscription-id}/resourceGroups/rg1/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name'
      }
    }
  }
  tags: {
    imagetemplate_tag1: 'IT_T1'
    imagetemplate_tag2: 'IT_T2'
  }
}
```
