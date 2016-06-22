# gulp-build-qunit-from-json
===================

A [gulp](https://github.com/gulpjs/gulp) plugin to build a QUnit test file from a JSON object.


## Usage


First install `gulp-build-qunit-from-json` as a development dependency:

```shell
npm install gulp-build-qunit-from-json --save-dev
```

Then, add it to your gulpfile.js:

```javascript
var jsonToQUnit = require('gulp-build-qunit-from-json');
```

Then create a task that uses it:

```javascript
gulp.task('do-something', function() {
	gulp.src('./app/**/*.json')
	.pipe(jsonToQUnit(jsonObj, 'jsonObj', ['regexp', 'exclude', 'list']))
	.pipe(gulp.dest('./dist/out/'));
});
```

## API

### jsonToQUnit(obj, stack [, exclude_list])

#### obj
Type: `object`

The object to recurse through.

#### stack

Type: `String`

A string reprensenting the first node.

#### exclude_list

Type: `Array`
Default: `undefined`

An array of paths to exclude.

## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)
