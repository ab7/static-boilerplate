# Static Boilerplate

This is the front end boilerplate I use when creating a new static website. It features [Sass](http://sass-lang.com/) for CSS pre-processing and [Grunt](http://gruntjs.com/) to automate CSS and Javascript compiling and minification. There are two main tasks for development and production; `dev` and `pro`. The `dev` task simply monitors HTML, Sass and Javascript files for changes and reloads the browser. The `pro` task will prepare all files in a separate directory (`dist`) for production.


## Getting Started

1. You will need to have `npm` installed on your system. `npm` is the package manager for [node.js](http://nodejs.org/), it installs automatically with node. They have pre-compiled binaries available for easy installation so check it out if you don't already have node installed.

2. If this the first time you're running Grunt, you will need to install the global command line interface.

        npm install -g grunt-cli

3. After renaming the directory to your new project name, you can fill out the info in the `package.json` file. `npm` will complain if you choose not to, but everything should still work.

4. Next navigate to to root directory of the project and run:

        npm install

    This will install all the Grunt dependencies into a directory called `node_modules`.

5. To have the browser automatically reload when you save changes you need to have [LiveReload](http://livereload.com/). If you use Chrome for development, you can use this [extension](http://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei?hl=en).


## Development Task

        grunt dev

#### Watch
* Watches for changes in the static directory and re-compiles on file change.
* https://github.com/gruntjs/grunt-contrib-watch

#### Sass
* Compiles Sass files into a single expanded CSS file.
* https://github.com/gruntjs/grunt-contrib-sass


## Production Task

        grunt pro

#### Concatenate
* Combines all Javascript and CSS files.
* https://github.com/gruntjs/grunt-contrib-concat

#### Auto-prefixer
* Adds any required CSS prefixes based on the [Can I use](http://caniuse.com/) database.
* https://github.com/nDmitry/grunt-autoprefixer

#### CSSmin
* Compresses combined CSS file.
* https://github.com/gruntjs/grunt-contrib-cssmin

#### Uglify
* Compresses combined Javascript file.
* https://github.com/gruntjs/grunt-contrib-uglify

#### Copy
* Copies images folder to production directory if any files exist.
* https://github.com/gruntjs/grunt-contrib-copy

#### Process HTML
* Combines all link and script elements into single element.
* https://github.com/dciccale/grunt-processhtml

#### CheckJS
* Custom task I wrote to delete `main.js` file and remove the script element from `index.html` if no Javascript was used in the project.
