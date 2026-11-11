# Developers

**English** · [中文](../zh/developers.md)

Everything on Awesome is open: an HTTP API, a TypeScript SDK, verified contracts and skills for AI agents.

| | |
|---|---|
| [SDK](https://github.com/Awesomechain/SDK) | `npm install github:Awesomechain/SDK viem` |
| [Contracts](https://github.com/Awesomechain/Contracts) | Solidity sources, deployments, docs, 400+ tests |
| [Skills](https://github.com/Awesomechain/Skills) | agent skills: read the market, launch, trade, claim |

## HTTP API

Base URL: `https://xn--nib-9na0w.xyz`. JSON in and out; errors are `{ "error": "…" }` with a 4xx/5xx status.

| Path prefix | Chain |
|---|---|
| `/api` | BNB Chain |
| `/api/c/<chain>` | `base`, `arbitrum`, `hyperevm`, `monad`, `xlayer`, `elysium`, `robinhood`, `arc` (same routes as BNB Chain) |
| `/api/c/solana` | Solana |
| `GET /api/c` | every chain and whether it is live |

### Read

| Route | Returns |
|---|---|
| `GET /config` | the chain, its deployment and the live launch settings |
| `GET /stats` | coins, graduations, 24 h trades and volume |
| `GET /coins?sort=new\|trending\|mcap\|graduating\|burned&limit=&offset=&q=&launchType=&creator=&host=` | coins |
| `GET /coins/:address` | one coin |
| `GET /coins/:address/trades?limit=` | trades, newest first |
| `GET /coins/:address/candles?interval=1\|15\|60\|300\|900\|3600\|14400\|86400` | candles |
| `GET /coins/:address/holders`, `/burns` | holders, burns |
| `GET /trades/recent`, `/burns/recent` | across every coin |
| `GET /search?q=` | coins and pairing tokens |
| `GET /claims/:address` | what a wallet can collect, with ready transactions |
| `GET /coins/:address/squad`, `/drip/:coin/epochs`, `/drip/:coin/proof/:address` | Squad and Holder Drip |
| `GET /events` | live launches, trades, burns and graduations (Server-Sent Events) |
| `GET /api/main-token`, `/api/main-token/candles` | $牛逼 |
| `GET /api/feed?tab=all\|launches\|posts\|x\|trades` | the Feed |

### Build transactions

These return unsigned transactions (`{ to, data, value, chainId, gas? }`) for any wallet to sign. `GET` with a query
string or `POST` with a JSON body.

| Route | Input |
|---|---|
| `/tx/launch` | `name`, `symbol`, `metadataUri`, `host`, `buyWei`, `launchType` (0-4 or `devBag`…), `squad`, `from` |
| `/tx/quote`, `/tx/swap` | `coin`, `side` (buy/sell), `amountIn`, `payWith` (bnb/host), `slippageBps`, `from` |
| `/tx/claim` | `address` |
| `POST /api/metadata` | `name`, `symbol`, `description`, `links`, `image` (data URL) → `uri` for `metadataUri` |

Example:

```sh
curl "https://xn--nib-9na0w.xyz/api/tx/quote?coin=0x…&amountIn=10000000000000000"
```

### Solana

`/api/c/solana`: `coins`, `coins/:mint`, `coins/:mint/trades|candles|holders|escrow`, `POST launch/prepare` →
sign → `POST tx/send` → `POST launch/confirm`, `POST swap/quote`, `POST swap/tx`. The SDK wraps all of them
(`awesome.solana`).

## SDK in 30 seconds

```ts
import { AwesomeClient } from "@awesomechain/sdk";

const awesome = new AwesomeClient();
const coins = await awesome.coins({ sort: "trending", limit: 10 });
const { tx } = await awesome.buildSwap({ coin: coins[0].address, amountIn: 10n ** 16n, from: me });
```

## On-chain

Index the factory's `CoinLaunched` and the hook's `SwapFee`, `Graduated` events, or call the router directly. The
[Contracts integration guide](https://github.com/Awesomechain/Contracts/blob/main/docs/en/integration.md) has
`cast` and viem examples for every action.
