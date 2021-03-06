# grunt-phpdocumentor

> Runs the PHPDocumentor documentation generator tool.

This build includes phpDocumentor version 2.0.1, other versions can be specified by the `bin` option 

This plugin runs the command : ```phpdoc -d dir -t target```.

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-phpdocumentor --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-phpdocumentor');
```

## The "phpdocumentor" task

### Overview
In your project's Gruntfile, add a section named `phpdocumentor` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  phpdocumentor: {
    dist: {
        bin: 'bin/phpdoc',
        directory: './',
        target: 'docs',
        ignore: 'baddir1/*,badfile, ...',
        template: 'zend'
    }                
  },
})
```

### Options

#### options.bin( optional )
Type: `String`
Default value: `phpdoc`

Path to the phpdoc executable, by default it will use the one that come with task. It is located on the bin folder.

#### options.directory( optional )
Type: `String`
Default value: `./`

Comma-separated list of directories to (recursively) parse (multiple values allowed). It will default to the folder where Gruntfile is located.

#### options.target( optional )
Type: `String`
Default value: `docs`

Path where to store the generated output. It will default to a folder named 'docs' 

#### options.ignore( optional )
Type: `String`
Default value: ``

Paths or files to ignore, separated by commas.

#### options.template ( optional )
Type: `String`
Default value: `default`

Name of the template to use (you can get a list of them with `phpdoc template:list`)

### Usage Examples

```grunt phpdocumentor```

## Release History
0.4.0 - Added more parameters and upgraded included phpDocumentor phar to 2.0.1
0.1.0 - Including ```phpDocumentor version 2.0.0a12``` on the bin, giving default to all options
