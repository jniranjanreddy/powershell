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
