## Enumerating -  /ɪˈnjuː.mə.reɪt/
```
PS C:\Users\Devops> Get-Hotfix

Source        Description      HotFixID      InstalledBy          InstalledOn
------        -----------      --------      -----------          -----------
WINDEVOPS     Update           KB5020872     NT AUTHORITY\SYSTEM  15-12-2022 00:00:00
WINDEVOPS     Update           KB5000736                          09-04-2021 00:00:00
WINDEVOPS     Security Update  KB5012170     NT AUTHORITY\SYSTEM  27-10-2022 00:00:00
WINDEVOPS     Update           KB5015684     NT AUTHORITY\SYSTEM  18-11-2022 00:00:00
WINDEVOPS     Security Update  KB5022282     NT AUTHORITY\SYSTEM  13-01-2023 00:00:00
WINDEVOPS     Update           KB5016705     NT AUTHORITY\SYSTEM  20-10-2022 00:00:00
WINDEVOPS     Update           KB5018506     NT AUTHORITY\SYSTEM  12-11-2022 00:00:00
WINDEVOPS     Update           KB5020372     NT AUTHORITY\SYSTEM  14-12-2022 00:00:00
WINDEVOPS     Security Update  KB5003742                          19-10-2022 00:00:00


PS C:\Users\Devops> Get-Hotfix | select HotFixID

HotFixID
--------
KB5020872
KB5000736
KB5012170
KB5015684
KB5022282
KB5016705
KB5018506
KB5020372
KB5003742

PS C:\Users\Devops> Get-Hotfix | ForEach-Object HotFixID
KB5020872
KB5000736
KB5012170
KB5015684
KB5022282
KB5016705
KB5018506
KB5020372
KB5003742

PS C:\Users\Devops> Get-Hotfix | ForEach-Object HotFixID | measure
Count    : 9
Average  :
Sum      :
Maximum  :
Minimum  :
Property :

PS C:\Users\Devops> 1..5 | ForEach-Object {Write-Host "$_"}
1
2
3
4
5
PS C:\Users\Devops>

PS C:\Users\Devops> 1..5 | ForEach-Object {Write-Host "Hello: $_"}
Hello: 1
Hello: 2
Hello: 3
Hello: 4
Hello: 5

```

