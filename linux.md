# Linux

### Hegedoc
https://hedgedoc.groot.rocks/s/4hccyGqSJ

## System

Display Linux system information
``` 
uname -a  
```
Display kernel release information
``` 
uname -r  
```
Show how long the system has been running and loaded
``` 
uptime  
```
Show system host name
``` 
hostname  
```
Display the IP address of the host
``` 
hostname -l  
```
Show system reboot history
``` 
last reboot  
```
Show current date and time
``` 
date  
```
Show this month's calendar
``` 
cal  
```
Display who is online
``` 
w  
```
Who you are logged in as
``` 
whoami  
```
Display information about user
``` 
finger user  

```
```


## Users

Show the active user id with login and group
``` 
id  
```
Show last logins in the system
``` 
last  
```
Show who is logged on the system
``` 
who  
```
Add group "admin"
``` 
group add admin  
```
g admin -m sam
Create user "sam"
``` 
useradd -c "Sam Tomshi"  
```
Delete user sam
``` 
userdel sam  
```
Add user sam
``` 
adduser sam  
```
Modify user information
``` 
usermod  
```
```



## File permission related

Change the permissions of file to octal
``` 
chmod octal file-name  
```
#### example
Set rwx permission for owner, group and other
``` 
chmod 777  
```
Set rwx permission for owner, rw for group and other
``` 
chmod 755  
```
Change owner on the file
``` 
chown owner-user file  
```
Change owner and group owner of the file 
``` 
chown owner-user:owner-group of the file  
```
Change owner and group owner of the directory
``` 
chown owner-user:owner-group of the direcotry  
```
```

## Hardware

Detected hardware and boot messages
``` 
dmesg  
```
CPU model
``` 
cat /proc/cpuinfo  
```
Hardware memory
``` 
cat /proc/meminfo  
```
Lists the number of interrupts per CPU per I/O device
``` 
lshw  
```
Displays Block device related information in Linux
``` 
lsblk  
```
Used and free memory (-m for MB)
``` 
free -m  
```
Show PCI devices
``` 
lspci -tv  
```
Show USB devices
``` 
lsusb -tv  
```
Show hardware info from BIOS
``` 
dmidecode  
```
Show Info about disk data
``` 
hdparm -l /dev/sda  
```
Do a read speed test on disk data
``` 
hdparm -tT /dev/sda  
```
Test for unreadable blocks on disk sda
``` 
badblocks -s /dev/sda  
```

```
```


## File commands

Display all information about files/directories
``` 
ls -la  
```
Show the path of the corrent directory
``` 
pwd  
```
Create new direcory
``` 
mkdir  
```
Delete file
``` 
rm  
```
Delete directory recursively
``` 
rm -r directory-name  
```
Forcefully remove directory recursively
``` 
rm -rf directory-name  
```
copy file 1 to file 2
``` 
cp file1 file2  
```
Copy dir 1 to dir 2, create if doesn't exist
``` 
cp -r dir 1 dir 2  
```
Rename source to dest
Move source to directory
``` 
mv file 1 file 2  
```
Create symbolic link to file-name
``` 
ln -s /path/to/file-name link-name  
```
Create or update file
``` 
touch file  
```
Place standard input into file
``` 
cat > file   
```
Output content of file
``` 
more file  
```
Output first 10 lines of file
``` 
head file  
```
Output last 10 lines of file
``` 
tail file  
```
Output contens of file as grows starting with the last 10 lines
``` 
tail -f file   
```
Encrypt file
``` 
gpg -c file  
```
Decrypt file
``` 
gpg file.gpg  
```
Print number of bytes, words and lines in file
``` 
wc  
```
Execute command lines from standard input
``` 
xargs  
```


```
```

## Process related
Display your current active processes
``` 
ps  
```
Find all process id related to telnet process
``` 
ps aux | grep "telnet"  
```
Memory map of process
``` 
pmap  
```
Display all running processes
``` 
top  
```
Kill process with mentioned pid
``` 
kill pid  
```
Kill all processes named proc
``` 
killall proc  
```
Send signal to a process with its name
``` 
pkill process-name  
```
Resume suspended jobs without bringing them to foreground
``` 
bg  
```
Brings the most recent jobs to foreground
``` 
fg  
```
Brings job n to the foreground
``` 
fg n  
```



```
```

## Direcory traverse

To go up on level of the directory tree
``` 
cd ..  
```
To go to $HOME directory
``` 
cd  
```
Change to /test directory
``` 
cd /test  
```


```
```

## Network

Display all network interfaces and ip address 
(a iproute2 comand, powerful than ifconfig)
``` 
ip addr show  
```
Set ip address
``` 
address and 192.168.0.1 dev eth0  
```
Linux tool to show ethernet status
``` 
ethtool eth0  
```
Linux tool so thow ethernet status
``` 
mii-tool eth0  
```
Send echo request to test connection
``` 
ping host  
```
Get who is information for domain
``` 
whois domain  
```
Get DNS information for domain
``` 
dig domain  
```
Reverse lookup host
``` 
dig -x domain  
```
Lookup DNS ip addresse for the name
``` 
host google.com  
```
Lookup local ip address
``` 
hostname -i  
```
Download file
``` 
wget file  
```
Listing all active listening ports
``` 
netstat -tupl  
```
```
## Login (SSH and Telnet)

Connect to host as user
``` 
ssh user@host  
```
Connect to host using specific port
``` 
ssh -p port user@host  
```
Connect to the system using telnet port
``` 
telnet host  
```
```
## Compression / Archives

Create tar named home.tar containing home/
``` 
tar cf home.tar home  
```
Extract the files from file.tar
``` 
tar xf home.tar home  
```
Create a tar with gzip compression
``` 
tar czf file.tar.gz  
```
Compress file and renames it to file.gz
``` 
gzip file  
```
```

## File transfer

Secure Copy
``` 
scp  
```
Secure copy file.txt to remote host /tmp folder rsync
``` 
scp file.txt server2:/tmp  
```
Synchronize source to destination
``` 
rsync -a /home/apps/backup/  
```

###  Disk usage


Show free space on mounted filesystem
``` 
df -h  
```
Show free inodes on mounted filesystem
``` 
df -i  
```
Show disks partitions sizes and types
``` 
fdisk -l  
```
Display disk usage in human readable from
``` 
du -ah  
```
Display total disk usage on the current directory 
``` 
du -sh  
```
Displays target mount point for all filesystems
``` 
findmnt  
```
Mount a device
``` 
mount device-path mount-point 
```


## Search
Search for pattern in files
``` 
grep pattern files  
```
Search recursively for pattern in dir
``` 
grep -r pattern dir  
```
Find all instances of file
``` 
locate file  
```
Find file names that start  with "index"
``` 
find /home/tom -name "index"  
```
Find files larger than 1000k in /home
``` 
find /home -size +10000k  
```

## Install from source 

``` 
./configure  
```
``` 
make  
```
``` 
make install  
```

## Install package
Install rpm based packages
``` 
rpm -i pkgname.rpm
```
Remove package
``` 
rpm -e pkgname
