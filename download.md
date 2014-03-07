---
layout: default
title: pages1 - download
---

### Version

The latest released version is {{ site.calc_version }} .

The latest development version is available at <{{site.calc_git_url}}>.

### Download pre-compiled binaries

Pre-compiled binaries are available for the following platforms:

* [Linux]({{site.calc_bin_linux_url}})
* [Mac OS X]({{site.calc_bin_macosx_url}})
* [FreeBSD 10]({{site.calc_bin_freebsd_url}})

### HomeBrew/LinuxBrew

On Mac OS X with [HomeBrew](http://brew.sh/) or on Linux with [LinuxBrew](https://github.com/Homebrew/linuxbrew/), install `calc` by running the following:

```sh
brew install agordon/gordon/calc
```

### Compile from source code

To compile from source code, download [{{site.calc_src_tarball_filename}}]({{site.calc_src_tarball_url}})

```sh
wget {{site.calc_src_tarball_url}}
tar -xzf {{site.calc_src_tarball_filename}}
cd calc-{{site.calc_version}}
./configure
make
make check
sudo make install
```

### Compile from GIT repository

To compile from the [GIT repository]({{site.calc_git_url}}), run the following commands:

```sh
git clone {{site.calc_git_url}}
cd calc
./bootstrap
./configure
make
make check
sudo make install
```

### Prerequisites

To compile from the GIT repository, the following programs are needed: automake,autoconf,gcc/clang,gperf,help2man.

On **Debian/Ubuntu** systems, use the following command:

```sh
sudo apt-get install build-essential help2man gperf autoconf automake gettext
```

On **Mac OS X** with XCode and HomeBrew, use the following commands:

```sh
brew install help2man
```

