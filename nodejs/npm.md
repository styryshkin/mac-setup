# npm

## CLI commands

* `npm doctor` - Check your environments
* `npm init [--force|-f|--yes|-y|--scope]` - Create a package.json file

  **EXAMPLES**

  Create a new React-based project using `create-react-app`:

  ```text
  npm init react-app ./my-react-app
  ```

  Generate it without having it ask any questions:

  ```text
  npm init -y
  ```

* `npm install [-g]` - Install a package
  * **alias**: npm i
  * **common options**: \[-P\|--save-prod\|-D\|--save-dev\|-O\|--save-optional\]\[-e\|--save-exact\] \[-B\|--save-bundle\]\[--no-save\] \[--dry-run\]
    * **-P, --save-prod**: Package will appear in your dependencies. This is the default unless -D or -O are present.
    * **-D, --save-dev**: Package will appear in your devDependencies.
    * **-O, --save-optional**: Package will appear in your optionalDependencies.
    * **--no-save**: Prevents saving to dependencies.
    * **-g or --global**: Installs the current package context as a global package
* `npm outdated [-g]` - Check for outdated packages
* `npm uninstall [-g]` - Remove a package
* `npm update [-g]` - Update a package

