# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:

'''
DEVELOPED BY : MUKHIL S
REGISTER NUMBER : 212225040263
'''
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20103831.png)


cat < file2
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20104955.png)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105157.png)
 
comm file1 file2
 ## OUTPUT

 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105303.png)
 
diff file1 file2
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105337.png)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105806.png)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105924.png)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20105845.png)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110303.png)


grep hello newfile 
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110401.png)


grep -v hello newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110448.png)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110518.png)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110551.png)


grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20110728.png)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111500.png)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111530.png)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111556.png)


egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111714.png)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111751.png)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111811.png)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20111909.png)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113009.png)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113045.png)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113121.png)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113136.png)

cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113425.png)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113443.png)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113502.png)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113537.png)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113554.png)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113615.png)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113631.png)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113651.png)


seq 10 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20113726.png)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114213.png)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114246.png)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114345.png)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114659.png)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114746.png)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20114816.png)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20115125.png)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20115145.png)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
```
Desktop/
Desktop/README.license
Documents/
Downloads/
file1
file11
file2
file21
file22
file23
Music/
newfile
os/
os/ex01/
os/ex01/OS-Linux-commands-Shell-script/
os/ex01/OS-Linux-commands-Shell-script/.git/
os/ex01/OS-Linux-commands-Shell-script/.git/branches/
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/applypatch-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/commit-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/fsmonitor-watchman.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/post-update.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-applypatch.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-commit.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-merge-commit.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-push.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-rebase.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-receive.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/prepare-commit-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/push-to-checkout.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/update.sample
os/ex01/OS-Linux-commands-Shell-script/.git/info/
os/ex01/OS-Linux-commands-Shell-script/.git/info/exclude
os/ex01/OS-Linux-commands-Shell-script/.git/description
os/ex01/OS-Linux-commands-Shell-script/.git/refs/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/main
os/ex01/OS-Linux-commands-Shell-script/.git/refs/tags/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/objects/
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.pack
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.idx
os/ex01/OS-Linux-commands-Shell-script/.git/objects/info/
os/ex01/OS-Linux-commands-Shell-script/.git/packed-refs
os/ex01/OS-Linux-commands-Shell-script/.git/logs/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/main
os/ex01/OS-Linux-commands-Shell-script/.git/logs/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/config
os/ex01/OS-Linux-commands-Shell-script/.git/index
os/ex01/OS-Linux-commands-Shell-script/LICENSE
os/ex01/OS-Linux-commands-Shell-script/README.md
os/ex01/OS-Linux-commands-Shell-script/file2
os/ex01/OS-Linux-commands-Shell-script/file1
Pictures/
Public/
Templates/
Templates/prog/
Templates/prog/ObjC.m
Templates/prog/assembly.asm
Templates/prog/bash-sh.sh
Templates/prog/c#.cs
Templates/prog/c++.cpp
Templates/prog/c.c
Templates/prog/falcon.fal
Templates/prog/golang.go
Templates/prog/header.h
Templates/prog/java.java
Templates/prog/nim.nim
Templates/prog/perl.pl
Templates/prog/perl6.pl
Templates/prog/perlModule.pm
Templates/prog/python3.py
Templates/prog/ruby.rb
Templates/prog/rust.rs
Templates/prog/shellcode.s
Templates/text/
Templates/text/document.odt
Templates/text/plaintext.txt
Templates/text/presentation.odp
Templates/text/spreadsheet.ods
Templates/web/
Templates/web/css.css
Templates/web/html.html
Templates/web/javascript.js
Templates/web/php.php
Templates/web/xml.xml
urllist.txt
Videos/

```
mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
```
drwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Desktop/
-rwxr-xr-x mukhil/mukhil  2107 2026-04-23 16:50 Desktop/README.license
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Documents/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Downloads/
-rw-r--r-- mukhil/mukhil    61 2026-04-25 07:01 file1
-rw-r--r-- mukhil/mukhil    29 2026-04-25 07:26 file11
-rw-r--r-- mukhil/mukhil    70 2026-04-25 07:04 file2
-rw-r--r-- mukhil/mukhil   131 2026-04-25 08:16 file21
-rw-r--r-- mukhil/mukhil   155 2026-04-25 08:17 file22
-rw-r--r-- mukhil/mukhil   210 2026-04-25 08:04 file23
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Music/
-rw-r--r-- mukhil/mukhil    96 2026-04-25 07:43 newfile
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:31 os/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:52 os/ex01/OS-Linux-commands-Shell-script/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/branches/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/
-rwxr-xr-x mukhil/mukhil   478 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/applypatch-msg.sample
-rwxr-xr-x mukhil/mukhil   896 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/commit-msg.sample
-rwxr-xr-x mukhil/mukhil  4726 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/fsmonitor-watchman.sample
-rwxr-xr-x mukhil/mukhil   189 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/post-update.sample
-rwxr-xr-x mukhil/mukhil   424 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-applypatch.sample
-rwxr-xr-x mukhil/mukhil  1643 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-commit.sample
-rwxr-xr-x mukhil/mukhil   416 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-merge-commit.sample
-rwxr-xr-x mukhil/mukhil  1374 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-push.sample
-rwxr-xr-x mukhil/mukhil  4898 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-rebase.sample
-rwxr-xr-x mukhil/mukhil   544 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-receive.sample
-rwxr-xr-x mukhil/mukhil  1492 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/prepare-commit-msg.sample
-rwxr-xr-x mukhil/mukhil  2783 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/push-to-checkout.sample
-rwxr-xr-x mukhil/mukhil  3650 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/hooks/update.sample
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/info/
-rw-r--r-- mukhil/mukhil   240 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/info/exclude
-rw-r--r-- mukhil/mukhil    73 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/description
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/
-rw-r--r-- mukhil/mukhil    41 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/main
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/tags/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/
-rw-r--r-- mukhil/mukhil    30 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/HEAD
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/objects/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/
-r--r--r-- mukhil/mukhil 35706 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.pack
-r--r--r-- mukhil/mukhil  2444 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.idx
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/objects/info/
-rw-r--r-- mukhil/mukhil   112 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/packed-refs
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/
-rw-r--r-- mukhil/mukhil   206 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/HEAD
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/
-rw-r--r-- mukhil/mukhil   206 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/main
-rw-r--r-- mukhil/mukhil   206 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/logs/HEAD
-rw-r--r-- mukhil/mukhil    21 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/HEAD
-rw-r--r-- mukhil/mukhil   281 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/config
-rw-r--r-- mukhil/mukhil   209 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/.git/index
-rw-r--r-- mukhil/mukhil 35149 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/LICENSE
-rw-r--r-- mukhil/mukhil 14116 2026-04-24 07:47 os/ex01/OS-Linux-commands-Shell-script/README.md
-rw-r--r-- mukhil/mukhil     0 2026-04-24 07:52 os/ex01/OS-Linux-commands-Shell-script/file2
-rw-r--r-- mukhil/mukhil     0 2026-04-24 07:52 os/ex01/OS-Linux-commands-Shell-script/file1
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Pictures/
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Public/
drwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Templates/
drwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Templates/prog/
-rwxr-xr-x mukhil/mukhil   233 2026-04-23 16:50 Templates/prog/ObjC.m
-rwxr-xr-x mukhil/mukhil   239 2026-04-23 16:50 Templates/prog/assembly.asm
-rwxr-xr-x mukhil/mukhil    45 2026-04-23 16:50 Templates/prog/bash-sh.sh
-rwxr-xr-x mukhil/mukhil   114 2026-04-23 16:50 Templates/prog/c#.cs
-rwxr-xr-x mukhil/mukhil   110 2026-04-23 16:50 Templates/prog/c++.cpp
-rwxr-xr-x mukhil/mukhil   106 2026-04-23 16:50 Templates/prog/c.c
-rwxr-xr-x mukhil/mukhil    53 2026-04-23 16:50 Templates/prog/falcon.fal
-rwxr-xr-x mukhil/mukhil    87 2026-04-23 16:50 Templates/prog/golang.go
-rwxr-xr-x mukhil/mukhil    74 2026-04-23 16:50 Templates/prog/header.h
-rwxr-xr-x mukhil/mukhil   135 2026-04-23 16:50 Templates/prog/java.java
-rwxr-xr-x mukhil/mukhil    19 2026-04-23 16:50 Templates/prog/nim.nim
-rwxr-xr-x mukhil/mukhil    52 2026-04-23 16:50 Templates/prog/perl.pl
-rwxr-xr-x mukhil/mukhil    50 2026-04-23 16:50 Templates/prog/perl6.pl
-rwxr-xr-x mukhil/mukhil    20 2026-04-23 16:50 Templates/prog/perlModule.pm
-rwxr-xr-x mukhil/mukhil    54 2026-04-23 16:50 Templates/prog/python3.py
-rwxr-xr-x mukhil/mukhil    49 2026-04-23 16:50 Templates/prog/ruby.rb
-rwxr-xr-x mukhil/mukhil    56 2026-04-23 16:50 Templates/prog/rust.rs
-rwxr-xr-x mukhil/mukhil   825 2026-04-23 16:50 Templates/prog/shellcode.s
drwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Templates/text/
-rwxr-xr-x mukhil/mukhil  7782 2026-04-23 16:50 Templates/text/document.odt
-rwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Templates/text/plaintext.txt
-rwxr-xr-x mukhil/mukhil 25371 2026-04-23 16:50 Templates/text/presentation.odp
-rwxr-xr-x mukhil/mukhil  6662 2026-04-23 16:50 Templates/text/spreadsheet.ods
drwxr-xr-x mukhil/mukhil     0 2026-04-23 16:50 Templates/web/
-rw-r--r-- mukhil/mukhil    45 2026-04-23 16:50 Templates/web/css.css
-rwxr-xr-x mukhil/mukhil   109 2026-04-23 16:50 Templates/web/html.html
-rw-r--r-- mukhil/mukhil     0 2026-04-23 16:50 Templates/web/javascript.js
-rwxr-xr-x mukhil/mukhil    10 2026-04-23 16:50 Templates/web/php.php
-rwxr-xr-x mukhil/mukhil    12 2026-04-23 16:50 Templates/web/xml.xml
-rw-r--r-- mukhil/mukhil    52 2026-04-25 08:21 urllist.txt
drwxr-xr-x mukhil/mukhil     0 2026-04-24 07:24 Videos/
```

