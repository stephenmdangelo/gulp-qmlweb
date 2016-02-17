## Installation

Add the following dependencies to your `package.json`:

```
{
  "name": "QmlWebProject",
  "devDependencies": {
    "gulp": "~3.6.0",
    "gulp-concat": "~2.1.7",
    "gulp-qmlweb": "git://github.com/qmlweb/gulp-qmlweb.git"
  }
}
```

## Usage
```
var qml = require('gulp-qmlweb');
var concat = require('gulp-concat');

gulp.task('scripts', function() {
  return gulp.src(['qml/**/*.qml', 'qml/**/*.js'])
    .pipe(qml())
    .pipe(concat('qrc.js'))
    .pipe(gulp.dest('./dist/'));
});
```

This will compile all your QML sources (qml and javascript) and concatenate them in the `/dist/qrc.js` file.
