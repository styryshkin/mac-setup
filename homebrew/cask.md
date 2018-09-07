# Homebrew Cask

Homebrew Cask extends Homebrew and brings its elegance, simplicity, and speed to the installation and management of GUI macOS applications such as Atom and Google Chrome.

## Getting Started

First ensure you have Homebrew version `0.9.5` or higher:

```
$ brew --version
0.9.5
```

## Frequently Used Commands

Homebrew-Cask is implemented as a subcommand of Homebrew. All Homebrew-Cask commands begin with brew cask. Homebrew-Cask has its own set of command verbs many of which are similar to Homebrew’s. The most frequently-used commands are:

- `install` — installs the given Cask
- `uninstall` — uninstalls the given Cask
- `list` — lists installed Casks

## Searching for Casks

To search for Casks, use `brew search`. Let’s see if there’s a Cask for Google Chrome:

```
$ brew search google-chrome
==> Casks
google-chrome
homebrew/cask-versions/google-chrome-beta
homebrew/cask-versions/google-chrome-canary
homebrew/cask-versions/google-chrome-dev
```

## Installing Casks

The command `brew cask install` accepts one or multiple Cask tokens.

```
brew cask install google-chrome
```

## Uninstalling Casks

```
brew cask uninstall google-chrome
```

This will both uninstall the Cask and remove applications which were moved to `/Applications`.

## Other Commands
- `info` — displays information about the given Cask
- `list` — with no args, lists installed Casks; given installed Casks, lists staged files (with --full-name, include tap name)
- `fetch` — downloads remote application files for the given Cask to the local cache (with --force, re-download even if already cached)
- `doctor` — checks for configuration issues
- `cleanup` — cleans up cached downloads (with `--outdated`, only cleans old downloads)
- `home` — opens the homepage of the given Cask; or with no arguments, the Homebrew-Cask project page
- `zap` — try to remove all files associated with a Cask (may include resources shared with other applications)
- `outdated` - lists all outdated Casks
- `upgrade` - updates all outdated Casks
