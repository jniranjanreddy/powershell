## Powershell Basics.

## "Windows Write-HOST" is equal to echo command in Unix"

```
PS C:\Users\Devops> help *user*

Name                              Category  Module                    Synopsis
----                              --------  ------                    --------
Set-WinUserLanguageList           Cmdlet    International             Set-WinUserLanguageList...
New-WinUserLanguageList           Cmdlet    International             New-WinUserLanguageList...
Get-WinUserLanguageList           Cmdlet    International             Get-WinUserLanguageList...
New-LocalUser                     Cmdlet    Microsoft.PowerShell.L... New-LocalUser...
Rename-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Rename-LocalUser...
Enable-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Enable-LocalUser...
Remove-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Remove-LocalUser...
Set-LocalUser                     Cmdlet    Microsoft.PowerShell.L... Set-LocalUser...
Get-LocalUser                     Cmdlet    Microsoft.PowerShell.L... Get-LocalUser...
Disable-LocalUser                 Cmdlet    Microsoft.PowerShell.L... Disable-LocalUser...
Set-PcsvDeviceUserPassword        Function  PcsvDevice                ...
Restore-UevUserSetting            Cmdlet    UEV                       Restore-UevUserSetting...
```
## It shows the version and Source
```
PS C:\Users\Devops> help *user*

Name                              Category  Module                    Synopsis
----                              --------  ------                    --------
Set-WinUserLanguageList           Cmdlet    International             Set-WinUserLanguageList...
New-WinUserLanguageList           Cmdlet    International             New-WinUserLanguageList...
Get-WinUserLanguageList           Cmdlet    International             Get-WinUserLanguageList...
New-LocalUser                     Cmdlet    Microsoft.PowerShell.L... New-LocalUser...
Rename-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Rename-LocalUser...
Enable-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Enable-LocalUser...
Remove-LocalUser                  Cmdlet    Microsoft.PowerShell.L... Remove-LocalUser...
Set-LocalUser                     Cmdlet    Microsoft.PowerShell.L... Set-LocalUser...
Get-LocalUser                     Cmdlet    Microsoft.PowerShell.L... Get-LocalUser...
Disable-LocalUser                 Cmdlet    Microsoft.PowerShell.L... Disable-LocalUser...
Set-PcsvDeviceUserPassword        Function  PcsvDevice                ...
Restore-UevUserSetting            Cmdlet    UEV                       Restore-UevUserSetting...

```
## Filter by Module
PS C:\Users\Devops> Get-Command *user* -Module UEV
```
CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Restore-UevUserSetting                             2.1.639.0  UEV
```

## Find command will find all commands, It require Nuget
```
PS C:\Users\Devops> find-Command

NuGet provider is required to continue
PowerShellGet requires NuGet provider version '2.8.5.201' or newer to interact with NuGet-based repositories. The NuGet provider must be available in 'C:\Program
Files\PackageManagement\ProviderAssemblies' or 'C:\Users\Devops\AppData\Local\PackageManagement\ProviderAssemblies'. You can also install the NuGet provider by
running 'Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force'. Do you want PowerShellGet to install and import the NuGet provider now?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y")
```
##  This is pop-up a windows for GUI commands like ISE - Integrated Script Editor
```
PS C:\Users\Devops> show-command
```
## get alias
```
PS C:\Users\Devops> Get-Command cat
CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           cat -> Get-Content

PS C:\Users\Devops> Get-Command ls
CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           ls -> Get-ChildItem
```
## How to check what modules are loaded.
```
PS C:\Users\Devops> Get-Module

ModuleType Version    Name                                ExportedCommands
---------- -------    ----                                ----------------
Manifest   3.1.0.0    Microsoft.PowerShell.Management     {Add-Computer, Add-Content, Checkpoint-Computer, Clear-Content...}
Manifest   3.1.0.0    Microsoft.PowerShell.Utility        {Add-Member, Add-Type, Clear-Variable, Compare-Object...}
Binary     1.0.0.1    PackageManagement                   {Find-Package, Find-PackageProvider, Get-Package, Get-PackageProvider...}
Script     1.0.0.1    PowerShellGet                       {Find-Command, Find-DscResource, Find-Module, Find-RoleCapability...}
Script     2.0.0      PSReadline                          {Get-PSReadLineKeyHandler, Get-PSReadLineOption, Remove-PSReadLineKeyHandler, Set-PSReadLineKeyHandler...}
Binary     2.1.639.0  UEV                                 {Clear-UevAppxPackage, Clear-UevConfiguration, Disable-Uev, Disable-UevAppxPackage...}
```
## List available Modules.
```
PS C:\Users\Devops> Get-Module -Listavailable
PS C:\Users\Devops> Find-Module az

Version    Name                                Repository           Description
-------    ----                                ----------           -----------
9.3.0      Az                                  PSGallery            Microsoft Azure PowerShell - Cmdlets to manage resources in Azure. This module is compatible wit...

PS C:\Users\Devops> Get-Computerinfo


WindowsBuildLabEx                                       : 19041.1.amd64fre.vb_release.191206-1406
WindowsCurrentVersion                                   : 6.3
WindowsEditionId                                        : Professional
WindowsInstallationType                                 : Client
WindowsInstallDateFromRegistry                          : 19-10-2022 10:41:15
WindowsProductId                                        : 00330-80000-00000-AA799
WindowsProductName                                      : Windows 10 Pro
WindowsRegisteredOrganization                           :
WindowsRegisteredOwner                                  : Devops
WindowsSystemRoot                                       : C:\Windows
WindowsVersion                                          : 2009
BiosCharacteristics                                     : {7, 9, 11, 12...}
BiosBIOSVersion                                         : {LENOVO - 1580, R0GET58W (1.58 ), Lenovo - 1580}
BiosBuildNumber                                         :
BiosCaption                                             : R0GET58W (1.58 )
```











