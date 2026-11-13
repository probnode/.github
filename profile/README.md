<img src="assets/probnode-logo-round.svg" alt="ProbNode" width="64" height="64" align="left">

**ProbNode** records Polymarket's order books and trades, every market and every change of the
book, and delivers them as parquet and csv files with a sha256 for every file, alongside a public
record of what was captured.

<br clear="left">

## About

- **Data:** the full order book (every change of every price level), every trade, the market
  definitions, and the feed-gap journal for each hour.
- **Coverage you can check:** for every outcome token and UTC hour, the milliseconds recorded, the
  gaps and the uptime, free and without a key.
- **Clients:** a Python SDK and command line, and an MCP server for AI agents, all open source
  under the MIT license.

## Resources

| | |
|---|---|
| Documentation | https://probnode.com/docs |
| API reference (OpenAPI 3.1) | https://probnode.com/openapi.json |
| Help centre | https://probnode.com/help |
| Plans and pricing | https://probnode.com/pricing |
| Python SDK and CLI | [probnode-sdk](https://github.com/probnode/probnode-sdk) · `pip install probnode-sdk` |
| MCP server | [probnode-mcp](https://github.com/probnode/probnode-sdk/tree/main/packages/probnode-mcp) · `pip install probnode-mcp` |

## Contact

- Email: hello@probnode.com
- Web: https://probnode.com
- Security issues: please report privately, see the [security policy](https://github.com/probnode/probnode-sdk/blob/main/SECURITY.md).
