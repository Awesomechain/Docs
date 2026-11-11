# Pairings (BNB Chain)

**English** · [中文](../zh/pairings.md)

A coin normally pairs with BNB. On BNB Chain it can instead pair with a **pairing token**, so that every trade of the
new coin also does something for that token's community.

| Pairing token | Burns it? |
|---|---|
| **four.meme** tokens | yes |
| **flap.sh** tokens | yes |
| **Locked-LP** tokens (PancakeSwap V2 liquidity mostly burned) | yes |
| **Another Awesome coin** (up to 3 levels deep) | yes |
| **Tokenized stocks** (bStocks, Ondo) | no |

## The $50K gate

A token can pair new coins only while its **market cap is at least $50,000**, checked at every launch:

- the price is the median of recent readings (at least 5, a minute apart), each one clamped to within 10% of the
  median, so a one-block pump can't fake it;
- a newly registered token waits 30 minutes before its first launch;
- the Pairings page shows each token's market cap, status and the coins launched on it.

## Burns

Part of every fee of a coin on a burnable pairing token **burns that pairing token**, in the same transaction. If the
pairing token is itself an Awesome coin on another token, the burn climbs the chain and every level burns (for
example 70% / 30% across two levels, or 60% / 20% / 20% across three).

## Buying with BNB

You don't need to hold the pairing token. Buy with BNB and the router buys the pairing token and then the coin, in one
transaction (selling works the other way). Tokenized stocks may not be available in every region.
