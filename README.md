# Learning React

## What is react?

React is a declarative, efficient, and flexible JavaScript library for building user interfaces.

## Component

- Components are mix of XML tags and JS. 
- React lets you compose complex UIs from small and isolated pieces of code called `components`.

### Example

```js
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
        </ul>
      </div>
    );
  }
}
```

# Day - 1

I am going to refer the [Reference URL](https://reactjs.org/tutorial/tutorial.html) for all the source files I willl create and log my own experience in doing so.

## Option - 2 

I will be using the [option-2](https://reactjs.org/tutorial/tutorial.html#setup-option-2-local-development-environment) setting up a local dev environment.

- Code 

```bash 
> tic-tac-toe % code -v    
1.74.3
97dec172d3256f8ca4bfb2143f3f76b503ca0534
arm64
```

- OSX

```bash
> sw_vers
ProductName:            macOS
ProductVersion:         13.1
BuildVersion:           22C65
```
- NPM

```bash
> npm version
{
  npm: '8.15.0',
  node: '18.7.0',
  v8: '10.2.154.13-node.9',
  uv: '1.44.2',
  zlib: '1.2.11',
  brotli: '1.0.9',
  ares: '1.18.1',
  modules: '108',
  nghttp2: '1.48.0',
  napi: '8',
  llhttp: '6.0.7',
  openssl: '1.1.1q',
  cldr: '40.0',
  icu: '70.1',
  tz: '2021a3',
  unicode: '14.0'
}
```

### Place holder APP

- Use `create-react-app` command to create the source files

A quick peak into what the command endorses

```bash
npx create-react-app --help
Usage: create-react-app <project-directory> [options]

Options:
  -V, --version                            output the version number
  --verbose                                print additional logs
  --info                                   print environment debug info
  --scripts-version <alternative-package>  use a non-standard version of react-scripts
  --template <path-to-template>            specify a template for the created project
  --use-pnp                                
  -h, --help                               output usage information
    Only <project-directory> is required.

    A custom --scripts-version can be one of:
      - a specific npm version: 0.8.2
      - a specific npm tag: @next
      - a custom fork published on npm: my-react-scripts
      - a local path relative to the current working directory: file:../my-react-scripts
      - a .tgz archive: https://mysite.com/my-react-scripts-0.8.2.tgz
      - a .tar.gz archive: https://mysite.com/my-react-scripts-0.8.2.tar.gz
    It is not needed unless you specifically want to use a fork.

    A custom --template can be one of:
      - a custom template published on npm: cra-template-typescript
      - a local path relative to the current working directory: file:../my-custom-template
      - a .tgz archive: https://mysite.com/my-custom-template-0.8.2.tgz
      - a .tar.gz archive: https://mysite.com/my-custom-template-0.8.2.tar.gz

    If you have any problems, do not hesitate to file an issue:
      https://github.com/facebook/create-react-app/issues/new
```

#### Step - 1 `npx create-react-app .`

It will show progress like below 

```bash
npx create-react-app .     

Creating a new React app in /Users/ss670121/sourcebox/github.com/tic-tac-toe.

Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts with cra-template...

(#####⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂⠂) ⠸ idealTree:express: sill placeDep ROOT multicast-dns@7.2.5 OK for: bonjour-service@1.1.0 want: ^7.2.5
```

and eventually it will publish some files the in the current directory

```bash
npx create-react-app .     

Creating a new React app in /Users/ss670121/sourcebox/github.com/tic-tac-toe.

Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts with cra-template...


added 1416 packages in 27s

231 packages are looking for funding
  run `npm fund` for details

Initialized a git repository.

Installing template dependencies using npm...

added 54 packages in 4s

231 packages are looking for funding
  run `npm fund` for details
Removing template package using npm...


removed 1 package, and audited 1470 packages in 3s

231 packages are looking for funding
  run `npm fund` for details

6 high severity vulnerabilities

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.

Created git commit.

Success! Created tic-tac-toe at /Users/ss670121/sourcebox/github.com/tic-tac-toe
Inside that directory, you can run several commands:

  npm start
    Starts the development server.

  npm run build
    Bundles the app into static files for production.

  npm test
    Starts the test runner.

  npm run eject
    Removes this tool and copies build dependencies, configuration files
    and scripts into the app directory. If you do this, you can’t go back!

We suggest that you begin by typing:

  cd /Users/ss670121/sourcebox/github.com/tic-tac-toe
  npm start

You had a `README.md` file, we renamed it to `README.old.md`

Happy hacking!
```


#### Step - 2 `rm -rf ./src/*`

```bash
rm -rf src/*
zsh: sure you want to delete all 8 files in /Users/samarthya/sourcebox/github.com/tic-tac-toe/src [yn]? y
```

#### Step - 3

Add a `index.js` & `index.css` in `src/`

```bash
touch src/index.js src/index.css
```

#### Step - 4

Publish the `index.js` as under

```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
```

> Validate by running `npm start` and you should see an empty page when you browse to `http://localhost:3000`

__**Note**:__ Ignore the ESList warnings that you see on the console. They are expected.

