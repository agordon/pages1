---
layout: default
title: pages1 - download
---

### Version

### Download pre-compiled binaries

Pre-compiled binaries are available for the following platforms:

* [Linux](https://github.com/agordon/pages1/releases/XXX)
* [Mac OS X](https://igthub.com/agordon/pages1/releases/XXX)
* [FreeBSD 10](https://github.com/agordon/pages1/releases/XXX)

### HomeBrew/LinuxBrew

On Mac OS X with [HomeBrew](http://brew.sh/) or on Linux with [LinuxBrew](https://github.com/Homebrew/linuxbrew/), install `calc` by running the following:

```sh
$ brew install agordon/gordon/calc
```

### Compile from source code

To compile from source code, download [calc-X.Y.Z.tar.gz](https://github.com/agordon/pages1/releases/XXX) file, and run the following commands:

```sh
$ wget https://github.com/agordon/pages1/releases/calc-X.Y.Z.tar.gz
$ tar -xzf calc-X.Y.Z.tar.gz
$ cd calc-X.Y.Z
$ ./configure
$ make
$ make check
$ sudo make install
```

### Compile from GIT repository

To compile from the [GIT repository](https://github.com/agordon/pages1), run the following commands:

```sh
$ git clone https://github.com/agordon/pages1.git
$ cd calc
$ ./bootstrap
$ ./configure
$ make
$ make check
$ sudo make install
```

### Prerequisites

To compile from the GIT repository, the following programs are needed: automake,autoconf,gcc/clang,gperf,help2man.

On Debian/Ubuntu systems, use the following command:

```sh
$ sudo apt-get install help2man gperf
```

On Mac OS X with XCode and HomeBrew, use the following commands:

```sh
$ brew install help2manhelp2man valgrind gperf
```

