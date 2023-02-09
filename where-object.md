## where object is used to filter the fields
```
PS C:\Users\Devops> Get-Service | select -first 10

Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_97b5a6d     Agent Activation Runtime_97b5a6d
Running  AESMService        Intel® SGX AESM
Stopped  AJRouter           AllJoyn Router Service
Stopped  ALG                Application Layer Gateway Service
Stopped  AppIDSvc           Application Identity
Running  Appinfo            Application Information
Stopped  AppMgmt            Application Management
Stopped  AppReadiness       App Readiness
Stopped  AppVClient         Microsoft App-V Client
Running  AppXSvc            AppX Deployment Service (AppXSVC)

PS C:\Users\Devops> Get-Service | select -first 10

Status   Name               DisplayName
------   ----               -----------
Stopped  AarSvc_97b5a6d     Agent Activation Runtime_97b5a6d
Running  AESMService        Intel® SGX AESM
Stopped  AJRouter           AllJoyn Router Service
Stopped  ALG                Application Layer Gateway Service
Stopped  AppIDSvc           Application Identity
Running  Appinfo            Application Information
Stopped  AppMgmt            Application Management
Stopped  AppReadiness       App Readiness
Stopped  AppVClient         Microsoft App-V Client
Running  AppXSvc            AppX Deployment Service (AppXSVC)

PS C:\Users\Devops> Get-Service | select -first 10 | Where-Object Status -eq "running"

Status   Name               DisplayName
------   ----               -----------
Running  AESMService        Intel® SGX AESM
Running  Appinfo            Application Information
Running  AppXSvc            AppX Deployment Service (AppXSVC)


PS C:\Users\Devops> Get-Service | select -first 10 | Where-Object Name -eq "Appinfo"

Status   Name               DisplayName
------   ----               -----------
Running  Appinfo            Application Information


PS C:\Users\Devops> Get-Service | select -first 10 | Where-Object DisplayName -eq "Intelr SGX AESM"

Status   Name               DisplayName
------   ----               -----------
Running  AESMService        Intel® SGX AESM

```

## Get a process status
```
PS C:\Users\Devops> (Get-Service | select -first 10 | Where-Object Name -eq "Appinfo").Status
Running
```
## Advanced filters
```
PS C:\Users\Devops> Get-Service | Where-Object {$_.Status -eq "running" -AND $_.Name -LIKE "*win*"}

Status   Name               DisplayName
------   ----               -----------
Running  WinDefend          Microsoft Defender Antivirus Service
Running  WinHttpAutoProx... WinHTTP Web Proxy Auto-Discovery Se...
Running  Winmgmt            Windows Management Instrumentation
Running  WinRM              Windows Remote Management (WS-Manag...
```
## To check how long it take to execute the command
```
PS C:\Users\Devops> Measure-Command {Get-Service | Where-Object {$_.Status -eq "running" -AND $_.Name -LIKE "*win*"}}
Days              : 0
Hours             : 0
Minutes           : 0
Seconds           : 0
Milliseconds      : 28
Ticks             : 280548
TotalDays         : 3.24708333333333E-07
TotalHours        : 7.793E-06
TotalMinutes      : 0.00046758
TotalSeconds      : 0.0280548
TotalMilliseconds : 28.0548
```












