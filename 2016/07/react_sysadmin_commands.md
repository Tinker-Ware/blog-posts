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
------------|-------
Parameters:| directory name

Example:
```
vagrant@tinkerware:~$ mkdir /home/user/Documents/newFolder
```
Directories to use in the exercise:
  - */opt/tinker/shared_files/tinkerware_react*

___


**- ssh**| Logging into remote machines
---------|----------------
Parameters:|user, ip

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



**- su**|  Login as user
---------|-------
Parameters:| User name

Example:
```
vagrant@tinkerware:~$ su - jhon
jhon@tinkerware:~$
```
User this exercise:
  - *intern1*

___


# CREATE USER AND GROUP

**- groupadd** |  Create new group
---------------|-----------
Parameters:| Group name

Example:
```
vagrant@tinkerware:~$ groupadd newgroup
```
To use in this exercise:
  - *sysadmin*

___

**- useradd**|  Create new user
-------|-----
Parameters:|
-s|The name of the user's login shell.
-m|Create the user's home directory if it does not exist.
-d|The user's login directory
-g|The group of the user's initial login group.
-G|Extra groups which the user is also a member of.

Example:

`vagrant@tinkerware:~$ useradd -s /bin/bash -m -d /home/${USER} -g ${GROUP} -G ${EXTRA_GROUPS} ${USER} `
```
vagrant@tinkerware:~$ useradd -s /bin/bash -m -d /home/john -g developer -G sudo john 
```

To use in this exercise:
  - *intern1*


___

**- passwd**| Define Password for new user
--------|-------
Parameters:| User name

Example:
```
vagrant@tinkerware:~$ passwd jhon
```

___


# INSTALL PACKAGES:

**- curl**| Transfer a URL
---------|---------
Parameters:| url
-s| Silent. Don't show progress metter or error messages.
-L| Remake te request if the server has moved to a different location.

Example:

```
# Run downloaded script
vagrant@tinkerware:~$ curl -sL https://raw.githubusercontent.com/roman-huliak/hello-world-bash/master/app.sh  | bash -
```

To use in this exercise:
 - *Node.js v4.x*
 - *https://github.com/nodesource/distributions*


___



**- apt**| Command-line tool to handle packages.
---------|--------
Parameters:| package to install

Example:
```
root@tinkerware:~$ apt-get install vim
vagrant@tinkerware:~$ sudo apt-get install htop
```

To use in this exercise:

package:
  - *curl*
  - *build-essential*
  - *git*
  - *nodejs*
  - *emacs*


### Upgrade
```
apt-get update
apt-get upgrade
apt-get upgrade -f
```

___



**- npm**| Package manager for JavaScript
-------|--------
Parameters:| package to install

Example:
```
vagrant@tinkerware:~$ npm install gulp
```

To use this exercise:
package:
  - *react*


___




# REPOSITORIES

**-git**| Revision control system command line tool.
---------|----------
Parameters:| url, path(optional)
clone | clone project url
checkout | move to a version of the code.

Example:
```
vagrant@tinkerware:~$ git clone https://github.com/roman-huliak/hello-world-bash.git
```

To use this exercise:

url:
  - *https://github.com/Tinker-Ware/provisioning-webpage.git*
  - *https://github.com/reactjs/react-tutorial.git*

# SERVICES

**-service**| Run a System V init script
--------------|-----------
Parameters:| service name
restart |
start |
stop |

## Restart ssh service
Example:
```
vagrant@tinkerware:~$ sudo service nginx restart
```

Services to use this exercise:
  - *ssh*

## Run React service
Example:
```
vagrant@tinkerware:~$ node server.js
```

___




# Files to change

Files to use this exercise:

`/etc/ssh/sshd_config`

`/etc/sudoers` - Command: visudo

`HOME/.ssh/authorized_keys`


#Extra notes

https://github.com/nodesource/distributions

## SERVER DESCRIPTION
Distribution and Kernel:
```
root@tinkerware:~# uname -a
Linux tinkerware 3.16.0-4-amd64 #1 SMP Debian 3.16.7-ckt25-2 (2016-04-08) x86_64 GNU/Linux
```
CPU:
```
root@tinkerware:~# lscpu
Architecture:          x86_64
CPU op-mode(s):        32-bit, 64-bit
Byte Order:            Little Endian
CPU(s):                1
```

Disk Space:
```
root@tinkerware:~# df
Filesystem     1K-blocks     Used Available Use% Mounted on
/dev/sda1        9620408  1350964   7757700  15% /
udev               10240        0     10240   0% /dev
tmpfs             101256     4420     96836   5% /run
tmpfs             253132        0    253132   0% /dev/shm
tmpfs               5120        0      5120   0% /run/lock
tmpfs             253132        0    253132   0% /sys/fs/cgroup
vagrant        143575768 52988892  90586876  37% /vagrant
```

Memory:
```
root@tinkerware:~# free
                 total       used       free     shared    buffers     cached
    Mem:        506268     108864     397404       4728      10508      48368
    -/+ buffers/cache:      49988     456280
    Swap:       473084          0     473084
```

More commands to get System Information:
  - man
  - hostname
  - dnsdomainname
  - lscpu
  - free
  - df
  - du
  - lspci
  - uptime
  - last {reboot|shutdown}
  - htop
  - In files: /proc/*, /var/log/dmesg
