---
layout: post
title:  "How did we build windows version"
date:   2016-03-07 12:46:17
TAG: "blog"
categories: coyim update
---

## TL;DR

[![Build status](https://ci.appveyor.com/api/projects/status/hcmdu0qtlcljq19v?svg=true)](https://ci.appveyor.com/project/tcz001/coyim)

## Thanks to Appveyor

CoyIM is currently built using Appveyor ci, it's a similar tool like Travis for Windows platform, if you'd like to know how we use appveryor, please refer to our `.appveyor` file in repo.

## GTK dependencies

CoyIM is a GUI application with GTK support(using GoTK, a wrapper in golang), so it requires a build environment like other GTK applications.

### MSYS2 and MinGW

Right now MSYS2 and MinGW are the most common way to setup GTK env on windows.
It's by default with the features provided by Pacman, a package tool on Arch Linux,
You can imagine a small linux virtual environment in windows, that's MSYS2, although
all the dependencies are actually natively built from source on windows.

The file `ci/install-deps-windows.bat` in repo describe the way to install MSYS2 and MinGW
and also using pacman to resolve all the dependencies we need.

**MSYS2 & MinGW:**

    download from https://sourceforge.net/projects/msys2/
    unzip it into any place you want, u will see a cute bash in \usr\bin\

**Pacman:**

	pacman --noconfirm --needed -Sy make gcc
	pacman --noconfirm --needed -Sy mingw-w64-x86_64-gtk3

These packages are actually compiled on windows, and you can directly use it as DLL for any applications.
Check them in `/mingw64/**/*.dll`.

### Golang

Golang has a nice compiler on windows, and we actually did nothing special to make it work for CoyIM.

### CLI version (xmpp-client)

Now we don't have client version on windows, because it uses a system call which doesn't exist on Windows OS.
And it won't have good experience when you use it on CMD.exe or PowerShell, because of the UNIX prompt color.

If any idea/doubt about this, feel free to contact with us on Github or Twitter.
