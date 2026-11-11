# Claiming

**English** · [中文](../zh/claiming.md)

Open **Profile** with your wallet connected. It lists the coins you launched and the fees you can claim, and the
coin page of a Squad or Holder Drip coin shows your share there too. Press **Claim** and confirm in your wallet.

| You are | You can claim | Paid in |
|---|---|---|
| The creator of a **Dev Bag** coin | its creator share | the coin's pair token (BNB, ETH, …) |
| A member of a **Squad** | your fixed share | the pair token |
| A holder of a **Holder Drip** coin | your share of each posted epoch | the pair token |

Notes:

- Claims never expire, except Holder Drip epochs: unclaimed amounts return to the coin's pot after **90 days** and
  are shared in later epochs.
- Payouts can be sent by anyone (a friend, a bot, the site) but always go to the rightful wallet.
- Flywheel and Bull Run coins have nothing to claim: their creator share is spent on burns.
- On Solana, fees are paid out from the coin's escrow by Awesome's payout bot, following the launch type.

## For developers

`GET /api/claims/<address>` returns every claim with ready-to-send transactions. See [Developers](developers.md) and
the [SDK](https://github.com/Awesomechain/SDK) (`awesome.claims(address)`).
