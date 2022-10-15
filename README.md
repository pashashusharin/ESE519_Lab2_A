# ESE519_Lab2_A
SDK Setup Guide

This setup is to setup SDK on windows system to work with Qt PY device with RP2040 board. 

For building projects install [Cmake](https://cmake.org/)   and 
[GNU Embedded Toolchain for Arm](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads). Make sure to read the instructions carefylly, for windows use the following executable arm-gnu-toolchain-12.2.mpacbti-bet1-mingw-w64-i686-arm-none-eabi.exe or the .zip file with the same name
 


Windows specific components to install in order to build code on RP2040:  
[Arm GNU Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/downloads)  
[CMake](https://cmake.org/download/)  
[Build Tools for Visual Studio 2022](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2022)  
[Python 3.10](https://www.python.org/downloads/windows/)  
[Git](https://git-scm.com/download/win)  
  
After all the tools are installed get some SDK examples for the RP2040 board. In the Developer Command Prompt for VS code type in: 

```
C:\Users\pico\Downloads> git clone -b master https://github.com/raspberrypi/pico-sdk.git
C:\Users\pico\Downloads> cd pico-sdk
C:\Users\pico\Downloads\pico-sdk> git submodule update --init
C:\Users\pico\Downloads\pico-sdk> cd ..
C:\Users\pico\Downloads> git clone -b master https://github.com/raspberrypi/pico-examples.git
```

To build create first build type in: 

```
C:\Users\pico\Downloads> cd pico-examples
C:\Users\pico\Downloads\pico-examples> mkdir build
C:\Users\pico\Downloads\pico-examples> cd build
C:\Users\pico\Downloads\pico-examples\build> cmake -G "NMake Makefiles" ..
C:\Users\pico\Downloads\pico-examples\build> nmake
```
