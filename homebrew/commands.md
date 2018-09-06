# Commands

## Check system for potential problems

Doctor exits with a non-zero status if any potential problems are found. Please note that these warnings are just used to help the Homebrew maintainers with debugging if you file an issue. If everything you use Homebrew for is working fine: please don’t worry or file an issue; just ignore this.

```
brew doctor
```

## Open `formula`’s homepage in a browser

```
brew home formula
```

## Display brief statistics

### Display brief statistics for your Homebrew installation

```
brew info
```

### Display information about `formula` and analytics data

Pass `--verbose` to see more detailed analytics data.

```
brew info formula (--verbose)
```

## Install formula

`formula` is usually the name of the formula to install.

```
brew install [--debug] [--env=(std|super)] [--ignore-dependencies|--only-dependencies] [--cc=compiler] [--build-from-source|--force-bottle] [--include-test] [--devel|--HEAD] [--keep-tmp] [--build-bottle] [--force] [--verbose] [--display-times] formula [options …]: Install formula
```

If `--debug` (or `-d`) is passed and brewing fails, open an interactive debugging session with access to IRB or a shell inside the temporary build directory.

If `--env=std` is passed, use the standard build environment instead of superenv.

If `--env=super` is passed, use superenv even if the formula specifies the standard build environment.

If `--ignore-dependencies` is passed, skip installing any dependencies of any kind. If they are not already present, the formula will probably fail to install.

If `--only-dependencies` is passed, install the dependencies with specified options but do not install the specified formula.

If `--cc=compiler` is passed, attempt to compile using compiler. compiler should be the name of the compiler’s executable, for instance gcc-8 for gcc 8, gcc-4.2 for Apple’s GCC 4.2, or gcc-4.9 for a Homebrew-provided GCC 4.9. In order to use LLVM’s clang, use llvm_clang. To specify the Apple-provided clang, use clang. This parameter will only accept compilers that are provided by Homebrew or bundled with macOS. Please do not file issues if you encounter errors while using this flag.

If `--build-from-source` (or `-s`) is passed, compile the specified formula from source even if a bottle is provided. Dependencies will still be installed from bottles if they are available.

If `HOMEBREW_BUILD_FROM_SOURCE` is set, regardless of whether `--build-from-source` was passed, then both formula and the dependencies installed as part of this process are built from source even if bottles are available.

If `--force-bottle` is passed, install from a bottle if it exists for the current or newest version of macOS, even if it would not normally be used for installation.

If `--include-test` is passed, install testing dependencies. These are only needed by formulae maintainers to run brew test.

If `--devel` is passed, and formula defines it, install the development version.

If `--HEAD` is passed, and formula defines it, install the HEAD version, aka master, trunk, unstable.

If `--keep-tmp` is passed, the temporary files created during installation are not deleted.

If `--build-bottle` is passed, prepare the formula for eventual bottling during installation.

If `--force` (or `-f`) is passed, install without checking for previously installed keg-only or non-migrated versions

If `--verbose` (or `-v`) is passed, print the verification and postinstall steps.

If `--display-times` is passed, install times for each formula are printed at the end of the run.

Installation options specific to formula may be appended to the command, and can be listed with `brew options formula`.

## List all installed formulae

```
brew list, ls [--full-name] [-1] [-l] [-t] [-r]
```

If `--full-name` is passed, print formulae with fully-qualified names.

If `--full-name` is not passed, other options (i.e. -1, -l, -t and -r) are passed to ls which produces the actual output.

## Display install options specific to formulae

```
brew options [--compact] (--all|--installed|formulae)
```

If `--compact` is passed, show all options on a single line separated by spaces.

If `--all` is passed, show options for all formulae.

If `--installed` is passed, show options for all installed formulae.

## Show formulae that have an updated version available

```
brew outdated [--quiet|--verbose|--json=version] [--fetch-HEAD]
```

By default, version information is displayed in interactive shells, and suppressed otherwise.

If `--quiet` is passed, list only the names of outdated brews (takes precedence over `--verbose`).

If `--verbose` (or `-v`) is passed, display detailed version information.

If `--json=version` is passed, the output will be in JSON format. Currently the only accepted value for version is v1.

If `--fetch-HEAD` is passed, fetch the upstream repository to detect if the HEAD installation of the formula is outdated. Otherwise, the repository’s HEAD will be checked for updates when a new stable or devel version has been released.

## Display all locally available formulae

```
brew search, -S
```

## Display all locally available casks

```
brew search --casks
```

## Perform a substring search of cask tokens and formula names for `text`

```
brew search [--desc] (text|/text/)
```

If `text` is surrounded with slashes, then it is interpreted as a regular expression.

If `--desc` is passed, search formulae with a description matching text and casks with a name matching text.

## List all installed taps

```
brew tap
```

## Uninstall `formula`

```
brew uninstall, rm, remove [--force] [--ignore-dependencies] formula
```

If `--force` (or `-f`) is passed, and there are multiple versions of formula installed, delete all installed versions.

If `--ignore-dependencies` is passed, uninstalling won’t fail, even if formulae depending on formula would still be installed.

## Fetch the newest version of Homebrew

```
brew update [--merge] [--force]
```

If `--merge` is specified then git merge is used to include updates (rather than git rebase).

If `--force` (or `-f`) is specified then always do a slower, full update check even if unnecessary.

## Upgrade outdated, unpinned brews

```
brew upgrade [install-options] [--cleanup] [--fetch-HEAD] [--ignore-pinned] [--display-times] [formulae]
```

If `--cleanup` is specified or HOMEBREW_UPGRADE_CLEANUP is set then remove previously installed version(s) of upgraded formulae.

If `--fetch-HEAD` is passed, fetch the upstream repository to detect if the HEAD installation of the formula is outdated. Otherwise, the repository’s HEAD will be checked for updates when a new stable or devel version has been released.

If `--ignore-pinned` is passed, set a 0 exit code even if pinned formulae are not upgraded.

If `--display-times` is passed, install times for each formula are printed at the end of the run.

If formulae are given, upgrade only the specified brews (unless they are pinned; see pin, unpin).

## Display Homebrew’s install path

```
brew --prefix
```

## Display the location in the cellar where `formula` is or would be installed

```
brew --prefix formula
```

## Display where Homebrew’s .git directory is located

```
brew --repository
```

## Print the version number of Homebrew

```
brew --version
```
