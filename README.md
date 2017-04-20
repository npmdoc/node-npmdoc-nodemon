# npmdoc-nodemon

#### api documentation for  [nodemon (v1.11.0)](http://nodemon.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-nodemon.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nodemon) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nodemon.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nodemon)

#### Simple monitor script for use during development of a node.js app.

[![NPM](https://nodei.co/npm/nodemon.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/nodemon)

- [https://npmdoc.github.io/node-npmdoc-nodemon/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-nodemon/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nodemon/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nodemon/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nodemon/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nodemon/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "nodemon",
    "homepage": "http://nodemon.io",
    "author": {
        "name": "Remy Sharp",
        "url": "http://github.com/remy"
    },
    "bin": {
        "nodemon": "./bin/nodemon.js"
    },
    "engines": {
        "node": ">=0.8"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/remy/nodemon.git"
    },
    "description": "Simple monitor script for use during development of a node.js app.",
    "keywords": [
        "monitor",
        "development",
        "restart",
        "autoload",
        "reload",
        "terminal"
    ],
    "license": "MIT",
    "main": "./lib/nodemon",
    "scripts": {
        "coverage": "istanbul cover _mocha -- --timeout 30000 --ui bdd --reporter list test/**/*.test.js",
        "lint": "jscs lib/**/*.js -v",
        ":spec": "node_modules/.bin/mocha --timeout 30000 --ui bdd test/**/*.test.js",
        "test": "npm run lint && npm run spec",
        "spec": "for FILE in test/**/*.test.js; do echo $FILE; ./node_modules/.bin/mocha --timeout 30000 $FILE; if [ $? -ne 0 ]; then exit 1; fi; sleep 1; done",
        "web": "node web",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post"
    },
    "devDependencies": {
        "async": "1.4.2",
        "coffee-script": "~1.7.1",
        "connect": "~2.19.1",
        "istanbul": "~0.2.10",
        "jscs": "2.1.1",
        "mocha": "2.3.3",
        "should": "~4.0.0",
        "semantic-release": "4.3.5"
    },
    "dependencies": {
        "chokidar": "^1.4.3",
        "debug": "^2.2.0",
        "es6-promise": "^3.0.2",
        "ignore-by-default": "^1.0.0",
        "lodash.defaults": "^3.1.2",
        "minimatch": "^3.0.0",
        "ps-tree": "^1.0.1",
        "touch": "1.0.0",
        "undefsafe": "0.0.3",
        "update-notifier": "0.5.0"
    },
    "version": "1.11.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
