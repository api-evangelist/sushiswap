# SushiSwap API Plans

SushiSwap provides access to its Pricing, Quote, and Swap APIs through a developer portal at https://sushi.com/portal. API keys are optional for basic usage but required for higher-volume access and unlocking additional tiers.

## Free Tier (No API Key)

- Access to Pricing, Quote, and Swap APIs without registration
- Subject to lower rate limits and no SLA guarantees
- Suitable for development, testing, and low-volume integrations
- No authentication header required; API key parameter is omitted

## API Key Tier (Portal Registration)

- Obtain a key at https://sushi.com/portal
- Higher rate limits than the unauthenticated tier
- API key passed as `apiKey` query parameter or via authorization header
- Unlocks optional gas simulation via `simulate=true` parameter on the Swap API
- Access to Blade V2 RFQ protocol for blue-chip token trading

## Enterprise / Custom

- Contact Sushi Labs for high-volume, dedicated infrastructure arrangements
- Custom rate limits and SLA available
- Suitable for DEX aggregators, wallets, and institutional trading desks

## Supported Networks

All plans cover the following chains (non-exhaustive):

- Ethereum (chainId: 1)
- Arbitrum One (chainId: 42161)
- Optimism (chainId: 10)
- Polygon PoS (chainId: 137)
- Avalanche C-Chain (chainId: 43114)
- BNB Smart Chain (chainId: 56)
- Base (chainId: 8453)
- Blast (chainId: 81457)
- Linea (chainId: 59144)
- Fantom (chainId: 250)
- Stellar (chainId: -4)
- 30+ additional EVM-compatible networks

## Resources

- Developer Portal: https://sushi.com/portal
- Pricing Page: https://sushi.com/portal/pricing
- Documentation: https://docs.sushi.com
