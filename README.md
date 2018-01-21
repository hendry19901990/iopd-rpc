iopd-rpc.js
===============
 
A client library to connect to IoP Core RPC in JavaScript.

## Get Started

iopd-rpc.js runs on [node](http://nodejs.org/), and can be installed via [npm](https://npmjs.org/):

```bash
npm install iopd-rpc
```

## Examples

```javascript

  var iopcore = require('iopcore-lib');
  var RpcClient = require('iopd-rpc');

  var config = {
    protocol: 'http',
    user: 'user',
    pass: 'pass',
    host: '127.0.0.1',
    port: '18332',
  };

  var rpc = new RpcClient(config);

  rpc.getPeerInfo(function(err, res) {
	if (err)
	  console.log(err);
	else
	  console.log(res.result);
  });

  rpc.getBlockchainInfo(function(err, res) {
	if (err)
	  console.log(err);
	else
	  console.log(res.result);
  });

  rpc.listAccounts(1, function(err, res) {
	if (err)
	  console.log(err);
	else
	  console.log(res.result);
  });
```

## License

Code released under [the MIT license](https://github.com/hendry19901990/iopcore-lib/blob/master/LICENSE).

Copyright 2017 IoP, Inc. Iopcore is a trademark maintained by IoPCommunity, Inc.
