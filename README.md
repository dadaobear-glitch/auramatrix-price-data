# AuraMatrix price data

What AI compute costs, with a source for every number: list prices of language-model APIs per channel, and GPU rental prices
per provider. This repository is the open copy of what [auramatrix.ai](https://auramatrix.ai) publishes, refreshed every day.

**Licence: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).** Use it for anything, including commercially. Give credit as:

> Source: AuraMatrix (auramatrix.ai)

## Files

| File | What it holds |
|---|---|
| `latest/llm-token-prices.csv` | One row per model, channel and plan: input, output, cached and cache-write price per 1M tokens, currency, trust status, when it was observed and the source page |
| `latest/gpu-prices-usd.csv` | GPU rental prices in USD per GPU-hour: provider, kind (on demand, spot, reserved, market), machine, vCPUs, memory, network |
| `latest/gpu-prices-china-cny.csv` | GPU rental prices in mainland China, in CNY as published (never converted), with stock per zone |
| `latest/price-changes.csv` | Observed and vendor-announced price changes |
| `latest/indices.json` | The trial token price indices by tier |
| `latest/dataset.json` | The full token price dataset as the site serves it (records, sources with snapshot hashes, billing rules, daily checks) |
| `daily/YYYY-MM-DD.json` | Everything above for one day in one file |

## What the numbers are

- **List prices as published**, not invoices. The channel's or provider's own page is authoritative.
- **Every record names its source** and the time it was observed. Records are added, never edited: a new price is a new record.
- **Currencies are never converted.** USD and CNY prices are separate files.
- **A missing value is unknown, not zero.**
- A GPU price from a provider that sells whole machines is the machine price divided by its GPU count.
- Coverage: models and channels from the United States and China.

How the data is collected and checked: <https://auramatrix.ai/prices/methodology>. How often it has been right: <https://auramatrix.ai/prices/accuracy>.

## Use it from an AI assistant

The same data is an MCP server (no key): `https://auramatrix.ai/mcp`. Setup: <https://auramatrix.ai/connect>.
JSON without MCP: `https://auramatrix.ai/prices/index.json`, `https://auramatrix.ai/prices/v1/compute`.

Corrections: hello@auramatrix.ai

---

AuraMatrix 价格数据：大模型 API 的 token 标价（按渠道）和 GPU 租价（按供应方），每天更新，每个数字都有来源。许可为 CC BY 4.0，使用时请注明“来源：AuraMatrix (auramatrix.ai)”。人民币价格按公布的原样记录，不换算。
