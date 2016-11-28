# Draft Documentation

The following repository contains two gitbook projects where draft documentation can be written for a release, its based on [GitBook Toolchain](https://toolchain.gitbook.com/) toolset.

## User Documentation
### docs-src
This folder contains the source documentation that makes up the User documentation

### docs
This folder contains the compiled GitBook for the **User documentation** and is available as a GitHub pages [project site](https://contensis.github.io/docs/index.html)


## API Documentation
The API docs uses the [API theme](https://github.com/GitbookIO/theme-api) for GitBooks and has its own configutation options.

### api-src
This folder contains the source documentation that makes up the API documentation

### api
This folder contains the compiled GitBook for the **API documentation** and is available as a GitHub pages [project site](https://contensis.github.io/api/index.html)

## Installation

### Github
1. Install [GitHub Desktop](https://desktop.github.com/)
2. Clone the https://github.com/contensis/contensis.github.io.git repository

### GitBook Dependencies
The best way to install GitBook is via NPM (Node package manager).

If you've not installed node before header over to the node.js [download page] (https://nodejs.org/en/download/) to find the installer for your OS. If you're on windows you'll need to reboot for the PATH variable to take effect.

Once installed at a command prompt, simply run the following command to install GitBook:

```
$ npm install gitbook-cli -g
```

### Serve a local copy of a book
When you are writing documentation, its helpful to see it in the context of the GitBook site. You can serve a local copy of the book that will automatically refresh as you make changes.

1. Use the terminal and navigate to the root of your contensis.github.io repository
2. Running the following command will start a local server for the user docs.

  **User Docs**
  ```
  $ gitbook serve docs-src
  ```

  **API Docs**
  ```
  $ gitbook serve api-src
  ```

3. You'll see a similar output as below

  ```
  Live reload server started on port: 35729
  Press CTRL+C to quit ...

  info: 8 plugins are installed
  info: loading plugin "toggle-chapters"... OK
  info: loading plugin "livereload"... OK
  info: loading plugin "highlight"... OK
  info: loading plugin "search"... OK
  info: loading plugin "lunr"... OK
  info: loading plugin "sharing"... OK
  info: loading plugin "fontsettings"... OK
  info: loading plugin "theme-default"... OK
  info: found 8 pages
  info: found 1 asset files
  info: >> generation finished with success in 3.2s !

  Starting server ...
  Serving book on http://localhost:4000
  ```
4. Navigate to the localhost location specified in the output in your favorite browser and you should see a site similar to the screenshot below

![GitBook Example](/help/gitbook-example.png)


### Build the static site
Whilst serving a local copy of the book allows you to see what your working on we need to create a production version of the site to be served by GitHub pages.

1. Use the terminal and navigate to the root of your contensis.github.io repository
2. Running the following commands for the particular documentation will create a build that can be committed with your changes.

  **User Docs**
  ```
  $ gitbook build docs-src docs
  ```

  **API Docs**
  ```
  $ gitbook build api-src api
  ```

3. You'll see a similar output as below

    ```
    info: 8 plugins are installed
    info: 7 explicitly listed
    info: loading plugin "toggle-chapters"... OK
    info: loading plugin "highlight"... OK
    info: loading plugin "search"... OK
    info: loading plugin "lunr"... OK
    info: loading plugin "sharing"... OK
    info: loading plugin "fontsettings"... OK
    info: loading plugin "theme-default"... OK
    info: found 8 pages
    info: found 1 asset files
    info: >> generation finished with success in 3.1s !
    ```
4. Any pages that you have added or amended can now be committed alongside the static site.
