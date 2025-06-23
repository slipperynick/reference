# Top macOS Terminal Commands

This document lists **essential macOS terminal commands**, grouped by category.

---

## 1. System & Security Commands
- `csrutil status` – Check if System Integrity Protection (SIP) is enabled  
- `fs_usage` – Display file system activity in real time  
- `firmwarepasswd -check` – Check if the firmware password is enabled  
- `system_profiler SPApplicationsDataType` – Display a detailed report of installed applications  
- `sw_vers` – Show the current macOS version and build number  
- `defaults read` – Read a plist file  
- `crontab -l` – List currently installed cron jobs  
- `plutil` – Manipulate property list files  

---

## 2. System Utilities
- `osascript` – Execute AppleScript scripts  
- `pbcopy` – Copy data to the clipboard  
- `pbpaste` – Paste data from the clipboard  
- `pmset` – Manage power settings  
- `caffeinate` – Prevent macOS from sleeping  
- `tmutil` – Manage Time Machine backups  
- `say` – Convert text to speech  
- `screencapture` – Capture screenshots  
- `networksetup` – Manage network configurations  

---

## 3. User & Directory Management
- `dscl` – Manage users and groups  
- `launchctl` – Manage system services (launch daemons)  
- `qlmanage` – Quick Look preview management tool  
- `diskutil` – Manage disks and volumes  
- `systemsetup` – Configure system settings (time zone, startup disk, etc.)  
- `softwareupdate` – Check and install macOS updates  
- `dsenableroot` – Enable or disable the root user  
- `dseditgroup` – Manage user groups  

---

## 4. Networking & Monitoring
- `airport` – Manage Wi-Fi networks  
- `nc` – Read and write network connections  
- `tcpdump` – Capture and analyze network traffic  
- `ipconfig` – Configure and display network interfaces  
- `ifconfig` – Configure network interfaces  
- `scutil` – Query and configure network settings  
- `netstat` – Display network status  
- `ping <host>` – Test network connectivity  
- `traceroute <host>` – Show the path of network packets  

---

## 5. Process & System Monitoring
- `top` – Display system activity  
- `htop` – Interactive process viewer  
- `pgrep <process>` – Search for a process  
- `pkill <process>` – Kill a process by name  
- `du` – Estimate file space usage  
- `df` – Show disk space usage  
- `ps aux` – List all running processes  

---

## 6. File & Disk Management
- `ls` – List directory contents  
- `find <path> -name "<filename>"` – Search for files  
- `cd <directory>` – Change the current working directory  
- `cp <source> <destination>` – Copy files or directories  
- `mv <source> <destination>` – Move or rename files  
- `rm <file>` – Delete files  
- `mkdir <directory>` – Create a new directory  
- `rmdir <directory>` – Remove empty directories  
- `chmod <permissions> <file>` – Change file permissions  
- `chown <user>:<group> <file>` – Change file ownership  

---

## 7. Compression & Archiving
- `zip <archive.zip> <file>` – Compress files into a ZIP archive  
- `unzip <archive.zip>` – Extract files from a ZIP archive  
- `tar -cvf archive.tar <directory>` – Create a tar archive  
- `tar -xvf archive.tar` – Extract a tar archive  
- `bzip2 <file>` – Compress using Bzip2  
- `gunzip <file.gz>` – Decompress a Gzip file  

---

## 8. Text Processing
- `cat <file>` – Display file contents  
- `less <file>` – View file with scrolling  
- `grep "<pattern>" <file>` – Search for text in a file  
- `awk '{print $1}' <file>` – Process text by column  
- `sed 's/foo/bar/g' <file>` – Replace text in a file  
- `cut -d: -f1 <file>` – Extract a specific column from text  
- `sort <file>` – Sort lines in a file  
- `uniq <file>` – Remove duplicate lines  

---

## 9. Miscellaneous Commands
- `whoami` – Show the current user  
- `hostname` – Show the system hostname  
- `uptime` – Show system uptime  
- `date` – Show or set the system date and time  
- `history` – Show command history  
- `man <command>` – Show the manual page for a command  
- `exit` – Close the terminal session  

---
## 10. Utils
- `bat` - A updated and more feature rich version of cat