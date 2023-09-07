# Linux

## System

Display Linux system information
<mark style="background-color: #d65cad">uname -a</mark>  
<br>
Display kernel release information
<mark style="background-color: #d65cad">uname -r</mark>  
<br>
Show how long the system has been running and loaded
<mark style="background-color: #d65cad">uptime</mark>  
<br>
Show system host name
<mark style="background-color: #d65cad">hostname</mark>  
<br>
Display the IP address of the host
<mark style="background-color: #d65cad">hostname -l</mark>  
<br>
Show system reboot history
<mark style="background-color: #d65cad">last reboot</mark>  
<br>
Show current date and time
<mark style="background-color: #d65cad">date</mark>  
<br>
Show this month's calendar
<mark style="background-color: #d65cad">cal</mark>  
<br>
Display who is online
<mark style="background-color: #d65cad">w</mark>  
<br>
Who you are logged in as
<mark style="background-color: #d65cad">whoami</mark>  
<br>
Display information about user
<mark style="background-color: #d65cad">finger user</mark>  

<br>
<br>


## Users

Show the active user id with login and group
<mark style="background-color: #038ca1">id</mark>  
<br>
Show last logins in the system
<mark style="background-color: #038ca1">last</mark>  
<br>
Show who is logged on the system
<mark style="background-color: #038ca1">who</mark>  
<br>
Add group "admin"
<mark style="background-color: #038ca1">group add admin</mark>  
<br>
g admin -m sam
Create user "sam"
<mark style="background-color: #038ca1">useradd -c "Sam Tomshi"</mark>  
<br>
Delete user sam
<mark style="background-color: #038ca1">userdel sam</mark>  
<br>
Add user sam
<mark style="background-color: #038ca1">adduser sam</mark>  
<br>
Modify user information
<mark style="background-color: #038ca1">usermod</mark>  
<br>
<br>



## File permission related

Change the permissions of file to octal
<mark style="background-color: #d69015">chmod octal file-name</mark>  
<br>
#### example
Set rwx permission for owner, group and other
<mark style="background-color: #d69015">chmod 777</mark>  
<br>
Set rwx permission for owner, rw for group and other
<mark style="background-color: #d69015">chmod 755</mark>  
<br>
Change owner on the file
<mark style="background-color: #d69015">chown owner-user file</mark>  
<br>
Change owner and group owner of the file 
<mark style="background-color: #d69015">chown owner-user:owner-group of the file</mark>  
<br>
Change owner and group owner of the directory
<mark style="background-color: #d69015">chown owner-user:owner-group of the direcotry</mark>  
<br>
<br>
<br>
<br>


## Hardware

Detected hardware and boot messages
<mark style="background-color: #89e09d">dmesg</mark>  
<br>
CPU model
<mark style="background-color: #89e09d">cat /proc/cpuinfo</mark>  
<br>
Hardware memory
<mark style="background-color: #89e09d">cat /proc/meminfo</mark>  
<br>
Lists the number of interrupts per CPU per I/O device
<mark style="background-color: #89e09d">lshw</mark>  
<br>
Displays Block device related information in Linux
<mark style="background-color: #89e09d">lsblk</mark>  
<br>
Used and free memory (-m for MB)
<mark style="background-color: #89e09d">free -m</mark>  
<br>
Show PCI devices
<mark style="background-color: #89e09d">lspci -tv</mark>  
<br>
Show USB devices
<mark style="background-color: #89e09d">lsusb -tv</mark>  
<br>
Show hardware info from BIOS
<mark style="background-color: #89e09d">dmidecode</mark>  
<br>
Show Info about disk data
<mark style="background-color: #89e09d">hdparm -l /dev/sda</mark>  
<br>
Do a read speed test on disk data
<mark style="background-color: #89e09d">hdparm -tT /dev/sda</mark>  
<br>
Test for unreadable blocks on disk sda
<mark style="background-color: #89e09d">badblocks -s /dev/sda</mark>  
<br>

<br>
<br>


## File commands

