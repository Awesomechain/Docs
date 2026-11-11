# Fees

**English** · [中文](../zh/fees.md)

## What a trade costs

| | Fee |
|---|---|
| BNB Chain | **1%** of every buy and sell |
| Uniswap v4 chains | **1%**, or the fee the creator picked at launch (0.25% - 5%) |
| Solana | the venue's fee (Pump.fun; Raydium LaunchLab tiers 1% - 5%) |
| First 10 seconds after a launch | 50% (the [sniper window](trading.md#the-sniper-window)) |

The fee is taken on the native (or pair-token) side of the trade, inside the pool, in the same transaction.
Launching itself costs only gas.

## Where every fee goes

| Share | Goes to |
|---|---|
| **60%** | the coin's [launch type](launch-types.md): the creator, buyback and burn, $牛逼 burn, holders or a squad |
| **10%** | the Awesome platform |
| **10%** | 牛逼 staking |
| **20%** | buying back **$牛逼** and burning it |

The 20% buyback and burn comes from **every chain**: fees earned on Base, Solana or any other chain buy and burn
$牛逼 too.

Coins paired with a burnable pairing token (four.meme, flap.sh, locked-LP or another Awesome coin) also burn their
pairing token with every trade. See [Pairings](pairings.md).

## Where to see it

- Each coin page shows the fees its trades have paid and what its launch type did with them.
- The $牛逼 page shows how much $牛逼 has been burned.
- Every fee is on-chain: the hook emits a `SwapFee` event on every trade and the fee vault records every payout.
  See the [Contracts](https://github.com/Awesomechain/Contracts).
