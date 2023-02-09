# How to read a file in pipeline
```
PS C:\Users\Devops> cat .\IPS.txt
192.168.9.1
8.8.8.8
1.1.1.1

PS C:\Users\Devops> Get-Content .\IPS.txt
ComputerName           : 192.168.9.1
RemoteAddress          : 192.168.9.1
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.9.252
PingSucceeded          : True
PingReplyDetails (RTT) : 1 ms

ComputerName           : 8.8.8.8
RemoteAddress          : 8.8.8.8
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.9.252
PingSucceeded          : True
PingReplyDetails (RTT) : 20 ms

ComputerName           : 1.1.1.1
RemoteAddress          : 1.1.1.1
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.9.252
PingSucceeded          : True
PingReplyDetails (RTT) : 32 ms

1.1.1.1 
```

# CVS
```
C:\Users\Devops>cat.\port.csv
computername,Port 
192.168.99.1,80  
8.8.8.8,53

1.1.1.1,53

PS C:\Users\Devops> Import-Csv .\port.csv | Test-NetConnection
WARNING: TCP connect to (192.168.99.1 : 80) failed
WARNING: Ping to 192.168.99.1 failed with status: TimedOut


ComputerName           : 192.168.99.1
RemoteAddress          : 192.168.99.1
RemotePort             : 80
InterfaceAlias         : Wi-Fi
SourceAddress          : 192.168.9.252
PingSucceeded          : False
PingReplyDetails (RTT) : 0 ms
TcpTestSucceeded       : False

ComputerName     : 8.8.8.8
RemoteAddress    : 8.8.8.8
RemotePort       : 53
InterfaceAlias   : Wi-Fi
SourceAddress    : 192.168.9.252
TcpTestSucceeded : True

ComputerName     : 1.1.1.1
RemoteAddress    : 1.1.1.1
RemotePort       : 53
InterfaceAlias   : Wi-Fi
SourceAddress    : 192.168.9.252
TcpTestSucceeded : True

PS C:\Users\Devops> Help Test-NetConnection -Parameter Port

-Port <Int32>
    Specifies the TCP port number on the remote computer. The cmdlet uses this port number to test connectivity to the remote computer.

    Required?                    true
    Position?                    named
    Default value                none
    Accept pipeline input?       True (ByPropertyName)
    Accept wildcard characters?  false
    
  PS C:\Users\Devops> (Get-NetIPAddress -InterfaceAlias Ethernet -AddressFamily IPv4)


IPAddress         : 169.254.108.220
InterfaceIndex    : 8
InterfaceAlias    : Ethernet
AddressFamily     : IPv4
Type              : Unicast
PrefixLength      : 16
PrefixOrigin      : WellKnown
SuffixOrigin      : Link
AddressState      : Tentative
ValidLifetime     : Infinite ([TimeSpan]::MaxValue)
PreferredLifetime : Infinite ([TimeSpan]::MaxValue)
SkipAsSource      : False
PolicyStore       : ActiveStore


PS C:\Users\Devops> (Get-NetIPAddress -InterfaceAlias Ethernet -AddressFamily IPv4).IPAddress
169.254.108.220

PS C:\Users\Devops> Test-Connection -Computername  (Get-Content .\IPS.txt)

Source        Destination     IPV4Address      IPV6Address                              Bytes    Time(ms)
------        -----------     -----------      -----------                              -----    --------
WINDEVOPS     192.168.9.1                                                               32       1
WINDEVOPS     192.168.9.1                                                               32       1
WINDEVOPS     192.168.9.1                                                               32       1
WINDEVOPS     192.168.9.1                                                               32       2
WINDEVOPS     8.8.8.8         8.8.4.4                                                   32       20
WINDEVOPS     8.8.8.8         8.8.4.4                                                   32       19
WINDEVOPS     8.8.8.8         8.8.4.4                                                   32       18
WINDEVOPS     8.8.8.8         8.8.4.4                                                   32       26
WINDEVOPS     1.1.1.1         1.1.1.1                                                   32       27
WINDEVOPS     1.1.1.1         1.1.1.1                                                   32       26
WINDEVOPS     1.1.1.1         1.1.1.1                                                   32       25
WINDEVOPS     1.1.1.1         1.1.1.1                                                   32       26





















```
