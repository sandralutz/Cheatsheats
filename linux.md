# Linux

## System
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```

Display Linux system information
<span style="color: #d65cad">
uname -a
</span>
<br>
Display kernel release information
<span style="color:#d65cad">uname -r</span>
<br>
Show how long the system has been running and loaded
<span style="color:#d65cad">uptime</span>
<br>
Show system host name
<span style="color:#d65cad">hostname</span>
<br>
Display the IP address of the host
<span style="color:#d65cad">hostname -l</span>
<br>
Show system reboot history
<span style="color:#d65cad">last reboot</span>
<br>
Show current date and time
<span style="color:#d65cad">date</span>
<br>
Show this month's calendar
<span style="color:#d65cad">cal</span>
<br>
Display who is online
<span style="color:#d65cad">w</span>
<br>
Who you are logged in as
<span style="color:#d65cad">whoami</span>
<br>
Display information about user
<span style="color:#d65cad">finger user</span>

<br>
<br>


## Users

Show the active user id with login and group
<span style="color:#038ca1">id</span>
<br>
Show last logins in the system
<span style="color:#038ca1">last</span>
<br>
Show who is logged on the system
<span style="color:#038ca1">who</span>
<br>
Add group "admin"
<span style="color:#038ca1">group add admin</span>
<br>
g admin -m sam
Create user "sam"
<span style="color:#038ca1">useradd -c "Sam Tomshi"</span>
<br>
Delete user sam
<span style="color:#038ca1">userdel sam</span>
<br>
Add user sam
<span style="color:#038ca1">adduser sam</span>
<br>
Modify user information
<span style="color:#038ca1">usermod</span>
<br>
<br>



## File permission related

Change the permissions of file to octal
<span style="color:#d69015">chmod octal file-name</span>
<br>
#### example
Set rwx permission for owner, group and other
<span style="color:#d69015">chmod 777</span>
<br>
Set rwx permission for owner, rw for group and other
<span style="color:#d69015">chmod 755</span>
<br>
Change owner on the file
<span style="color:#d69015">chown owner-user file</span>
<br>
Change owner and group owner of the file 
<span style="color:#d69015">chown owner-user:owner-group of the file</span>
<br>
Change owner and group owner of the directory
<span style="color:#d69015">chown owner-user:owner-group of the direcotry</span>
<br>
<br>
<br>
<br>


## Hardware

Detected hardware and boot messages
<span style="color:#89e09d">dmesg</span>
<br>
CPU model
<span style="color:#89e09d">cat /proc/cpuinfo</span>
<br>
Hardware memory
<span style="color:#89e09d">cat /proc/meminfo</span>
<br>
Lists the number of interrupts per CPU per I/O device
<span style="color:#89e09d">lshw</span>
<br>
Displays Block device related information in Linux
<span style="color:#89e09d">lsblk</span>
<br>
Used and free memory (-m for MB)
<span style="color:#89e09d">free -m</span>
<br>
Show PCI devices
<span style="color:#89e09d">lspci -tv</span>
<br>
Show USB devices
<span style="color:#89e09d">lsusb -tv</span>
<br>
Show hardware info from BIOS
<span style="color:#89e09d">dmidecode</span>
<br>
Show Info about disk data
<span style="color:#89e09d">hdparm -l /dev/sda</span>
<br>
Do a read speed test on disk data
<span style="color:#89e09d">hdparm -tT /dev/sda</span>
<br>
Test for unreadable blocks on disk sda
<span style="color:#89e09d">badblocks -s /dev/sda</span>
<br>

<br>
<br>


## File commands

Display all information about files/directories
<span style="color:#5c469e">ls -la</span>
<br>
Show the path of the corrent directory
<span style="color:#5c469e">pwd</span>
<br>
Create new direcory
<span style="color:#5c469e">mkdir</span>
<br>
Delete file
<span style="color:#5c469e">rm</span>
<br>
Delete directory recursively
<span style="color:#5c469e">rm -r directory-name</span>
<br>
Forcefully remove directory recursively
<span style="color:#5c469e">rm -rf directory-name</span>
<br>
copy file 1 to file 2
<span style="color:#5c469e">cp file1 file2</span>
<br>
Copy dir 1 to dir 2, create if doesn't exist
<span style="color:#5c469e">cp -r dir 1 dir 2</span>
<br>
Rename source to dest
Move source to directory
<span style="color:#5c469e">mv file 1 file 2</span>
<br>
Create symbolic link to file-name
<span style="color:#5c469e">ln -s /path/to/file-name link-name</span>
<br>
Create or update file
<span style="color:#5c469e">touch file</span>
<br>
Place standard input into file
<span style="color:#5c469e">cat > file </span>
<br>
Output content of file
<span style="color:#5c469e">more file</span>
<br>
Output first 10 lines of file
<span style="color:#5c469e">head file</span>
<br>
Output last 10 lines of file
<span style="color:#5c469e">tail file</span>
<br>
Output contens of file as grows starting with the last 10 lines
<span style="color:#5c469e">tail -f file </span>
<br>
Encrypt file
<span style="color:#5c469e">gpg -c file</span>
<br>
Decrypt file
<span style="color:#5c469e">gpg file.gpg</span>
<br>
Print number of bytes, words and lines in file
<span style="color:#5c469e">wc</span>
<br>
Execute command lines from standard input
<span style="color:#5c469e">xargs</span>
<br>


<br>
<br>

## Process related
Display your current active processes
<span style="color:#ab0f46">ps</span>
<br>
Find all process id related to telnet process
<span style="color:#ab0f46">ps aux | grep "telnet"</span>
<br>
Memory map of process
<span style="color:#ab0f46">pmap</span>
<br>
Display all running processes
<span style="color:#ab0f46">top</span>
<br>
Kill process with mentioned pid
<span style="color:#ab0f46">kill pid</span>
<br>
Kill all processes named proc
<span style="color:#ab0f46">killall proc</span>
<br>
Send signal to a process with its name
<span style="color:#ab0f46">pkill process-name</span>
<br>
Resume suspended jobs without bringing them to foreground
<span style="color:#ab0f46">bg</span>
<br>
Brings the most recent jobs to foreground
<span style="color:#ab0f46">fg</span>
<br>
Brings job n to the foreground
<span style="color:#ab0f46">fg n</span>
<br>



<br>
<br>

## Direcory traverse

To go up on level of the directory tree
<span style="color:#3257a1">cd ..</span>
<br>
To go to $HOME directory
<span style="color:#3257a1">cd</span>
<br>
Change to /test directory
<span style="color:#3257a1">cd /test</span>
<br>


<br>
<br>

## Network

Display all network interfaces and ip address 
(a iproute2 comand, powerful than ifconfig)
<span style="color:#baa507">ip addr show</span>
<br>
Set ip address
<span style="color:#baa507">address and 192.168.0.1 dev eth0</span>
<br>
Linux tool to show ethernet status
<span style="color:#baa507">ethtool eth0</span>
<br>
Linux tool so thow ethernet status
<span style="color:#baa507">mii-tool eth0</span>
<br>
Send echo request to test connection
<span style="color:#baa507">ping host</span>
<br>
Get who is information for domain
<span style="color:#baa507">whois domain</span>
<br>
Get DNS information for domain
<span style="color:#baa507">dig domain</span>
<br>
Reverse lookup host
<span style="color:#baa507">dig -x domain</span>
<br>
Lookup DNS ip addresse for the name
<span style="color:#baa507">host google.com</span>
<br>
Lookup local ip address
<span style="color:#baa507">hostname -i</span>
<br>
Download file
<span style="color:#baa507">wget file</span>
<br>
Listing all active listening ports
<span style="color:#baa507">netstat -tupl</span>
<br>












future colors
3d8503
6c4987
a83200
3d2c8f
a7b02a


<span style="color:#3d8503">
Text content
</span>
