# flogger - An opinionated friendly logging utility

Flogger is a library to be used in the development of javascript applications and utilities. It is intended to be lightweight requiring only 3 external libraries which can be obtained easily. These libraries are:

Library 		| Reason
:-- 			| :--
WinJS 			| Namespaces, Classes and event mixins
Chalk			| Coloring on console
Lodash			| Reliable reduce, map, etc

## usage

The most basic usage is to require flogger and then use it with a default or specific log level

```js
var flog = require('flogger')('myapp-name');		// Instantiate flogger with your app name
flog("Hello World 1"); 								// Default loglevel (info)
flog.warn("Hello World 2"); 						// Specific floglevel
flog(flog.levels.DEBUG, "Hello World 3");			// Specific floglevel
flog("Custom", "Hello World 4");					// Custom floglevel (string)
```

The above would print out

```
28/11/16-12:23:16 | myapp-name | info | "Hello World 1"
28/11/16-12:23:22 | myapp-name | warn | "Hello World 2"
28/11/16-12:23:48 | myapp-name | debug | "Hello World 3"
28/11/16-12:24:11 | myapp-name | Custom | "Hello World 4"
```

## (f)log levels

The default floglevels are

* info
* warn
* error
* debug
* silly *(Inspired by [winston](https://github.com/winstonjs/winston))*

### references

* [How to Get Node.js Logging Right](https://blog.risingstack.com/node-js-logging-tutorial/)
