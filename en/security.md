# Security

**English** · [中文](../zh/security.md)

## What can never change

- **A coin's supply.** 1,000,000,000 tokens, minted once. No one can mint more; burns only lower it.
- **A coin's liquidity.** Locked in its pool forever. There is no function that removes it.
- **A coin's rules.** Its fee, sniper window, fee split and graduation price are fixed at launch.
- **A coin's launch type** and its squad.
- **The token contract.** No owner, no tax, no pause, no blacklist.
- **The pool hook.** No admin and no upgrade.

## What the admin can do

The admin can change the settings of **future** launches (inside fixed limits, for example a fee between 0.25% and
5%), pause new launches, and manage which tokens can be pairing tokens. The admin **can't** touch an existing coin,
its pool, its fees or anyone's claims, and can't move anyone's funds.

## What the keeper can do

Awesome's keeper runs Flywheel and Bull Run buybacks and posts Holder Drip epochs. It can only spend a coin's creator
share the way that coin's launch type says.

## Verified and tested

- Every contract is verified on its chain's explorer, and the published source rebuilds the exact deployed bytecode.
- More than 400 tests: unit, fuzzing, invariants, attack simulations and live-chain forks.

Details: [Contracts security model](https://github.com/Awesomechain/Contracts/blob/main/docs/en/security.md).

## Staying safe

- Use only **niúbī.xyz** (`xn--nib-9na0w.xyz`). Bookmark it.
- Never share your seed phrase. Awesome will never ask for it.
- Anyone can launch a coin. Do your own research; locked liquidity doesn't make a coin a good investment.
- Check contract addresses on the [Chains](chains.md) page.
