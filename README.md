# Subgraph-template

<div align=center style="background:lightgrey">
<img src="./logo.png" width=100" height="100" />
</div>
<div align=center>
<img src="https://img.shields.io/badge/nodejs^14-blue"/>
<img src="https://img.shields.io/badge/graph^0.30.0-blue"/>
<img src="https://img.shields.io/badge/subgraph^0.0.5-blue"/>
</div>

English | [简体中文](./README_zh.md)


TheGraph exposes a GraphQL endpoint to query the events and entities within the xxx chain and xxx ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.


## Subgraphs
01. **[Demo](https://thegraph.com/hosted-service/subgraph/lingcoder/xxx)**: Tracks data for Demo.


## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.
