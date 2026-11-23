# HoldTheWheel MCP client examples

Plan and approve automation in a shared workspace with spend limits and an audit trail. Know the cost of each action before you run it.

This repository holds small, working examples for the hosted **HoldTheWheel** MCP server. It is maintained by Elite AI Empire. The server itself is hosted; nothing here runs it.

- Product: https://holdthewheel.eliteaiempire.com/
- MCP endpoint (streamable HTTP): `https://holdthewheel.eliteaiempire.com/mcp`
- OpenAPI: https://holdthewheel.eliteaiempire.com/openapi.json
- Pricing, machine readable: https://holdthewheel.eliteaiempire.com/pricing.json
- Discovery file: https://holdthewheel.eliteaiempire.com/.well-known/mcp.json

## Tools

| Tool | What it does |
|---|---|
| `holdthewheel_cost_model` | Returns monthly price, monthly credit cap, hard-stop credits and worst-case model cost for every tier. Pricing: {"unit": "call", "price_usd": 0, "free_quota": " |
| `holdthewheel_about` | What Hold The Wheel does and what is free Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is publish |
| `holdthewheel_pricing` | Where prices live and what costs nothing Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is publishe |
| `get_company_info` | Operator, support email, postal address, products and key pages. Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed vo |
| `list_pricing` | Current plans and prices in USD: plan, interval, amount_usd, currency, what_you_get. No account needed. |
| `get_checkout_link` | Checkout URL for a plan. With no arguments: the main paid plan. Where the site supports it the URL is a Stripe-hosted Checkout session (created unpaid; a human  |
| `search_site` | Keyword search over the public pages and workflow examples. Returns title, URL and a one-line summary. Pricing: {"unit": "call", "price_usd": 0, "free_quota": " |
| `usage_get` | Usage for the calling key (last 30 days) |

## Try it

```bash
bash examples/initialize.sh
python3 examples/client.py
```

`examples/client.py` uses only the Python standard library. It sends `initialize` and `tools/list` and prints the result. No key is needed for the public read tools. Tools that need an account say so in their description.

## Registry

Listed in the official MCP registry. Server manifest: `server.json`.

## Licence

MIT. See `LICENSE`.
