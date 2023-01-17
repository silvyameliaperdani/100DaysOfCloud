
# User & Group Management, File Permissions [Mentor : Diana Zuniarti ]

## Introduction
at this cal meeting we will learn about access rights on linux and file permissions on linux

## Cloud Research
## Type - type User 
![image](https://user-images.githubusercontent.com/121029600/211991754-a6071567-8a6b-4f82-bae5-253afef1ea98.png)
1. Regular User, namely an ordinary user who has only certain (limited) rights / privileges. This normal user can only use the computer from the usage system. Regular users are usually marked with a "$" symbol.
2. Administrator user, which is the root user, where this user has all the rights / privileges, such as creating users, changing, editing and deleting files or systems that exist on Linux. The root user is usually marked with a "#" symbol.
- The user information is in the /etc/passwd file

![image](https://user-images.githubusercontent.com/121029600/211994000-950e588e-f455-4f6f-846a-51f08ffbe7f0.png)

From the picture above, each has its meaning:
1. Users
2. Passwords
3. User ID
4. Group ID
5. Complete information / description of the user
6. Home directory of users
7. Shell to execute a command
## Create Users
There are 2 commands to create a user:
1. Adduser -> is administrative (complete) where if we create a user, we can set a password, create a user and their home directory, and can also provide complete information about the user.

![image](https://user-images.githubusercontent.com/121029600/211995731-2d3ad33a-416c-4797-95ca-a8abe3995390.png)

If we look at the /etc/passwd file as follows:

![image](https://user-images.githubusercontent.com/121029600/211995863-f4f754d4-6538-4bd7-8a40-c822482096dc.png)

2. Useradd -> Creates a normal user, where if we create a user with this command without setting a password, without a home directory, and without providing complete information about the user.

![image](https://user-images.githubusercontent.com/121029600/211999394-b4d89798-441b-466c-96be-3118c68bcad4.png)

If we look at the /etc/passwd file as follows:

![image](https://user-images.githubusercontent.com/121029600/211999571-dfa5ebde-e579-4cf5-be65-9de2ca266496.png)

NOTES :
1. Create a user with adduser

![image](https://user-images.githubusercontent.com/121029600/211999819-17367134-2d56-4f3e-9ca4-7bf53e4a8c32.png)

2. Create a user with useradd

![image](https://user-images.githubusercontent.com/121029600/211999947-bcdd5a59-34fa-4226-96e8-5047c6a516ca.png)

- It can be seen that the user tkj1 is given the shell /bin/bash permission, which means he can run commands
- And the user tkj2 looks /bin/sh which means there is no shell permission to run the command


## Create Group 
- Groupadd, this command is for creating groups

![image](https://user-images.githubusercontent.com/121029600/212008943-f3949f4a-5cb9-42ec-b0e1-1338ddea1b29.png)

## There are 2 ways to add a user to a group:
1. adduser 

example : adduser username groupname

![image](https://user-images.githubusercontent.com/121029600/212009141-bc2f1ead-b201-415f-b7b3-195188578e31.png)

 2. usermod 
 
 example : usermod -G groupname username
 
![image](https://user-images.githubusercontent.com/121029600/212009788-e4ece868-a8a2-4f75-a74f-ee8346c6b324.png)

 ## Permission File 
 
 ![image](https://user-images.githubusercontent.com/121029600/212010401-c0f6d42b-868e-443d-905a-ae0135b4f565.png)

Information :
-	r : read 
-	w : write 
-	x : execute 
1. – (shows files or directories) if files are marked with “-” if directories are marked with “d”
2. rw- ( has owner where he has access to read, write )
3. r-- (has a group where he has read access only )
4. r-- (has another where he also only has read access
5. root ( file / directory owner)
6. root (group files / directories)
7. Jan 12 03:57 (when the file was created and last modified)
8. File1.txt (filename)

There are 3 commands that we use in file permissions
- Chmod : change file permissions
- Chown : change file owner and group owner
- Chgrp : change group owner

## Chmod 

![image](https://user-images.githubusercontent.com/121029600/212013140-39bdc6bd-8ea0-4755-a637-97e54def5bc3.png)

This command is to change the permissions of a file / directory

There are 2 ways:
1. Numeric (number)

![image](https://user-images.githubusercontent.com/121029600/212013248-251617d7-9b83-4854-aa82-7b5176dbca87.png)

In the picture above I have changed the access rights to file1.txt so that the owner has read, write, execute access and for the group it has read and execute access, and for others it also has read and execute access.

2.	Alphabetic 

![image](https://user-images.githubusercontent.com/121029600/212013461-6fa9d4dc-2856-4156-9415-d42d4ed8286b.png)

In the image above I have changed the group access to read and execute

## Chown 
Change file ownership and group ownership

![image](https://user-images.githubusercontent.com/121029600/212013803-be19a527-fdf3-4c73-a181-6a26e3039e10.png)

In the picture above I have changed the owner of file1.txt which previously belonged to root, I changed it to the tkj1 user, and I also changed the group, which originally had root, I changed to TKJ

## Chgrp 
Changing the group ownership of a file / directory

![image](https://user-images.githubusercontent.com/121029600/212014205-4189b52f-1168-4663-a601-6f72e14cc0ac.png)

in the picture above I have changed the group owner that previously had tk I changed to have root

 ## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1614774572854935552)









