This page will guide you through all the required steps to compile the server core on Ubuntu. Compiling VMaNGOS on Linux is much easier than doing it on Windows, since you can install all dependencies through the terminal.

### Required software:
- G++ Compiler
- CMake
- Git

### Required dependencies:
- ACE
- TBB
- MySQL Connector/C
- OpenSSL
- Zlib

## 1. Installing G++

First we need to install the compiler.
```
sudo apt install g++
```

## 2. Installing TBB

The TBB library is used to provide better performance and scalability for memory allocation/deallocation operations in multithreaded applications, compared to the default allocator. This dependency is optional and can be skipped if you specify the USE_STD_MALLOC option when configuring with CMake.
```
sudo apt-get install -y libtbb-dev
export TBB_ROOT_DIR=/usr/include/tbb
```

## 3. Installing ACE

The ACE library is used for Networking, Threading and File System access.
```
sudo apt-get install -qq libace-dev
export ACE_ROOT=/usr/include/ace
```