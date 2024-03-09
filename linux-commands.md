# linux most used commands cheetsheet

```
apt-get update & apt-get upgrade -y
```

```
# sudo - execute a command as another user or with elevated privileges
sudo

# whoami - display the current user name
whoami

# useradd - add a new user to the system
sudo useradd <user-name>
sudo adduser <user-name> <other-parameters>
useradd harry

# su - switch user to become another user
su <user-name>
su john

exit

# passwd - change the password for a user
sudo passwd <user-name>

# userdel - delete a user from the system
userdel harry


# finger - displays all the information about user
apt-get install finger
finger <user-name>


# which - locate a program or command in the system path
which <command-name>
which vim

where <command-name>
whatis <command-name>
whereis <command-name>
```

```
# man - manual for a command
# the synopsis section under man output gives the syntax of the command
man <command-name>
man ls
```


```
clear

reset

# history - display a list of previously executed commands
history
!<history-number-of-command>
!102

HISTTIMEFORMAT="%Y-%m-%d %T "
add this variable to .bashrc/.zshrc to make it permenant


<cmd-1> && <cmd-2>
<cmd-1>;<cmd-2>;

# matrix style animation in command line
cmatrix

# zoom in to the command prompt
ctrl +
# zoom out in the command prompt
ctrl -

```


```

# ls - list the files and directories in the current directory
ls
ls -l
ls -l <file-name>
ls -a
ls -al
ls /etc

# tee - redirect output to both a file and the console
ls | tee file.txt

# pwd - print the current working directory
pwd


# cd - change the current directory
cd
cd /usr/bin
cd /<click-tab>


cd ../
cd -
cd ~


pushd <dir-name>
popd <dir-name>


# root directory and user directory marker


open .
xdg-open

# touch - create a new empty file or update the timestamp of an existing file
touch <file-name>
touch <file-name-1> <file-name-2>
touch <file-name>{0..10}
touch <already-existed-file> # do not update anything just change the modified timestamp
touch shayan.txt


# echo - display text or variables to the console
echo "hello world"
echo "hello world" > test.txt
echo "hello world" >> test.txt


truncate -s 0 <file-name>

# rm - remove files or directories
rm <file-name>
rm -v <file-name> # -v for verbose
rm <file-name-1> <file-name-2>
rm example.txt
rm -r <non-empty-dir> # -r for recusrive, delete directly and all its contents
rm -ri <non-empty-dir> # -i for interactive


# mkdir - create a new directory
mkdir <dir-name>
# -p will create all the nested folders if that is not present already 
mkdir -p /dir1/dir2/dir3

# rmdir - remove a directory
rmdir <dir-name>


# cp - copy files or directories
cp <file-name> <file-name-with-path>
cp -r <dir-1> <dir-1-copy> # copy dir-1 content to dir-1-copy folder, -r is needed as folder is not empty


# mv - move or rename files or directories
mv <file-name> <file-name-with-path>
mv <file-name> <new-file-name>
mv example.txt backup/
```

```
# cat - concatenate and display files
cat <file-name>
cat <file-name> | sort
cat example.txt
cat <file-1> <file-2> <file-3>
cat <file-1> <file-2> <file-3> > <file-name>



# sort - sort lines of text in a file or input
cat file.txt
# banana
# orange
# apple
sort file.txt
# apple
# banana
# orange

sort -n numeric-files # -n for numberic values


# uniq - remove duplicate lines from a file or input
cat file.txt
# apple
# orange
# banana
# apple
# banana
uniq file.txt
# apple
# orange
# banana



less <file-name>


# head/tail - display the first/last few lines of a file or input

# display first 10 lines
head <file-name>
head -f <file-name>
head file.txt


# display last 10 lines
tail <file-name>
tail -f <file-name>


cmp <file-name-1> <file-name-2>
diff <file-name-1> <file-name-2>
```


```
find <dir-name> -name <name-of-file>
find <other-parameters>

# locate - locate any file on the system
locate file.txt
```

```
# file permissions
# The first digit represents the owner of the file/directory
# The second digit represents the group that the file/directory belongs to
# The third digit represents all other users
# 0 (no permission)
# 1 (execute only)
# 2 (write only)
# 3 (write and execute)
# 4 (read only)
# 5 (read and execute)
# 6 (read and write)
# 7 (read, write, and execute)

# chmod - change the permissions of a file or directory
chmod <file-name> <file-mod>
chmod +x <file-name>
chmod 700 file.txt

# chown - change the owner of a file or directory
chown <user-name> <file-name>
chown new_owner example.txt
```


```
# ifconfig - display or configure network interfaces
ifconfig
ip address
ip address | grep eth0
ip address | grep eth0 | grep inet
ip address | grep eth0 | grep inet | awk '{print $2}
```

```
# ssh - connect to a remote server securely
ssh username@ip-address

# scp - securely copy files between systems
scp myfile.txt user@remotehost:/home/user/
```

```
# for dns
cat /etc/resolv.conf
resolvectl status


# ping - test network connectivity
ping <ip-address>
ping 8.8.8.8
ping google.com -c 8



traceroute <url>


# netstat - display network connection information
netstat
netstat -tulpn

ss 
ss -tulpn


# route - view or configure network routing tables
route [options] [add/delete/show]


# allow port 80 to the system
sudo ufw allow 80
sudo ufw enable
sudo ufw status


wget <downloadable-url>

curl <url>
curl <downloadable-url> > <file-name>
```

```
# uname - display system information
uname
uname -r
uname -a
```


```
free
```

```
# df - display disk space usage
df
df -H

# du - display disk usage by file or directory
du

# mount - mount a file system
mount
mount | column -t
sudo mount /dev/sdb1 /mnt/usb

# umount - unmount a file system
sudo umount /mnt/usb
```

```
# ps - display information about running processes
ps
ps aux


# top - display system resource usage and processes
top
# htop - an interactive process viewer and system monitor in a human readable format
htop

# kill - terminate a process
kill [PID]

# kill can take different flags, -9 is for SIGKILL, -15 is for SIGTERM
# -9 for forcefull termination, -15 is for gracefull shutdown
kill -9 <process-id>
kill -15 <process-id>

# -l to list all the flags
kill -l

killall

pkill -f <process-name>
```



```
job
ctrl + z


bg

fg

# & is to run the command in background
<command-name> &

```
```
# tar create or extract compressed archive files
# x: extract files from an archive
# t: list the contents of an archive
# r: append files to an existing archive
# z: use gzip compression
# j: use bzip2 compression
# cf: create file
# xf: extract file
tar cf archive.tar file1 file2 file3

zip <zip-file-name> <content-file-or-folder>
unzip <zip-file-name>


# gzip - compress files
gzip file.txt

# gunzip - decompress compressed files
gunzip file.txt.gz
```

```
# systemctl - control system services and settings

# Start the nginx service
sudo systemctl start <service-name>

# Check the status of the nginx service
sudo systemctl status <service-name>

# Stop the nginx service
sudo systemctl stop <service-name>


systemctl start nginx
systemctl status nginx
systemctl stop nginx


# service - control system serv
service apache2 start
```

```
# uptime - display system uptime and load average
uptime

sudo reboot
sudo shutdown -h now


# date - display or set the system date and time
date
```


```

neofetch
```

```
# edit the ~/.bash_prompt to create custom prompt in command line
# find the sample prompt here https://www.learnlinux.tv/10-linux-terminal-tips-and-tricks-to-enhance-your-workflow/
# add that into .bashrc/.zshrc and comment out the PS1 command 
# add the source ~/.bash_prompt
```