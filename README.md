# SushiSwap (sushiswap)

SushiSwap is a multi-chain decentralized exchange (DEX) protocol offering REST APIs for accessing liquidity pools, token prices, swap quotes, trading routes, and exchange analytics across 30+ blockchain networks. The Sushi API suite enables developers to integrate token pricing, generate swap quotes, and execute on-chain transactions programmatically via a unified base URL with per-chain routing.

**APIs.json:** [https://www.sushi.com](https://www.sushi.com)

## Tags

- DeFi
- Decentralized Exchange
- DEX
- Cryptocurrency
- Web3
- Blockchain
- Multi-Chain
- Liquidity
- Swap
- Token Pricing

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### Sushi Price API

Returns token prices in USD across multiple chains. Provides both aggregate price maps for all tokens on a given chain and individual token price lookups by contract address.

- **Human URL:** [https://docs.sushi.com/api/examples/swap](https://docs.sushi.com/api/examples/swap)
- **Base URL:** `https://api.sushi.com/price/v1`

#### Tags

- Token Pricing
- USD
- Multi-Chain

#### Properties

- [Documentation](https://docs.sushi.com/api/examples/swap)
- [OpenAPI](https://docs.sushi.com/blade-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Graph Q L](graphql/sushiswap-graphql.md)

### Sushi Quote API

Generates swap quotes for a given token pair and amount on a specified chain. Returns estimated output amounts, price impact, and routing information without committing to an on-chain transaction.

- **Human URL:** [https://docs.sushi.com/api/examples/quote](https://docs.sushi.com/api/examples/quote)
- **Base URL:** `https://api.sushi.com/quote/v7`

#### Tags

- Quote
- Swap
- Price Impact
- Routing

#### Properties

- [Documentation](https://docs.sushi.com/api/examples/quote)
- [OpenAPI](https://docs.sushi.com/blade-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Sushi Swap API

Generates complete swap transaction call data ready for on-chain execution. Integrates liquidity from Sushi V2/V3, Uniswap V2/V3, Curve, Algebra, Quickswap, Pancake, Camelot, and other sources via the Route Processor 4 (RP4) aggregator across 30+ EVM networks and Stellar.

- **Human URL:** [https://docs.sushi.com/api/examples/swap](https://docs.sushi.com/api/examples/swap)
- **Base URL:** `https://api.sushi.com/swap/v7`

#### Tags

- Swap
- DEX Aggregator
- Liquidity
- Multi-Chain
- Transaction

#### Properties

- [Documentation](https://docs.sushi.com/api/examples/swap)
- [OpenAPI](https://docs.sushi.com/blade-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Portal](https://sushi.com/portal)

## Common Properties

- [Portal](https://sushi.com/portal)
- [Documentation](https://docs.sushi.com)
- [OpenAPI](https://docs.sushi.com/blade-v2-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](https://sushi.com/portal/pricing)
- [GitHub Organization](https://github.com/sushiswap)
- [Privacy Policy](https://www.sushi.com/privacy)
- [Terms of Service](https://www.sushi.com/terms)
- [Blog](https://www.sushi.com/blog)
- [Discord](https://discord.gg/NVPXN4e)
- [Twitter](https://twitter.com/sushiswap)
- [Rate Limits](/rate-limits/rate-limits.md)
- [Plans](/plans/plans.md)
- [Fin Ops](/finops/finops.md)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
