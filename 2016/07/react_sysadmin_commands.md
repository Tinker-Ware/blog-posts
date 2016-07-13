Cheat sheet for Tinkerware exercise
===

## NAVIGATE

 **- cd** | Go to a direcotry path
----------|----------
Parameters:|Path

Example:
```
vagrant@tinkerware:~$ cd /home/user/pictures
```

Directories to use in the exercise:
  - *~/Documents/tinkerware/deploy-exercise* #in host
  - */opt/tinker/shared_files/tinkerware_react*     #in vagrant
___

**- mkdir** |  Create directory
-|-
Parameters:| directory name

Example:
```
vagrant@tinkerware:~$ mkdir /home/user/Documents/newFolder
```
Directories to use in the exercise:
  - */opt/tinker/shared_files/tinkerware_react*
 ___
|**- ssh**| Logging into remote machines|
|-|-|
|Parameters:|user, ip|

Example:
```
vagrant@tinkerware:~$ ssh john@192.168.10.10
```
To use in the exercise:
user:
  - *intern1*
ip:
  - *192.168.33.10*
___
|**- su**|  Login as user |
|-|-|
|Parameters:| User name|

Example:
```
vagrant@tinkerware:~$ su - jhon
jhon@tinkerware:~$
```
User this exercise:
  - *intern1*
___


# CREATE USER AND GROUP

|**- groupadd**|  Create new group |
|-|-|
|Parameters:| Group name|

Example:
```
vagrant@tinkerware:~$ groupadd newgroup
```
To use in this exercise:
  - *sysadmin*
___

|**- useradd**|  Create new user |
|-|-|
|Parameters:| |
|-s|The name of the user's login shell.|
|-m|Create the user's home directory if it does not exist.|
|-d|The user's login directory|
|-g|The group of the user's initial login group.|
|-G|Extra groups which the user is also a member of.|

Example:

`useradd -s /bin/bash -m -d /home/${USER} -g ${GROUP} -G ${EXTRA_GROUPS} ${USER} `
```
vagrant@tinkerware:~$ useradd -s /bin/bash -m -d /home/john -g developer -G sudo john 
```
___

|**- passwd**| Define Password for new user |
|-|-|
|Parameters:| User name|

Example:
```
vagrant@tinkerware:~$ passwd jhon
```

___


# INSTALL PACKAGES:

## curl
curl -sL https://deb.nodesource.com/setup_4.x | bash -

## apt
apt-get install sudo
sudo apt-get install {{ package }}
package:
  - curl <!-- (1) Transfer a URL -->
  - build-essential <!-- node dependency -->
  - git <!-- (1) Revision control system -->
  - nodejs <!-- Event-driven I/O server-side JavaScript environment based on V8 -->
  - emacs <!--(1) Best text editor -->

### Upgrade
apt-get update
apt-get upgrade
apt-get upgrade -f

## npm
  - npm install {{ package }}
package: (optional)
  - react

# REPOSITORIES

git clone {{ url }}
url:
  - https://github.com/Tinker-Ware/provisioning-webpage.git
  - https://github.com/reactjs/react-tutorial.git

# SERVICES

## Run React service
node server.js

## Restart ssh service
sudo service ssh restart

# Files to change
/etc/ssh/sshd_config
/etc/sudoers - `visudo`
HOME/.ssh/authorized_keys
