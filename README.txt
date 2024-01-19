Youtube Video:  https://youtu.be/tTg3AOTdU78


================================== 
=======     WESRanTrap     =======
==================================

Windows service based ransomware trap, eatch 10 sek. cheks if files in files.txt listed files are not 
enscripted. If enscripted writes to EventLog and shutdowns os.

-------------------------------------------------------------------
INSTALL:

copy folder WSRanTrap to c:\Windows\ProgramFiles
edit files.txt file (put files with full path)
EXAMPLE:
c:\VerryImportantDoc.docx

CONTENT OF c:\VerryImportantDoc.docx FILE:
blablablabal3441242534534blablalala
Do Not Delete or Change this file !!!!!!

file number is not limited, recomended to put for one in eatch users home documents direktory or if server 
is file server in base directory. Better what these files woud be first to enscrypt by atackers.


INSTALL WINDOWS SERVICE:
CMD with Administrative rights:
installutil WSRanTrap.exe

if command installutil not found:
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe WSRanTrap.exe

if get error:
C:\Program Files\WSRanTrap>C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe WSRanTrap.exe
Microsoft (R) .NET Framework Installation utility Version 4.7.3190.0
Copyright (C) Microsoft Corporation.  All rights reserved.

Exception occurred while initializing the installation:
System.IO.FileLoadException: Could not load file or assembly 'file:///C:\Program Files\WSRanTrap\WSRanTrap.exe' or one of its dependencies. Operation is not supported. (Exception from HRESULT: 0x80131515).

Right click on the WSRanTrap.exe properties and unblock it.

--------------------------------------------------------------------
UNINSTALL WINDOWS SERVICE: 

installutil /u WSRanTrap.exe

if not found:
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /u WSRanTrap.exe


---------------------------------------------------------------------
Start Windows Service:   WSRanTrap

check status and error in EvenLog > Windows Logs > Applications   [Source WSRanTrap]





