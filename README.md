# grunt-lodash

Simple grunt wrapper around the Lo-Dash builder.

[Lo-Dash](http://lodash.com/) was created & is maintained by
[John-David Dalton](http://allyoucanleet.com/), [Kit Cambridge](http://kitcambridge.github.com/) & [Mathias Bynens](http://mathiasbynens.be/)

This project is not associated with the people behind Lo-Dash (or Lo-Dash itself) in any way.

lodash only works with Lo-Dash version >= 0.7.0!

[![Build Status](https://secure.travis-ci.org/lodash/grunt-lodash.png?branch=master)](http://travis-ci.org/lodash/grunt-lodash)

## Getting Started
Install this grunt plugin next to your project's [Gruntfile][getting_started] with: `npm install grunt-lodash`

Then add this line to your project's `Gruntfile.js`.

```javascript
grunt.loadNpmTasks('grunt-lodash');
```

## Documentation
Load the grunt-lodash task as described in 'Getting started' and add your Lo-Dash builder
configuration to your grunt file:

Example Lo-Dash optimizer grunt file config entry:

```javascript
lodash: {
  build: {
    // output location
    dest: 'build/lodash.build.js',
    options: {
      // modifiers for prepared builds
      // backbone, legacy, modern, mobile, strict, underscore
      modifier: 'backbone'
    }
  }
}
```
As you might have guessed, this would produce the same output as

```shell
lodash backbone -o build/lodash.build.js
```

## All configuration options - More information can be found in the [Lo-Dash custom builds section](http://lodash.com/#custom-builds)
```javascript
lodash: {
  target: {
    // output location
    dest: 'build/lodash.build.js'
  },
  options: {
    // modifiers for prepared builds
    // backbone, legacy, modern, mobile, strict, underscore
    modifier: 'backbone',
    category: ['collections', 'functions'],
    exports: ['amd', 'commonjs', 'node'],
    iife: '!function(window,undefined){%output%}(this)',
    include: ['each', 'filter', 'map'],
    minus: ['result', 'shuffle'],
    plus: ['random', 'template'],
    template: './*.jst',
    settings: '{interpolate:/\\{\\{([\\s\\S]+?)\\}\\}/g}',
    moduleId: 'underscore',
    // With or without the --
    // These are the only tested options,
    // as the others don't make sense to use here
    flags: [
      '--stdout',
      'debug',
      '--minify',
      'source-map'
    ],
    // With or without the -
    shortFlags: [
      'c',
      '-d',
      'm',
      '-p'
    ]
  }
}
```

## Contributing
If you like to file an issue or submit a pull request, please check the [contributing guidelines](https://github.com/lodash/grunt-lodash/blob/master/CONTRIBUTING.md)

## Release History
Take a look at the [Changelog](https://github.com/lodash/grunt-lodash/blob/master/CHANGELOG.md)

## Resources
+ [grunt](https://github.com/gruntjs/grunt)
+ [Getting started](http://gruntjs.com/getting-started)
+ [Lo-Dash](http://lodash.com/)

## Author

| [![twitter/blainebublitz](http://secure.gravatar.com/avatar/ac1c67fd906c9fecd823ce302283b4c1?s=70)](http://twitter.com/blainebublitz "Follow @BlaineBublitz on Twitter") |
|---|
| [Blaine Bublitz](http://iceddev.com/) |


## Contributors

| [![twitter/jdalton](http://gravatar.com/avatar/299a3d891ff1920b69c364d061007043?s=70)](http://twitter.com/jdalton "Follow @jdalton on Twitter") | [![twitter/kitcambridge](http://gravatar.com/avatar/6662a1d02f351b5ef2f8b4d815804661?s=70)](https://twitter.com/kitcambridge "Follow @kitcambridge on Twitter") | [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias "Follow @mathias on Twitter") |
|---|---|---|
| [John-David Dalton](http://allyoucanleet.com/)| [Kit Cambridge](http://kitcambridge.github.io/) | [Mathias Bynens](http://mathiasbynens.be/) |
