# Trading212 Plugin for Claude Cowork

Connects Claude directly to your [Trading212](https://www.trading212.com/) account via the official Trading212 public API.

## What you can do

- View your portfolio, open positions, and account cash balance
- Place market, limit, stop, and stop-limit orders (with confirmation)
- Cancel orders
- Browse order history, dividends, and transaction records
- Search tradeable instruments and exchanges
- Manage Pies (portfolio buckets)
- Export account data as CSV
- Ask Claude to analyse your portfolio performance

## Setup

### 1. Get your Trading212 API key

1. Log in to Trading212.
2. Go to **Settings → API (Beta)**.
3. Generate a new API key.  
   See the [Trading212 help article](https://helpcentre.trading212.com/hc/en-us/articles/14584770928157-How-can-I-generate-an-API-key) for step-by-step guidance.

### 2. Install `uv` (Python package manager)

The server runs via `uv`. If you don't have it:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 3. Set environment variables in Cowork

After installing this plugin, go to **Settings → Plugins → Trading212 → Environment** and set:

| Variable | Value | Required |
|---|---|---|
| `TRADING212_API_KEY` | Your API key from step 1 | ✅ Yes |
| `TRADING212_API_SECRET` | API secret (newer auth flow) | Optional |
| `TRADING212_ENVIRONMENT` | `live` or `demo` | Defaults to `live` |

> Use `demo` if your API key was generated from the **Practice** account.

### 4. Pre-install dependencies (first time only)

Open Terminal and run:

```bash
cd ~/.claude/plugins/trading212/server
uv sync
```

This caches the Python dependencies so the server starts quickly.

## Source

MCP server by [Rohan Pandit](https://github.com/RohanAnandPandit/trading212-mcp-server) — MIT License.
