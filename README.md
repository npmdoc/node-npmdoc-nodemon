# api documentation for  [nodemon (v1.11.0)](http://nodemon.io)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nodemon.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nodemon)
#### Simple monitor script for use during development of a node.js app.

[![NPM](https://nodei.co/npm/nodemon.png?downloads=true)](https://www.npmjs.com/package/nodemon)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nodemon/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-nodemon_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nodemon/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-nodemon/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Remy Sharp",
        "url": "http://github.com/remy"
    },
    "bin": {
        "nodemon": "./bin/nodemon.js"
    },
    "bugs": {
        "url": "https://github.com/remy/nodemon/issues"
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
    "description": "Simple monitor script for use during development of a node.js app.",
    "devDependencies": {
        "async": "1.4.2",
        "coffee-script": "~1.7.1",
        "connect": "~2.19.1",
        "istanbul": "~0.2.10",
        "jscs": "2.1.1",
        "mocha": "2.3.3",
        "semantic-release": "4.3.5",
        "should": "~4.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "226c562bd2a7b13d3d7518b49ad4828a3623d06c",
        "tarball": "https://registry.npmjs.org/nodemon/-/nodemon-1.11.0.tgz"
    },
    "engines": {
        "node": ">=0.8"
    },
    "gitHead": "2cd85b1f609e9749d19afcdbd71368e6ab063f9d",
    "homepage": "http://nodemon.io",
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
    "maintainers": [
        {
            "name": "remy",
            "email": "remy@remysharp.com"
        }
    ],
    "name": "nodemon",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/remy/nodemon.git"
    },
    "scripts": {
        ":spec": "mocha --timeout 30000 --ui bdd test/**/*.test.js",
        "coverage": "istanbul cover _mocha -- --timeout 30000 --ui bdd --reporter list test/**/*.test.js",
        "lint": "jscs lib/**/*.js -v",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "spec": "for FILE in test/**/*.test.js; do echo $FILE; ./node_modules/.bin/mocha --timeout 30000 $FILE; if [ $? -ne 0 ]; then exit 1; fi; sleep 1; done",
        "test": "npm run lint && npm run spec",
        "web": "node web"
    },
    "version": "1.11.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module nodemon](#apidoc.module.nodemon)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>addListener (event, handler)](#apidoc.element.nodemon.addListener)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>emit ()](#apidoc.element.nodemon.emit)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>on (event, handler)](#apidoc.element.nodemon.on)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>once (event, handler)](#apidoc.element.nodemon.once)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>removeAllListeners (event)](#apidoc.element.nodemon.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>reset (done)](#apidoc.element.nodemon.reset)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>restart ()](#apidoc.element.nodemon.restart)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>version (callback)](#apidoc.element.nodemon.version)
1.  object <span class="apidocSignatureSpan">nodemon.</span>cli
1.  object <span class="apidocSignatureSpan">nodemon.</span>config
1.  object <span class="apidocSignatureSpan">nodemon.</span>monitor
1.  object <span class="apidocSignatureSpan">nodemon.</span>rules
1.  object <span class="apidocSignatureSpan">nodemon.</span>utils

#### [module nodemon.cli](#apidoc.module.nodemon.cli)
1.  [function <span class="apidocSignatureSpan">nodemon.cli.</span>parse (argv)](#apidoc.element.nodemon.cli.parse)

#### [module nodemon.config](#apidoc.module.nodemon.config)
1.  boolean <span class="apidocSignatureSpan">nodemon.config.</span>required
1.  boolean <span class="apidocSignatureSpan">nodemon.config.</span>run
1.  [function <span class="apidocSignatureSpan">nodemon.config.</span>load (settings, ready)](#apidoc.element.nodemon.config.load)
1.  [function <span class="apidocSignatureSpan">nodemon.config.</span>reset ()](#apidoc.element.nodemon.config.reset)
1.  number <span class="apidocSignatureSpan">nodemon.config.</span>timeout
1.  object <span class="apidocSignatureSpan">nodemon.config.</span>dirs
1.  object <span class="apidocSignatureSpan">nodemon.config.</span>options
1.  object <span class="apidocSignatureSpan">nodemon.config.</span>system
1.  string <span class="apidocSignatureSpan">nodemon.config.</span>signal

#### [module nodemon.monitor](#apidoc.module.nodemon.monitor)
1.  [function <span class="apidocSignatureSpan">nodemon.monitor.</span>run (options)](#apidoc.element.nodemon.monitor.run)
1.  [function <span class="apidocSignatureSpan">nodemon.monitor.</span>watch ()](#apidoc.element.nodemon.monitor.watch)

#### [module nodemon.rules](#apidoc.module.nodemon.rules)
1.  [function <span class="apidocSignatureSpan">nodemon.rules.</span>add ()](#apidoc.element.nodemon.rules.add)
1.  [function <span class="apidocSignatureSpan">nodemon.rules.</span>load (filename, callback)](#apidoc.element.nodemon.rules.load)
1.  [function <span class="apidocSignatureSpan">nodemon.rules.</span>reset ()](#apidoc.element.nodemon.rules.reset)
1.  object <span class="apidocSignatureSpan">nodemon.</span>rules
1.  object <span class="apidocSignatureSpan">nodemon.rules.</span>ignore
1.  object <span class="apidocSignatureSpan">nodemon.rules.</span>watch

#### [module nodemon.utils](#apidoc.module.nodemon.utils)
1.  boolean <span class="apidocSignatureSpan">nodemon.utils.</span>isLinux
1.  boolean <span class="apidocSignatureSpan">nodemon.utils.</span>isMac
1.  boolean <span class="apidocSignatureSpan">nodemon.utils.</span>isRequired
1.  boolean <span class="apidocSignatureSpan">nodemon.utils.</span>isWindows
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>clone (obj)](#apidoc.element.nodemon.utils.clone)
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>merge (source, target, result)](#apidoc.element.nodemon.utils.merge)
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>quiet ()](#apidoc.element.nodemon.utils.quiet)
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>regexpToText (t)](#apidoc.element.nodemon.utils.regexpToText)
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>reset ()](#apidoc.element.nodemon.utils.reset)
1.  [function <span class="apidocSignatureSpan">nodemon.utils.</span>stringify (exec, args)](#apidoc.element.nodemon.utils.stringify)
1.  object <span class="apidocSignatureSpan">nodemon.utils.</span>bus
1.  object <span class="apidocSignatureSpan">nodemon.utils.</span>log
1.  object <span class="apidocSignatureSpan">nodemon.utils.</span>version
1.  string <span class="apidocSignatureSpan">nodemon.utils.</span>home

#### [module nodemon.version](#apidoc.module.nodemon.version)
1.  [function <span class="apidocSignatureSpan">nodemon.</span>version (callback)](#apidoc.element.nodemon.version.version)
1.  [function <span class="apidocSignatureSpan">nodemon.version.</span>pin ()](#apidoc.element.nodemon.version.pin)



# <a name="apidoc.module.nodemon"></a>[module nodemon](#apidoc.module.nodemon)

#### <a name="apidoc.element.nodemon.addListener"></a>[function <span class="apidocSignatureSpan">nodemon.</span>addListener (event, handler)](#apidoc.element.nodemon.addListener)
- description and source-code
```javascript
addListener = function (event, handler) {
  if (!eventHandlers[event]) { eventHandlers[event] = []; }
  eventHandlers[event].push(handler);
  bus.on(event, handler);
  return nodemon;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.emit"></a>[function <span class="apidocSignatureSpan">nodemon.</span>emit ()](#apidoc.element.nodemon.emit)
- description and source-code
```javascript
emit = function () {
  bus.emit.apply(bus, [].slice.call(arguments));
  return nodemon;
}
```
- example usage
```shell
...
  } else {
child = spawn(sh, args);
  }

  if (config.required) {
var emit = {
  stdout: function (data) {
    bus.emit('stdout', data);
  },
  stderr: function (data) {
    bus.emit('stderr', data);
  },
};

// now work out what to bind to...
...
```

#### <a name="apidoc.element.nodemon.on"></a>[function <span class="apidocSignatureSpan">nodemon.</span>on (event, handler)](#apidoc.element.nodemon.on)
- description and source-code
```javascript
on = function (event, handler) {
  if (!eventHandlers[event]) { eventHandlers[event] = []; }
  eventHandlers[event].push(handler);
  bus.on(event, handler);
  return nodemon;
}
```
- example usage
```shell
...

## Pipe output to somewhere else

'''js
nodemon({
  script: ...,
  stdout: false // important: this tells nodemon not to output to console
}).on('readable', function() { // the 'readable' event indicates that data is ready to pick up
  this.stdout.pipe(fs.createWriteStream('output.txt'));
  this.stderr.pipe(fs.createWriteStream('err.txt'));
});
'''

## Using io.js for nodemon
...
```

#### <a name="apidoc.element.nodemon.once"></a>[function <span class="apidocSignatureSpan">nodemon.</span>once (event, handler)](#apidoc.element.nodemon.once)
- description and source-code
```javascript
once = function (event, handler) {
  if (!eventHandlers[event]) { eventHandlers[event] = []; }
  eventHandlers[event].push(handler);
  bus.once(event, function () {
    debug('bus.once(%s)', event);
    eventHandlers[event].splice(eventHandlers[event].indexOf(handler), 1);
    handler.apply(this, arguments);
  });
  return nodemon;
}
```
- example usage
```shell
...

## Controlling shutdown of your script

nodemon sends a kill signal to your application when it sees a file update. If you need to clean up on shutdown inside your script
 you can capture the kill signal and handle it yourself.

The following example will listen once for the 'SIGUSR2' signal (used by nodemon to restart), run the clean up process and then
kill itself for nodemon to continue control:

    process.once('SIGUSR2', function () {
      gracefulShutdown(function () {
        process.kill(process.pid, 'SIGUSR2');
      });
    });

Note that the 'process.kill' is *only* called once your shutdown jobs are complete. Hat tip to [Benjie Gillam](http://www.benjiegillam
.com/2011/08/node-js-clean-restart-and-faster-development-with-nodemon/) for writing this technique up.
...
```

#### <a name="apidoc.element.nodemon.removeAllListeners"></a>[function <span class="apidocSignatureSpan">nodemon.</span>removeAllListeners (event)](#apidoc.element.nodemon.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function (event) {
  // unbind only the 'nodemon.on' event handlers
  Object.keys(eventHandlers).filter(function (e) {
    return event ? e === event : true;
  }).forEach(function (event) {
    eventHandlers[event].forEach(function (handler) {
      bus.removeListener(event, handler);
      eventHandlers[event].splice(eventHandlers[event].indexOf(handler), 1);
    });
  });

  return nodemon;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.reset"></a>[function <span class="apidocSignatureSpan">nodemon.</span>reset (done)](#apidoc.element.nodemon.reset)
- description and source-code
```javascript
reset = function (done) {
  bus.emit('reset', done);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.restart"></a>[function <span class="apidocSignatureSpan">nodemon.</span>restart ()](#apidoc.element.nodemon.restart)
- description and source-code
```javascript
restart = function () {
  utils.log.status('restarting child process');
  bus.emit('restart');
  return nodemon;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.version"></a>[function <span class="apidocSignatureSpan">nodemon.</span>version (callback)](#apidoc.element.nodemon.version)
- description and source-code
```javascript
function version(callback) {
  // first find the package.json as this will be our root
  var promise = findPackage(path.dirname(module.parent.filename))
    .then(function (dir) {
    // now try to load the package
    var v = require(path.resolve(dir, 'package.json')).version;

    if (v && v !== '0.0.0') {
      return v;
    }

    root = dir;

    // else we're in development, give the commit out
    // get the last commit and whether the working dir is dirty
    var promises = [
      branch().catch(function () { return 'master'; }),
      commit().catch(function () { return '<none>'; }),
      dirty().catch(function () { return 0; }),
    ];

    // use the cached result as the export
    return Promise.all(promises).then(function (res) {
      var branch = res[0];
      var commit = res[1];
      var dirtyCount = parseInt(res[2], 10);
      var curr = branch + ': ' + commit;
      if (dirtyCount !== 0) {
        curr += ' (' + dirtyCount + ' dirty files)';
      }

      return curr;
    });
  }).catch(function (error) {
    console.log(error.stack);
    throw error;
  });

  if (callback) {
    promise.then(function (res) {
      callback(null, res);
    }, callback);
  }

  return promise;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.cli"></a>[module nodemon.cli](#apidoc.module.nodemon.cli)

#### <a name="apidoc.element.nodemon.cli.parse"></a>[function <span class="apidocSignatureSpan">nodemon.cli.</span>parse (argv)](#apidoc.element.nodemon.cli.parse)
- description and source-code
```javascript
parse = function (argv) {
  if (typeof argv === 'string') {
    argv = stringToArgs(argv);
  }

  return parse(argv);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.config"></a>[module nodemon.config](#apidoc.module.nodemon.config)

#### <a name="apidoc.element.nodemon.config.load"></a>[function <span class="apidocSignatureSpan">nodemon.config.</span>load (settings, ready)](#apidoc.element.nodemon.config.load)
- description and source-code
```javascript
load = function (settings, ready) {
  reset();
  var config = this;
  load(settings, config.options, config, function (options) {
    config.options = options;

    if (options.watch.length === 0) {
      // this is to catch when the watch is left blank
      options.watch.push('*.*');
    }

    if (options['watch_interval']) { // jshint ignore:line
      options.watchInterval = options['watch_interval']; // jshint ignore:line
    }

    config.watchInterval = options.watchInterval || null;
    if (options['signal']) { // jshint ignore:line
      config.signal = options.signal;
    }

    var cmd = command(config.options);
    config.command = {
      raw: cmd,
      string: utils.stringify(cmd.executable, cmd.args),
    };

    // now run automatic checks on system adding to the config object
    options.monitor = rulesToMonitor(options.watch, options.ignore, config);

    var cwd = process.cwd();
    debug('config: dirs', config.dirs);
    if (config.dirs.length === 0) {
      config.dirs.unshift(cwd);
    }

    bus.emit('config:update', config);
    pinVersion().then(function () {
      ready(config);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.config.reset"></a>[function <span class="apidocSignatureSpan">nodemon.config.</span>reset ()](#apidoc.element.nodemon.config.reset)
- description and source-code
```javascript
function reset() {
  rules.reset();

  config.dirs = [];
  config.options = { ignore: [], watch: [] };
  config.lastStarted = 0;
  config.loaded = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.monitor"></a>[module nodemon.monitor](#apidoc.module.nodemon.monitor)

#### <a name="apidoc.element.nodemon.monitor.run"></a>[function <span class="apidocSignatureSpan">nodemon.monitor.</span>run (options)](#apidoc.element.nodemon.monitor.run)
- description and source-code
```javascript
function run(options) {
  var cmd = config.command.raw;

  var runCmd = !options.runOnChangeOnly || config.lastStarted !== 0;
  if (runCmd) {
    utils.log.status('starting '' + config.command.string + ''');
  }

<span class="apidocCodeCommentSpan">  /*jshint validthis:true*/
</span>  restart = run.bind(this, options);
  run.restart = restart;

  config.lastStarted = Date.now();

  var stdio = ['pipe', 'pipe', 'pipe'];

  if (config.options.stdout) {
    stdio = ['pipe',
             process.stdout,
             process.stderr,];
  }

  var sh = 'sh';
  var shFlag = '-c';

  if (utils.isWindows) {
    sh = 'cmd';
    shFlag = '/c';
  }

  var executable = cmd.executable;

  // special logic for windows, as spaces in the paths need the path fragment
  // quoted, so it reads: c:\"Program Files"\nodejs\node.exe
  if (utils.isWindows && executable.indexOf(' ') !== -1) {
    var re = /\\((\w+\s+)+\w+)(?=([\\\.]))(?=([^"]*"[^"]*")*[^"]*$)/g;
    executable = executable.replace(re, '\\"$1"');
  }

  var args = runCmd ? utils.stringify(executable, cmd.args) : ':';
  var spawnArgs = [sh, [shFlag, args]];
  debug('spawning', args);

  if (utils.version.major === 0 && utils.version.minor < 8) {
    // use the old spawn args :-\
  } else {
    spawnArgs.push({
      env: utils.merge(options.execOptions.env, process.env),
      stdio: stdio,
    });
  }

  child = spawn.apply(null, spawnArgs);

  if (config.required) {
    var emit = {
      stdout: function (data) {
        bus.emit('stdout', data);
      },
      stderr: function (data) {
        bus.emit('stderr', data);
      },
    };

    // now work out what to bind to...
    if (config.options.stdout) {
      child.on('stdout', emit.stdout).on('stderr', emit.stderr);
    } else {
      child.stdout.on('data', emit.stdout);
      child.stderr.on('data', emit.stderr);

      bus.stdout = child.stdout;
      bus.stderr = child.stderr;
    }
  }

  bus.emit('start');

  utils.log.detail('child pid: ' + child.pid);

  child.on('error', function (error) {
    bus.emit('error', error);
    if (error.code === 'ENOENT') {
      utils.log.error('unable to run executable: "' + cmd.executable + '"');
      process.exit(1);
    } else {
      utils.log.error('failed to start child process: ' + error.code);
      throw error;
    }
  });

  child.on('exit', function (code, signal) {
    if (code === 127) {
      utils.log.error('failed to start process, "' + cmd.executable +
        '" exec not found');
      bus.emit('error', code);
      process.exit();
    }

    if (code === 2) {
      // something wrong with parsed command
      utils.log.error('failed to start process, possible issue with exec ' +
        'arguments');
      bus.emit('error', code);
      process.exit();
    }

    // In case we killed the app ourselves, set the signal thusly
    if (killedAfterChange) {
      killedAfterChange = false;
      signal = config.signal;
    }
    // this is nasty, but it gives it windows support
    if (utils.isWindows && signal === 'SIGTERM') {
      signal = config.signal;
    }

    if (signal === config.signal || code === 0) {
      // this was a clean exit, so emit exit, rather than crash
      debug('bus.emit(exit) via ' + config.signal);
      bus.emit('exit');

      // exit the monitor, but do it gracefully
      if (signal === config.signal) {
        return restart();
      } else if (code === 0) { // clean exit - wait until file change to restart
        if (runCmd) {
          utils.log.status('clean exit - waiting for changes before restart');
        }
        child = null;
      }
    } else {
      bus.emit('crash');
      if (options.exitcrash) {
        utils.log.fail('app crashed');
        if (!config.required) {
          process.exit(0);
        }
      } else {
        utils.log.fail('app crashed - waiting for file changes before' +
        ' starting...');
        child = null;
      }
    }

    if (config.options.restartable) {
      // stdin needs to kick in again to be able to listen to the
      // restart command
      process.stdin.resume();
    }
  });

  run.kill = function (noRestart, callback) ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.monitor.watch"></a>[function <span class="apidocSignatureSpan">nodemon.monitor.</span>watch ()](#apidoc.element.nodemon.monitor.watch)
- description and source-code
```javascript
function watch() {
  if (watchers.length) {
    debug('early exit on watch, still watching (%s)', watchers.length);
    return;
  }

  var dirs = [].slice.call(config.dirs);

  debugRoot('start watch on: %s', dirs.join(', '));
  debugRoot('ignore dirs regex(%s)', config.options.ignore.re);

  var promises = [];
  var watchedFiles = [];

  dirs.forEach(function (dir) {
    var promise = new Promise(function (resolve) {
      var ignored = config.options.ignore.re;
      var dotFilePattern = /[\/\\]\./;

      // don't ignore dotfiles if explicitly watched.
      if (!dir.match(dotFilePattern)) {
        ignored = [ignored, dotFilePattern];
      }

      var watcher = chokidar.watch(dir, {
        ignored: ignored,
        persistent: true,
        usePolling: config.options.legacyWatch || false,
        interval: config.options.pollingInterval,
      });

      watcher.ready = false;

      var total = 0;

      watcher.on('change', filterAndRestart);
      watcher.on('add', function (file) {
        if (watcher.ready) {
          return filterAndRestart(file);
        }

        watchedFiles.push(file);
        total++;
        debug('watching dir: %s', file);
      });
      watcher.on('ready', function () {
        watcher.ready = true;
        resolve(total);
        debugRoot('watch is complete');
      });

      watcher.on('error', function (error) {
        if (error.code === 'EINVAL') {
          utils.log.error('Internal watch failed. Likely cause: too many ' +
            'files being watched (perhaps from the root of a drive?\n' +
            'See https://github.com/paulmillr/chokidar/issues/229 for details');
        } else {
          utils.log.error('Internal watch failed: ' + error.message);
          process.exit(1);
        }
      });

      watchers.push(watcher);
    });
    promises.push(promise);
  });

  return Promise.all(promises).then(function (res) {
    var total = res.reduce(function (acc, curr) {
      acc += curr;
      return acc;
    }, 0);

    var count = total.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
    utils.log.detail('watching ' + count + ' files');
    return watchedFiles;
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.rules"></a>[module nodemon.rules](#apidoc.module.nodemon.rules)

#### <a name="apidoc.element.nodemon.rules.add"></a>[function <span class="apidocSignatureSpan">nodemon.rules.</span>add ()](#apidoc.element.nodemon.rules.add)
- description and source-code
```javascript
add = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.rules.load"></a>[function <span class="apidocSignatureSpan">nodemon.rules.</span>load (filename, callback)](#apidoc.element.nodemon.rules.load)
- description and source-code
```javascript
function load(filename, callback) {
  parse(filename, function (err, result) {
    if (err) {
      // we should have bombed already, but
      utils.log.error(err);
      callback(err);
    }

    if (result.raw) {
      result.raw.forEach(add.bind(null, rules, 'ignore'));
    } else {
      result.ignore.forEach(add.bind(null, rules, 'ignore'));
      result.watch.forEach(add.bind(null, rules, 'watch'));
    }

    callback(null, rules);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.rules.reset"></a>[function <span class="apidocSignatureSpan">nodemon.rules.</span>reset ()](#apidoc.element.nodemon.rules.reset)
- description and source-code
```javascript
reset = function () { // just used for testing
  rules.ignore.length = rules.watch.length = 0;
  delete rules.ignore.re;
  delete rules.watch.re;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.utils"></a>[module nodemon.utils](#apidoc.module.nodemon.utils)

#### <a name="apidoc.element.nodemon.utils.clone"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>clone (obj)](#apidoc.element.nodemon.utils.clone)
- description and source-code
```javascript
function clone(obj) {
  // Handle the 3 simple types, and null or undefined
  if (null === obj || 'object' !== typeof obj) {
    return obj;
  }

  var copy;

  // Handle Date
  if (obj instanceof Date) {
    copy = new Date();
    copy.setTime(obj.getTime());
    return copy;
  }

  // Handle Array
  if (obj instanceof Array) {
    copy = [];
    for (var i = 0, len = obj.length; i < len; i++) {
      copy[i] = clone(obj[i]);
    }
    return copy;
  }

  // Handle Object
  if (obj instanceof Object) {
    copy = {};
    for (var attr in obj) {
      if (obj.hasOwnProperty && obj.hasOwnProperty(attr)) {
        copy[attr] = clone(obj[attr]);
      }
    }
    return copy;
  }

  throw new Error('Unable to copy obj! Its type isn\'t supported.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.utils.merge"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>merge (source, target, result)](#apidoc.element.nodemon.utils.merge)
- description and source-code
```javascript
function merge(source, target, result) {
  if (result === undefined) {
    result = clone(source);
  }

  // merge missing values from the target to the source
  Object.getOwnPropertyNames(target).forEach(function (key) {
    if (source[key] === undefined) {
      result[key] = target[key];
    }
  });

  Object.getOwnPropertyNames(source).forEach(function (key) {
    var value = source[key];

    if (target[key] && typesMatch(value, target[key])) {
      // merge empty values
      if (value === '') {
        result[key] = target[key];
      }

      if (Array.isArray(value)) {
        if (value.length === 0 && target[key].length) {
          result[key] = target[key].slice(0);
        }
      } else if (typeof value === 'object') {
        result[key] = merge(value, target[key]);
      }
    }
  });

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.utils.quiet"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>quiet ()](#apidoc.element.nodemon.utils.quiet)
- description and source-code
```javascript
quiet = function () {
  // nukes the logging
  if (!this.debug) {
    for (var method in utils.log) {
      if (typeof utils.log[method] === 'function') {
        utils.log[method] = noop;
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.utils.regexpToText"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>regexpToText (t)](#apidoc.element.nodemon.utils.regexpToText)
- description and source-code
```javascript
regexpToText = function (t) {
  return t.replace(/\.\*\\./g, '*.')
          .replace(/\\{2}/g, '^^')
          .replace(/\\/g, '')
          .replace(/\^\^/g, '\\');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.utils.reset"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>reset ()](#apidoc.element.nodemon.utils.reset)
- description and source-code
```javascript
reset = function () {
  if (!this.debug) {
    for (var method in utils.log) {
      if (typeof utils.log[method] === 'function') {
        delete utils.log[method];
      }
    }
  }
  this.debug = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.utils.stringify"></a>[function <span class="apidocSignatureSpan">nodemon.utils.</span>stringify (exec, args)](#apidoc.element.nodemon.utils.stringify)
- description and source-code
```javascript
stringify = function (exec, args) {
  // serializes an executable string and array of arguments into a string
  args = args || [];

  return [exec].concat(args.map(function (arg) {
    // if an argument contains a space, we want to show it with quotes around
    // it to indicate that it is a single argument
    if (arg.indexOf(' ') === -1) {
      return arg;
    } else {
      // this should correctly escape nested quotes
      return JSON.stringify(arg);
    }
  })).join(' ').trim();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nodemon.version"></a>[module nodemon.version](#apidoc.module.nodemon.version)

#### <a name="apidoc.element.nodemon.version.version"></a>[function <span class="apidocSignatureSpan">nodemon.</span>version (callback)](#apidoc.element.nodemon.version.version)
- description and source-code
```javascript
function version(callback) {
  // first find the package.json as this will be our root
  var promise = findPackage(path.dirname(module.parent.filename))
    .then(function (dir) {
    // now try to load the package
    var v = require(path.resolve(dir, 'package.json')).version;

    if (v && v !== '0.0.0') {
      return v;
    }

    root = dir;

    // else we're in development, give the commit out
    // get the last commit and whether the working dir is dirty
    var promises = [
      branch().catch(function () { return 'master'; }),
      commit().catch(function () { return '<none>'; }),
      dirty().catch(function () { return 0; }),
    ];

    // use the cached result as the export
    return Promise.all(promises).then(function (res) {
      var branch = res[0];
      var commit = res[1];
      var dirtyCount = parseInt(res[2], 10);
      var curr = branch + ': ' + commit;
      if (dirtyCount !== 0) {
        curr += ' (' + dirtyCount + ' dirty files)';
      }

      return curr;
    });
  }).catch(function (error) {
    console.log(error.stack);
    throw error;
  });

  if (callback) {
    promise.then(function (res) {
      callback(null, res);
    }, callback);
  }

  return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nodemon.version.pin"></a>[function <span class="apidocSignatureSpan">nodemon.version.</span>pin ()](#apidoc.element.nodemon.version.pin)
- description and source-code
```javascript
function pin() {
  return version().then(function (v) {
    version.pinned = v;
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
