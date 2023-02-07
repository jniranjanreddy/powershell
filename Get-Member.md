## Get-Member
```
1. Powershell Objects, prpoerties, and Methods
2. "X-Ray" of the powershell pipeline
3. "DotNotation" Syntax = Object.property
4. Storing Objects in variable
5. Usining Parenthesis to refer objects
```

```
PS C:\Users\Devops> get-host


Name             : ConsoleHost
Version          : 5.1.19041.2364
InstanceId       : 4393dcda-27ec-4fa5-9f3f-850a0110ab8f
UI               : System.Management.Automation.Internal.Host.InternalHostUserInterface
CurrentCulture   : en-IN
CurrentUICulture : en-US
PrivateData      : Microsoft.PowerShell.ConsoleHost+ConsoleColorProxy
DebuggerEnabled  : True
IsRunspacePushed : False
Runspace         : System.Management.Automation.Runspaces.LocalRunspace


PS C:\Users\Devops> (get-host).Version

Major  Minor  Build  Revision
-----  -----  -----  --------
5      1      19041  2364

PS C:\Users\Devops> (get-host).Version

Major  Minor  Build  Revision
-----  -----  -----  --------
5      1      19041  2364


```
