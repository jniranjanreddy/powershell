# powershell

```
S C:\Users\Devops> $PSVersionTable

Name                           Value                                                                                                 
----                           -----                                                                                                 
PSVersion                      5.1.19041.1682                                                                                        
PSEdition                      Desktop                                                                                               
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}                                                                               
BuildVersion                   10.0.19041.1682                                                                                       
CLRVersion                     4.0.30319.42000                                                                                       
WSManStackVersion              3.0                                                                                                   
PSRemotingProtocolVersion      2.3                                                                                                   
SerializationVersion           1.1.0.1                                                                                               


PS C:\Users\Devops> $psversiontable

Name                           Value                                                                                                 
----                           -----                                                                                                 
PSVersion                      5.1.19041.1682                                                                                        
PSEdition                      Desktop                                                                                               
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}                                                                               
BuildVersion                   10.0.19041.1682                                                                                       
CLRVersion                     4.0.30319.42000                                                                                       
WSManStackVersion              3.0                                                                                                   
PSRemotingProtocolVersion      2.3                                                                                                   
SerializationVersion           1.1.0.1                                                                                               

S C:\Users\Devops> Get-HotFix

Source        Description      HotFixID      InstalledBy          InstalledOn               
------        -----------      --------      -----------          -----------               
DESKTOP-NO... Update           KB5020613     NT AUTHORITY\SYSTEM  11-11-2022 00:00:00       
DESKTOP-NO... Update           KB5000736                          09-04-2021 00:00:00       
DESKTOP-NO... Security Update  KB5012170     NT AUTHORITY\SYSTEM  27-10-2022 00:00:00       
DESKTOP-NO... Update           KB5015684     NT AUTHORITY\SYSTEM  18-11-2022 00:00:00       
DESKTOP-NO... Security Update  KB5019959     NT AUTHORITY\SYSTEM  12-11-2022 00:00:00       
DESKTOP-NO... Update           KB5016705     NT AUTHORITY\SYSTEM  20-10-2022 00:00:00       
DESKTOP-NO... Update           KB5018506     NT AUTHORITY\SYSTEM  12-11-2022 00:00:00       
DESKTOP-NO... Security Update  KB5003742                          19-10-2022 00:00:00 

Start-Transcript
Stop-Transcript
help Get-Service -ShowWindow



PS C:\Users\Devops> Get-PSReadLineKeyHandler

PS C:\Users\Devops> $PSVersionTable.PSVersion
Major  Minor  Build  Revision
-----  -----  -----  --------
5      1      19041  1682


```
