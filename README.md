# SinceredogeSwap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Binance Smart Chain and SinceredogeSwap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.

## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/blocks)**: Tracks all blocks on Binance Smart Chain.

2. **[Exchange](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/blocks)**: Tracks all SinceredogeSwap Exchange data with price, volume, liquidity, ...

3. **[Farm Auctions](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/farm-auctions)**: Tracks all SinceredogeSwap Farm Auctions with auctions and bids.

4. **[Lottery](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/lottery)**: Tracks all SinceredogeSwap Lottery with rounds, draws and tickets.

5. **[NFT Market (v1)](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/nft-market)**: Tracks all SinceredogeSwap NFT Market for ERC-721.

6. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/pairs)**: Tracks all SinceredogeSwap Pairs and Tokens.

7. **[Pancake Squad](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/pancake-squad)**: Tracks all Sinceredoge Squad metrics with Owners, Tokens (including metadata), and Transactions.

8. **[Prediction (v1)](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/prediction)**: Tracks all SinceredogeSwap Prediction (v1) with market, rounds, and bets.

9. **[Prediction (v2)](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/prediction-v2)**: Tracks all SinceredogeSwap Prediction (v2) with market, rounds, and bets.

10. **[Profile](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/profile)**: Tracks all SinceredogeSwap Profile with teams, users, points and campaigns.

11. **[SmartChef](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/smartchef)**: Tracks all SinceredogeSwap SmartChef (a.k.a. Syrup Pools) with tokens and rewards.

12. **[Timelock](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/timelock)**: Tracks all SinceredogeSwap Timelock queued, executed, and cancelled transactions.

13. **[Trading Competition (v1)](https://thegraph.com/legacy-explorer/subgraph/sinceredogeswap/trading-competition-v1)**: Tracks all metrics for the Easter Battle (April 07—14, 2021).

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

4. Run `graph auth --product hosted-service <ACCESS_TOKEN>`

5. Deploy via `yarn deploy`.

## v1

To access subgraphs related to PancakeSwap v1 ecosystem ([article](https://pancakeswap.medium.com/the-great-migration-vote-4093cb3edf23)), use [`v1`](https://github.com/pancakeswap/pancake-subgraph/tree/v1) branch.
