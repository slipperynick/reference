# 🖥️ Windows 11 Command Line & PowerShell Reference

A comprehensive reference for Windows 11 command-line (CMD) and PowerShell commands, covering system administration, networking, security, disk management, and troubleshooting.

---

## 📂 File & Directory Management

### **Command Prompt (CMD)**
- `dir` – List files and directories  
- `cd <path>` – Change directory  
- `mkdir <folder>` – Create a new directory  
- `copy <source> <destination>` – Copy files  
- `move <source> <destination>` – Move files  
- `del <filename>` – Delete a file  
- `rmdir /s /q <folder>` – Delete a directory  
- `attrib +h <file>` – Hide a file  
- `tree <directory>` – Display directory structure  

### **PowerShell**
- `Get-ChildItem` (aliases: `ls`, `gci`) – List directory contents  
- `Set-Location <path>` (aliases: `cd`, `sl`) – Change directory  
- `New-Item -Path <folder> -ItemType Directory` – Create a new directory  
- `Remove-Item -Path <file>` – Delete a file  
- `Copy-Item -Path <file> -Destination <folder>` – Copy files  
- `Move-Item -Path <file> -Destination <folder>` – Move files  

---

## 🖥️ System Information & Management

### **Command Prompt (CMD)**
- `systeminfo` – Display detailed system information  
- `tasklist` – List all running processes  
- `taskkill /PID <id> /F` – Terminate a process  
- `wmic cpu get name` – Get CPU information  
- `wmic memorychip get capacity` – Get RAM information  
- `msconfig` – Open System Configuration  
- `winver` – Show Windows version  
- `shutdown /r /t 0` – Restart system immediately  
- `control` – Open Control Panel  

### **PowerShell**
- `Get-ComputerInfo` – Get detailed system information  
- `Get-Process` – Get running processes  
- `Stop-Process -Id <PID>` – Terminate a process  
- `Get-Service` – Get a list of running services  
- `Restart-Computer` – Restart Windows  
- `Start-Process <application>` – Run an application  
- `Measure-Command { <command> }` – Measure execution time of a command  

---

## 🌐 Networking & Internet

### **Command Prompt (CMD)**
- `ipconfig /all` – Show detailed IP configuration  
- `ping <hostname/IP>` – Test network connectivity  
- `tracert <hostname>` – Trace network route  
- `netstat -ano` – View all active connections  
- `nslookup <domain>` – Perform DNS lookup  
- `arp -a` – View ARP table  
- `nbtstat -n` – View NetBIOS name table  
- `netsh wlan show profiles` – Show saved Wi-Fi profiles  
- `netsh wlan show profile name="<SSID>" key=clear` – Show Wi-Fi password  

### **PowerShell**
- `Test-NetConnection -ComputerName <hostname>` – Ping a host  
- `Get-NetIPAddress` – Get local IP addresses  
- `Get-NetTCPConnection` – Show active TCP connections  
- `Resolve-DnsName <domain>` – Perform DNS lookup  
- `Get-NetAdapter` – List network adapters  
- `Restart-NetAdapter -Name "<AdapterName>"` – Restart a network adapter  

---

## 🔧 Disk & Storage Management

### **Command Prompt (CMD)**
- `chkdsk /f c:` – Scan and fix disk errors  
- `diskpart` – Open Disk Partition Manager  
- `wmic logicaldisk get name,size` – Show disk info  
- `defrag C:` – Defragment the disk  
- `format <drive>` – Format a drive  
- `fsutil dirty query <drive>` – Check for dirty bit on a drive  

### **PowerShell**
- `Get-PhysicalDisk` – Get physical disk info  
- `Get-Volume` – Show all volumes and free space  
- `Clear-Disk -Number <diskNumber>` – Wipe a disk  
- `Format-Volume -DriveLetter C -FileSystem NTFS -NewFileSystemLabel "NewVolume"` – Format a drive  

---

## 🔥 Windows Security & User Management

### **Command Prompt (CMD)**
- `net user` – List local users  
- `net localgroup administrators` – List local admins  
- `net user <username> <password> /add` – Create a new user  
- `net user <username> /delete` – Delete a user  
- `wmic useraccount list full` – Get detailed user account info  

### **PowerShell**
- `Get-LocalUser` – List all local users  
- `New-LocalUser -Name "newuser" -Password (ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force)` – Create a new local user  
- `Remove-LocalUser -Name "olduser"` – Delete a local user  
- `Get-LocalGroupMember Administrators` – List local administrators  

---

## 🔄 Windows Updates & System Maintenance

### **Command Prompt (CMD)**
- `wuauclt /detectnow` – Check for Windows updates  
- `dism /online /cleanup-image /restorehealth` – Repair Windows image  
- `sfc /scannow` – Scan and repair system files  

### **PowerShell**
- `Get-WindowsUpdate` – Check for Windows updates  
- `Install-WindowsUpdate` – Install updates  
- `Restart-Computer` – Restart Windows  
- `Clear-EventLog -LogName System` – Clear logs  

---

## 📑 System Logging & Event Logs

### **Command Prompt (CMD)**
- `eventvwr` – Open Event Viewer  
- `wevtutil qe System /c:10 /f:text` – Get last 10 system logs  

### **PowerShell**
- `Get-EventLog -LogName System -Newest 10` – View system logs  
- `Clear-EventLog -LogName System` – Clear logs  

---

## 🎛️ Additional Utilities

### **Command Prompt (CMD)**
- `notepad` – Open Notepad  
- `calc` – Open Calculator  
- `mspaint` – Open Paint  
- `taskmgr` – Open Task Manager  
- `explorer` – Open File Explorer  
- `control` – Open Control Panel  
- `powershell` – Open PowerShell  
- `cmd` – Open Command Prompt  
- `snippingtool` – Open Snipping Tool  
- `diskmgmt.msc` – Open Disk Management  
- `firewall.cpl` – Open Windows Firewall  
- `regedit` – Open Registry Editor  

### **PowerShell**
- `Start-Process notepad` – Open Notepad  
- `Start-Process powershell -Verb runAs` – Open PowerShell as Admin  
- `Get-Help <command>` – Get help for any PowerShell command  

---

## 🏆 Windows 11 Specific Commands
- `Get-AppxPackage -AllUsers` – List installed Windows apps  
- `Remove-AppxPackage <PackageFullName>` – Uninstall an app  
- `winget install <package>` – Install an app via Windows Package Manager  
- `winget uninstall <package>` – Uninstall an app  
- `taskview` – Open Task View  
- `dfrgui` – Open Optimize Drives (Defragmenter)  
- `ms-settings:` – Open Windows Settings  

---

### **Windows Shortcuts**
- `Shift + Right Click` – Open CMD in folder  
- `Ctrl + Shift + Esc` – Open Task Manager  
- `Win + X` – Open Quick Access Menu  

---