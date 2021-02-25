# clover-node-types
## Usage
This repo contains Javascript bindings for clover-node-type modules.

In order to use the standard API against clover you must initialize the API's types object as follows:
```
npm install @clover-network/node-tpye

example:
const cloverTypes = require('@clover-network/node-tpye')
const { ApiPromise, WsProvider } = require('@polkadot/api');

async function nonce(){
    const wsProvider = new WsProvider ('wss://api.jisand.com');
    const api = await ApiPromise.create({ 
        provider: wsProvider,
        types: cloverTypes
     });
     var nonce = await api.rpc.system.accountNextIndex('5Gf3M6b4hy6D7QdGwaKGv1AteiuLzpPw4XVo9FmuHZbDG6qn');
     console.log(nonce)
}
nonce()