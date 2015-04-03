![](https://ci.appveyor.com/api/projects/status/ar0nqtlyomlwuhv7?svg=true)

####What is it?

An [Appease](http://appease.io) task template that pushes one or more NuGet packages to a .nupkg source

####How do I install it?

```PowerShell
Add-AppeaseTask `
    -DevOpName YOUR-DEVOP-NAME `
    -Name YOUR-TASK-NAME `
    -TemplateId PushNuGetPackage
```

####What parameters are required?

#####IncludeNupkgFilePath
description: a `string[]` representing included .nupkg file paths. Either literal or wildcard paths are supported.

####What parameters are optional?

#####ExcludeFileNameLike
description: a `string[]` representing .nupkg file names to exclude. Either literal or wildcard names are supported.

#####Recurse
description: a `switch` representing whether to recursively search directories below $IncludeNupkgFilePath.

#####SourceUrl
description: a `string` representing the url of the .nupkg source being pushed to.  
default: the official NuGet community feed (`https://nuget.org/api/v2/`)

#####ApiKey
description: a `string` representing the api key to use to authenticate against the .nupkg source being pushed to.