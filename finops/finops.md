# SushiSwap API FinOps

## Cost Model Overview

SushiSwap's Pricing, Quote, and Swap APIs do not publish explicit per-call pricing on their public documentation. Access is tiered by API key registration through the developer portal at https://sushi.com/portal.

## Cost Considerations

### API Usage Costs

- **Free / No API Key:** No direct monetary cost, subject to rate throttling
- **API Key (Portal):** Currently no stated subscription fee for standard API key access; pricing page at https://sushi.com/portal/pricing should be consulted for current tiers
- **Enterprise:** Custom pricing negotiated with Sushi Labs

### On-Chain Transaction Costs

When using the Swap API to execute transactions, consumers incur blockchain gas fees. These are not charged by Sushi but are required by the underlying network:

| Network | Typical Gas Range |
|---------|-------------------|
| Ethereum Mainnet | Variable (EIP-1559) |
| Arbitrum One | Lower than mainnet |
| Optimism | Lower than mainnet |
| Polygon PoS | Very low |
| BNB Smart Chain | Low |
| Avalanche | Low to medium |
| Base | Very low |

### Protocol Fees

SushiSwap charges a protocol swap fee on liquidity pool trades, typically 0.25%–0.30% of the trade amount depending on the pool type (V2 vs V3 vs Blade). These fees are deducted from the swap output, not billed separately.

| Pool Type | Protocol Fee |
|-----------|-------------|
| cpAMM (V2) | 0.30% per swap |
| clAMM (V3) | Variable (fee tier: 0.01%, 0.05%, 0.30%, 1.00%) |
| Blade (RFQ) | Negotiated with market makers |

## FinOps Recommendations

1. **Cache Price API responses** — Prices are block-level and can be cached for short intervals (10–15s) to reduce API call volume
2. **Use Quote before Swap** — Always pre-check routes via the Quote API before committing Swap calls that may fail
3. **Monitor 429 responses** — Track rate limit hits to identify when an API key upgrade or request reduction is needed
4. **Choose low-fee networks** — Route integrations through L2s (Arbitrum, Optimism, Base) to minimize end-user gas costs
5. **Select V3 fee tiers** — Use lower-fee V3 pools (0.01% or 0.05%) for stable or high-volume pairs

## References

- Developer Portal: https://sushi.com/portal
- Pricing Page: https://sushi.com/portal/pricing
- Documentation: https://docs.sushi.com
- Blog: https://www.sushi.com/blog
