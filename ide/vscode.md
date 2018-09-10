# Visual Studio Code

> Visual Studio Code is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux. It comes with built-in support for JavaScript, TypeScript and Node.js and has a rich ecosystem of extensions for other languages \(such as C++, C\#, Java, Python, PHP, Go\) and runtimes \(such as .NET and Unity\).

## Installation

1. Run in Terminal app:

```text
brew cask install visual-studio-code
```

1. Add VS Code to your Dock by right-clicking on the icon and choosing `Options`, `Keep in Dock`.

## Launching from the Command Line

You can also run VS Code from the terminal by typing 'code' after adding it to the path:

1. Launch VS Code.
2. Open the **Command Palette \(⇧⌘P\)** and type 'shell command' to find the **Shell Command: Install 'code' command in PATH** command.
3. Restart the terminal for the new `$PATH` value to take effect. You'll be able to type 'code .' in any folder to start editing files in that folder.

## Customization

There are many things you can do to customize VS Code.

### Change your theme

**Keyboard Shortcut**: `⌘K ⌘T`

**Theme**: `Material Theme Palenight High Contrast`

**Icon Theme**: `Material Theme Icons Palenight`

### Tune your settings

**Keyboard Shortcut**: `⌘,`

`editor.fontFamily`: "Operator Mono"

`editor.fontSize`: 13

`editor.fontLigatures`: true

`editor.formatOnPaste`: true

`editor.formatOnType`: false

`editor.renderWhitespace`: "all"

`editor.snippetSuggestions`: "top"

`editor.tabSize`: 2

`files.associations`: { ".babelrc": "json5" }

`files.autoSave`: "onFocusChange"

`explorer.decorations.badges`: false

`extensions.ignoreRecommendations`: false

`eslint.autoFixOnSave`: true

`git.autofetch`: true

`git.confirmSync`: false

`prettier.eslintIntegration`: true

### Install extensions

* [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

```text
code --install-extension formulahendry.auto-close-tag
```

* [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)

```text
code --install-extension formulahendry.auto-rename-tag
```

* [Code Navigation](https://marketplace.visualstudio.com/items?itemName=vikas.code-navigation)

```text
code --install-extension vikas.code-navigation
```

* [Create Unique Ids](https://marketplace.visualstudio.com/items?itemName=donjayamanne.createuniqueid)

```text
code --install-extension donjayamanne.createuniqueid
```

* [DotENV](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv)

```text
code --install-extension mikestead.dotenv
```

* [ES7 React/Redux/GraphQL/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets)

```text
code --install-extension dsznajder.es7-react-js-snippets
```

* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

```text
code --install-extension dbaeumer.vscode-eslint
```

* [Flow Language Support](https://marketplace.visualstudio.com/items?itemName=flowtype.flow-for-vscode)

```text
code --install-extension flowtype.flow-for-vscode
```

* [Formatting Toggle](https://marketplace.visualstudio.com/items?itemName=tombonnike.vscode-status-bar-format-toggle)

```text
code --install-extension tombonnike.vscode-status-bar-format-toggle
```

* [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

```text
code --install-extension eamodio.gitlens
```

* [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)

```text
code --install-extension PKief.material-icon-theme
```

* [Material Theme](https://marketplace.visualstudio.com/items?itemName=Equinusocio.vsc-material-theme)

```text
code --install-extension Equinusocio.vsc-material-theme
```

* [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

```text
code --install-extension esbenp.prettier-vscode
```

* [Sublime Babel](https://marketplace.visualstudio.com/items?itemName=joshpeng.sublime-babel-vscode)

```text
code --install-extension joshpeng.sublime-babel-vscode
```

