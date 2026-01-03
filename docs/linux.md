

# Linux Shell Commands – Cheat Sheet

> Scope: Bash-compatible shells on Linux  
> Goal: Fast lookup for real-world usage (admins, devs, DevOps)

---

## 0. Shell Basics
```bash
bash            # Start bash shell
exec command    # Replace current shell
exit            # Exit shell
```

---

## 1. Navigation

```bash
pwd
ls
ls -lah --group-directories-first
cd /path
cd ..
cd -
pushd dir
popd
dirs
```

---

## 2. Files & Directories

```bash
touch file
stat file
file file
mkdir dir
mkdir -p a/b/c
rmdir dir
cp src dst
cp -a src dst
mv src dst
rm file
rm -r dir
rm -rf dir
```

---

## 3. Viewing Files

```bash
cat file
tac file
less file
nl file
head -n 20 file
tail -n 20 file
tail -f file
watch -n 1 command
```

---

## 4. Search & Locate

```bash
grep "text" file
grep -rin "text" dir
grep -E "a|b" file
grep -v "pattern" file

find /path -name "*.log"
find . -type f -size +100M
find . -mtime -1

locate filename
updatedb
```

---

## 5. Text Processing (Core Linux Power)

### sed

```bash
sed 's/old/new/' file
sed 's/old/new/g' file
sed -i 's/old/new/g' file
sed -n '5,10p' file
```

### awk

```bash
awk '{print $1}' file
awk -F: '{print $1}' /etc/passwd
awk '$3 > 1000' file
```

### sort / uniq / cut / tr

```bash
sort file
sort -nr file
uniq
uniq -c
cut -d: -f1 file
tr 'a-z' 'A-Z'
```

---

## 6. Permissions & Ownership

```bash
ls -l
chmod 644 file
chmod 755 file
chmod -R 755 dir
chmod u+x script.sh
chown user file
chown user:group file
chown -R user:group dir
```

### Permission Numbers

* r = 4
* w = 2
* x = 1

---

## 7. Users & Groups

```bash
whoami
id
groups
who
w
last

useradd user
usermod -aG group user
userdel user
passwd user

groupadd group
groupdel group
```

---

## 8. Processes & Job Control

```bash
ps
ps aux
top
htop
atop

kill PID
kill -9 PID
pkill process
pgrep process

command &
jobs
fg %1
bg %1
disown
```

---

## 9. System Info

```bash
uname -a
hostname
uptime
free -h
vmstat
iostat
lsblk
mount
mount | column -t
```

---

## 10. Disk & Filesystems

```bash
df -h
du -sh dir
du -ah | sort -h

mount /dev/sdb1 /mnt
umount /mnt

blkid
fsck /dev/sda1
```

---

## 11. Networking

```bash
ip a
ip r
ss -tulnp
ping host
traceroute host

curl url
curl -I url
curl -X POST -d "a=b" url
wget url

nmcli
```

---

## 12. Archives & Compression

```bash
tar -cvf file.tar dir
tar -xvf file.tar
tar -czvf file.tar.gz dir
tar -xzvf file.tar.gz

gzip file
gunzip file.gz
zip -r file.zip dir
unzip file.zip
```

---

## 13. Package Management

### Debian / Ubuntu

```bash
apt update
apt upgrade
apt install pkg
apt remove pkg
apt purge pkg
apt search pkg
```

### RedHat / Fedora

```bash
dnf install pkg
dnf remove pkg
dnf search pkg
```

---

## 14. Environment Variables

```bash
env
printenv
export VAR=value
unset VAR
echo $VAR
source file
```

---

## 15. Bash Built-ins & Expansion

```bash
history
history | grep ssh
!!
!123
!ssh
```

### Globbing

```bash
*.txt
file?.log
{a,b,c}.txt
```

### Brace Expansion

```bash
mkdir dir{1..5}
echo {a..z}
```

---

## 16. Redirection & Pipes

```bash
cmd > out.txt
cmd >> out.txt
cmd < in.txt
cmd 2> err.txt
cmd &> all.txt
cmd1 | cmd2
cmd | tee file
```

---

## 17. Exit Codes & Logic

```bash
echo $?
true
false

cmd && echo "success"
cmd || echo "failed"
```

Common exit codes:

* 0 → success
* 1 → general error
* 127 → command not found
* 130 → script terminated (Ctrl+C)

---

## 18. Signals

```bash
kill -l
kill -SIGTERM PID
kill -SIGKILL PID
kill -SIGSTOP PID
kill -SIGCONT PID
```

---

## 19. SSH & Remote Work

```bash
ssh user@host
ssh -i key.pem user@host
scp file user@host:/path
scp -r dir user@host:/path
rsync -av --delete src/ dst/
```

---

## 20. Bash Scripting Essentials

```bash
#!/bin/bash

set -e
set -u
set -o pipefail

if [ -f file ]; then
  echo "exists"
fi

for f in *.txt; do
  echo "$f"
done

while read line; do
  echo "$line"
done < file
```

---

## 21. Scheduling

```bash
crontab -e
crontab -l
at 12:00
```

Cron format:

```
* * * * * command
| | | | |
| | | | └─ day of week
| | | └─── month
| | └───── day
| └─────── hour
└───────── minute
```

---

## 22. Debugging & Troubleshooting

```bash
strace command
lsof
lsof -i :8080
which command
whereis command
```

---

## 23. Dangerous Commands (DO NOT GUESS)

```bash
rm -rf /
chmod -R 777 /
dd if=/dev/zero of=/dev/sda
mkfs.ext4 /dev/sda
```

---

## 24. Keyboard Shortcuts

* Ctrl+C → interrupt
* Ctrl+Z → suspend
* Ctrl+D → EOF / exit
* Ctrl+A → start of line
* Ctrl+E → end of line
* Ctrl+R → reverse search
* Tab → autocomplete

---
