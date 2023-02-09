
## how to select Objects, like Head/Tail in UNIX.

```
-First
-Last
-Skip
-Index
-Unique
```


```
PS C:\Users\Devops> Get-Process | select -first 5

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    227      15     3136       8208              1812   0 aesm_service
    285      20     4856      19824       5.59   3064  15 BrccMCtl
    189      13     2360      11012      10.75  13484  15 BrMfcMon
    244      16     2292      14552       0.25  14160  15 BrMfcWnd
    354      24    72720     129052      32.78   2352  15 chrome

PS C:\Users\Devops> Get-Process | select -last 5

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    186      11     1692       5060               776   0 wininit
    279      12     2604      11284              7104  15 winlogon
    202      12     3760      11576              7024   0 WmiPrvSE
    257      14     2700       3376              5392   0 WMIRegistrationService
    345      15     4056       8408               788   0 WUDFHost
    
    
PS C:\Users\Devops> Get-Process | select -index 1,3,4

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    285      20     4856      19824       5.59   3064  15 BrccMCtl
    244      16     2292      14552       0.25  14160  15 BrMfcWnd
    369      24    72500     132844      48.91   2352  15 chrome


PS C:\Users\Devops> Get-Process | select -index 0,3,4

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    227      15     3136       8208              1812   0 aesm_service
    244      16     2292      14552       0.25  14160  15 BrMfcWnd
    366      24    72452     132812      48.91   2352  15 chrome    
    
    
    
```
