[![MSeeP.ai Security Assessment Badge](https://mseep.net/pr/hive-intel-crypto-mcp-onchain-dex-badge.png)](https://mseep.ai/app/hive-intel-crypto-mcp-onchain-dex)

# Hive MCP On-Chain DEX & Pool Analytics

## Overview
Model Context Protocol (MCP) server for on-chain decentralized exchange (DEX) and liquidity pool analytics. This MCP provides comprehensive tools for analyzing DEX trading, liquidity pools, and automated market makers (AMMs) across multiple blockchain networks.

## Connection Details
- **Transport**: HTTP (Remote only)
- **URL**: `https://mcp.hiveintelligence.xyz/hive_onchain_dex/mcp`
- **Protocol**: Model Context Protocol (MCP)

## Features
- Real-time DEX trading data
- Liquidity pool analytics and metrics
- Swap transaction monitoring
- Pool TVL (Total Value Locked) tracking
- Impermanent loss calculations
- Yield farming APR/APY analysis
- Cross-chain DEX aggregation
- Slippage estimation
- MEV (Maximum Extractable Value) detection
- Arbitrage opportunity identification

## Usage

### Claude Desktop Configuration
Add to your Claude Desktop configuration file:

```json
{
  "mcpServers": {
    "hive-onchain-dex": {
      "url": "https://mcp.hiveintelligence.xyz/hive_onchain_dex/mcp",
      "transport": "http"
    }
  }
}
```

### MCP Client Integration
```javascript
import { Client } from '@modelcontextprotocol/sdk';

const client = new Client({
  name: 'dex-analytics-client',
  version: '1.0.0'
});

await client.connect({
  url: 'https://mcp.hiveintelligence.xyz/hive_onchain_dex/mcp',
  transport: 'http'
});
```

## Available Tools

### `get_pool_info`
Retrieve detailed information about liquidity pools
```json
{
  "tool": "get_pool_info",
  "params": {
    "pool_address": "0x...",
    "chain": "ethereum"
  }
}
```

### `analyze_swap_activity`
Analyze recent swap transactions
```json
{
  "tool": "analyze_swap_activity",
  "params": {
    "token_pair": "ETH/USDC",
    "timeframe": "24h",
    "min_volume": 10000
  }
}
```

### `calculate_impermanent_loss`
Calculate impermanent loss for liquidity positions
```json
{
  "tool": "calculate_impermanent_loss",
  "params": {
    "position_id": "12345",
    "current_prices": true
  }
}
```

### `get_pool_tvl`
Track Total Value Locked in pools
```json
{
  "tool": "get_pool_tvl",
  "params": {
    "protocol": "uniswap_v3",
    "top_pools": 100
  }
}
```

### `find_arbitrage_opportunities`
Identify arbitrage opportunities across DEXs
```json
{
  "tool": "find_arbitrage_opportunities",
  "params": {
    "min_profit": 100,
    "chains": ["ethereum", "polygon", "arbitrum"]
  }
}
```

## Keywords
DEX, decentralized exchange, liquidity pool, AMM, automated market maker, DeFi, swap, trading, blockchain, Web3, TVL, total value locked, yield farming, APR, APY, impermanent loss, slippage, MEV, arbitrage, liquidity provider, LP tokens, pool analytics, on-chain data, cross-chain, multi-chain, MCP, Model Context Protocol, HTTP MCP server, remote MCP, Hive Intelligence, UniSwap, SushiSwap, PancakeSwap, decentralized trading, liquidity mining

## License
MIT

## Support
For issues and feature requests, please open an issue on GitHub.

## About Hive Intelligence
Part of the Hive Intelligence suite of blockchain analytics MCP servers.