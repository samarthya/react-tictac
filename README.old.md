# Learning React

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

