# Launching a coin

**English** · [中文](../zh/launching.md)

Press **Launch** in the header and fill in the form. The launch is one transaction from your wallet.

## 1. Chain

Pick the chain the coin lives on: BNB Chain, Base, Arbitrum, HyperEVM, Monad, X Layer, Elysium, Robinhood Chain, Arc
or Solana.

## 2. The coin

| Field | |
|---|---|
| **Name** | up to 32 bytes (about 32 Latin letters or 10 Chinese characters) |
| **Ticker** | up to 16 bytes, no spaces (Solana: up to 10 characters) |
| **Picture** | PNG, JPEG, WebP or GIF (GIFs under 1 MB). It is resized for you. |
| **Description** | optional |
| **Links** | website, X, Telegram (optional). With no website, the coin links to niúbī.xyz. |

The picture and details are stored as the coin's metadata and linked from the token contract forever.

## 3. Pair (BNB Chain)

By default a coin pairs with the chain's native coin (BNB, ETH, …). On BNB Chain you can instead pair it with a
**pairing token** (a four.meme, flap.sh or locked-LP token, a tokenized stock, or another Awesome coin). Its trades
then also burn that token. See [Pairings](pairings.md).

## 4. Launch type

Pick where the creator share of every fee goes. It can never be changed after launch.

| Type | Creator share |
|---|---|
| **Dev Bag** | you claim it |
| **Flywheel** | buys back the coin and burns it |
| **Bull Run** | buys $牛逼 and burns it (native pairs only) |
| **Holder Drip** | paid to the coin's holders |
| **Squad** | split between 2-5 wallets by fixed shares |

Details: [Launch types](launch-types.md).

## 5. Trading fee (Uniswap v4 chains)

On Base, Arbitrum, HyperEVM, Monad, X Layer, Elysium, Robinhood Chain and Arc you can pick the coin's trading fee,
from **0.25% to 5%**, fixed for the coin's life. A higher fee means more for the launch type and less for traders.
BNB Chain coins use 1%. On Solana, Raydium LaunchLab coins pick a fee tier from 1% to 5%.

## 6. First buy (optional)

Buy your own coin in the launch transaction, before anyone else can. It pays the normal fee (not the sniper fee) and
is capped at **5% of supply**. Coins paired with a locked-LP token need a first buy.

## 7. Pay from another chain (optional)

Short on gas on the chain you're launching on? **Pay from** lets you pay with BNB, SOL or another chain's coin; the
payment is bridged and the launch made for you in one flow, with the coin and the first-buy tokens going to your
wallet.

## 8. Launch

Press **Launch**, confirm in your wallet, and the coin is live the moment the transaction lands, with its page,
chart and share link.

## After launch

- Share the coin's page: `https://xn--nib-9na0w.xyz/v/<address>` (BNB Chain) or
  `https://xn--nib-9na0w.xyz/c/<chain>/<address>`.
- Creators can collect Dev Bag fees on the **Profile** page. See [Claiming](claiming.md).
- The creator role can be handed to another wallet (two steps: offer, then accept).

## Solana

Solana coins launch on **Pump.fun** or **Raydium LaunchLab**, pair with SOL, and use the same five launch types. The
creator fees those venues pay go to a fee escrow for the coin, and the launch type decides what happens to them.
