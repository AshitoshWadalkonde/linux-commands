# linux-commands
root & non root :
sudo -i		: to change to root user
in linux we need to use CLI 
CLI : Command line interface

file commands:
touch 		   	: to create a file
ls					  : to list the file  (short list)
ll					  : to list the file  (long list)
ls -a				: to see the hidden files (start with .)
ll -a				: to see the hidden files (start with .)
more 				: to see the content of a file
cat 				  : to see the content of a file
cat>file1		: to insert the content (first time)
ctrl + d 		: to save the content of file
cat>>file1		: to insert the content (second time + ....)
clear/ctrll :  to clear the sceern

======================================================================================================================================================
cp 					  : to copy content form one file to another file
mv					  : to move content form one file to another file
mv					  : to rename a file
rm 					  : to remove a file
rm -f				  : to remove a file forcefully
rm -f *			  : to remove all files forecfully
rm -f p*			  : to remove all files forecfully starting with p
touch file{1..10} : to create multiple files in a pattren
rm -f python{13..17} : to remove python13 to python17 files
echo "nareshit" > file1 : to insert nareshit into file1



in linux folder is also called as directory.

mkdir 			: to create a dir
pwd				: to print/present working directory
cd 				: to change directory
cd ..			: to get one dir back
cd ../../	   : to get two dir back
cd	 -			: to go to previous dir

touch dir1/raham : to create a file called raham inside dir1
mkdir dir1/dir2  : to create a dir2 inside dir1
rm -rf dir1/ : to remove recursive inside the dir1

yum install tree -y

package manager : yum (yellowdog update modifier)
install : action
pkg name : tree
permission : -y

head			: to print the top 10 lines
head -5		: to print the top 5 lines
head -12		: to print the top 12 lines
tail			: to print the bottom 10 lines
tail -5		: to print the bottom 5 lines
tail -12		: to print the bottom 12 lines
wc				: to print lines, words and char
sed -n '4,12p' file1  : to print line number 4 to 12


======================================================================================================================================================

DAY-02:

VIM EDITOR: To edit the files
i	 = used to insert the content
ecs	 = to get out of insert mode

WE HAVE 3 MODES:

3. SAVE MODE
:w	:	save
:q	:	quit
:wq	:	save and exit
:w!	:	forcefully save
:q!	:	forcefully quit
:wq!	:	forcefully save and exit 


2. INSERT MODE
i	:	It will insert the data 
I	:	Moves to beginning of the line
A	:	moves to the end of the line
o	:	moves down to that line
O	:	moves up to that line


1. COMMAND MODE
gg	:	top of the file
shift+g	:	bottom of the file
yy	:	copies single line
3yy	:	copies 3 lines
p	:	paste the copied line
3p	:	paste the copied line for 3 times
dd	:	deletes the line
3dd	:	deletes three lines
u	:	undo
/word	:	finds the particular word
:set number:	To set the numbers in line
:83	:	To go to 83rd line



=========================================================

-rw-r--r-- 1 root root 0 May  4 05:39 file1

FILE TYPES:

-			: Regular file
b			: blocked file
c      : charcter file
d			: directory
l			: link file
.      : hidden file


PERMISSIONS: (rw-r--r--)

Types of permissions: 3 types

Read				:	 r		: 4
Write				:   w		: 2
Executable	   :   x		: 1

Categories:

User
Group
Others

Methods to change permissions:

numerical method: chmod 777 file1
alphabetical method: chmod u=rwx,g=rx,o=rw file1

==============================================================

useradd raham 		: to create a user
cat /etc/passwd 		: to check user list
getent passwd			: to check user list
cat /etc/group 		: to check groups list
getent group			: to check user list
cd /home/				: to check the user directory
chown raham file1  : to change the ownership 
chgrp raham file1  : to change the group
chown raham:raham file2 : to chnage ownership and group at same time
usermod -aG DevOps Abraham: to add user to groups

==============================================================

DAY-03: 

ROOT: He is admin
SUPER USER: Created by Root user and can have all permission like root user
NORMAL USER:  Created by Root user and doesn't have any permissions.

CONVERTING NORMAL USER TO SUDO USER

1. useradd raham
2. passwd raham
3. visudo (100 -- > yy -- > p -- > raham -- > :wq)


uname				: to see the os 
uname -r			 : to see the kernel info
uname -a			: to see full info
hostname 		: to see the host
hostnamectl set-hostname raham : to change the hostname
sudo -i : to login to hostname
hostname -i  : to see the ip addr
ifconfig
ip addr
ip addr show

w/who 			: to check the login info
whoami			: to show the current user




==============================================================

GREP : GLOBAL REGULAR EXPRESSION PRINT
To search for the words 

grep class file1
grep CLASS file1 -i
grep class file1 -v
grep 'good\|todays\|class' file1

| : used when we are executing two commands at once
first command output will become input of second command



SED: Stream editor
rules : 
word shoule be perfectly give
if we miss % the only one word will be replaced
if we miss g at last first letter in the line will only be chnaged
