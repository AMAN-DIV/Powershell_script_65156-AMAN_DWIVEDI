Press Windows + X

Click Windows PowerShell (or PowerShell (Admin))

Type the commands one by one and press Enter:

-----------------------------------
Get-Process                       |
Start-Service -Name "wuauserv"    |
Get-ChildItem                     |
-----------------------------------

PS C:\WINDOWS\system32> Get-Process

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
-------  ------    -----      -----     ------     --  -- -----------
    184      10     2132      10484       0.06  16008   6 Adobe Crash P...
    190      11     4400      11252      60.55   7740   0 AggregatorHost
    165      11     1856       8552       8.00   3020   6 ApMsgFwd
    163      10     1776       7572       0.05  29180   6 ApntEx
    341      17     3660       9852       0.86  19600   6 Apoint
    415      23    14084      17540       0.22  13620   6 ApplicationFr...
     79       6     1088       4328       0.03  18180   6 ApRemote
    392      20     4508       9640       0.25   5152   0 armsvc
    576      28    94332      34320   2,135.91   4304   0 audiodg
    281      28     8772       1616       0.02   5012   6 backgroundTas...
    439      22    25604      54024       0.08  29328   6 backgroundTas...
    317      31    18152       3888       0.19  31704   6 backgroundTas...
    209      11     2896       8084       0.03   4736   0 bcmHostContro...
    238      11     2896       8576       0.23   4744   0 bcmHostStorag...
    223      11    36932       8424       0.05   3196   0 bcmUshUpgrade...
    644      27    77144      68872       0.80   1964   6 chrome
   1400      45   384924     259336      97.06   3136   6 chrome



=======================================================================================================================


1 Get-Process

Displays all running processes on the system.

Get-Process

2️⃣ Get-Service

Shows the status of all services.

Get-Service


3️⃣ Start-Service

Starts a stopped service.

Start-Service -Name "wuauserv"


4️⃣ Stop-Service

Stops a running service.

Stop-Service -Name "wuauserv"


5️⃣ Get-ChildItem

Lists files and folders in a directory.

Get-ChildItem

6️⃣ Set-Location

Changes the current directory.

Set-Location C:\Windows

7️⃣ Get-Command

Lists available cmdlets.

Get-Command
===============================================

** USER CREATION **
1️⃣ Create a new local user

Correct & safe way (PowerShell requires a secure password):

$Password = ConvertTo-SecureString "P@ssw0rd!" -AsPlainText -Force
New-LocalUser -Name "JohnDoe" -Password $Password -Description "IT Support"
