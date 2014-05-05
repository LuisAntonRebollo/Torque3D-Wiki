Prepare Linux for Torque 3D
-----------------------------
This version of Torque 3D supports being run under Linux Ubuntu.

### 64bit OS
Torque3D is a 32bit application, if you want to compile it into a 64-bit OS you must install Multiarch. 
Multiarch library lets you install packages from multiple architectures on the same machine.
```
sudo dpkg --add-architecture i386
sudo apt-get update
```

### Required libraries:
Prior to compiling Torque 3D under Linux, you will need to make sure you have the appropriate libraries and tools installed.  The exact packages will depend on which Linux distribution you are using.  
For example, under Ubuntu you will need:

* build-essential
* nasm
* xorg-dev
* ninja-build
* gcc-multilib
* g++-multilib
* cmake
* cmake-qt-gui
* libogg-dev
* libxft-dev
* libx11-dev
* libxxf86vm-dev
* libopenal-dev
* libfreetype6-dev

On 32 and 64bit OS:
```
sudo apt-get install git build-essential nasm xorg-dev ninja-build gcc-multilib g++-multilib cmake cmake-qt-gui
```

On 64bit OS:
```
sudo apt-get install libogg-dev:i386 libxft-dev:i386 libx11-dev:i386 libxxf86vm-dev:i386 libopenal-dev:i386 libfreetype6-dev:i386
```
On 32bit OS:
```
sudo apt-get install libogg-dev libxft-dev libx11-dev libxxf86vm-dev libopenal-dev libfreetype6-dev
```
