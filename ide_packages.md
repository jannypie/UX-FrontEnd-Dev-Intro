IDE Setup

*See code block below for copy/paste commands*
- [homebrew](brew.sh) to [install node](https://changelog.com/install-node-js-with-homebrew-on-os-x/)
- NPM for most dependencies, including Gulp
- [Gulp](https://www.npmjs.com/package/gulp) for most build processes
- [Bower](https://www.npmjs.com/package/bower), mostly for jQuery dependencies
- [Composer](https://getcomposer.org/) for PHP dependencies

1. Install homebrew
  - Update brew
  - Add brew to your $PATH
2. Use **homebrew** to install node
  - Will install `npm`
3. Use npm to install gulp

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
export PATH="/usr/local/bin:$PATH"
brew install node
npm install gulp
```

## packages.json

Pro tip: Check out the [interactive guide](http://browsenpm.org/package.json) if you are unfamiliar

### Core npm packages

These packages are meant as a skeleton, and can be extended with others as needed.

```
"dependencies": {
  "bower": "",                // bower
  "del": "",                  // node file manager
  "gulp": "*",                // gulp
  "gulp-autoprefixer": "",    // autoprefixer for CSS 
  "gulp-cache": "",           // cache for builds
  "gulp-clean": "",           // removes files/folders before builds
  "gulp-concat": "",          // concat files for minification
  "gulp-if": "",              // allows logic flows for gulp
  "gulp-imagemin": "",        // minifies images
  "gulp-jshint": "",          // jshint
  "gulp-minify-css": "",      // minify css
  "gulp-php2html": "*",       // compile php to html
  "gulp-plumber": "",         // helps gulp not break on builds
  "gulp-rename": "",          // renames files in build
  "gulp-replace": "",         // string replacement plugin
  "gulp-sass": "",            // convert sass to css
  "gulp-sitemap": "",         // generate sitemap.xml
  "gulp-shell": "",           // interfaces gulp w command line
  "gulp-svgmin": "",          // minimizes svgs
  "gulp-strip-debug": "",     // strips console, alert, debugger from js
  "gulp-uglify": "",          // minify js
  "gulp-util": "",            // adds utility to gulp
  "gulp-watch": "",           // listens to file changes to run builds
}
```

### dev-dependencies

```
 "devDependencies": {
  "gulp-livereload": "",      // works with Chrome/FF livereload plugin
  },
```
