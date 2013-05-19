# grunt-markdown-pdf [![Build Status](https://travis-ci.org/alanshaw/grunt-markdown-pdf.png)](https://travis-ci.org/alanshaw/grunt-markdown-pdf) [![dependency Status](https://david-dm.org/alanshaw/grunt-markdown-pdf.png)](https://david-dm.org/alanshaw/grunt-markdown-pdf)

> Grunt plugin to convert markdown documents to PDF

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-markdown-pdf --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-markdown-pdf');
```

## The "markdownpdf" task

### Overview
In your project's Gruntfile, add a section named `markdownpdf` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  markdownpdf: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
})
```

### Options

#### options.phantomPath
Type: `String`
Default value: `Path provided by phantomjs module`

Path to phantom binary

#### options.cssPath
Type: `String`
Default value: `../pdf.css`

Path to custom CSS file, relative to the html5bp directory

#### options.paperFormat
Type: `String`
Default value: `A4`

'A3', 'A4', 'A5', 'Legal', 'Letter' or 'Tabloid'

#### options.paperOrientation
Type: `String`
Default value: `portrait`

'portrait' or 'landscape'

#### options.paperBorder
Type: `String`
Default value: `1cm`

Supported dimension units are: 'mm', 'cm', 'in', 'px'

#### options.renderDelay
Type: `Number`
Default value: `1000`

Delay in millis before rendering the PDF (give HTML and CSS a chance to load)

### Usage Examples

#### Default Options
In this example, the default options are used to convert all markdown files in the directory `src/` to PDFs in the directory `dest/`.

```js
grunt.initConfig({
  markdownpdf: {
    options: {},
    files: {
      src: "src/*.md"
      dest: "dest"
    }
  }
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

 * 2013-05-19   v0.0.0   Initial release