tar -xvf backup.tar
## OUTPUT
```
Desktop/
Desktop/README.license
Documents/
Downloads/
file1
file11
file2
file21
file22
file23
Music/
newfile
os/
os/ex01/
os/ex01/OS-Linux-commands-Shell-script/
os/ex01/OS-Linux-commands-Shell-script/.git/
os/ex01/OS-Linux-commands-Shell-script/.git/branches/
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/applypatch-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/commit-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/fsmonitor-watchman.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/post-update.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-applypatch.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-commit.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-merge-commit.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-push.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-rebase.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/pre-receive.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/prepare-commit-msg.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/push-to-checkout.sample
os/ex01/OS-Linux-commands-Shell-script/.git/hooks/update.sample
os/ex01/OS-Linux-commands-Shell-script/.git/info/
os/ex01/OS-Linux-commands-Shell-script/.git/info/exclude
os/ex01/OS-Linux-commands-Shell-script/.git/description
os/ex01/OS-Linux-commands-Shell-script/.git/refs/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/heads/main
os/ex01/OS-Linux-commands-Shell-script/.git/refs/tags/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/
os/ex01/OS-Linux-commands-Shell-script/.git/refs/remotes/origin/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/objects/
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.pack
os/ex01/OS-Linux-commands-Shell-script/.git/objects/pack/pack-c6c131cc2900889c159162c4e1042485acd5de62.idx
os/ex01/OS-Linux-commands-Shell-script/.git/objects/info/
os/ex01/OS-Linux-commands-Shell-script/.git/packed-refs
os/ex01/OS-Linux-commands-Shell-script/.git/logs/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/remotes/origin/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/
os/ex01/OS-Linux-commands-Shell-script/.git/logs/refs/heads/main
os/ex01/OS-Linux-commands-Shell-script/.git/logs/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/HEAD
os/ex01/OS-Linux-commands-Shell-script/.git/config
os/ex01/OS-Linux-commands-Shell-script/.git/index
os/ex01/OS-Linux-commands-Shell-script/LICENSE
os/ex01/OS-Linux-commands-Shell-script/README.md
os/ex01/OS-Linux-commands-Shell-script/file2
os/ex01/OS-Linux-commands-Shell-script/file1
Pictures/
Public/
Templates/
Templates/prog/
Templates/prog/ObjC.m
Templates/prog/assembly.asm
Templates/prog/bash-sh.sh
Templates/prog/c#.cs
Templates/prog/c++.cpp
Templates/prog/c.c
Templates/prog/falcon.fal
Templates/prog/golang.go
Templates/prog/header.h
Templates/prog/java.java
Templates/prog/nim.nim
Templates/prog/perl.pl
Templates/prog/perl6.pl
Templates/prog/perlModule.pm
Templates/prog/python3.py
Templates/prog/ruby.rb
Templates/prog/rust.rs
Templates/prog/shellcode.s
Templates/text/
Templates/text/document.odt
Templates/text/plaintext.txt
Templates/text/presentation.odp
Templates/text/spreadsheet.ods
Templates/web/
Templates/web/css.css
Templates/web/html.html
Templates/web/javascript.js
Templates/web/php.php
Templates/web/xml.xml
urllist.txt
Videos/

```
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174134.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174252.png)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174658.png)
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174744.png)
 
ls file1
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174838.png)


echo $?
## OUTPUT 
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20174932.png)
 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20175012.png)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20175352.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20175440.png)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20175717.png)


# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20175854.png)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180015.png)


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180106.png)


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180537.png)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180641.png)


# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180750.png)

 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20180856.png)
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20181008.png)
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20181118.png)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20181216.png)

 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20181725.png)

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182159.png)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182255.png)


cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182345.png)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182530.png)


cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182704.png)

 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20182914.png)
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20183051.png)

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20183215.png)
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20183422.png)
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/Mukhil0311/OS-Linux-commands-Shell-script/blob/main/Screenshot%202026-04-25%20183604.png)

# RESULT:
The Commands are executed successfully.
