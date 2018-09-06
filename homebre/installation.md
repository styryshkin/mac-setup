# Homebrew

Homebrew is a free and open-source software package management system that simplifies the installation of software on Apple's macOS operating system. Packages are collections of files that are bundled together that can be installed and removed as a group. A package manager is a tool which automates the process of installing, updating, and removing packages.

## Installation

## Install Command Line Tools

In order to install Homebrew, you need to install either the Xcode Command Line Tools (about 100 MB) or the full Xcode package (about 10 GB). Command Line Tools gives Mac users many commonly used tools, utilities, and compilers. One advantage of this is that when you install Command Line Tools, it installs Git which you need as Homebrew is essentially all Git and Ruby scripts underneath.

Paste that at a Terminal prompt.

```
xcode-select -p
```

If you see a path output, please skip to the "Install Homebrew" section. You already have Xcode or Xcode Command Line Tools installed.

If you see no output, type the following into your terminal to install Command Line Tools. If you see a prompt, click on Install.

```
xcode-select --install
```

## Install Homebrew

Open a terminal and type the command below. You’ll be prompted to give your password, which is usually the one that you also use to unlock your Mac when you start it up. After you enter your password, the installation will start.

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

The script explains what it will do and then pauses before it does it. There are more installation options [here](https://docs.brew.sh/Installation) (required for OS X Lion 10.7 and below).

## What Does Homebrew Do?

Homebrew installs the stuff you need that Apple didn’t.

```
brew install wget
```

Homebrew installs packages to their own directory and then symlinks their files into /usr/local.

```
cd /usr/local
find Cellar
Cellar/wget/1.16.1
Cellar/wget/1.16.1/bin/wget
Cellar/wget/1.16.1/share/man/man1/wget.1

ls -l bin
bin/wget -> ../Cellar/wget/1.16.1/bin/wget
```
