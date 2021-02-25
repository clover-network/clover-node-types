clover-node-types
Usage
This repo contains Typescript bindings for custom clover-node modules.

In order to use the standard API against Edgeware you must initialize the API's options object as follows:

import { cloverTypes } from '@clover/node-types';

const options: ApiOptions = {
  provider : new WsProvider('wss://api.jisand.com'),
  ...cloverTypes,
};

const api = new ApiRx(options);