Display all information about files/directories
<mark style="background-color: #5c469e">ls -la</mark>  
<br>
Show the path of the corrent directory
<mark style="background-color: #5c469e">pwd</mark>  
<br>
Create new direcory
<mark style="background-color: #5c469e">mkdir</mark>  
<br>
Delete file
<mark style="background-color: #5c469e">rm</mark>  
<br>
Delete directory recursively
<mark style="background-color: #5c469e">rm -r directory-name</mark>  
<br>
Forcefully remove directory recursively
<mark style="background-color: #5c469e">rm -rf directory-name</mark>  
<br>
copy file 1 to file 2
<mark style="background-color: #5c469e">cp file1 file2</mark>  
<br>
Copy dir 1 to dir 2, create if doesn't exist
<mark style="background-color: #5c469e">cp -r dir 1 dir 2</mark>  
<br>
Rename source to dest
Move source to directory
<mark style="background-color: #5c469e">mv file 1 file 2</mark>  
<br>
Create symbolic link to file-name
<mark style="background-color: #5c469e">ln -s /path/to/file-name link-name</mark>  
<br>
Create or update file
<mark style="background-color: #5c469e">touch file</mark>  
<br>
Place standard input into file
<mark style="background-color: #5c469e">cat > file </mark>  
<br>
Output content of file
<mark style="background-color: #5c469e">more file</mark>  
<br>
Output first 10 lines of file
<mark style="background-color: #5c469e">head file</mark>  
<br>
Output last 10 lines of file
<mark style="background-color: #5c469e">tail file</mark>  
<br>
Output contens of file as grows starting with the last 10 lines
<mark style="background-color: #5c469e">tail -f file </mark>  
<br>
Encrypt file
<mark style="background-color: #5c469e">gpg -c file</mark>  
<br>
Decrypt file
<mark style="background-color: #5c469e">gpg file.gpg</mark>  
<br>
Print number of bytes, words and lines in file
<mark style="background-color: #5c469e">wc</mark>  
<br>
Execute command lines from standard input
<mark style="background-color: #5c469e">xargs</mark>  
<br>


<br>
<br>

## Process related
Display your current active processes
<mark style="background-color: #ab0f46">ps</mark>  
<br>
Find all process id related to telnet process
<mark style="background-color: #ab0f46">ps aux | grep "telnet"</mark>  
<br>
Memory map of process
<mark style="background-color: #ab0f46">pmap</mark>  
<br>
Display all running processes
<mark style="background-color: #ab0f46">top</mark>  
<br>
Kill process with mentioned pid
<mark style="background-color: #ab0f46">kill pid</mark>  
<br>
Kill all processes named proc
<mark style="background-color: #ab0f46">killall proc</mark>  
<br>
Send signal to a process with its name
<mark style="background-color: #ab0f46">pkill process-name</mark>  
<br>
Resume suspended jobs without bringing them to foreground
<mark style="background-color: #ab0f46">bg</mark>  
<br>
Brings the most recent jobs to foreground
<mark style="background-color: #ab0f46">fg</mark>  
<br>
Brings job n to the foreground
<mark style="background-color: #ab0f46">fg n</mark>  
<br>



<br>
<br>

## Direcory traverse

To go up on level of the directory tree
<mark style="background-color: #3257a1">cd ..</mark>  
<br>
To go to $HOME directory
<mark style="background-color: #3257a1">cd</mark>  
<br>
Change to /test directory
<mark style="background-color: #3257a1">cd /test</mark>  
<br>


<br>
<br>

## Network

Display all network interfaces and ip address 
(a iproute2 comand, powerful than ifconfig)
<mark style="background-color: #baa507">ip addr show</mark>  
<br>
Set ip address
<mark style="background-color: #baa507">address and 192.168.0.1 dev eth0</mark>  
<br>
Linux tool to show ethernet status
<mark style="background-color: #baa507">ethtool eth0</mark>  
<br>
Linux tool so thow ethernet status
<mark style="background-color: #baa507">mii-tool eth0</mark>  
<br>
Send echo request to test connection
<mark style="background-color: #baa507">ping host</mark>  
<br>
Get who is information for domain
<mark style="background-color: #baa507">whois domain</mark>  
<br>
Get DNS information for domain
<mark style="background-color: #baa507">dig domain</mark>  
<br>
Reverse lookup host
<mark style="background-color: #baa507">dig -x domain</mark>  
<br>
Lookup DNS ip addresse for the name
<mark style="background-color: #baa507">host google.com</mark>  
<br>
Lookup local ip address
<mark style="background-color: #baa507">hostname -i</mark>  
<br>
Download file
<mark style="background-color: #baa507">wget file</mark>  
<br>
Listing all active listening ports
<mark style="background-color: #baa507">netstat -tupl</mark>  
<br>












future colors
3d8503
6c4987
a83200
3d2c8f
a7b02a
