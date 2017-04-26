# npmtest-smokestack

#### basic test coverage for  [smokestack (v3.4.1)](https://github.com/hughsk/smokestack)  [![npm package](https://img.shields.io/npm/v/npmtest-smokestack.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-smokestack) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-smokestack.svg)](https://travis-ci.org/npmtest/node-npmtest-smokestack)

#### Pipe your JavaScript into a browser, logging console output in Node

[![NPM](https://nodei.co/npm/smokestack.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/smokestack)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-smokestack/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-smokestack/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-smokestack/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-smokestack/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-smokestack/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-smokestack/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-smokestack/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-smokestack/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-smokestack/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-smokestack/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-smokestack/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-smokestack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-smokestack/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-smokestack/build/test-report.html](https://npmtest.github.io/node-npmtest-smokestack/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-smokestack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-smokestack/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-smokestack/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-smokestack/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-smokestack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-smokestack/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-smokestack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-smokestack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Hugh Kennedy",
        "url": "http://hughsk.io/"
    },
    "bin": {
        "smokestack": "bin/smokestack.js"
    },
    "browser": "browser.js",
    "bugs": {
        "url": "https://github.com/hughsk/smokestack/issues"
    },
    "dependencies": {
        "bl": "^0.9.4",
        "chrome-launch": "^1.1.4",
        "convert-source-map": "^1.0.0",
        "debug": "^2.1.3",
        "firefox-launch": "^1.0.2",
        "is-dom": "~1.0.5",
        "localtunnel": "^1.5.0",
        "minimist": "~1.1.1",
        "mkdirp": "^0.5.0",
        "rimraf": "~2.3.2",
        "shoe": "0.0.15",
        "source-map": "^0.4.2",
        "source-map-support": "^0.2.10",
        "split": "^0.3.3",
        "synthetic-dom-events": "^0.2.2",
        "tap-finished": "0.0.1",
        "through2": "^0.6.3",
        "wd": "^0.3.11",
        "xhr": "^2.0.1"
    },
    "description": "Pipe your JavaScript into a browser, logging console output in Node",
    "devDependencies": {
        "browserify": "^9.0.3",
        "pngparse-sync": "^1.0.2",
        "sliced": "0.0.5",
        "tap-spec": "^2.2.2",
        "tape": "~3.5.0"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "cb0d95fa455bce4214dd2750a7ace52403a60ff1",
        "tarball": "https://registry.npmjs.org/smokestack/-/smokestack-3.4.1.tgz"
    },
    "gitHead": "b730d65315fcf28a337b42601c52dd5e74b3d0cb",
    "homepage": "https://github.com/hughsk/smokestack",
    "keywords": [
        "chrome",
        "launch",
        "pipe",
        "stream",
        "exec",
        "eval",
        "run",
        "test",
        "terminal",
        "output",
        "browser"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "hughsk"
        },
        {
            "name": "timoxley"
        },
        {
            "name": "yoshuawuyts"
        }
    ],
    "name": "smokestack",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/hughsk/smokestack.git"
    },
    "scripts": {
        "prepublish": "browserify instrument.js -o bundle.js",
        "pretest": "npm run prepublish",
        "test": "npm run test:chrome && npm run test:firefox && npm run test:saucelabs",
        "test:chrome": "browser=chrome node test/index.js | tap-spec",
        "test:firefox": "browser=firefox node test/index.js | tap-spec",
        "test:saucelabs": "sauce=1 browser=chrome node test/index.js | tap-spec"
    },
    "version": "3.4.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
