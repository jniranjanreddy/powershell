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
























```
