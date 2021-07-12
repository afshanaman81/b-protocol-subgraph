# B.Protocol Subgraph

An example to help me get started with The Graph. For more information see the docs on https://thegraph.com/docs/.

# Idea
Project inspired by the bounty from The Graph https://www.notion.so/5d4be33daa13434691f4e23f55d56fd9?v=89605364ad434f61a5d6fa0f82cedb37&p=a6330d35c42e487fa6fcada1fac8fa16


# About this Project
- github: https://github.com/afshanaman81/b-protocol-subgraph

- Deployed to https://thegraph.com/explorer/subgraph/afshanaman81/b-protocol-subgraph

- Subgraph endpoints:
  - Queries (HTTP):     https://api.thegraph.com/subgraphs/name/afshanaman81/b-protocol-subgraph
  - Subscriptions (WS): wss://api.thegraph.com/subgraphs/name/afshanaman81/b-protocol-subgraph


How Tos:
- followed the docs https://thegraph.academy/developers/defining-a-subgraph/ 
  - to create a dummy project
  - 
- cloned the B Protocol repo (https://github.com/backstop-protocol/BPRO)
- found their smart contract address by searching gogole using `b protocol smart contract address` query. That gave a result for the Etherscan. 
- Also found the starting block (deploy date) using etherscan
- generated the smart contract abis of the BPRO by running `npm i && truffle compile` in that repo's root (in the folder `build/contracts`)
- then copied them over to the `abis` folder in this repo
- updated the `subgraph.yaml` file
  - set:
  - dataSources.name: BPRO
  - dataSources.source.address: ADDRESS FROM THE ETHERSCAN
  - dataSources.source.abi: BPRO
  - dataSources.mapping.entities: Checkpoint 
    - (its the `struct` in the contract. Do I need to provide all the variables of basic types, e.g the `name` and the `minter` variables?)
  - dataSources.mapping.abis.name and file
  - Added the events from the BPRO.sol to the dataSources.mapping.eventHandlers
- TODO: need to add event handlers to the `src/mapping.ts`



# Tutorials
- https://github.com/graphprotocol/graph-node/blob/master/docs/getting-started.md

- https://medium.com/protofire-blog/the-graph-building-a-subgraph-for-humanitydao-part-1-9b3f1c3feb8a

- https://medium.com/2key/thegraph-how-to-build-our-subgraph-on-thegraph-hosted-solution-2360938c0323
  
- https://docs.fantom.foundation/tutorials/deploying-subgraph-with-the-graph

- https://dev.to/dabit3/building-graphql-apis-on-ethereum-4poa

- https://www.youtube.com/watch?v=coa0Vw47qNc

# Actual Subgraph Repos
- https://github.com/Synthetixio/synthetix-subgraph

- https://github.com/Uniswap/uniswap-v3-subgraph

- https://github.com/graphprotocol/compound-V2-subgraph




# About B.Protocol

Website: https://www.bprotocol.org/

Code: https://github.com/backstop-protocol/BPRO

Smart Contract: https://etherscan.io/address/0xbbbbbbb5aa847a2003fbc6b5c16df0bd1e725f61

https://medium.com/b-protocol/b-protocol-is-live-8d0971b77ef9

