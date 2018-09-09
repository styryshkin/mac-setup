# zsh

> The Z shell (Zsh) is a Unix shell that can be used as an interactive login shell and as a command interpreter for shell scripting. Zsh is an extended Bourne shell with a large number of improvements.

## Installation

```
brew install zsh zsh-completions
```

Zsh should be set as your default shell.

```
$ echo $SHELL
/bin/zsh
```

If not, run `chsh -s $(which zsh)`

```
$ $SHELL --version
zsh 5.3 (x86_64-apple-darwin17.0)
```
