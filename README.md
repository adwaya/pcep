# pcep
entry level python programmer

# Installing Python3.7 on CentOS 7:

## Here are the commands that we'll run to build and install Python 3.7 on CentOS 7:
switch to root 
$ sudo -i
$ yum groupinstall -y "Development Tools"
$ yum install -y zlib-devel openssl-devel
$ cd /usr/src
$ wget https://python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz
$ tar xf Python-3.7.3.tar.xz
$ cd Python-3.7.3
$ ./configure --enable-optimizations --with-ensurepip=install
$ make altinstall
$ exitImportant: make altinstall causes it to not replace the built-in python executable.
Download and Install Python 3 from Source on Debian
Here are the commands that we'll run to build and install Python 3.7 on a Debian based machine:
$ sudo -i
$ apt update -y
$ apt install -y
wget
build-essential
libffi-dev
libgdbm-dev
libc6-dev
libssl-dev
zlib1g-dev
libbz2-dev
libreadline-dev
libsqlite3-dev
libncurses5-dev
libncursesw5-dev
xz-utils
tk-dev
$ cd /usr/src

$ wget https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz

$ tar xf Python-3.7.3.tar.xz

$ cd Python-3.7.3

$ ./configure --enable-optimizations --with-ensurepip=install

$ make altinstall
$ exit
Note: make altinstall causes it to not replace the built-in python executable.

Ensure Python 3 Works with Sudo
Make sure that secure_path in /etc/sudoers file includes /usr/local/bin. The line should look something like this:
Defaults secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin
Upgrade Pip (might not be necessary)
The version of pip that we have might be up-to-date, but it's a good practice to try to update it after the installation. We need to use the pip3.7 executable because we're working with Python 3, and we use sudo so that we can write files under the /usr/local directory.
$ sudo pip3.7 install --upgrade pip
