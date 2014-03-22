*This repository is a mirror of the [component](http://component.io) module [mathiasbynens/brnfckr](http://github.com/mathiasbynens/brnfckr). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/mathiasbynens-brnfckr`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# brnfckr, a brainfuck minifier written in JavaScript

[![Build status](https://travis-ci.org/mathiasbynens/brnfckr.svg?branch=master)](https://travis-ci.org/mathiasbynens/brnfckr) [![Dependency status](https://gemnasium.com/mathiasbynens/brnfckr.svg)](https://gemnasium.com/mathiasbynens/brnfckr)

For an online demo, see [mothereff.in/brainfuck-minifier](http://mothereff.in/brainfuck-minifier).

Feel free to fork if you see possible improvements!

## Installation and usage

Via [npm](http://npmjs.org/):

```bash
npm install brnfckr
```

Via [Bower](http://bower.io/):

```bash
bower install brnfckr
```

Via [Component](https://github.com/component/component):

```bash
component install mathiasbynens/brnfckr
```

In a browser:

```html
<script src="brnfckr.js"></script>
```

In [Narwhal](http://narwhaljs.org/), [Node.js](http://nodejs.org/), and [RingoJS](http://ringojs.org/):

```js
var brnfckr = require('brnfckr');
```

In [Rhino](http://www.mozilla.org/rhino/):

```js
load('brnfckr.js');
```

Using an AMD loader like [RequireJS](http://requirejs.org/):

```js
require(
  {
    'paths': {
      'brnfckr': 'path/to/brnfckr'
    }
  },
  ['brnfckr'],
  function(brnfckr) {
    console.log(brnfckr);
  }
);
```

Usage example:

```js
var code = 'lol . wat + heh [ huh . hah + oh ] yay';
brnfckr.minify(code); // '.+[.+]'
```

### Using the `brnfckr` binary

To use the `brnfckr` binary in your shell, simply install brnfckr globally using npm:

```bash
npm install -g brnfckr
```

After that you will be able to minify brainfuck programs from the command line:

```bash
$ brnfckr -c '.+[.+] prints out all ASCII characters'
.+[.+]
$ brnfckr -f foo.b
.+[.+]
```

See `brnfckr --help` for the full list of options.

## Support

brnfckr has been tested in at least Chrome 27, Firefox 3-19, Safari 4-6, Opera 10-12, IE 6-10, Node.js v0.10.0, Narwhal 0.3.2, RingoJS 0.8-0.9, PhantomJS 1.9.0 and Rhino 1.7RC4.

## Unit tests & code coverage

After cloning this repository, run `npm install` to install the dependencies needed for brnfckr development and testing. You may want to install Istanbul _globally_ using `npm install istanbul -g`.

Once that’s done, you can run the unit tests in Node using `npm test` or `node tests/tests.js`. To run the tests in Rhino, Ringo, Narwhal, and web browsers as well, use `grunt test`.

To generate [the code coverage report](http://rawgithub.com/mathiasbynens/brnfckr/master/coverage/brnfckr/brnfckr.js.html), use `grunt cover`.

## Author

| [![twitter/mathias](https://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](http://mathiasbynens.be/) |

## License

brnfckr is available under the [MIT](http://mths.be/mit) license.
