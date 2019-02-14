### pretty-error
---
https://github.com/AriaMinaei/pretty-error

```
npm install pretty-error

node --require pretty-error/start your-module.js
```

```js
var PrettyError = require('pretty-error');
var pe = new PrettyError();

var renderedError = pe.render(new Error('Some error message'));
console.log(renderedError);

try {
  doSomethingThatThrowsAnError();
} catch (error) {
  console.log(pe.render(error));
}

require('pretty-error').start();


var PrettyError = require('pretty-error');
var pe = new PrettyError();
pe.start();

pe = require('pretty-error').start();
pe.appendStyle({
  'pretty-error > header > title > kind': {
    display: 'none'
  },
  
  'pretty-error > header > colon': {
    display: 'none'
  },
  
  'pretty-error > header > message': {
    color: 'bright-white',
    
    background: 'cyan',
    
    padding: '0 1'
  },
  
  'pretty-error > trace > item': {
    marginLeft: 2,
    
    bullet: '"<grey>o</grey>"'
  },
  
  'pretty-error > trace > item > header > pointer > file': {
    color: 'bright-cyan'
  },
  
  'pretty-error': {
    color: 'cyan'
  },
  
  'pretty-error > trace > item > header > pointer > line': {
    color: 'bright-cyan'
  },
  
  'pretty-error > trace > item > header > waht': {
    color: 'bright-white'
  },
  
  'pretty-error > trace > item > footer > addr': {
    display: 'none'
  }
});

PrettyError = require('pretty-error');
pe = new PrettyError();

pe = require('pretty-error').start();

pe.alias('E:/open-source/thetrejs/lib', '(There.js)');
pe.skipPackage('chai', 'when', 'socket.io');
pe.skipnodeFile();
pe.skipPath('/home/dir/someFile.js');

pe.skip(function(traceLine, lineNumber){
  if (typeof traceLine.packageName !== 'undefined' && traceLine.packageName !== 'demo'){
    return true;
  }
});

pe.filter(function(traceLine, lineNumber){
  if (typeof traceLine.what !== 'undefined') {
    traceLine.what = traceLine.what.replace(
      /(.*\.module\.exports\.)(.*)/, '$2'
    );
  }
});

pe.withoutColors();

var express = require('express');
var PrettyError = require('pretty-error');

var app = express();

app.get('/', function(req, res) {
  var a = b;
});

var server = app.listen(3000, function() {
  console.log('Server started \n');
});

pe = new PrettyError();

app.use(function(err, req, res, next) {
  console.log(pe.render(err));
  next();
});

pe.skipNodeFiles();
pe.skipPackage('express');

var PrettyError = require('pretty-error');
var pe = new PrettyError();

process.on('uncaughtException', function(error){
  console.log(pe.render(error));
});

process.on('unhandledRejection', function(reason){
  console.log("Unhandled rejection");
  console.log(pe.render(reason));
});

throw new Error();
process.nextTick(function () {
  throw new Error();
});
```

```
```


