# [](#css-modules)css-modules

Notes about [css-modules](https://github.com/css-modules)

## [](#todo)todo

-   [ ] try [factor-bundle](https://github.com/substack/factor-bundle) with css modules

-   [ ] look at how [parcelify](https://github.com/rotundasoftware/parcelify) handles rebuilds of changes to node\_modules

-   [ ] do we get any useful info about css modules from [disc](http://hughsk.io/disc/) ?

-   [ ] source maps

-   [ ] see if there's anything useful here: <https://github.com/ForbesLindesay/acorn-compile/blob/master/test/index.js>

## [](#test-suite)test suite

Goals:

-   develop a suite of end-to-end tests that cover all css-modules functionality
-   run the same test cases in different implementations (eg. webpack / browserify)
-   provide a simple "how to" reference for different things you can do with css-modules

## [](#questions)questions

-   Q. why does editing a shared css file rebuild correctly, but editing the main one include _everything_ in the bundle?

-   Q. how does it go with a .css.js module?

-   Q. would icss be better as a js module that exports objects?
