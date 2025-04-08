# Foundations Installations

## Node.js
Node.js has several actively maintained versions. The current version of Node.js is considered "Stable" and there are other prior versions which are still being maintained. The most significant of these are considered `LTS` or in a long term support plan.

If you are using the same machine you used for the client-side, there is no need to install Node again, although it might be a good idea to check and see if there are any updates. If you are running the most current `LTS` version of Node, then you are good to go! We'll dive deeper into that by introducing `NVM` (_Node Version Manager_)

### Node Version Manager
Discovering the latest LTS version is a cinch once you have [Node Version Manager (NVM)]('https://github.com/nvm-sh/nvm') installed. `NVM` is a tool that allows you to install, run and manage different versions of Node.js on your system. It is designed to be installed per-user and invoked per-shell, making it a convenient way to work with different Node.js versions for different projects or tasks. In other words it facilitates switching between multiple versions of Node.js.

Here's the installation script. Run this in your terminal.
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```
Once the installation completes we'll need to _source_ your shell.

```bash
source ~/.zshrc
```

Now if you should have the ability to run the `nvm` command and use its tools. Let's make sure your installation was successful.

```bash
nvm --version
```
> If you're getting `nvm is not a command` instead of a version number (e.g. 0.39.7) something went wrong. Try it again, or reach out for assistance.

### Checking Node.js version
Now that `nvm` is installed we can check your current version of Node.js.

```bash
nvm ls
```

Some Windows users may notice something similar to this:

```bash
->       system
iojs -> N/A (default)
node -> stable (-> N/A) (default)
unstable -> N/A (default)
```

That is because when you installed Node.js it was installed in Windows and not in _Windows Sub-system for Linux_ (wsl). If this is the case you can just enter the following line in your terminal, which will default your Node.js and npm versions to your system version.

```bash
nvm use system
```

OR

To update to the latest stable version:

```bash
nvm install stable
```
> Note: This is NOT the latest `LTS` version. It is the Node.js version with the latest stable features.

Let's run the list command again to see what we've done!

```bash
nvm ls
```

Now you should see something similar to this:

```
->      v22.2.0
         system
default -> stable (-> v22.2.0)
iojs -> N/A (default)
unstable -> N/A (default)
node -> stable (-> v22.2.0) (default)
stable -> 22.2 (-> v22.2.0) (default)
lts/* -> lts/iron (-> N/A)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.12 (-> N/A)
lts/fermium -> v14.21.3 (-> N/A)
lts/gallium -> v16.20.2 (-> N/A)
lts/hydrogen -> v18.20.2 (-> N/A)
lts/iron -> v20.13.1 (-> N/A)
```

These are versions of Node.js that are now available to use. You'll notice that the default is the `stable` version. We want to make the latest `LTS` version our default though, so let's change that now.

```bash
nvm use v20.13.1
```

Now you should see that `Node.js` version and also the `npm` version that is baked into it when you check the `Node.js` and `npm` versions.

```bash
node -v
npm -v
```

### Node Package Manager (NPM)
Node.js comes bundled with npm, the Node Package Manager. It allows you to effortlessly pull in 3-party libraries hosted on github and save them to your specific project, or save them globally when the module is something you need to access from anywhere on the command line.

By now you should be familiar with `npm` as you have undoubtedly, at some point, dug into various `package.json` files to inspect dev dependencies or other settings and run countless npm commands from your terminal so we won't go into much detail here, but there is an additional resource at the end of this chapter if you want to read more about npm.

## TypeScript Compiler
TypeScript is a statically typed superset of JavaScript that adds optional static typing to the language. It allows developers to write cleaner, more maintainable code by catching errors during development rather than at runtime.

TypeScript needs to be compiled into JavaScript to run in Node.js or the browser. We will be installing TypeScript for each project we build individually.

## Node.js and other Extensions for VS Code
[npm]('https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script'): The npm extension provides two features: running npm scripts defined in the package.json in the editor and validating the packages listed in the package.json.

[npm intellisense]('https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense'): The npm Intellisense extension introduces autocomplete behavior when you use require() to import modules into your code.

[TypeScript Importer]('https://marketplace.visualstudio.com/items?itemName=pmneo.tsimporter'): Automatically searches for TypeScript definitions in workspace files and provides all known symbols as completion item to allow code completion.

[Move TS]('https://marketplace.visualstudio.com/items?itemName=stringham.move-ts'): Moves TypeScript files and folders containing TypeScript and updates their relative import paths.

[dotENV]('https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv'): It’s quite common to configure Node.js applications using environment variables. And, one of the most popular modules for managing environment variables is dotenv. The DotENV extension for VS Code adds convenient syntax highlighting when editing a .env file.

### And a fun, organizational one!
[Material Icon Theme]('https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme'): The Material Icon Theme adds a ton of icons to VS Code for different file types. Being able to quickly distinguish different files in project can be a great time saver!

## 🔍 Additional Materials
1. [Node releases]('https://nodejs.org/en/about/previous-releases')
1. [Node Version Manager (NVM)]('https://github.com/nvm-sh/nvm')
1. [Node Package Manager (NPM)]('https://docs.npmjs.com/')
1. [TypeScript]('https://www.typescriptlang.org/docs/')
