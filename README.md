# Pattern Lab for Sustainable Agriculture & Food Systems (SAFS) at MSU

Contact: [Katie Fritz](http://katiemfritz.com)

## Resources
- [MSU Web Standards](http://cabs.msu.edu/web/msu-web-standards.html#sResources)

## Stack

- [Pattern Lab Node Gulp Edition](https://github.com/pattern-lab/edition-node-gulp)
- [Prerequisites for Pattern Lab Node Gulp](https://github.com/pattern-lab/edition-node-gulp#prerequisites) - Node, NPM, Gulp
- [Twig Engine for Pattern Lab/Node](https://github.com/pattern-lab/patternengine-node-twig) - for Twig templating (Craft CMS compatiblity)
- Sass support [see setup notes](https://gist.github.com/KatieMFritz/38dda99e71bb7cef7afa2ff57f63f2f4)


## Installing

`npm` is a dependency management and package system which can pull in all of the Gulp Edition's dependencies for you. To accomplish this:

* download or `git clone` this repository to an install location.

* run the following

    ```
    cd install/location
    npm install
    ```

Running `npm install` from a directory containing a `package.json` file will download all dependencies defined within.


## Helpful Commands

These are some helpful commands you can use on the command line for working with Pattern Lab.

### List all of the available commands

To list all available commands type:

    gulp patternlab:help

### Generate Pattern Lab

To generate the front-end for Pattern Lab type:

    gulp patternlab:build

### Watch for changes and re-generate Pattern Lab

To watch for changes, re-generate the front-end, and server it via a BrowserSync server,  type:

    gulp patternlab:serve

BrowserSync should open [http://localhost:3000](http://localhost:3000) in your browser.
