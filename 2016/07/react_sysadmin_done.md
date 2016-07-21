apt-get install sudo
groupadd sysadmin
useradd -s /bin/bash -m -d /home/intern1 -g sysadmin -G sudo intern1
visudo > edit to add new user below root.
passwd intern1
su - intern1
mkdir /opt/tinker
cd /opt/tinker
sudo apt-get install git
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_4.x | bash -
git clone https://github.com/reactjs/react-tutorial.git
cd react-tutorial
node install
node server.js
