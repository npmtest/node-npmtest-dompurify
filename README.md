# npmtest-dompurify

#### basic test coverage for  [dompurify (v0.8.5)](https://github.com/cure53/DOMPurify)  [![npm package](https://img.shields.io/npm/v/npmtest-dompurify.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-dompurify) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-dompurify.svg)](https://travis-ci.org/npmtest/node-npmtest-dompurify)

#### DOMPurify is a DOM-only, super-fast, uber-tolerant XSS sanitizer for HTML, MathML and SVG. It's written in JavaScript and works in all modern browsers (Safari, Opera (15+), Internet Explorer (10+), Firefox and Chrome - as well as almost anything else usin

[![NPM](https://nodei.co/npm/dompurify.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/dompurify)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-dompurify/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-dompurify/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-dompurify/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-dompurify/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-dompurify/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-dompurify/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-dompurify/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-dompurify/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-dompurify/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-dompurify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-dompurify/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-dompurify/build/test-report.html](https://npmtest.github.io/node-npmtest-dompurify/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-dompurify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-dompurify/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-dompurify/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-dompurify/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dompurify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dompurify/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-dompurify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-dompurify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mario Heiderich",
        "url": "https://cure53.de/"
    },
    "bugs": {
        "url": "https://github.com/cure53/DOMPurify/issues"
    },
    "dependencies": {},
    "description": "DOMPurify is a DOM-only, super-fast, uber-tolerant XSS sanitizer for HTML, MathML and SVG. It's written in JavaScript and works in all modern browsers (Safari, Opera (15+), Internet Explorer (10+), Firefox and Chrome - as well as almost anything else usin",
    "devDependencies": {
        "jquery": "^2.2.3",
        "jsdom": "8.x.x",
        "jshint": "^2.9.2",
        "json-loader": "^0.5.4",
        "karma": "^0.13.22",
        "karma-browserstack-launcher": "1.0.0",
        "karma-chrome-launcher": "^1.0.1",
        "karma-firefox-launcher": "^1.0.0",
        "karma-fixture": "^0.2.6",
        "karma-html2js-preprocessor": "^1.0.0",
        "karma-json-fixtures-preprocessor": "0.0.6",
        "karma-qunit": "^1.0.0",
        "karma-webpack": "^1.7.0",
        "pre-commit": "^1.1.2",
        "qunit-parameterize": "^0.4.0",
        "qunit-tap": "^1.5.0",
        "qunitjs": "^1.23.1",
        "uglify-js": "^2.6.2",
        "webpack": "^1.13.0"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "5bc591b61e222243cc827ca382d7a2e2660c1a44",
        "tarball": "https://registry.npmjs.org/dompurify/-/dompurify-0.8.5.tgz"
    },
    "files": [
        "src",
        "dist"
    ],
    "gitHead": "4222069a807a819dc6cb0a6cc0a1b99ef1ca4c56",
    "homepage": "https://github.com/cure53/DOMPurify",
    "keywords": [
        "dom",
        "xss",
        "html",
        "svg",
        "mathml",
        "security",
        "secure",
        "sanitizer",
        "sanitize",
        "filter",
        "purify"
    ],
    "license": "MPL-2.0 OR Apache-2.0",
    "main": "src/purify.js",
    "maintainers": [
        {
            "name": "cure53"
        },
        {
            "name": "fhemberger"
        }
    ],
    "name": "dompurify",
    "optionalDependencies": {},
    "pre-commit": [
        "lint",
        "minify",
        "amend-minified"
    ],
    "repository": {
        "type": "git",
        "url": "git://github.com/cure53/DOMPurify.git"
    },
    "scripts": {
        "amend-minified": "scripts/amend-minified.sh",
        "build-demo": "node scripts/build-demo.js",
        "lint": "jshint src/purify.js",
        "minify": "scripts/minify.sh",
        "test": "npm run lint && npm run test:jsdom && npm run test:karma -- --browsers Firefox,Chrome",
        "test:ci": "npm run lint && npm run test:jsdom && (([ \"${TRAVIS_PULL_REQUEST}\" != \"false\" ] || [ \"${TEST_BROWSERSTACK}\" != \"true\" ]) || karma start test/karma.conf.js --log-level error --reporters dots --single-run)",
        "test:jsdom": "node test/jsdom-node-runner --dot",
        "test:karma": "karma start test/karma.conf.js --log-level warn --single-run"
    },
    "version": "0.8.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
