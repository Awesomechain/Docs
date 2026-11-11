# Trading

**English** · [中文](../zh/trading.md)

## The curve

On the EVM chains every coin has **1,000,000,000** tokens, all locked in its pool from the start:

- **800M on the curve**: the price rises as people buy and falls as they sell, like a bonding curve.
- **200M in the tail**: liquidity above the graduation price, so the pool can never be bought out.

The liquidity is locked forever: nobody can remove it, and nobody can add their own, so the price you see is the
price the curve sets. The price can't fall below the launch price.

## Graduation

When the curve has raised its target, the coin **graduates**:

| Chain | Target |
|---|---|
| BNB Chain | 16 BNB |
| Base, Arbitrum, Robinhood Chain | 5.25 ETH |
| HyperEVM, Elysium | 150 HYPE |
| Monad | 660,000 MON |
| X Layer | 114 OKB |
| Arc | 11,000 USDC |

(Coins paired with a pairing token have their target set in that token at launch.) Graduation changes nothing for
traders: the coin keeps trading in the same pool, with the same fee. There's no migration, no new pool, and no
moment when liquidity moves.

## The sniper window

For the **first 10 seconds** after a launch, buys pay a **50% fee** and one buy can take at most **1% of supply**.
It makes sniping bots pay for being first. The creator's own first buy, made in the launch transaction, pays the
normal fee. After 10 seconds the normal fee applies.

## Placing a trade

1. Open the coin page and enter an amount: native coin (or pair token) to buy, tokens to sell.
2. Check the quote: what you get, the price impact and the fee.
3. Set slippage (default 1%). The trade reverts if the price moves against you by more than that.
4. Confirm in your wallet. Selling for the first time needs an approval transaction first.

Coins paired with another token can be bought and sold with the native coin in one transaction: the router goes
through the pair token for you.

## The chart

Every coin page has a live candle chart (from 1-second to 1-day candles), with the trades, holders and burns listed
under it.

## Solana

Solana coins trade on their venue's curve (Pump.fun or Raydium LaunchLab), and after graduation through Jupiter, all
from the same coin page.

## Fees

Every trade pays a small fee to the pool. See [Fees](fees.md).
