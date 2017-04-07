Homestead是以太坊平台的主要版本，也是第一个发布版。它包含了几个协议的更改、提供了进一步网络升级的功能。以太坊的第一个版本叫Frontier，是供开发者学习研究之用的beta版。

## 以太坊发展里程碑：

预发布 Step 0：Olympic testnet--2015年5月

发布 Step One：Frontier --2015年7月30

发布 Step Two：Homestead --2016年3月14

发布 Step Three：Metropolis --TBA

发布 Step Four: Serenity - TBA

Homestead标志着由测试版进入了稳定版本。Homestead引入了1150000个区块。一旦以太坊的区块链达到了1150000个，以太坊将进行硬分叉（hard fork）来实现一些重大的改变，如下节所述。

## Homestead硬分叉

狭义上理解，以太坊是一套协议。Homestead带有一些不向后兼容协议变化，因此需要一个硬分叉。这些变化包括如下所述：

* EIP 2：

  * 通过交易创建合约的成本从21000到53000.使用CREATE操作码从合约中创建的不受影响。
  * 交易签名中的s值（s-value）大于secp256k1n/2现在被认为不合法了。
  * 合约创建时如果没有足够的gas支付状态改变的费用，创建将失败，而不是创建一个空的合约。
  * 改变难度，调整算法。

* EIP 7：DELEGATECALL：在0xf4上添加新的操作码DELEGATECALL，新操作码同CALLCODE相似，除了它将发送者和值传播范围由父范围到子范围。该调用和原来的调用有相同的发送者和值。这意味着合约能够存储通行信息，同时遵循它的父合约的msg.sender和msg.value。Great for contracts which create contracts but don’t repeat additional information which saves gas



