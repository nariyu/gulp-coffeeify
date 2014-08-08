# gulp-coffeeify

Gulp task for browserify with coffee-script.

## USAGE

### Install

```
$ npm install gulp-coffeeify --save-dev
```

### Example

```javascript
var gulp = require('gulp');
var coffeeify = require('gulp-coffeeify');

// Basic usage
gulp.task('scripts', function() {
	gulp.src('src/coffee/**/*.coffee')
		.pipe(coffeeify())
		.pipe(gulp.dest('./build/js'));
});
```

## Options

### aliases

```javascript
var gulp = require('gulp');
var coffeeify = require('gulp-coffeeify');
gulp.task('scripts', function() {
  gulp.src('src/coffee/**/*.coffee')
    .pipe(coffeeify({
      aliases: [
        {
          cwd: 'src/coffee/app',
          base: 'app'
        }
      ]
    }))
    .pipe(gulp.dest('./build/js'));
});
```

You can use `src/coffee/app/views/View.coffee` as `var View = require('app/views/View');`

## License
Copyright (c) 2014 Yusuke Narita
Licensed under the MIT license.
