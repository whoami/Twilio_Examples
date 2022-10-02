# Guide to setup Node environment


## Install NodeJs

How you install Node.js varies depending on your operating system.

### OS X:

The easiest way to install Node.js on OS X is to use [the official installer from nodejs.org](https://nodejs.org/en/#download). You can also use [Homebrew](http://brew.sh/) if you prefer.

To manage and switch between versions of Node.js on your machine, we recommend using [nvm](https://github.com/nvm-sh/nvm).

### Windows:

The easiest way to install Node.js on Windows is [the official installer from nodejs.org](https://nodejs.org/en/#download). You can also use [Chocolatey](https://chocolatey.org/) if you prefer.

To manage and switch between versions of Node.js on your machine, we recommend using [nvm-windows](https://github.com/coreybutler/nvm-windows).

### Linux:

The Node.js [installation method](https://nodejs.org/en/download/package-manager/) varies by distribution.

To manage and switch between versions of Node.js on your machine, we recommend using [nvm](https://github.com/nvm-sh/nvm).


### Initialise a new project with `npm init`.

Before starting any new Node.js project we should run `npm init` to create a new `package.json` file for our project.

Create a new empty directory in your development environment and run `npm init`. You'll then answer a few basic questions about your project, and npm will create a new `package.json` file for you when you're done.

```
$ npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (my-project)
version: (1.0.0)
description: A sample Twilio project
entry point: (index.js)
test command:
git repository:
keywords:
author: Jane Doe
license: (ISC)
About to write to /Users/<your-username>/my-project/package.json:

{
  "name": "my-project",
  "version": "1.0.0",
  "description": "A sample Twilio project",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Jane Doe",
  "license": "ISC"
}

Is this OK? (yes) yes
```
Now we're ready to install our Node.js dependencies.

### Install ExpressJS and Twilio Helper Library

We’re almost ready to write an Express web application, but first we need to install the Express package using `npm`.

```
# Use npm to install the express and twilio packages
$ npm install express twilio
# List the installed dependencies and their versions
$ npm ls
my-project@1.0.0 /Users/<your-username>/my-project
├── express@4.17.1
└── twilio@3.67.2
```

Node.js uses npm to manage dependencies, so the command to install Express and the Twilio SDK to our development environment is `npm install express twilio`.

Installing these packages tells npm to add the Express and Twilio packages to the dependencies object in our project's `package.json` file. When we want to install these same packages again in the future - like on a production server - we can just run `npm install`.
