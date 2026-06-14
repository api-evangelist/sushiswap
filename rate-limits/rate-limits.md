# SushiSwap API Rate Limits

SushiSwap enforces rate limits across its Pricing, Quote, and Swap API endpoints. When a limit is exceeded, the API returns HTTP 429 (Too Many Requests). Specific numeric thresholds are not publicly published and vary by API tier.

## Rate Limit Behavior

- **HTTP Status on Exceeded Limit:** 429 Too Many Requests
- **Error Format:** RFC 7807 Problem Details JSON response
- **Rate limit scope:** Applied per API key (or per IP for unauthenticated requests)

## Tiers

| Tier | Authentication | Rate Limit |
|------|---------------|------------|
| Unauthenticated | No API key | Low (undisclosed) |
| API Key | `apiKey` query param or header | Higher (undisclosed) |
| Enterprise | Custom arrangement | Custom |

## Error Response Example

```json
{
  "type": "https://docs.sushi.com/api/errors/rate-limit-exceeded",
  "title": "Rate Limit Exceeded",
  "status": 429,
  "detail": "You have exceeded the allowed number of requests. Please retry after the reset window."
}
```

## Standardized Error Types

The API uses 13 standardized error types in RFC 7807 format, including:

- `rate-limit-exceeded` — too many requests within the time window
- `invalid-api-key` — provided key not recognized or expired
- `insufficient-balance` — wallet balance too low for the requested swap
- `insufficient-allowance` — token spend approval not granted
- `validation-error` — malformed or missing required parameters
- `no-route-found` — no viable liquidity path for the swap pair
- `data-freshness-error` — stale pricing data detected

## Best Practices

- Always include an `apiKey` from https://sushi.com/portal to avoid IP-based shared limits
- Implement exponential backoff when receiving 429 responses
- Cache price responses locally (prices update on a block-by-block cadence)
- Use the Quote API to check viability before calling the Swap API

## References

- Developer Portal (API Keys): https://sushi.com/portal
- Documentation: https://docs.sushi.com
