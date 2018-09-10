# NodeJs

## Why use Homebrew to install NodeJS?

If you are installing NodeJS via the installer from [https://nodejs.org/](https://nodejs.org/) then you have to use `sudo` to make sure that it installs correctly. After that you have to make changes in your system `$PATH` by adding the path of the node executable. And if you want to uninstall node then you have track all the files that were created and get rid of them. In short its a long process.

That's why Homebrew is used. It makes the job easy. It will install/uninstall Node easily.

## Install Node via Homebrew

```text
brew install node
```

If everything installed successfully then you can type in the following command in the terminal to check the Node and NPM version.

```text
$ node -v
v10.9.0
```

```text
$ npm -v
6.2.0
```

