# api documentation for  [crapify (v1.2.0)](https://github.com/bcoe/crapify)  [![npm package](https://img.shields.io/npm/v/npmdoc-crapify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-crapify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-crapify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-crapify)
#### a proxy for simulating slow, spotty, HTTP connections

[![NPM](https://nodei.co/npm/crapify.png?downloads=true)](https://www.npmjs.com/package/crapify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-crapify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-crapify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-crapify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-crapify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-crapify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ben Coe",
        "email": "ben@npmjs.com"
    },
    "bin": {
        "crapify": "./bin/crapify.js"
    },
    "dependencies": {
        "chalk": "^0.5.1",
        "lodash": "^2.4.1",
        "monkey-proxy": "^1.2.0",
        "throttle": "^1.0.3",
        "yargs": "^1.3.3"
    },
    "description": "a proxy for simulating slow, spotty, HTTP connections",
    "devDependencies": {
        "async": "^0.9.0",
        "code": "^1.2.1",
        "lab": "^5.1.1",
        "nock": "^0.53.0",
        "request": "^2.51.0"
    },
    "directories": {},
    "dist": {
        "shasum": "92f1e884920a508900f6374b5c3a661a896b8cbb",
        "tarball": "https://registry.npmjs.org/crapify/-/crapify-1.2.0.tgz"
    },
    "git": {
        "url": "git://github.com/bcoe/crapify.git"
    },
    "gitHead": "cd5917c7d58770419fa351770ae5b454e30facd8",
    "homepage": "https://github.com/bcoe/crapify",
    "keywords": [
        "proxy",
        "slow",
        "connection-limit"
    ],
    "license": "ISC",
    "main": "index.js",
    "maintainers": [
        {
            "name": "bcoe",
            "email": "bencoe@gmail.com"
        }
    ],
    "name": "crapify",
    "optionalDependencies": {},
    "preferGlobal": true,
    "readme": "ERROR: No README data found!",
    "scripts": {
        "test": "lab -v -c --timeout 5000"
    },
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module crapify](#apidoc.module.crapify)
1.  [function <span class="apidocSignatureSpan"></span>crapify (opts)](#apidoc.element.crapify.crapify)
1.  [function <span class="apidocSignatureSpan">crapify.</span>crappy_stream (opts)](#apidoc.element.crapify.crappy_stream)
1.  object <span class="apidocSignatureSpan">crapify.</span>crapify.prototype
1.  object <span class="apidocSignatureSpan">crapify.</span>crappy_stream.prototype

#### [module crapify.crapify](#apidoc.module.crapify.crapify)
1.  [function <span class="apidocSignatureSpan">crapify.</span>crapify (opts)](#apidoc.element.crapify.crapify.crapify)

#### [module crapify.crapify.prototype](#apidoc.module.crapify.crapify.prototype)
1.  [function <span class="apidocSignatureSpan">crapify.crapify.prototype.</span>start ()](#apidoc.element.crapify.crapify.prototype.start)
1.  [function <span class="apidocSignatureSpan">crapify.crapify.prototype.</span>stop (cb)](#apidoc.element.crapify.crapify.prototype.stop)

#### [module crapify.crappy_stream](#apidoc.module.crapify.crappy_stream)
1.  [function <span class="apidocSignatureSpan">crapify.</span>crappy_stream (opts)](#apidoc.element.crapify.crappy_stream.crappy_stream)
1.  [function <span class="apidocSignatureSpan">crapify.crappy_stream.</span>super_ (options)](#apidoc.element.crapify.crappy_stream.super_)

#### [module crapify.crappy_stream.prototype](#apidoc.module.crapify.crappy_stream.prototype)
1.  [function <span class="apidocSignatureSpan">crapify.crappy_stream.prototype.</span>_flush (done)](#apidoc.element.crapify.crappy_stream.prototype._flush)
1.  [function <span class="apidocSignatureSpan">crapify.crappy_stream.prototype.</span>_transform (chunk, encoding, next)](#apidoc.element.crapify.crappy_stream.prototype._transform)



# <a name="apidoc.module.crapify"></a>[module crapify](#apidoc.module.crapify)

#### <a name="apidoc.element.crapify.crapify"></a>[function <span class="apidocSignatureSpan"></span>crapify (opts)](#apidoc.element.crapify.crapify)
- description and source-code
```javascript
function Crapify(opts) {
  // set default options if none are specified.
  _.extend(this, {
    port: 5000,
    speed: 5000,
    concurrency: 10,
    dropFrequency: 0,
    sleep: 0,
    close: false
  }, opts)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.crapify.crappy_stream"></a>[function <span class="apidocSignatureSpan">crapify.</span>crappy_stream (opts)](#apidoc.element.crapify.crappy_stream)
- description and source-code
```javascript
function CrappyStream(opts) {
  this.dropFrequency = opts.dropFrequency;
  this.byteCount = parseInt(Math.random() * opts.dropFrequency);
  Transform.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.crapify.crapify"></a>[module crapify.crapify](#apidoc.module.crapify.crapify)

#### <a name="apidoc.element.crapify.crapify.crapify"></a>[function <span class="apidocSignatureSpan">crapify.</span>crapify (opts)](#apidoc.element.crapify.crapify.crapify)
- description and source-code
```javascript
function Crapify(opts) {
  // set default options if none are specified.
  _.extend(this, {
    port: 5000,
    speed: 5000,
    concurrency: 10,
    dropFrequency: 0,
    sleep: 0,
    close: false
  }, opts)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.crapify.crapify.prototype"></a>[module crapify.crapify.prototype](#apidoc.module.crapify.crapify.prototype)

#### <a name="apidoc.element.crapify.crapify.prototype.start"></a>[function <span class="apidocSignatureSpan">crapify.crapify.prototype.</span>start ()](#apidoc.element.crapify.crapify.prototype.start)
- description and source-code
```javascript
start = function () {
  var _this = this;

  this.server = proxy(http.createServer(), {
    transformRequest: [crappyStreamFactory, throttleFactory],
    transformResponse: [crappyStreamFactory, throttleFactory],
    sleep: this.sleep,
    concurrency: this.concurrency,
    close: this.close
  });

  this.server.listen(this.port, function () {
    console.log(chalk.yellow('proxy serving on :' + _this.port + ' at ' + _this.speed + ' bytes/sec, max concurrency = ' + _this
.concurrency + ', dropped bytes frequency = ' + _this.dropFrequency));
  });

  this.server.on('connection', function (socket) {
    _this.socket = socket;
  });

  function crappyStreamFactory () {
    return new CrappyStream({
      dropFrequency: _this.dropFrequency
    });
  }

  function throttleFactory () {
    return new Throttle(_this.speed);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.crapify.crapify.prototype.stop"></a>[function <span class="apidocSignatureSpan">crapify.crapify.prototype.</span>stop (cb)](#apidoc.element.crapify.crapify.prototype.stop)
- description and source-code
```javascript
stop = function (cb) {
  var _this = this;

  this.server.close(function () {
    _this.socket.destroy();
    return cb();
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.crapify.crappy_stream"></a>[module crapify.crappy_stream](#apidoc.module.crapify.crappy_stream)

#### <a name="apidoc.element.crapify.crappy_stream.crappy_stream"></a>[function <span class="apidocSignatureSpan">crapify.</span>crappy_stream (opts)](#apidoc.element.crapify.crappy_stream.crappy_stream)
- description and source-code
```javascript
function CrappyStream(opts) {
  this.dropFrequency = opts.dropFrequency;
  this.byteCount = parseInt(Math.random() * opts.dropFrequency);
  Transform.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.crapify.crappy_stream.super_"></a>[function <span class="apidocSignatureSpan">crapify.crappy_stream.</span>super_ (options)](#apidoc.element.crapify.crappy_stream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform))
    return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function')
      this._transform = options.transform;

    if (typeof options.flush === 'function')
      this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function() {
    if (typeof this._flush === 'function')
      this._flush(function(er) {
        done(stream, er);
      });
    else
      done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.crapify.crappy_stream.prototype"></a>[module crapify.crappy_stream.prototype](#apidoc.module.crapify.crappy_stream.prototype)

#### <a name="apidoc.element.crapify.crappy_stream.prototype._flush"></a>[function <span class="apidocSignatureSpan">crapify.crappy_stream.prototype.</span>_flush (done)](#apidoc.element.crapify.crappy_stream.prototype._flush)
- description and source-code
```javascript
_flush = function (done) {
  return done();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.crapify.crappy_stream.prototype._transform"></a>[function <span class="apidocSignatureSpan">crapify.crappy_stream.prototype.</span>_transform (chunk, encoding, next)](#apidoc.element.crapify.crappy_stream.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, encoding, next) {
  if (this.dropFrequency !== 0) {
    var i = 0,
      ii = 0,
      buffer = new Buffer(chunk.length);

    // Iterate over the bytes of a chunk with 'i', and copy a byte into
    // a temporary buffer at index 'ii' if it is not to be dropped.
    // Note that this method drops bytes in a uniform distribution.
    for (; i < chunk.length; i++) {
      this.byteCount++;
      if (this.byteCount % this.dropFrequency === 0) {
        continue;
      }
      buffer[ii] = chunk[i];
      ii++;
    }

    // Since the buffer may be shorter due to dropped bytes, it is needed
    // to slice off the unassigned bytes at the end of the buffer.
    this.push(buffer.slice(0, ii));

  } else {
    // Skip iterating over bytes if nothing is to be dropped, just write
    // it and get it over with.
    this.push(chunk);
  }

  return next();
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
