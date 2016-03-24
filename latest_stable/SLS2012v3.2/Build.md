# Install

* Vagrant
* Virtual Box
* Optional:
	* git for windows (https://git-scm.com/), this installs a bash terminal for Windows. Makes life a bit easier.

# Build

In Windows

$ cd <this directory>
$ vagrant up

Wait while the Ubuntu image downloads and installs

$ vagrant ssh

In the Ubuntu virtual machine

$ sudo apt-get install build-essential libopencv-dev libncurses-dev
$ cd /vagrant
$ make
$ ./SLS2012v3

In your favorite text editor, look for `//TODO` to port from Windows to Linux in these files:

* `SLS2012.cpp`
* `Utilities.cpp`
