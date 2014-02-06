# Default Grunt Installation

Install the contents of this package into your project’s webroot.

## Requirements

- Node.js
- [Grunt.js installed globally](http://wiki.local/Grunt)
- Sass

## Included Tasks

- Sass compilation to CSS
- CSS Autoprefixing
- CSS Minification
- JavaScript Concatentation
- JavaScript Minification

## Watching Files

To have Grunt watch your files for changes, run this command from the build directory:

`grunt watch`

## Install Node Modules

The necessary node modules are no longer included in this repo.  Please run the following command from the build directory upon first use:

`npm install`

or

`sudo npm install`

## Destination Folders

    |--- /css
    |   |--- base.compiled.css 			/* compiled css output for development */
    |   |--- base.compiled.min.css 		/* compiled, minified css output for production */
	|
    |-- /js
        |--- plugins.compiled.js 		/* concatenated, linted 3rd plugin/module code for development */
        |--- plugins.compiled.min.js 	/* concatenated, linted, minified 3rd plugin/module code for production */
        |--- main.js 					/* main app code for development */
        |--- main.min.js 				/* minified main app code for development */
    	|
    	|--- /vendor  /* Not touched by Grunt - load independently of other scripts. */     

## .hgignore

Add these lines to your .hgignore file in your project to prevent adding the sass cache and node modules to your repo:

    glob:*.sass-cache*
    glob:*node_modules*


All other files are fine to go in your repo.