<p align="center">
  <a href="https://probnode.com"><img src="https://raw.githubusercontent.com/probnode/.github/main/profile/assets/banner.png?v=4" alt="ProbNode - Polymarket historical data, every change of the book" width="100%"></a>
</p>

<p align="center">
  <a href="https://probnode.com/login"><b>Get a free API key</b></a> ·
  <a href="https://probnode.com/docs"><b>Docs</b></a> ·
  <a href="https://probnode.com/catalog"><b>Catalog</b></a> ·
  <a href="https://probnode.com/pricing"><b>Pricing</b></a> ·
  <a href="https://probnode.com/openapi.json"><b>OpenAPI</b></a>
</p>

## About ProbNode

**Polymarket historical data, every change of the book.**

We record every price level of every outcome token, every trade, and every on-chain fill with the
wallets on both sides. Nothing is sampled, nothing is throttled, and every row carries both
clocks: the venue's own time and our receive time.

Know what you are buying before you pay. Our coverage ledger is public. For every token and UTC
hour it shows the milliseconds we recorded and every gap, and you can read it free, without a key.
Every file ships with a sha256.

One flat price per plan. No row meter, no surprise invoice. Start on the Free plan today.

<p align="center">
  <a href="https://probnode.com/docs/schemas"><img src="https://raw.githubusercontent.com/probnode/.github/main/profile/assets/schemas.png?v=2" alt="The 18 ProbNode schemas, from L3 fills to L0 bars" width="100%"></a>
</p>

## Why ProbNode

- **The book itself.** It is not a candle drawn afterwards. You see what was resting on the other
  side at the exact moment you would have traded, at full depth.
- **Who traded.** We read every `OrderFilled` from our own Polygon node, with maker and taker,
  joined to the trades.
- **18 schemas, one source.** They range from raw L3 fills to top of book, trade-quotes and OHLCV
  bars from 1 s to 1 d, all built from the same lossless recording.
- **Fresh every hour.** Each closed hour is checked, then published. It arrives as Parquet,
  csv.gz or our lossless Probe format.
- **Built for code and for agents.** We publish official clients for Python, Rust and C++, a CLI
  and an MCP server.

## Start in a minute

```bash
pip install probnode-sdk
probnode login
probnode export will-x-happen 2026-11-12 --format parquet   # one market, one UTC day, full book
```

```python
import probnode, pandas as pd

client = probnode.Client()
book = pd.read_parquet(client.export_book("will-x-happen", "2026-11-12"))  # sha256-checked
```

On Rust, run `cargo add probnode`. On C++, use `find_package(probnode)`. AI agents can use
`pip install probnode-mcp`.

## Resources

- [Documentation](https://probnode.com/docs): the quick start, the API reference, every schema
  column by column, and examples.
- [Catalog and coverage ledger](https://probnode.com/catalog): every market we hold, hour by hour,
  free to browse.
- [Help centre](https://probnode.com/help): answers to the questions buyers ask before the invoice.

## Open source

| | |
|---|---|
| [**probnode-sdk**](https://github.com/probnode/probnode-sdk) | The official Python client, the CLI and the MCP server. MIT |
| [**probnode-rs**](https://github.com/probnode/probnode-rs) | The official Rust client. It is async and blocking, with typed models and sha256-checked downloads. Apache-2.0 |
| [**probnode-cpp**](https://github.com/probnode/probnode-cpp) | The official C++ client: C++17, CMake, sha256-checked downloads. Apache-2.0 |
| [**probe**](https://github.com/probnode/probe) | Probe is our lossless order-book file format. This repository has the specification, conformance vectors, and the Rust and Python readers. Apache-2.0 |

## Contact

Do you have a question, need a dataset, or want a trial for your team? Write to
[hello@probnode.com](mailto:hello@probnode.com).

Please report security issues privately, as described in our
[security policy](https://github.com/probnode/probnode-sdk/blob/main/SECURITY.md).
