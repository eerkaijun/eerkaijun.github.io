## Open Source Projects

I'm a firm believer of open source collaborations. If there are more open source projects, the world will be a better place.

### Private Accounts

[Private Accounts](https://github.com/eerkaijun/private-accounts) is an open source module that allows users to create private accounts on any EVM chains. It allows users to transact privately on a public blockchain without needing any underlying protocol changes. I've written a detailed ETH research post on the architecture and design [here](https://ethresear.ch/t/private-accounts-module-on-ethereum-without-underlying-protocol-changes/16297).


### 0xFable

[0xFable](https://github.com/0xFableOrg/0xFable) is a fully on-chain trading card game. I mostly contributed to the ZK circuits that are used to manage the private states of the game, such as the players' hands and card drawing. The circuits are written in Circom and we use Groth16 for the proving system.

The motivation for putting the entire game logic on-chain is to make the game fully extensible and composable. Developers can easily write plugins to the game without needing to worry about platform risk or vendor lock-in. Building an on-chain game is also a great way to push the boundaries of what is possible on blockchains.


### Roll-op

[Roll-op](https://github.com/0xFableOrg/roll-op) is a command line tool that allows developers to easily spin up a rollup using [OpStack](https://docs.optimism.io/stack/getting-started). Developers just need to specify desired parameters in a config file. It is similar to many rollup-as-a-service (RaaS) providers, but we fully open source it.