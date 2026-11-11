# 开发者

[English](../en/developers.md) · **中文**

Awesome 上的一切都是开放的：HTTP API、TypeScript SDK、已验证的合约，以及给 AI 智能体用的技能。

| | |
|---|---|
| [SDK](https://github.com/Awesomechain/SDK) | `npm install github:Awesomechain/SDK viem` |
| [Contracts](https://github.com/Awesomechain/Contracts) | Solidity 源码、部署记录、文档、400+ 个测试 |
| [Skills](https://github.com/Awesomechain/Skills) | 智能体技能：读取行情、发射、交易、领取 |

## HTTP API

Base URL：`https://xn--nib-9na0w.xyz`。输入输出均为 JSON；出错时返回 `{ "error": "…" }`，状态码为 4xx/5xx。

| 路径前缀 | 链 |
|---|---|
| `/api` | BNB Chain |
| `/api/c/<chain>` | `base`、`arbitrum`、`hyperevm`、`monad`、`xlayer`、`elysium`、`robinhood`、`arc`（路由与 BNB Chain 相同） |
| `/api/c/solana` | Solana |
| `GET /api/c` | 所有链及其是否已上线 |

### 读取

| 路由 | 返回 |
|---|---|
| `GET /config` | 该链、它的部署信息和当前的发射设置 |
| `GET /stats` | 币数量、毕业数、24 小时成交笔数和成交量 |
| `GET /coins?sort=new\|trending\|mcap\|graduating\|burned&limit=&offset=&q=&launchType=&creator=&host=` | 币列表 |
| `GET /coins/:address` | 单个币 |
| `GET /coins/:address/trades?limit=` | 成交记录，最新的在前 |
| `GET /coins/:address/candles?interval=1\|15\|60\|300\|900\|3600\|14400\|86400` | K 线 |
| `GET /coins/:address/holders`, `/burns` | 持有人、销毁记录 |
| `GET /trades/recent`, `/burns/recent` | 所有币的汇总 |
| `GET /search?q=` | 币和配对代币 |
| `GET /claims/:address` | 某个钱包可领取的内容，附带现成的交易 |
| `GET /coins/:address/squad`, `/drip/:coin/epochs`, `/drip/:coin/proof/:address` | Squad（团队分成）和 Holder Drip（持有人分红） |
| `GET /events` | 实时的发射、成交、销毁和毕业（Server-Sent Events） |
| `GET /api/main-token`, `/api/main-token/candles` | $牛逼 |
| `GET /api/feed?tab=all\|launches\|posts\|x\|trades` | 动态 |

### 构建交易

这些接口返回未签名的交易（`{ to, data, value, chainId, gas? }`），任何钱包都可以签名。可以用 `GET` 加查询字符串，也可以用 `POST` 加 JSON 请求体。

| 路由 | 参数 |
|---|---|
| `/tx/launch` | `name`、`symbol`、`metadataUri`、`host`、`buyWei`、`launchType`（0-4 或 `devBag`…）、`squad`、`from` |
| `/tx/quote`, `/tx/swap` | `coin`、`side`（buy/sell）、`amountIn`、`payWith`（bnb/host）、`slippageBps`、`from` |
| `/tx/claim` | `address` |
| `POST /api/metadata` | `name`、`symbol`、`description`、`links`、`image`（data URL）→ 返回用于 `metadataUri` 的 `uri` |

示例：

```sh
curl "https://xn--nib-9na0w.xyz/api/tx/quote?coin=0x…&amountIn=10000000000000000"
```

### Solana

`/api/c/solana`：`coins`、`coins/:mint`、`coins/:mint/trades|candles|holders|escrow`、`POST launch/prepare` →
签名 → `POST tx/send` → `POST launch/confirm`、`POST swap/quote`、`POST swap/tx`。SDK 把它们全部封装好了（`awesome.solana`）。

## 30 秒上手 SDK

```ts
import { AwesomeClient } from "@awesomechain/sdk";

const awesome = new AwesomeClient();
const coins = await awesome.coins({ sort: "trending", limit: 10 });
const { tx } = await awesome.buildSwap({ coin: coins[0].address, amountIn: 10n ** 16n, from: me });
```

## 链上

索引 factory 的 `CoinLaunched` 事件以及 hook 的 `SwapFee`、`Graduated` 事件，或者直接调用 router。
[Contracts 集成指南](https://github.com/Awesomechain/Contracts/blob/main/docs/en/integration.md) 为每个操作都提供了 `cast` 和 viem 示例。
