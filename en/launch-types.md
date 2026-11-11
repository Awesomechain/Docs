# Launch types

**English** · [中文](../zh/launch-types.md)

Every coin picks a **launch type** at launch. It decides where the **creator share** (60%) of every trading fee goes.
It is written on-chain at launch and **can never be changed**, so holders always know what the fees do.

## Dev Bag

The creator share is **the creator's**, claimable any time on the Profile page. Classic and simple.

- Anyone can trigger the payout, but it only ever goes to the creator.
- The creator can hand the coin over to another wallet (offer, then accept), and the fees follow.

## Flywheel

The creator share **buys back the coin in its own pool and burns it**. Every trade shrinks the supply.

- The buyback is run regularly by Awesome's keeper, or by the creator.
- Nobody else can trigger it, so no one can time a trade around it.
- Burned tokens are destroyed (`burn()`): the total supply goes down for good.

## Bull Run

The creator share **buys $牛逼 and burns it**. A coin that pumps $牛逼 with every trade.

- Native-paired coins only.
- On BNB Chain it happens on-chain: the fee buys $牛逼 through allowed PancakeSwap pools and sends it to
  `0x000000000000000000000000000000000000dEaD`. The contract checks the $牛逼 arrived there.
- On the other chains, the Bull Run share is sent to BNB Chain to buy and burn $牛逼.
- The site shows how much $牛逼 Bull Run coins have burned.

## Holder Drip

The creator share is **paid to the coin's holders**, in proportion to what they hold.

- Every epoch, a snapshot of holders is taken (pools, contracts and the burn address left out) and published as a
  merkle tree.
- Holders claim their share on the Profile page (anyone can send a holder's claim; it always pays the holder).
- Unclaimed amounts are returned to the pot after 90 days and go to the next epochs.

## Squad

The creator share is **split between 2 to 5 wallets** by fixed shares set at launch (for example 50 / 30 / 20).

- Each member claims their own share whenever they like; one member's claim never changes another's.
- Members and shares can't be changed after launch.

## Comparing them

| | Who benefits | Good for |
|---|---|---|
| Dev Bag | the creator | creators who build and promote the coin |
| Flywheel | every holder (less supply) | community coins, deflation |
| Bull Run | $牛逼 holders | coins riding the 牛逼 narrative |
| Holder Drip | holders, paid in the native coin or pair token | "hold and earn" coins |
| Squad | a team | teams, collabs, KOL launches |

Whatever the type, the rest of each fee is split the same way: see [Fees](fees.md).
