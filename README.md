<a href="https://cartesi.io/">
  <img src="https://avatars.githubusercontent.com/u/37696266?s=200&v=4" alt="Cartesi logo" width="80" height="80">
</a>

# Cartesi

Cartesi is an open-source framework for building application-specific rollups on Ethereum and other EVM-compatible chains.
Applications run off-chain as ordinary Linux programs, with the languages, libraries, and tools available for RISC-V Linux.

[Build your first application](https://docs.cartesi.io/get-started/quickstart/) or [explore the documentation](https://docs.cartesi.io/).

## Core technology

**[Cartesi Machine](https://github.com/cartesi/machine-emulator)** is a deterministic RISC-V emulator that runs Linux.
Anyone can reproduce a computation and check its result.
An experimental [ZK integration](https://github.com/cartesi/machine-emulator/tree/main/risc0) proves Machine state transitions, with [on-chain verification](https://github.com/cartesi/machine-emulator/tree/main/risc0/solidity).

**Cartesi Rollups** combines the Machine, [smart contracts](https://github.com/cartesi/rollups-contracts), and the [Cartesi Rollups Node](https://github.com/cartesi/rollups-node) into an SDK for application-specific rollups.
Each application is its own rollup, with its own Machine and state.
The node reads inputs recorded on the base chain, executes the application off-chain, and submits claims about the results for on-chain settlement.
Deployment and node operation are permissionless: anyone can deploy an application and run a node.

**[Dave](https://github.com/cartesi/dave)** is Cartesi's permissionless fraud-proof system.
Applications using it allow anyone to [validate execution](https://github.com/cartesi/dave/tree/main/cartesi-rollups/node) and dispute incorrect results through an [on-chain Machine verifier](https://github.com/cartesi/machine-solidity-step).

## Explore and contribute

Cartesi is developed as an open-source public good, with infrastructure available for anyone to use, inspect, and contribute to.

- [CLI](https://github.com/cartesi/cli): create, build, and run an application.
- [Sequencer](https://github.com/cartesi/sequencer): add optional low-latency soft confirmations and batch inputs for submission to the base chain.
- [Engineering map](ENGINEERING_MAP.md): find repositories, component status, and dependencies.
- [Developer community](https://discord.gg/cartesi): ask questions and discuss what you are building.

Contributions are welcome through each repository's contribution guidelines.
Licenses vary by component: the Cartesi Machine uses LGPL-3.0; the on-chain Machine verifier, Dave, Rollups Contracts, Rollups Node, Sequencer, and the CLI use Apache-2.0.
See each repository for its full license terms and dependency notices.
