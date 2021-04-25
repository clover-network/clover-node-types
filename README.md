[![npm version](https://img.shields.io/npm/v/@clover-network/node-types.svg)](https://www.npmjs.com/package/eslint)
[![MIT][license-badge]][license]

# clover-node-types
## Usage
This repo contains Javascript bindings for clover-node-type modules.

In order to use the standard API against clover you must initialize the API's types object as follows:

```bash
npm install @clover-network/node-types
```

example:
```javascript
const cloverTypes = require('@clover-network/node-types');
const { ApiPromise, WsProvider } = require('@polkadot/api');

async function connectToClover(){
    const wsProvider = new WsProvider ('wss://api.clover.finance');
    const api = await ApiPromise.create({ 
        provider: wsProvider,
        types: cloverTypes
     });
     var nonce = await api.rpc.system.accountNextIndex('5Gf3M6b4hy6D7QdGwaKGv1AteiuLzpPw4XVo9FmuHZbDG6qn');
     console.log(nonce);
}
connectToClover();
```

[license-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license]: https://github.com/clover-network/clover-node-types/blob/master/LICENSE
