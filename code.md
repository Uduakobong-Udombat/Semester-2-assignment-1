The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.


[vagrant@localhost ~]$ mkdir code test personal misc
[vagrant@localhost ~]$ ls
code misc personal test

a.Change directory to the tests directory using absolute pathname
[vagrant@localhost ~]$ cd /home/vagrant/test
[vagrant@localhost test]$

b.Change directory to the tests directory using relative pathname
[vagrant@localhost ~]$ cd ./test
[vagrant@localhost test]$

c.Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory

[vagrant@localhost ~]$ echo "Hello A" > ./misc/FileA.txt
[vagrant@localhost ~]$

d.Create an empty file named fileB in the misc directory
[vagrant@localhost ~]$ touch ./misc/FileB.txt

e.Copy contents of fileA into fileC
[vagrant@localhost ~]$ cp ./misc/FileA.txt ./misc/FileB.txt
[vagrant@localhost ~]$

f.Move contents of fileB into fileD
[vagrant@localhost ~]$ mv ./misc/FileB.txt ./misc/FileD.txt
[vagrant@localhost ~]$

g.Create a tar archive called misc.tar for the contents of misc directory
[vagrant@localhost ~]$ tar -cf misc.tar misc
[vagrant@localhost ~]$

h.Compress the tar archive to create a misc.tar.gz file
[vagrant@localhost ~]$ tar -czf misc.tar.gz misc
[vagrant@localhost ~]$

I. Create a user and force the user to change his/her password upon login
[vagrant@localhost ~]$ sudo useradd yuddie
[vagrant@localhost ~]$ sudo passwd --expire yuddie
Expiring password for user yuddie.
passwd: Success

J. Lock a users password
[vagrant@localhost ~]$ sudo passwd -l newuser
Locking password for user newuser.
passwd: Success

K. Create a user with no login shell
[vagrant@localhost ~]$ sudo useradd nkakad --shell /usr/sbin/nologin
[vagrant@localhost ~]$

L. Disable password based authentication for ssh
M. Disable root login
