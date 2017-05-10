# Pattern Lab for Sustainable Agriculture & Food Systems (SAFS) at MSU

Contact: [Katie Fritz](http://katiemfritz.com)

## Resources
- [MSU Web Standards](http://cabs.msu.edu/web/msu-web-standards.html#sResources)
- [MSU Coding Guidelines](http://cabs.msu.edu/web/msu-web-standards.html#s8)
- [Pattern Lab](https://patternlab.io)

## Stack

- [Pattern Lab Node Gulp Edition](https://github.com/pattern-lab/edition-node-gulp)
- [Prerequisites for Pattern Lab Node Gulp](https://github.com/pattern-lab/edition-node-gulp#prerequisites) - Node, NPM, Gulp
- [Twig Engine for Pattern Lab/Node](https://github.com/pattern-lab/patternengine-node-twig) - for Twig templating (Craft CMS compatiblity)
- Sass support: [see setup notes](https://gist.github.com/KatieMFritz/38dda99e71bb7cef7afa2ff57f63f2f4)


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

These are some helpful commands you can use on the command line for working with Pattern Lab. To list all available commands type: `gulp patternlab:help`

### Generate Pattern Lab

To generate the front-end for Pattern Lab type:

    gulp patternlab:build

### Watch for changes and re-generate Pattern Lab

To watch for changes, re-generate the front-end, and server it via a BrowserSync server,  type:

    gulp patternlab:serve

BrowserSync should open [http://localhost:3000](http://localhost:3000) in your browser.

## CSS Architecture

The CSS for this project is inspired by Atomic Design principes and these blog posts:
 - https://www.lullabot.com/articles/bem-atomic-design-a-css-architecture-worth-loving
 - https://blog.alexdevero.com/atomic-design-scalable-modular-css-sass/

 It uses Sass ([see setup notes](https://gist.github.com/KatieMFritz/38dda99e71bb7cef7afa2ff57f63f2f4)) for more robust organization.

 All scss files can be found in `source/css/scss`.
 ```
 - 00_base
    - _colors.scss (color variables)
    - _reset.scss
    - _space.scss (spacing variables)
    - _typography.scss (fonts and base typography)
    - _utilities.scss (utility or helper classes; use sparingly)
 - 01_atoms
    - styles applied to atom-level components. Prefix classes with a-.
 - 02_molecules
    - styles applied to molecule-level components. Prefix classes with m-.
 - 03_organisms
    - styles applied to organism-level components. Prefix classes with o-.
 - 04_templates
```
All scss files are imported into `main.scss`, which gets compiled into `main.css`.

To add new styles:
- First make sure the styles don't exist; use a project-wide search if needed.
- Identify the component you are modifying or adding.
- For new components, add a new scss file in the appropriate folder, with the appropriate prefix.
- Classes should also be given the appropriate prefix.
- Do not use `!important` to override existing styles, unless you are adding a new utility class that can apply to any component.

 _Do not change `pattern-scaffolding.css` - it's a Pattern Lab asset._
