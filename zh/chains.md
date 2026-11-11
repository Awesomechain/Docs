# 链

[English](../en/chains.md) · **中文**

| 链 | 原生币 | 交易场所 | 毕业目标 | 币的页面 |
|---|---|---|---|---|
| **BNB Chain** | BNB | PancakeSwap Infinity | 16 BNB | `/v/<address>` |
| **Base** | ETH | Uniswap v4 | 5.25 ETH | `/c/base/<address>` |
| **Arbitrum** | ETH | Uniswap v4 | 5.25 ETH | `/c/arbitrum/<address>` |
| **HyperEVM** | HYPE | Uniswap v4 | 150 HYPE | `/c/hyperevm/<address>` |
| **Monad** | MON | Uniswap v4 | 660,000 MON | `/c/monad/<address>` |
| **X Layer** | OKB | Uniswap v4 | 114 OKB | `/c/xlayer/<address>` |
| **Elysium** | HYPE | Uniswap v4 | 150 HYPE | `/c/elysium/<address>` |
| **Robinhood Chain** | ETH | Uniswap v4 | 5.25 ETH | `/c/robinhood/<address>` |
| **Arc** | USDC | Uniswap v4 | 11,000 USDC | `/c/arc/<address>` |
| **Solana** | SOL | Pump.fun、Raydium LaunchLab | 以平台为准 | `/c/solana/<mint>` |

每条 EVM 链上都是同样的合约、同样的规则、同样的发射类型。配对代币（four.meme、flap.sh、锁仓 LP、股票）在 BNB Chain 上；在其他链上，币与原生币或其他 Awesome 币配对。

## 合约地址

每个合约都已在所在链的区块浏览器上验证。完整记录：[Contracts/deployments](https://github.com/Awesomechain/Contracts/tree/main/deployments)。

### BNB Chain (56)

| 合约 | 地址 |
|---|---|
| Factory | [`0x82BcF05C1b7f49eC6e0Ba07d83eC15538F2CC569`](https://bscscan.com/address/0x82BcF05C1b7f49eC6e0Ba07d83eC15538F2CC569) |
| Router | [`0x868dcB84422910BF93C6d517a853f931a2943F97`](https://bscscan.com/address/0x868dcB84422910BF93C6d517a853f931a2943F97) |
| Fee vault | [`0x07f46cf4E7864bf61D80e0AB684C0122Ce01Fddb`](https://bscscan.com/address/0x07f46cf4E7864bf61D80e0AB684C0122Ce01Fddb) |
| Locker | [`0xc768562b1E9b943Aa9eb39767Bf1126aD5a6cf40`](https://bscscan.com/address/0xc768562b1E9b943Aa9eb39767Bf1126aD5a6cf40) |
| Hook | [`0xDd21fAD629cB7e3A73c4dBE695990aa3d159168d`](https://bscscan.com/address/0xDd21fAD629cB7e3A73c4dBE695990aa3d159168d) |
| Pair registry | [`0x36d2AE336d23A89671068281D8957AC379de7f9b`](https://bscscan.com/address/0x36d2AE336d23A89671068281D8957AC379de7f9b) |

### Base、Arbitrum、Monad、X Layer、Elysium、Robinhood Chain、Arc

这七条链上的地址完全相同：

| 合约 | 地址 |
|---|---|
| Factory | `0xBd7677dE392022aFE248146480AdbD31D6Ac14cA` |
| Router | `0x17781bd269DAbeE24fAF5C23e6c14FA84E328047` |
| Fee vault | `0x4192E04B59F97327E36236a7A97AA538543e190A` |
| Locker | `0x1FbA689e17Cb43098b74D05E574FeFB7a1161108` |
| Pair registry | `0xBd83232907ABFD36de2B1E2b193CDf60d74Fc17B` |

Hook（每条链单独挖出地址）：

| 链 | Hook |
|---|---|
| Base | `0xE802ae1D6E52E5b21332Be64B3E962a35970f8eC` |
| Arbitrum | `0x7f8E20905C05E19f756BACb082a28dd3a6b578Ec` |
| Monad | `0x3D800fE713b87b1F191D76f4F63A60543Bcc78Ec` |
| X Layer | `0x7f8E20905C05E19f756BACb082a28dd3a6b578Ec` |
| Elysium | `0x13F55fBc0a2dfCd0AA99C990cf2cE7e9f190f8eC` |
| Robinhood Chain | `0x50D9e09dCF76239034556e7e08e71F0410bD78Ec` |
| Arc | `0x50D9e09dCF76239034556e7e08e71F0410bD78Ec` |

### HyperEVM (999)

| 合约 | 地址 |
|---|---|
| Factory | `0x17781bd269DAbeE24fAF5C23e6c14FA84E328047` |
| Router | `0xcBD6C0Caa5Ccce16cF86C8C2ee52bC15d9b70300` |
| Fee vault | `0x1FbA689e17Cb43098b74D05E574FeFB7a1161108` |
| Locker | `0xBd7677dE392022aFE248146480AdbD31D6Ac14cA` |
| Hook | `0x88c80569B9309DEE8737B4d844Ea311A794838ec` |
| Pair registry | `0x4192E04B59F97327E36236a7A97AA538543e190A` |

## 跨链支付

发射表单中的 **Pay from**（跨链支付）选项让你用 BNB、SOL 或其他链的币，为某条链上的发射付款：付款自动跨链，发射一气呵成。
