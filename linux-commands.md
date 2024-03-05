# linux most used commands cheetsheet

apt-get update & apt-get upgrade -y



whoami

sudo useradd <user-name>
sudo adduser <user-name> <other-parameters>

su <user-name>
exit

sudo passwd <user-name>

apt-get install finger
finger <user-name>


where <command-name>
whatis <command-name>
whereis <command-name>


man <command-name>


ctrl + c
ctrl + z
fg

ctrl + u
ctrl + a
ctrl + e

<cmd-1> && <cmd-2>
<cmd-1>;<cmd-2>;

sudo !!

clear
ctrl + l / cmd + k

reset

history
!<history-number-of-command>
HISTTIMEFORMAT="%Y-%m-%d %T "
add this variable to .bashrc/.zshrc to make it permenant


ls
ls -l
ls -l <file-name>
ls -a
ls -al

pwd

cd
cd /usr/bin
cd ../
cd /<click-tab>
cd -
cd ~

pushd <dir-name>
popd <dir-name>

// root directory and user directory marker
touch <file-name>
touch <file-name>{0..10}

echo "hello world"
echo "hello world" > test.txt
echo "hello world" >> test.txt

truncate -s 0 <file-name>

rm <file-name>

mkdir <dir-name>
rmdir <dir-name>
rm -r <non-empty-dir>

cp <file-name> <file-name-with-path>

mv <file-name> <file-name-with-path>
mv <file-name> <new-file-name>


cat <file-name>
cat <file-name> | sort

less <file-name>

head <file-name>
head -f <file-name>

tail <file-name>
tail -f <file-name>


cmp <file-name-1> <file-name-2>
diff <file-name-1> <file-name-2>


find <dir-name> -name <name-of-file>
find <other-parameters>

// file permissions
chmod <file-name> <file-mod>
chmod +x <file-name>

chown <user-name> <file-name>


ifconfig
ip address
ip address | grep eth0
ip address | grep eth0 | grep inet
ip address | grep eth0 | grep inet | awk '{print $2}

// for dns
cat /etc/resolv.conf
resolvectl status

ping <ip-address>

traceroute <url>

netstat
netstat -tulpn

ss 
ss -tulpn

// allow port 80 to the system
sudo ufw allow 80
sudo ufw enable
sudo ufw status

uname
uname -r
uname -a


mount
mount | column -t

wget <downloadable-url>

curl <url>
curl <downloadable-url> > <file-name>

ssh username@ip-address


free

df
df -H

ps
ps -aux

top
htop

// -9 for forcefull termination
kill -9 <process-id>

pkill -f <process-name>



zip <zip-file-name> <content-file-or-folder>
unzip <zip-file-name>


sudo systemctl start <service-name>
sudo systemctl sudo <service-name>
sudo systemctl stop <service-name>


sudo reboot
sudo shutdown -h now