# The Problem

Mocha.js installs a global called `process` [see here](https://github.com/visionmedia/mocha/blob/master/mocha.js#L5237). A comment says it is only to allow mocha.js to run untouched, not to allow running node code in the browser, however this has some unfortunate side effects for some libraries that use `process` for environment detection.

r.js is one of those libraries that uses `process` for environment detection [see here](https://github.com/jrburke/r.js/blob/master/dist/r.js#L2536).