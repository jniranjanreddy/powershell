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
```
## Start-Transcript:
```
Start-Transcript -Path "C:\Temp\PowerShell_transcript.txt"
Stop-Transcript
```


```
help Get-Service -ShowWindow


PS C:\Users\Devops> Get-PSReadLineKeyHandler

PS C:\Users\Devops> $PSVersionTable.PSVersion
Major  Minor  Build  Revision
-----  -----  -----  --------
5      1      19041  1682
```
# How to create a Directory
```
 new-item scripts -Type directory
 wget -Uri https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1 -OutFile winrm.ps1 .\winrm.ps1
```
## How to check Network Details
```
 Get-NetIPAddress
 
```
## ceck to see if server has Internet or Not
```
PS C:\Users\Devops> Test-NetConnection
ComputerName           : internetbeacon.msedge.net
RemoteAddress          : 13.107.4.52
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.109.116
PingSucceeded          : True
PingReplyDetails (RTT) : 46 ms
```
## How to test a port.
```
PS C:\Users\Devops> Test-NetConnection windevops -Port 80                                                                                                        WARNING: TCP connect to (fe80::7a52:411a:29a2:ba8%24 : 80) failed                                                                                               WARNING: TCP connect to (192.168.56.1 : 80) failed                                                                                                             WARNING: TCP connect to (192.168.109.116 : 80) failed                                                                                                                   
ComputerName           : windevops
RemoteAddress          : fe80::7a52:411a:29a2:ba8%24
RemotePort             : 80
InterfaceAlias         : VirtualBox Host-Only Network
SourceAddress          : fe80::7a52:411a:29a2:ba8%24
PingSucceeded          : True
PingReplyDetails (RTT) : 0 ms
TcpTestSucceeded       : False
```
## How to Traceroute 
```
PS C:\Users\Devops> Test-NetConnection google.com -TraceRoute


ComputerName           : google.com
RemoteAddress          : 142.250.183.238
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.109.116
PingSucceeded          : True
PingReplyDetails (RTT) : 62 ms
TraceRoute             : 192.168.109.123
                         0.0.0.0
                         10.72.212.41
                         172.25.124.208
                         0.0.0.0
                         0.0.0.0
                         0.0.0.0
                         0.0.0.0
                         0.0.0.0
                         0.0.0.0
                         72.14.217.254
                         74.125.242.129
                         209.85.253.85
                         142.250.183.238
```
## How to resolve DNS
```
PS C:\Users\Devops> Resolve-DnsName google.com

Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
google.com                                     AAAA   245   Answer     2404:6800:4002:810::200e
google.com                                     A      122   Answer     142.250.182.142


PS C:\Users\Devops> Resolve-DnsName microsoft.com

Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
microsoft.com                                  A      1387  Answer     20.81.111.85
microsoft.com                                  A      1387  Answer     20.84.181.62
microsoft.com                                  A      1387  Answer     20.103.85.33
microsoft.com                                  A      1387  Answer     20.53.203.50
microsoft.com                                  A      1387  Answer     20.112.52.29

PS C:\Users\Devops>
```
## Read a file, Get-Content, type,
```
Get-Context test1.txt 
```
