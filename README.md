# grunt-psdslicer

> The grunt-psdslicer parses a Photoshop file (.psd) to retrieve user-sliced data. The information can be used in a template file out of which a distribution file will be generated.

## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-psdslicer --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-psdslicer');
```

## The "grunt-psdslicer" task

### Overview
In your project's Gruntfile, add a section named `grunt-psdslicer` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  psdslicer: {
    psd: // path to your psd file,  
    template: // path to your template file,  
    dest: // The destination for the build file. (css usually)  
  },
})
```

### Usage Examples

```js
var path = require('path');
grunt.initConfig({
  psdslicer: {
    myTask: {
      psd: 'src/psd/spritesheet.psd',  
      template: 'src/template/template.css',
      dest: 'src/css/main.css'  
    }  
  }  
})  
```

### Acknowledgements

The psd-slicer uses movableink's The PSD.js node module to parse psd files.

### Mustache Templates

Templates are parsed using mustache. To obtain slice information, simply specify a slice name and its property between {{ and }}.  

ie.) {{ mySlice.width }}

Each slice information has following properties:

- `name`
Name of the spritesheet image

- `width` 
Width of the slice in the psd

- `height`
Height of the slice in the psd

- `x`
X coordinates of the slice in the psd

- `y`
Y coordinates of the slice in the psd

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
