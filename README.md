# npmdoc-wpapi

#### api documentation for  [wpapi (v1.0.3)](https://github.com/wp-api/node-wpapi)  [![npm package](https://img.shields.io/npm/v/npmdoc-wpapi.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-wpapi) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-wpapi.svg)](https://travis-ci.org/npmdoc/node-npmdoc-wpapi)

#### An isomorphic JavaScript client for interacting with the WordPress REST API

[![NPM](https://nodei.co/npm/wpapi.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/wpapi)

- [https://npmdoc.github.io/node-npmdoc-wpapi/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-wpapi/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-wpapi/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-wpapi/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "K.Adam White",
        "url": "http://www.kadamwhite.com"
    },
    "bugs": {
        "url": "https://github.com/wp-api/node-wpapi/issues"
    },
    "dependencies": {
        "es6-promise": "^3.2.1",
        "li": "^1.0.1",
        "lodash.uniq": "^4.3.0",
        "node.extend": "^1.1.5",
        "parse-link-header": "^0.4.1",
        "qs": "^6.2.0",
        "route-parser": "0.0.4",
        "superagent": "^3.3.1"
    },
    "description": "An isomorphic JavaScript client for interacting with the WordPress REST API",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "combyne": "^2.0.0",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-clean": "^1.0.0",
        "grunt-contrib-jshint": "^1.0.0",
        "grunt-contrib-yuidoc": "^1.0.0",
        "grunt-zip": "^0.17.1",
        "istanbul": "^0.4.4",
        "jscs": "^3.0.6",
        "jscs-stylish": "^0.3.1",
        "jshint": "^2.9.2",
        "jshint-stylish": "^2.2.0",
        "json-loader": "^0.5.4",
        "kramed": "^0.5.6",
        "load-grunt-tasks": "^3.5.0",
        "lodash.reduce": "^4.6.0",
        "minimist": "^1.2.0",
        "mocha": "^2.5.3",
        "prompt": "^1.0.0",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0",
        "webpack": "^1.13.1"
    },
    "directories": {},
    "dist": {
        "shasum": "e2ffdfb1181e2856140e78e1c74406d3839ba226",
        "tarball": "https://registry.npmjs.org/wpapi/-/wpapi-1.0.3.tgz"
    },
    "gitHead": "e2c89fd650baf03e72ef730cb7539b9b593162de",
    "homepage": "https://github.com/wp-api/node-wpapi",
    "keywords": [
        "api",
        "client",
        "cms",
        "wordpress"
    ],
    "license": "MIT",
    "main": "wpapi.js",
    "maintainers": [
        {
            "name": "kadamwhite"
        }
    ],
    "name": "wpapi",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/wp-api/node-wpapi.git"
    },
    "scripts": {
        "build": "webpack && webpack --config webpack.config.minified.js",
        "docs": "grunt docs",
        "jekyll": "node bin/jekyll",
        "jscs": "jscs Gruntfile.js wpapi.js bin build lib tests --reporter node_modules/jscs-stylish/jscs-stylish.js",
        "jshint": "jshint --reporter=node_modules/jshint-stylish/index.js Gruntfile.js wpapi.js bin build lib tests",
        "lint": "npm run jshint && npm run jscs || true",
        "mocha": "_mocha tests --recursive --reporter=nyan",
        "pretest": "npm run lint",
        "release-docs": "node build/scripts/release-docs",
        "release-npm": "npm run build && npm test && npm publish",
        "test": "istanbul cover _mocha -- tests --recursive --reporter=nyan",
        "test:all": "_mocha tests --recursive --reporter=nyan",
        "test:ci": "npm run lint && istanbul cover _mocha -- tests/unit --recursive --reporter=list",
        "test:integration": "_mocha tests/integration --recursive --reporter=nyan",
        "test:unit": "_mocha tests/unit --recursive --reporter=nyan",
        "update-default-routes-json": "node ./lib/data/update-default-routes-json",
        "watch": "grunt watch",
        "zip": "npm run build && grunt zip"
    },
    "version": "1.0.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
