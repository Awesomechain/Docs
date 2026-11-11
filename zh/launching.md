# 发射一个币

[English](../en/launching.md) · **中文**

点击页头的 **发币（Launch）**，填好表单。整个发射只需从你的钱包发出一笔交易。

## 1. 链

选择币所在的链：BNB Chain、Base、Arbitrum、HyperEVM、Monad、X Layer、Elysium、Robinhood Chain、Arc 或 Solana。

## 2. 币的信息

| 字段 | |
|---|---|
| **名称** | 最多 32 字节（约 32 个拉丁字母或 10 个汉字） |
| **代号** | 最多 16 字节，不能有空格（Solana：最多 10 个字符） |
| **图片** | PNG、JPEG、WebP 或 GIF（GIF 需小于 1 MB）。会自动帮你调整尺寸。 |
| **简介** | 可选 |
| **链接** | 官网、X、Telegram（可选）。不填官网的话，币会链接到 niúbī.xyz。 |

图片和各项信息会作为币的元数据保存，并永久链接在代币合约上。

## 3. 交易对（BNB Chain）

默认情况下，币与该链的原生币（BNB、ETH……）配对。在 BNB Chain 上，你也可以改为与一个 **配对代币** 配对（four.meme、flap.sh 或锁仓
LP 代币、股票代币，或另一个 Awesome 币）。这样它的每笔交易也会销毁那个代币。详见[配对](pairings.md)。

## 4. 发射类型

选择每笔手续费中的创建者分成流向哪里。发射后永远无法更改。

| 类型 | 创建者分成 |
|---|---|
| **Dev Bag（开发者钱包）** | 由你领取 |
| **Flywheel（飞轮回购）** | 回购本币并销毁 |
| **Bull Run（牛市燃烧）** | 买入 $牛逼 并销毁（仅限原生币交易对） |
| **Holder Drip（持有人分红）** | 发给该币的持有人 |
| **Squad（团队分成）** | 按固定比例分给 2-5 个钱包 |

详情：[发射类型](launch-types.md)。

## 5. 交易手续费（Uniswap v4 链）

在 Base、Arbitrum、HyperEVM、Monad、X Layer、Elysium、Robinhood Chain 和 Arc 上，你可以为币选择交易手续费，范围 **0.25% 到
5%**，终身固定。费率越高，发射类型拿到的越多，交易者的成本也越高。BNB Chain 上的币统一为 1%。在 Solana 上，Raydium LaunchLab 的币可选
1% 到 5% 的费率档位。

## 6. 首笔买入（可选）

在发射交易里抢在所有人之前买入你自己的币。它按正常费率收费（不收防狙击费），上限为 **总量的 5%**。与锁仓 LP 代币配对的币必须有首笔买入。

## 7. 跨链支付（可选）

要发射的链上 gas 不够？**Pay from**（跨链支付）让你用 BNB、SOL 或其他链的币来付款；付款会自动跨链，发射也一并替你完成，币和首笔买入得到的代币都会打到你的钱包。

## 8. 发射

点击 **发币（Launch）**，在钱包里确认。交易一上链，币就上线了，页面、K 线和分享链接一应俱全。

## 发射之后

- 分享币的页面：`https://xn--nib-9na0w.xyz/v/<address>`（BNB Chain）或
  `https://xn--nib-9na0w.xyz/c/<chain>/<address>`。
- 创建者可以在 **我的（Profile）** 页面领取 Dev Bag 手续费。详见[领取](claiming.md)。
- 创建者身份可以转交给另一个钱包（两步：先发起转让，再由对方接受）。

## Solana

Solana 上的币在 **Pump.fun** 或 **Raydium LaunchLab** 上发射，与 SOL 配对，同样使用这五种发射类型。这些平台支付的创建者手续费会进入该币的手续费托管账户，由发射类型决定如何处理。
