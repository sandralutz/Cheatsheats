# Linux

## System

Display Linux system information
```
uname -a
<br>
Display kernel release information
```
uname -r
```
<br>
Show how long the system has been running and loaded
```
uptime
```
<br>
Show system host name
```
hostname
```
<br>
Display the IP address of the host
```
hostname -l
```
<br>
Show system reboot history
```
last reboot
```
<br>
Show current date and time
```
date
```
<br>
Show this month's calendar
```
cal
```
<br>
Display who is online
```
w
```
<br>
Who you are logged in as
```
whoami
```
<br>
Display information about user
```
finger user
```

<br>
<br>


## Users

Show the active user id with login and group
```
id
```
<br>
Show last logins in the system
```
last
```
<br>
Show who is logged on the system
```
who
```
<br>
Add group "admin"
```
group add admin
```
<br>
g admin -m sam
Create user "sam"
```
useradd -c "Sam Tomshi"
```
<br>
Delete user sam
```
userdel sam
```
<br>
Add user sam
```
adduser sam
```
<br>
Modify user information
```
usermod
```
<br>
<br>



## File permission related

Change the permissions of file to octal
```
chmod octal file-name
```
<br>
#### example
Set rwx permission for owner, group and other
```
chmod 777
```
<br>
Set rwx permission for owner, rw for group and other
```
chmod 755
```
<br>
Change owner on the file
```
chown owner-user file
```
<br>
Change owner and group owner of the file 
```
chown owner-user:owner-group of the file
```
<br>
Change owner and group owner of the directory
```
chown owner-user:owner-group of the direcotry
```
<br>
<br>
<br>
<br>


## Hardware

Detected hardware and boot messages
```
dmesg
```
<br>
CPU model
```
cat /proc/cpuinfo
```
<br>
Hardware memory
```
cat /proc/meminfo
```
<br>
Lists the number of interrupts per CPU per I/O device
```
lshw
```
<br>
Displays Block device related information in Linux
```
lsblk
```
<br>
Used and free memory (-m for MB)
```
free -m
```
<br>
Show PCI devices
```
lspci -tv
```
<br>
Show USB devices
```
lsusb -tv
```
<br>
Show hardware info from BIOS
```
dmidecode
```
<br>
Show Info about disk data
```
hdparm -l /dev/sda
```
<br>
Do a read speed test on disk data
```
hdparm -tT /dev/sda
```
<br>
Test for unreadable blocks on disk sda
```
badblocks -s /dev/sda
```
<br>

<br>
<br>


## File commands

Display all information about files/directories
```
ls -la
```
<br>
Show the path of the corrent directory
```
pwd
```
<br>
Create new direcory
```
mkdir
```
<br>
Delete file
```
rm
```
<br>
Delete directory recursively
```
rm -r directory-name
```
<br>
Forcefully remove directory recursively
```
rm -rf directory-name
```
<br>
copy file 1 to file 2
```
cp file1 file2
```
<br>
Copy dir 1 to dir 2, create if doesn't exist
```
cp -r dir 1 dir 2
```
<br>
Rename source to dest
Move source to directory
```
mv file 1 file 2
```
<br>
Create symbolic link to file-name
```
ln -s /path/to/file-name link-name
```
<br>
Create or update file
```
touch file
```
<br>
Place standard input into file
```
cat > file 
```
<br>
Output content of file
```
more file
```
<br>
Output first 10 lines of file
```
head file
```
<br>
Output last 10 lines of file
```
tail file
```
<br>
Output contens of file as grows starting with the last 10 lines
```
tail -f file 
```
<br>
Encrypt file
```
gpg -c file
```
<br>
Decrypt file
```
gpg file.gpg
```
<br>
Print number of bytes, words and lines in file
```
wc
```
<br>
Execute command lines from standard input
```
xargs
```
<br>


<br>
<br>

## Process related
Display your current active processes
```
ps
```
<br>
Find all process id related to telnet process
```
ps aux | grep "telnet"
```
<br>
Memory map of process
```
pmap
```
<br>
Display all running processes
```
top
```
<br>
Kill process with mentioned pid
```
kill pid
```
<br>
Kill all processes named proc
```
killall proc
```
<br>
Send signal to a process with its name
```
pkill process-name
```
<br>
Resume suspended jobs without bringing them to foreground
```
bg
```
<br>
Brings the most recent jobs to foreground
```
fg
```
<br>
Brings job n to the foreground
```
fg n
```
<br>



<br>
<br>

## Direcory traverse

To go up on level of the directory tree
```
cd ..
```
<br>
To go to $HOME directory
```
cd
```
<br>
Change to /test directory
```
cd /test
```
<br>


<br>
<br>

## Network

Display all network interfaces and ip address 
(a iproute2 comand, powerful than ifconfig)
```
ip addr show
```
<br>
Set ip address
```
address and 192.168.0.1 dev eth0
```
<br>
Linux tool to show ethernet status
```
ethtool eth0
```
<br>
Linux tool so thow ethernet status
```
mii-tool eth0
```
<br>
Send echo request to test connection
```
ping host
```
<br>
Get who is information for domain
```
whois domain
```
<br>
Get DNS information for domain
```
dig domain
```
<br>
Reverse lookup host
```
dig -x domain
```
<br>
Lookup DNS ip addresse for the name
```
host google.com
```
<br>
Lookup local ip address
```
hostname -i
```
<br>
Download file
```
wget file
```
<br>
Listing all active listening ports
```
netstat -tupl
```
<br>












future colors
3d8503
6c4987
a83200
3d2c8f
a7b02a


```

Text content

```
