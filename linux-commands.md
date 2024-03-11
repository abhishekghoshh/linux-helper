# linux most used commands cheetsheet

#### custom shortcuts 
```
# this will fuzzyfind any commands manual page
compgen -c | fzf | xargs man
```

```
apt-get update & apt-get upgrade -y
```

```
# sudo - execute a command as another user or with elevated privileges
# Run command with the security privileges of the superuser (Super User DO)
sudo

# whoami - display the current user name
whoami

# Show the user you are logged in as and the groups you are part of
id

# Show the groups you are part of
groups

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
# To navigate and search 
ctrl + f
ctrl + b
g
G
/string  -> search
h  -> to display help
q  -> for quit

man –k ifconfig  -> Search all man files for ifconfig
man –k "copy files"   -> Search all man files for the sting in quotes
```


```
# Clears the screen
clear

# Resets the terminal display
reset

# history - display a list of previously executed commands,
history

# Shows the stuff typed - add a number to limit the last n items
history n

!<history-number-of-command>
!102

HISTTIMEFORMAT="%Y-%m-%d %T "
add this variable to .bashrc/.zshrc to make it permenant


# Interactively search through previously typed commands
ctrl + r

# to forward search (works in ZSH for me but not bash)
ctrl + s

# Execute the last command typed that starts with 'value'
![value]

# Print to the console the last command typed that starts with 'value'
![value]:p

# execute previous command
!!

# Print to the console the last command typed
!!:p

# execute previous command in sudo mode
sudo !!





# Run command A and then B, regardless of success of A
[command-a]; [command-b]

# Run command B if A succeeded
[command-a] && [command-b]

# Run command B if A failed
[command-a] || [command-b]

# Run command A in background
[command-a] &

# Run command A and then pass the result to command B e.g ps auxwww | grep google
[command-a] | [command-b]


# open line in the editor
ctrl + x then ctrl + e



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

# in a list format
ls -l
ls -l <file-name>

# Long listing of parent directory
ls -l ..

# -a means files in the current directory including hidden files
ls -a

# all files in list format
ls -al

# Long listing with Human readable file sizes
ls -lh

# Entire content of folder recursively
ls -R

# list files in /etc
ls /etc
# List files in the /var directory
ls -a /var/



# tee - redirect output to both a file and the console
ls | tee file.txt

```

#### Traverse directory
```
# pwd - print the current working directory
pwd

# cd - change the current directory

# go to Home directory
cd

# Change directory e.g. cd Documents
cd [folder]
cd /usr/bin
cd /<click-tab>

# go to Home directory
cd ~

# go to the root of drive
cd /

# go to the previous directory
cd -

# Move 1 levels up
cd ../




pushd <dir-name>
popd <dir-name>


# root directory and user directory marker

# . respresent Current folder, e.g. ls .
# .. resposent Parent/enclosing directory, e.g. ls ..

```

```
# Opens a file ( as if you double clicked it )
open .
xdg-open

# Opens the file using the nano editor
nano [file]

# Opens the file using the vim editor
vim [file]


# touch - create a new empty file or update the timestamp of an existing file
touch <file-name>
touch <file-name-1> <file-name-2>
touch <file-name>{0..10}
touch <already-existed-file> # do not update anything just change the modified timestamp
touch shayan.txt


# echo - display text or variables to the console
echo "hello world"
# single arrow (>) will override the content
echo "hello world" > test.txt
# double arrow (>>) will append the content
echo "hello world" >> test.txt


truncate -s 0 <file-name>

# rm - remove files or directories
rm <file-name>

# -v for verbose
rm -v <file-name>
rm <file-name-1> <file-name-2>
rm example.txt

# -r for recusrive, delete directly and all its contents, Remove a directory and contents
rm -r <non-empty-dir>

# -i for interactive, Remove with confirmation
rm -ri <non-empty-dir>

# Force removal without confirmation
rm -f [file]

# this command will delete everything in the system
rm -rf /


# mkdir - create a new directory
mkdir <dir-name>

# Create a new directory called test
mkdir test

# -p will create all the nested folders if that is not present already 
mkdir -p /dir1/dir2/dir3

# Make directory and subdirectory in a single command
mkdir -p test2/test2

#  Make multiple directories
mkdir test2 test3 

# rmdir - remove a directory
rmdir <dir-name>

# Deletes the text.txt file in the directory called test
rmr test/text.txt


# cp - copy files or directories, Copy file to directory
cp [file] [dir]
cp <file-name> <file-name-with-path>

# Copies text.txt to a new file called text2.txt, Overwrites the existing text2.txt with a copy of text.txt
cp [file] [newfile]
cp text.txt text2.txt

# copy dir-1 content to dir-1-copy folder, -r is needed as folder is not empty
cp -r <dir-1> <dir-1-copy>


# mv - move or rename files or directories, Move/Rename, e.g. mv file1.ad /tmp
mv <file-name> <file-name-with-path>
mv <file-name> <new-file-name>
mv [file] [new filename]
mv example.txt backup/

# Moves text.txt to a different directory
mv text.txt test/

# Moves all txt files to a different directory
mv *.txt test/



# List all files and subfolders and files within subfolders within the test directory
tree /etc
```

```
# cat - concatenate and display files, Concatenate to screen
cat <file-name>
cat <file-name> | sort
cat example.txt
cat <file-1> <file-2> <file-3>
cat <file-1> <file-2> <file-3> > <file-name>


# Copies file contents to clipboard
pbcopy < [file]

# Paste clipboard contents
pbpaste

# Paste clipboard contents into file, pbpaste > paste-test.txt
pbpaste > [file]


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
head cloud-init.log  -> Displays the first 10 lines of the file
head -n 5 cloud-init.log  -> Displays the first 5 lines of the file


# display last 10 lines
tail <file-name>
tail -f <file-name>


cmp <file-name-1> <file-name-2>

# Compares the two text files
diff <file-name-1> <file-name-2>
```


```
# find the files in a directory
find <dir-name> -name <name-of-file>
find <other-parameters>
# Searches within /var and subdirectories
find /var -name *.log

# locate - locate any file on the system
locate file.txt
locate cloud-init.log  -> Displays directory containing cloud-init.log
locate -I cloud-init.log  -> Displays directory containing cloud-init.log and ignores cas
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
# ifconfig - display or configure network interfaces, Display all network interfaces
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


# ping - test network connectivity, Test the destination at 8.8.8.8 by sending ICMP packets
ping <ip-address>
ping 8.8.8.8
ping -c 5 8.8.8.8    ->   # Test the destination at 8.8.8.8 by sending five ICMP packets



traceroute <url>


# netstat - display network connection information
netstat
netstat -tulpn
netstat -r   ->  Display the route table
netstat -np | grep "80"   -> isplay open connections for a specific port

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
# df - display disk space usage, free space on storage devices
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


# top - display system resource usage and processes, Displays active processes. Press q to quit
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



```
# Sed command is mostly used to replace the text in a file
sed <pattern-or-text> <file-name>

echo 'Hello, world!' | sed 's/world/universe'   => Hello, universe!


# search in a text or file
# Displays any lines of the file ssh_config that include the term user
grep user /etc/ssh/ssh_config
# Use quotes if the string has spaces, -i option: Ignore upper/lower case
grep -i "COMMAND LINE" /etc/ssh/ssh_config
grep -R 127.0.0.1 /etc/  -> Search all files in the etc directory
grep user /etc/ssh/ssh_config > sample.txt  -> Sends search results to a text file
ls | grep crontab


awk

sed

rsync
```