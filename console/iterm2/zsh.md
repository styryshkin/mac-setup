# Zsh

> The Z shell \(Zsh\) is a Unix shell that can be used as an interactive login shell and as a command interpreter for shell scripting. Zsh is an extended Bourne shell with a large number of improvements.

## Installation

```text
brew install zsh zsh-completions
```

To use the brew `zsh` as your default shell, run: 

```text
sudo dscl . -create /Users/$USER UserShell /usr/local/bin/zsh
```

```text
$ $SHELL --version
zsh 5.3 (x86_64-apple-darwin17.0)
```

