# SushiSwap (sushiswap)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
