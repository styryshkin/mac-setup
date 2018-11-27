# Oh My Zsh

> Oh My Zsh is an open source, community-driven framework for managing your zsh configuration.

## Getting Started

### Prerequisites

* `Zsh` should be installed \(v4.3.9 or more recent\)
* `curl` or `wget` should be installed
* `git` should be installed

### Basic Installation

**via curl**

```text
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

**via wget**

```text
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

## Using Oh My Zsh

### Plugins

Oh My Zsh comes with a shitload of plugins to take advantage of. You can take a look in the [plugins](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins) directory and/or the [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) to see what's currently available.

**Enabling Plugins** Once you spot a plugin \(or several\) that you'd like to use with Oh My Zsh, you'll need to enable them in the `.zshrc` file. You'll find the zshrc file in your `$HOME` directory. Open it with your favorite text editor and you'll see a spot to list all the plugins you want to load.

```text
vim ~/.zshrc
```

* [git](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins#git)
* [vscode](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins#vscode)

```text
plugins=(
  git
  vscode
)
```

### Themes

List of themes can be found [here](https://wiki.github.com/robbyrussell/oh-my-zsh/themes).

To use theme, need to edit the `~/.zshrc` file.

```text
ZSH_THEME="robbyrussell"
```

To use a different theme, simply change the value to match the name of your desired theme.

**Install Powerlevel9k**

To install this theme for use in Oh-My-Zsh, clone this repository into your OMZ `custom/themes` directory.

```text
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```

Select this theme in `~/.zshrc`:

```text
ZSH_THEME="powerlevel9k/powerlevel9k"
```

**Configurations**

* [punctual-zsh-theme](https://github.com/dannynimmo/punctual-zsh-theme)
* [mavam's Configuration](https://github.com/bhilburn/powerlevel9k/wiki/Show-Off-Your-Config#mavams-configuration)

To use configuration, need to edit the `~/.zshrc`f ile.

