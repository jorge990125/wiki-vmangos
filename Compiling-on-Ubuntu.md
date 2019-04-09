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

The ACE library is essential, since it's used for Networking, Threading and File System access.
```
sudo apt-get install -qq libace-dev
export ACE_ROOT=/usr/include/ace
```

## 4. Installing Git

To download the source code for VMaNGOS, you should install Git. This can be avoided if you choose to manually download the zip archive from the website, but it's better to use Git, as it makes pulling updates from the main repository much easier.
```
sudo apt install git
```

## 5. Installing CMake

Since this is a cross-platform project, we use CMake to generate the appropriate solution files for every environment.
```
sudo apt install cmake
```

## 6. Installing MySQL Connector/C

Account, character and game data is stored inside the database, so we need the MySQL connector library to read and write data to it.
```
sudo apt-get install libmysqlclient-dev
```