# api documentation for  [node-tweet-stream (v2.0.1)](https://github.com/SpiderStrategies/node-tweet-stream#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-tweet-stream.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-tweet-stream) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-tweet-stream.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-tweet-stream)
#### A twitter module to hook into the public filter streaming, seamlessly updating the tracking keywords.

[![NPM](https://nodei.co/npm/node-tweet-stream.png?downloads=true)](https://www.npmjs.com/package/node-tweet-stream)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-tweet-stream/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-tweet-stream_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-tweet-stream/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-tweet-stream/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-tweet-stream/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nathan Bowser",
        "email": "nathan.bowser@spiderstrategies.com"
    },
    "bugs": {
        "url": "https://github.com/SpiderStrategies/node-tweet-stream/issues"
    },
    "dependencies": {
        "event-stream": "~3.1.0",
        "request": "^2.55.0",
        "split": "^0.3.0"
    },
    "description": "A twitter module to hook into the public filter streaming, seamlessly updating the tracking keywords.",
    "devDependencies": {
        "mocha": "~1.17.1",
        "nock": "~0.27.2"
    },
    "directories": {},
    "dist": {
        "shasum": "fb4ff15fd695211d0fde59f6e6557afc48e1d791",
        "tarball": "https://registry.npmjs.org/node-tweet-stream/-/node-tweet-stream-2.0.1.tgz"
    },
    "gitHead": "f16a1c4802726f0bcbe231e37af4f2ef9ca0e675",
    "homepage": "https://github.com/SpiderStrategies/node-tweet-stream#readme",
    "keywords": [
        "twitter",
        "streaming",
        "twitter public",
        "tweet"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "koopa",
            "email": "nbowser@gmail.com"
        }
    ],
    "name": "node-tweet-stream",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/SpiderStrategies/node-tweet-stream.git"
    },
    "scripts": {
        "test": "mocha -R spec test"
    },
    "version": "2.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-tweet-stream](#apidoc.module.node-tweet-stream)
1.  [function <span class="apidocSignatureSpan">node-tweet-stream.</span>super_ (options)](#apidoc.element.node-tweet-stream.super_)



# <a name="apidoc.module.node-tweet-stream"></a>[module node-tweet-stream](#apidoc.module.node-tweet-stream)

#### <a name="apidoc.element.node-tweet-stream.super_"></a>[function <span class="apidocSignatureSpan">node-tweet-stream.</span>super_ (options)](#apidoc.element.node-tweet-stream.super_)
- description and source-code
```javascript
function Writable(options) {
  // Writable ctor is applied to Duplexes, too.
  // 'realHasInstance' is necessary because using plain 'instanceof'
  // would return false, as no '_writableState' property is attached.

  // Trying to use the custom 'instanceof' for Writable here will also break the
  // Node.js LazyTransform implementation, which has a non-trivial getter for
  // '_writableState' that would lead to infinite recursion.
  if (!(realHasInstance.call(Writable, this)) &&
      !(this instanceof Stream.Duplex)) {
    return new Writable(options);
  }

  this._writableState = new WritableState(options, this);

  // legacy.
  this.writable = true;

  if (options) {
    if (typeof options.write === 'function')
      this._write = options.write;

    if (typeof options.writev === 'function')
      this._writev = options.writev;
  }

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
