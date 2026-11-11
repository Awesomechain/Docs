# 领取

[English](../en/claiming.md) · **中文**

连接钱包后打开 **我的（Profile）**。这里会列出你发射的币和你可以领取的手续费；Squad（团队分成）或 Holder Drip（持有人分红）币的页面上也会显示你的份额。点击 **领取（Claim）**，然后在钱包里确认。

| 你的身份 | 可以领取 | 以什么支付 |
|---|---|---|
| **Dev Bag（开发者钱包）** 币的创建者 | 它的创建者分成 | 该币的计价代币（BNB、ETH……） |
| **Squad** 的成员 | 你的固定份额 | 计价代币 |
| **Holder Drip** 币的持有人 | 每个已发布轮次中你的份额 | 计价代币 |

说明：

- 领取永不过期，Holder Drip 的轮次除外：未领取的金额在 **90 天** 后退回该币的奖池，在之后的轮次中重新分配。
- 任何人（朋友、机器人、网站）都可以代为发起发放，但钱始终打到应得的钱包。
- Flywheel（飞轮回购）和 Bull Run（牛市燃烧）币没有可领取的东西：它们的创建者分成都用于销毁。
- 在 Solana 上，手续费由 Awesome 的发放机器人按发射类型从该币的托管账户中支付。

## 开发者

`GET /api/claims/<address>` 会返回所有可领取项，并附带可直接发送的交易。详见[开发者](developers.md)和
[SDK](https://github.com/Awesomechain/SDK)（`awesome.claims(address)`）。
