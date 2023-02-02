## Powershell Basics.
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













