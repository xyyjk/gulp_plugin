###gulp-make-css-url-version

a plugin for gulp.js to replace version for images in css files,the version should be file's md5 or time stamp;

###Installation

npm install gulp-make-css-url-version

###Usage

<pre>
var makeUrlVer = require('gulp-make-css-url-version');

gulp.task('stylesheets', function() {
  gulp.src('css/*.css')
    .pipe(makeUrlVer())
    .pipe(gulp.dest('dist'))
});
</pre>

###Options

useDate :make version with time stamp

<pre>
    var makeUrlVer = require('gulp-make-css-url-version');

    gulp.task('stylesheets', function() {
        gulp.src('css/*.css')
        .pipe(makeUrlVer({useDate:true}))
        .pipe(gulp.dest('dist'))
    });
</pre>

###Example

before: index.css

<pre>
/* loading */
.i-loading{width:32px;height:32px;background:url(../images/loading.gif) no-repeat;}    
</pre>

after: index.css

<pre>
/* loading */
.i-loading{width:32px;height:32px;background:url(../images/loading.gif?v=Je0sUcMH0mhJPWdZdpHzXg%3D%3D) no-repeat}
</pre>




