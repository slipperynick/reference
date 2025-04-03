# Linux Command Reference

## **Networking Commands**
- `ifconfig -a | grep en1` – View Ethernet interface statistics.
- `tcpdump -i en1` – Sniff or view Ethernet interface traffic.
- `netstat -an` – View all active connections without resolving hostnames.
- `dmesg` – View kernel buffer logs.
- `arp -an` – View MAC address table.
- `nmap` – Network scanner.
- `nmap -sP 192.168.1.0/24` – Ping hosts on a Class C subnet.
- `python -m SimpleHTTPServer` – Create a simple HTTP server for file sharing.
- `mount | column -t` – View mounted filesystems.
- `mtr` – Combine ping and traceroute.
- `whois domain.com` – View WHOIS information of a domain.
- `lft` – Layer 4 traceroute.
- `lsof -P -i -n` – See connected sockets.
- `ping google.com` – Send ICMP echo request.
- `htop` – Interactive process viewer.
- `iftop` – View real-time bandwidth usage.
- `ip addr show` – Show all network interfaces.
- `iwconfig` – Show wireless network interfaces.
- `route -n` – Display routing table.
- `sudo ufw allow ssh` – Allow SSH in UFW firewall.
- `sudo ufw allow http` – Allow HTTP in UFW firewall.
- `sudo ufw status verbose` – Check UFW firewall status.
- `firewall-cmd --add-port=9100/tcp --permanent` – Add a firewall rule.

## **System Information**
- `uptime` – Check system uptime.
- `uname -a` – Get system kernel information.
- `lsb_release -a` – Show OS details.
- `mpstat 1` – Show CPU usage.
- `df -h` – Show disk usage.
- `du -h` – Show directory size.
- `cat /etc/resolv.conf` – View DNS settings.
- `cat /etc/fstab` – View filesystem mount points.
- `vmstat 1` – View system performance.
- `htop` – View running processes.
- `ps aux | grep process` – Search for a running process.
- `task` – Command-line to-do list.

## **File & Directory Management**
- `ls -t` – List files by modification time.
- `mkdir mydir` – Create a new directory.
- `chmod 750 mydir` – Set directory permissions.
- `chown user:group file` – Change file ownership.
- `cp source.txt dest.txt` – Copy a file.
- `mv oldname.txt newname.txt` – Rename a file.
- `rm -rf dir/` – Delete a directory.
- `touch newfile.txt` – Create an empty file.
- `find / -name "*.log"` – Find all log files.
- `find / -name passwd -print 2> /dev/null` – Find password files while ignoring errors.

## **Archiving & Compression**
- `tar cfzv archive.tar.gz files*` – Create a compressed tar archive.
- `tar xvzf archive.tar.gz` – Extract a tar archive.
- `zip myfile.zip file1 file2` – Compress files into a ZIP archive.
- `unzip myfile.zip` – Extract a ZIP file.

## **Text Processing**
- `grep -i "error" logfile.txt` – Case-insensitive search in logs.
- `grep -v "DEBUG" logfile.txt` – Exclude lines with "DEBUG".
- `grep -r "keyword" /var/log` – Recursive search.
- `sed 's/foo/bar/g' file.txt` – Replace "foo" with "bar" in a file.
- `awk '{print $1}' file.txt` – Print the first column.
- `cut -d " " -f 4` – Extract the 4th field from a space-separated file.
- `tr -d ":"` – Remove colons from input.
- `sort file.txt` – Sort lines alphabetically.
- `uniq file.txt` – Remove duplicate lines.
- `wc -l file.txt` – Count lines in a file.

## **Process & User Management**
- `ps aux` – Show all running processes.
- `kill -9 <pid>` – Force kill a process.
- `pkill firefox` – Kill Firefox process.
- `usermod -aG sudo username` – Add user to the sudo group.
- `sudo usermod -a -G admin <USER>` – Add user to admin group.
- `passwd` – Change user password.
- `whoami` – Show the current user.
- `groups` – Show groups of the current user.

## **Package Management**
### Debian-based (Ubuntu, Debian)
- `sudo apt-get update` – Update package lists.
- `sudo apt-get upgrade` – Upgrade all packages.
- `sudo apt-get remove package` – Remove a package.
- `dpkg -l` – List installed packages.
- `dpkg-query -L <package>` – Show package contents.

### RedHat-based (CentOS, Fedora)
- `yum update` – Update all packages.
- `yum install <package>` – Install a package.
- `yum remove <package>` – Remove a package.

## **Disk & Storage**
- `df -h` – Show disk usage.
- `du -sh *` – Show size of all files in a directory.
- `lsblk` – List all available block devices.
- `mkfs.ext4 /dev/sdb1` – Format disk as ext4.
- `mount /dev/sdb1 /mnt` – Mount a disk.
- `umount /mnt` – Unmount a disk.

## **Security & Permissions**
- `sudo` – Execute command as superuser.
- `chmod 750 file` – Set file permissions.
- `chown user:group file` – Change file owner.
- `sudo dpkg-statoverride --update --add root admin 4750 /bin/su` – Restrict `su` usage.
- `sudo netstat -tulpn` – View open ports and listening services.

## **Docker Commands**
- `docker ps -a` – Show all containers.
- `docker images` – Show available images.
- `docker pull ubuntu` – Pull an image from Docker Hub.
- `docker run -it ubuntu` – Run an interactive Ubuntu container.
- `docker rm $(docker ps -a -q -f status=exited)` – Remove stopped containers.

## **Git Commands**
- `git clone repo-url` – Clone a Git repository.
- `git pull origin main` – Pull latest changes.
- `git push origin main` – Push changes to remote.
- `git checkout -b new-branch` – Create and switch to a new branch.
- `git merge branch-name` – Merge a branch into the current one.
- `git log --oneline --graph` – Show commit history.

## **Firewall & Security**
- `sudo ufw enable` – Enable UFW firewall.
- `sudo ufw allow 22/tcp` – Allow SSH access.
- `sudo ufw deny 80/tcp` – Deny HTTP access.
- `sudo ufw status verbose` – Show UFW status.

## **System Monitoring**
- `top` – Show running processes.
- `htop` – Interactive process viewer.
- `vmstat 1` – System performance monitoring.
- `iostat` – Show disk I/O stats.
- `tshark -D` – List available network interfaces for packet capture.

## **Useful One-Liners**
- `ls -l | awk '{print $9}'` – List file names only.
- `echo "Hello World" | tee file.txt` – Write to file and display output.
- `echo $(date +%F)` – Print current date.
- `find / -type f -name "*.conf"` – Find all configuration files.

---
