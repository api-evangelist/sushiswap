# SushiSwap GraphQL API

## Description

SushiSwap exposes its on-chain data through The Graph Protocol subgraphs. The primary subgraph covers the SushiSwap V2 AMM (Automated Market Maker), providing queryable access to factory statistics, token data, liquidity pairs, swaps, mints, burns, liquidity positions, and time-series analytics. A separate xSushi subgraph tracks the SushiBar staking contract (xSUSHI).

These subgraphs are deployed on the decentralized Graph Network and on The Graph's hosted service across multiple EVM-compatible chains including Ethereum, Arbitrum, Polygon, Optimism, Avalanche, BSC, and others.

## Endpoints

### V2 AMM Subgraph (Ethereum Mainnet)
- **Hosted Service:** `https://api.thegraph.com/subgraphs/name/sushi-v2/sushiswap-ethereum`
- **Decentralized Network:** `https://gateway-arbitrum.network.thegraph.com/api/[api-key]/subgraphs/id/...`

### xSushi (SushiBar) Subgraph
- **Hosted Service:** `https://api.thegraph.com/subgraphs/name/sushiswap/xsushi`

### Query Method
All endpoints accept HTTP POST requests with a JSON body:
```json
{
  "query": "{ pairs(first: 10, orderBy: volumeUSD, orderDirection: desc) { id token0 { symbol } token1 { symbol } volumeUSD } }"
}
```

## Documentation

- Developer Docs: https://docs.sushi.com
- Subgraphs GitHub: https://github.com/sushiswap/subgraphs
- The Graph Explorer: https://thegraph.com/explorer?search=sushiswap

## Key Entity Types

### V2 AMM
- `UniswapFactory` - Global DEX factory statistics (volume, liquidity, transaction counts)
- `Token` - ERC-20 token metadata and aggregate trading statistics
- `Pair` - Liquidity pool pairs with reserves, prices, and volume
- `User` - Liquidity provider accounts
- `LiquidityPosition` - User LP token balances per pair
- `LiquidityPositionSnapshot` - Historical snapshots of liquidity positions
- `Transaction` - On-chain transactions containing swaps, mints, and burns
- `Mint` - Liquidity addition events
- `Burn` - Liquidity removal events
- `Swap` - Token swap events
- `Bundle` - ETH/USD price oracle reference
- `UniswapDayData` - Daily aggregate protocol statistics
- `PairHourData` - Hourly per-pair volume and reserve data
- `PairDayData` - Daily per-pair volume and reserve data
- `TokenDayData` - Daily per-token volume and price data

### xSushi (SushiBar)
- `XSushi` - Global SushiBar statistics (staking ratios, APR, supply)
- `Transaction` - Stake/unstake transactions (MINT/BURN/TRANSFER)
- `User` - xSUSHI holder balances and history
- `FeeSender` - Contracts sending trading fees to SushiBar
- `Fee` - Individual fee events
- `HourSnapshot` - Hourly SushiBar snapshots
- `DaySnapshot` - Daily SushiBar snapshots
- `WeekSnapshot` - Weekly SushiBar snapshots

## Example Queries

### Top Pairs by Volume
```graphql
{
  pairs(first: 5, orderBy: volumeUSD, orderDirection: desc) {
    id
    token0 { symbol name }
    token1 { symbol name }
    volumeUSD
    reserveUSD
    txCount
  }
}
```

### Recent Swaps
```graphql
{
  swaps(first: 10, orderBy: timestamp, orderDirection: desc) {
    id
    pair { token0 { symbol } token1 { symbol } }
    amount0In
    amount1Out
    amountUSD
    timestamp
  }
}
```

### Token Day Data
```graphql
{
  tokenDayDatas(first: 7, orderBy: date, orderDirection: desc,
    where: { token: "0x6b3595068778dd592e39a122f4f5a5cf09c90fe2" }) {
    date
    dailyVolumeUSD
    totalLiquidityUSD
    priceUSD
  }
}
```

## Schema Source

The official SDL schema is available at:
- V2: https://github.com/sushiswap/subgraphs/blob/master/subgraphs/v2/schema.graphql
- xSushi: https://github.com/sushiswap/subgraphs/blob/master/subgraphs/xsushi/schema.graphql
