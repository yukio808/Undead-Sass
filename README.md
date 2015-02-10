# Undead Sass

## Sass and Gulp exercise

### Goals

_in your own forked repo_

1. setup gulp to watches and compiles sass files to the public css directory
2. use sass to style `index.html` so that it matches the layouts in the `layouts` directory

_you may accomplish these goals without following the steps outlined below_

### Steps to achieve goals

### setup forked repo

1. fork and clone this repo

### make sure you have all required dependencies

_If you have not have npm and gulp, you need to install them._

1. `brew install npm`
2. `npm install -g gulp`

### setup gulp + sass

1. initialize your forked project with npm libs, `npm init`
2. setup your `.gitignore` file to ignore `node_modules`
3. add and commit your 2 new files to be tracked in git
4. install and save required dependencies using `npm install -D [node_module name]`
  1. `gulp`
  2. `gulp-sass`
5. setup sass source directory `mkdir sass/`
6. setup sass source file `touch sass/styles.scss`
7. setup sass compiled output directory `mkdir public/css`
8. setup Gulpfile `touch gulpfile.js`
9. setup Gulpfile task, with `watch_sass` and `default` tasks
  1. `subl gulpfile.js`
  2. [contents of gulpfile.js](http://i.imgur.com/H2u49eL.png)
10. test gulp task
  1. 'hello world' of sass, `subl sass/styles.scss`
    ````
    $dark-color : #333333;
    
    body {
      background: $dark-color;
    }
    ````
  2. run `gulp` in your terminal
  3. check output, `ls public/css` (should say styles.css)
  4. inspect output, `cat public/css/styles.css` ( should be proper css )
11. once gulp and sass are wired up correctly, commit your new files
12. make sure to keep your "gulp" terminal running and visible, if your sass source is invalid, it will crash the watching gulp process, and you will want to see the error message that will output in that terminal. Then you can restart your `gulp` watcher after fixing your errors.

### style index.html

1. (on a seperate terminal, since gulp is being held open), navigate to your `public/` subdirectory, then run an `http-server`
2. open a browser to make sure you can see `public/index.html` rendered
3. setup your `public/index.html` to link to your `public/css/styles.css` stylesheet.
4. If it works, your background shold be gray. commit your work.
5. Editing only your `sass/styles.scss` file, style your html page so that it matches the layout in `layouts/undead_sass.png`
6. Once done, commit and push your work.