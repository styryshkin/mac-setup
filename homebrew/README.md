# Homebrew

> Homebrew is a free and open-source software package management system that simplifies the installation of software on Apple's macOS operating system. Packages are collections of files that are bundled together that can be installed and removed as a group. A package manager is a tool which automates the process of installing, updating, and removing packages.

## Installation

### Requirements

- An Intel CPU
- OS X 10.11 or higher
- Command Line Tools (CLT) for Xcode: `xcode-select --install`, [developer.apple.com/download](https://developer.apple.com/download/) or [Xcode](https://itunes.apple.com/us/app/xcode/id497799835)
- A Bourne-compatible shell for installation (e.g. bash or zsh)

### Install Homebrew

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
$ cd /usr/local
$ find Cellar
Cellar/wget/1.16.1
Cellar/wget/1.16.1/bin/wget
Cellar/wget/1.16.1/share/man/man1/wget.1

$ ls -l bin
bin/wget -> ../Cellar/wget/1.16.1/bin/wget
```
