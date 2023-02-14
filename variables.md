## This topic is about Variables..
```
PS C:\Users\Devops> "The server name is $SERVERname"
The server name is Server001

PS C:\Users\Devops> "The server $SERVERname is $SERVERname"
The server Server001 is Server001

PS C:\Users\Devops> "The server `$SERVERname is $SERVERname" # back tick
The server $SERVERname is Server001
```
## Casting Varriable types..
```
[string]
[int]
[double]
[bool]
[datetime]
Type Operators
-is
-isnot
-as
```
```
PS C:\Users\Devops> $num = 1234
PS C:\Users\Devops> $num.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     Int32                                    System.ValueType

PS C:\Users\Devops> $num = "Hello"
PS C:\Users\Devops> $num.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     String                                   System.Object

PS C:\Users\Devops> [string]$ComputerName = "Server01"
PS C:\Users\Devops> [string]$ComputerName.getType()

PS C:\Users\Devops> $num2 = 12.333333
PS C:\Users\Devops> $num2
12.333333
PS C:\Users\Devops> $num2 -as [int]
12
PS C:\Users\Devops> $num2
12.333333
PS C:\Users\Devops>

PS C:\Users\Devops> "1/1/2022"
1/1/2022
PS C:\Users\Devops> [datetime]"1/1/2022"
01 January 2022 00:00:00

PS C:\Users\Devops> [string[]]$Hostname =  "Server001"
PS C:\Users\Devops> $Hostname += "Server002"
PS C:\Users\Devops> $Hostname
Server001
Server002
PS C:\Users\Devops>


```
