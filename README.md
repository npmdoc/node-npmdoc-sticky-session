# api documentation for  sticky-session (v1.1.2)  [![npm package](https://img.shields.io/npm/v/npmdoc-sticky-session.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sticky-session) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sticky-session.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sticky-session)
#### Sticky session balancer based on a `cluster` module

[![NPM](https://nodei.co/npm/sticky-session.png?downloads=true)](https://www.npmjs.com/package/sticky-session)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sticky-session/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sticky-session_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sticky-session/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sticky-session/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sticky-session/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Fedor Indutny",
        "email": "fedor.indutny@gmail.com"
    },
    "dependencies": {
        "debug": "^2.2.0",
        "ip": "^1.0.0"
    },
    "description": "Sticky session balancer based on a 'cluster' module",
    "devDependencies": {
        "jscs": "^2.1.1",
        "jshint": "^2.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "716ce738452bbe9eedec506311895a3d64803de1",
        "tarball": "https://registry.npmjs.org/sticky-session/-/sticky-session-1.1.2.tgz"
    },
    "engines": {
        "node": ">= 0.12.0"
    },
    "gitHead": "e0de9b7786255bf5d4c23f9714699b8d12e9882a",
    "license": "MIT",
    "main": "./lib/sticky-session",
    "maintainers": [
        {
            "name": "fedor.indutny",
            "email": "fedor.indutny@gmail.com"
        },
        {
            "name": "indutny",
            "email": "fedor@indutny.com"
        },
        {
            "name": "tlhunter",
            "email": "tlhunter@gmail.com"
        }
    ],
    "name": "sticky-session",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "scripts": {
        "lint": "jscs lib/*.js lib/**/*.js && jshint lib/*.js lib/**/*.js",
        "test": "npm run lint && (echo test/*-test.js | xargs node)"
    },
    "version": "1.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sticky-session](#apidoc.module.sticky-session)
1.  [function <span class="apidocSignatureSpan">sticky-session.</span>Master (workerCount, env)](#apidoc.element.sticky-session.Master)
1.  [function <span class="apidocSignatureSpan">sticky-session.</span>Master.super_ (options, connectionListener)](#apidoc.element.sticky-session.Master.super_)
1.  [function <span class="apidocSignatureSpan">sticky-session.</span>listen (server, port, options)](#apidoc.element.sticky-session.listen)
1.  object <span class="apidocSignatureSpan">sticky-session.</span>Master.prototype
1.  object <span class="apidocSignatureSpan">sticky-session.</span>Master.super_.prototype

#### [module sticky-session.Master](#apidoc.module.sticky-session.Master)
1.  [function <span class="apidocSignatureSpan">sticky-session.</span>Master (workerCount, env)](#apidoc.element.sticky-session.Master.Master)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.</span>super_ (options, connectionListener)](#apidoc.element.sticky-session.Master.super_)

#### [module sticky-session.Master.prototype](#apidoc.module.sticky-session.Master.prototype)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>balance (socket)](#apidoc.element.sticky-session.Master.prototype.balance)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>hash (ip)](#apidoc.element.sticky-session.Master.prototype.hash)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>respawn (worker)](#apidoc.element.sticky-session.Master.prototype.respawn)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>spawnWorker ()](#apidoc.element.sticky-session.Master.prototype.spawnWorker)

#### [module sticky-session.Master.super_](#apidoc.module.sticky-session.Master.super_)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.</span>super_ ()](#apidoc.element.sticky-session.Master.super_.super_)

#### [module sticky-session.Master.super_.prototype](#apidoc.module.sticky-session.Master.super_.prototype)
1.  boolean <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>listening
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_emitCloseIfDrained ()](#apidoc.element.sticky-session.Master.super_.prototype._emitCloseIfDrained)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_listen2 (address, port, addressType, backlog, fd)](#apidoc.element.sticky-session.Master.super_.prototype._listen2)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_setupSlave (socketList)](#apidoc.element.sticky-session.Master.super_.prototype._setupSlave)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>address ()](#apidoc.element.sticky-session.Master.super_.prototype.address)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>close (cb)](#apidoc.element.sticky-session.Master.super_.prototype.close)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>getConnections (cb)](#apidoc.element.sticky-session.Master.super_.prototype.getConnections)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>listen ()](#apidoc.element.sticky-session.Master.super_.prototype.listen)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>listenFD ()](#apidoc.element.sticky-session.Master.super_.prototype.listenFD)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>ref ()](#apidoc.element.sticky-session.Master.super_.prototype.ref)
1.  [function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>unref ()](#apidoc.element.sticky-session.Master.super_.prototype.unref)



# <a name="apidoc.module.sticky-session"></a>[module sticky-session](#apidoc.module.sticky-session)

#### <a name="apidoc.element.sticky-session.Master"></a>[function <span class="apidocSignatureSpan">sticky-session.</span>Master (workerCount, env)](#apidoc.element.sticky-session.Master)
- description and source-code
```javascript
function Master(workerCount, env) {
  net.Server.call(this, {
    pauseOnConnect: true
  }, this.balance);

  this.env = env || {};

  this.seed = (Math.random() * 0xffffffff) | 0;
  this.workers = [];

  debug('master seed=%d', this.seed);

  this.once('listening', function() {
    debug('master listening on %j', this.address());

    for (var i = 0; i < workerCount; i++)
      this.spawnWorker();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_"></a>[function <span class="apidocSignatureSpan">sticky-session.</span>Master.super_ (options, connectionListener)](#apidoc.element.sticky-session.Master.super_)
- description and source-code
```javascript
function Server(options, connectionListener) {
  if (!(this instanceof Server))
    return new Server(options, connectionListener);

  EventEmitter.call(this);

  if (typeof options === 'function') {
    connectionListener = options;
    options = {};
    this.on('connection', connectionListener);
  } else if (options == null || typeof options === 'object') {
    options = options || {};

    if (typeof connectionListener === 'function') {
      this.on('connection', connectionListener);
    }
  } else {
    throw new TypeError('options must be an object');
  }

  this._connections = 0;

  Object.defineProperty(this, 'connections', {
    get: internalUtil.deprecate(() => {

      if (this._usingSlaves) {
        return null;
      }
      return this._connections;
    }, 'Server.connections property is deprecated. ' +
       'Use Server.getConnections method instead.'),
    set: internalUtil.deprecate((val) => {
      return (this._connections = val);
    }, 'Server.connections property is deprecated.'),
    configurable: true, enumerable: false
  });

  this._handle = null;
  this._usingSlaves = false;
  this._slaves = [];
  this._unref = false;

  this.allowHalfOpen = options.allowHalfOpen || false;
  this.pauseOnConnect = !!options.pauseOnConnect;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.listen"></a>[function <span class="apidocSignatureSpan">sticky-session.</span>listen (server, port, options)](#apidoc.element.sticky-session.listen)
- description and source-code
```javascript
function listen(server, port, options) {
  if (!options)
    options = {};

  if (cluster.isMaster) {
    var workerCount = options.workers || os.cpus().length;

    var master = new Master(workerCount, options.env);
    master.listen(port);
    master.once('listening', function() {
      server.emit('listening');
    });
    return false;
  }

  // Override close callback to gracefully close server
  var oldClose = server.close;
  server.close = function close() {
    debug('graceful close');
    process.send({ type: 'close' });
    return oldClose.apply(this, arguments);
  };

  process.on('message', function(msg, socket) {
    if (msg !== 'sticky:balance' || !socket)
      return;

    debug('incoming socket');
    server._connections++;
    socket.server = server;
    server.emit('connection', socket);
  });
  return true;
}
```
- example usage
```shell
...
var cluster = require('cluster'); // Only required if you want the worker id
var sticky = require('sticky-session');

var server = require('http').createServer(function(req, res) {
  res.end('worker: ' + cluster.worker.id);
});

if (!sticky.listen(server, 3000)) {
  // Master code
  server.once('listening', function() {
    console.log('server started on 3000 port');
  });
} else {
  // Worker code
}
...
```



# <a name="apidoc.module.sticky-session.Master"></a>[module sticky-session.Master](#apidoc.module.sticky-session.Master)

#### <a name="apidoc.element.sticky-session.Master.Master"></a>[function <span class="apidocSignatureSpan">sticky-session.</span>Master (workerCount, env)](#apidoc.element.sticky-session.Master.Master)
- description and source-code
```javascript
function Master(workerCount, env) {
  net.Server.call(this, {
    pauseOnConnect: true
  }, this.balance);

  this.env = env || {};

  this.seed = (Math.random() * 0xffffffff) | 0;
  this.workers = [];

  debug('master seed=%d', this.seed);

  this.once('listening', function() {
    debug('master listening on %j', this.address());

    for (var i = 0; i < workerCount; i++)
      this.spawnWorker();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.</span>super_ (options, connectionListener)](#apidoc.element.sticky-session.Master.super_)
- description and source-code
```javascript
function Server(options, connectionListener) {
  if (!(this instanceof Server))
    return new Server(options, connectionListener);

  EventEmitter.call(this);

  if (typeof options === 'function') {
    connectionListener = options;
    options = {};
    this.on('connection', connectionListener);
  } else if (options == null || typeof options === 'object') {
    options = options || {};

    if (typeof connectionListener === 'function') {
      this.on('connection', connectionListener);
    }
  } else {
    throw new TypeError('options must be an object');
  }

  this._connections = 0;

  Object.defineProperty(this, 'connections', {
    get: internalUtil.deprecate(() => {

      if (this._usingSlaves) {
        return null;
      }
      return this._connections;
    }, 'Server.connections property is deprecated. ' +
       'Use Server.getConnections method instead.'),
    set: internalUtil.deprecate((val) => {
      return (this._connections = val);
    }, 'Server.connections property is deprecated.'),
    configurable: true, enumerable: false
  });

  this._handle = null;
  this._usingSlaves = false;
  this._slaves = [];
  this._unref = false;

  this.allowHalfOpen = options.allowHalfOpen || false;
  this.pauseOnConnect = !!options.pauseOnConnect;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sticky-session.Master.prototype"></a>[module sticky-session.Master.prototype](#apidoc.module.sticky-session.Master.prototype)

#### <a name="apidoc.element.sticky-session.Master.prototype.balance"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>balance (socket)](#apidoc.element.sticky-session.Master.prototype.balance)
- description and source-code
```javascript
function balance(socket) {
  var addr = ip.toBuffer(socket.remoteAddress || '127.0.0.1');
  var hash = this.hash(addr);

  debug('balacing connection %j', addr);
  this.workers[hash % this.workers.length].send('sticky:balance', socket);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.prototype.hash"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>hash (ip)](#apidoc.element.sticky-session.Master.prototype.hash)
- description and source-code
```javascript
function hash(ip) {
  var hash = this.seed;
  for (var i = 0; i < ip.length; i++) {
    var num = ip[i];

    hash += num;
    hash %= 2147483648;
    hash += (hash << 10);
    hash %= 2147483648;
    hash ^= hash >> 6;
  }

  hash += hash << 3;
  hash %= 2147483648;
  hash ^= hash >> 11;
  hash += hash << 15;
  hash %= 2147483648;

  return hash >>> 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.prototype.respawn"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>respawn (worker)](#apidoc.element.sticky-session.Master.prototype.respawn)
- description and source-code
```javascript
function respawn(worker) {
  var index = this.workers.indexOf(worker);
  if (index !== -1)
    this.workers.splice(index, 1);
  this.spawnWorker();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.prototype.spawnWorker"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.prototype.</span>spawnWorker ()](#apidoc.element.sticky-session.Master.prototype.spawnWorker)
- description and source-code
```javascript
function spawnWorker() {
  var worker = cluster.fork(this.env);

  var self = this;
  worker.on('exit', function(code) {
    debug('worker=%d died with code=%d', worker.process.pid, code);
    self.respawn(worker);
  });

  worker.on('message', function(msg) {
    // Graceful exit
    if (msg.type === 'close')
      self.respawn(worker);
  });

  debug('worker=%d spawn', worker.process.pid);
  this.workers.push(worker);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sticky-session.Master.super_"></a>[module sticky-session.Master.super_](#apidoc.module.sticky-session.Master.super_)

#### <a name="apidoc.element.sticky-session.Master.super_.super_"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.</span>super_ ()](#apidoc.element.sticky-session.Master.super_.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sticky-session.Master.super_.prototype"></a>[module sticky-session.Master.super_.prototype](#apidoc.module.sticky-session.Master.super_.prototype)

#### <a name="apidoc.element.sticky-session.Master.super_.prototype._emitCloseIfDrained"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_emitCloseIfDrained ()](#apidoc.element.sticky-session.Master.super_.prototype._emitCloseIfDrained)
- description and source-code
```javascript
_emitCloseIfDrained = function () {
  debug('SERVER _emitCloseIfDrained');

  if (this._handle || this._connections) {
    debug('SERVER handle? %j   connections? %d',
          !!this._handle, this._connections);
    return;
  }

  process.nextTick(emitCloseNT, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype._listen2"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_listen2 (address, port, addressType, backlog, fd)](#apidoc.element.sticky-session.Master.super_.prototype._listen2)
- description and source-code
```javascript
_listen2 = function (address, port, addressType, backlog, fd) {
  debug('listen2', address, port, addressType, backlog, fd);

  // If there is not yet a handle, we need to create one and bind.
  // In the case of a server sent via IPC, we don't need to do this.
  if (this._handle) {
    debug('_listen2: have a handle already');
  } else {
    debug('_listen2: create a handle');

    var rval = null;

    if (!address && typeof fd !== 'number') {
      rval = createServerHandle('::', port, 6, fd);

      if (typeof rval === 'number') {
        rval = null;
        address = '0.0.0.0';
        addressType = 4;
      } else {
        address = '::';
        addressType = 6;
      }
    }

    if (rval === null)
      rval = createServerHandle(address, port, addressType, fd);

    if (typeof rval === 'number') {
      var error = exceptionWithHostPort(rval, 'listen', address, port);
      process.nextTick(emitErrorNT, this, error);
      return;
    }
    this._handle = rval;
  }

  this._handle.onconnection = onconnection;
  this._handle.owner = this;

  var err = _listen(this._handle, backlog);

  if (err) {
    var ex = exceptionWithHostPort(err, 'listen', address, port);
    this._handle.close();
    this._handle = null;
    process.nextTick(emitErrorNT, this, ex);
    return;
  }

  // generate connection key, this should be unique to the connection
  this._connectionKey = addressType + ':' + address + ':' + port;

  // unref the handle if the server was unref'ed prior to listening
  if (this._unref)
    this.unref();

  process.nextTick(emitListeningNT, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype._setupSlave"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>_setupSlave (socketList)](#apidoc.element.sticky-session.Master.super_.prototype._setupSlave)
- description and source-code
```javascript
_setupSlave = function (socketList) {
  this._usingSlaves = true;
  this._slaves.push(socketList);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.address"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>address ()](#apidoc.element.sticky-session.Master.super_.prototype.address)
- description and source-code
```javascript
address = function () {
  if (this._handle && this._handle.getsockname) {
    var out = {};
    this._handle.getsockname(out);
    // TODO(bnoordhuis) Check err and throw?
    return out;
  } else if (this._pipeName) {
    return this._pipeName;
  } else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.close"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>close (cb)](#apidoc.element.sticky-session.Master.super_.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  function onSlaveClose() {
    if (--left !== 0) return;

    self._connections = 0;
    self._emitCloseIfDrained();
  }

  if (typeof cb === 'function') {
    if (!this._handle) {
      this.once('close', function() {
        cb(new Error('Not running'));
      });
    } else {
      this.once('close', cb);
    }
  }

  if (this._handle) {
    this._handle.close();
    this._handle = null;
  }

  if (this._usingSlaves) {
    var self = this;
    var left = this._slaves.length;

    // Increment connections to be sure that, even if all sockets will be closed
    // during polling of slaves, 'close' event will be emitted only once.
    this._connections++;

    // Poll slaves
    this._slaves.forEach(function(slave) {
      slave.close(onSlaveClose);
    });
  } else {
    this._emitCloseIfDrained();
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.getConnections"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>getConnections (cb)](#apidoc.element.sticky-session.Master.super_.prototype.getConnections)
- description and source-code
```javascript
getConnections = function (cb) {
  function end(err, connections) {
    process.nextTick(cb, err, connections);
  }

  if (!this._usingSlaves) {
    return end(null, this._connections);
  }

  // Poll slaves
  var left = this._slaves.length;
  var total = this._connections;

  function oncount(err, count) {
    if (err) {
      left = -1;
      return end(err);
    }

    total += count;
    if (--left === 0) return end(null, total);
  }

  this._slaves.forEach(function(slave) {
    slave.getConnections(oncount);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.listen"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>listen ()](#apidoc.element.sticky-session.Master.super_.prototype.listen)
- description and source-code
```javascript
listen = function () {
  var self = this;

  var lastArg = arguments[arguments.length - 1];
  if (typeof lastArg === 'function') {
    self.once('listening', lastArg);
  }

  var port = toNumber(arguments[0]);

  // The third optional argument is the backlog size.
  // When the ip is omitted it can be the second argument.
  var backlog = toNumber(arguments[1]) || toNumber(arguments[2]);

  if (arguments.length === 0 || typeof arguments[0] === 'function') {
    // Bind to a random port.
    listen(self, null, 0, null, backlog);
  } else if (arguments[0] !== null && typeof arguments[0] === 'object') {
    var h = arguments[0];
    h = h._handle || h.handle || h;

    if (h instanceof TCP) {
      self._handle = h;
      listen(self, null, -1, -1, backlog);
    } else if (typeof h.fd === 'number' && h.fd >= 0) {
      listen(self, null, null, null, backlog, h.fd);
    } else {
      // The first argument is a configuration object
      if (h.backlog)
        backlog = h.backlog;

      if (typeof h.port === 'number' || typeof h.port === 'string' ||
          (typeof h.port === 'undefined' && 'port' in h)) {
        // Undefined is interpreted as zero (random port) for consistency
        // with net.connect().
        assertPort(h.port);
        if (h.host)
          listenAfterLookup(h.port | 0, h.host, backlog, h.exclusive);
        else
          listen(self, null, h.port | 0, 4, backlog, undefined, h.exclusive);
      } else if (h.path && isPipeName(h.path)) {
        const pipeName = self._pipeName = h.path;
        listen(self, pipeName, -1, -1, backlog, undefined, h.exclusive);
      } else {
        throw new Error('Invalid listen argument: ' + h);
      }
    }
  } else if (isPipeName(arguments[0])) {
    // UNIX socket or Windows pipe.
    const pipeName = self._pipeName = arguments[0];
    listen(self, pipeName, -1, -1, backlog);

  } else if (arguments[1] === undefined ||
             typeof arguments[1] === 'function' ||
             typeof arguments[1] === 'number') {
    // The first argument is the port, no IP given.
    assertPort(port);
    listen(self, null, port, 4, backlog);

  } else {
    // The first argument is the port, the second an IP.
    assertPort(port);
    listenAfterLookup(port, arguments[1], backlog);
  }

  function listenAfterLookup(port, address, backlog, exclusive) {
    require('dns').lookup(address, function(err, ip, addressType) {
      if (err) {
        self.emit('error', err);
      } else {
        addressType = ip ? addressType : 4;
        listen(self, ip, port, addressType, backlog, undefined, exclusive);
      }
    });
  }

  return self;
}
```
- example usage
```shell
...
var cluster = require('cluster'); // Only required if you want the worker id
var sticky = require('sticky-session');

var server = require('http').createServer(function(req, res) {
  res.end('worker: ' + cluster.worker.id);
});

if (!sticky.listen(server, 3000)) {
  // Master code
  server.once('listening', function() {
    console.log('server started on 3000 port');
  });
} else {
  // Worker code
}
...
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.listenFD"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>listenFD ()](#apidoc.element.sticky-session.Master.super_.prototype.listenFD)
- description and source-code
```javascript
function deprecated() {
  warned = exports.printDeprecationMessage(msg, warned, deprecated);
  if (new.target) {
    return Reflect.construct(fn, arguments, new.target);
  }
  return fn.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.ref"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>ref ()](#apidoc.element.sticky-session.Master.super_.prototype.ref)
- description and source-code
```javascript
ref = function () {
  this._unref = false;

  if (this._handle)
    this._handle.ref();

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sticky-session.Master.super_.prototype.unref"></a>[function <span class="apidocSignatureSpan">sticky-session.Master.super_.prototype.</span>unref ()](#apidoc.element.sticky-session.Master.super_.prototype.unref)
- description and source-code
```javascript
unref = function () {
  this._unref = true;

  if (this._handle)
    this._handle.unref();

  return this;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
