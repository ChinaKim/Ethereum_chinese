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

* EIP 8：改变了RLPxDiscovery协议和RLPxTCP传输协议，以确保运行在以太坊网络上的所有客户端软件能够应对未来网络协议的升级。旧的客户端无法更新网络协议，而且，如果hello包不符预期的话，会拒绝通信。这次更新意味着今后的客户端将能够接受不断增长的网络更新以及握手协议。

这些改变具有以下好处：

* EIP-2/1 消除那些过多的通过交易产生的合约，因为原来的交易成本为21000，而新的成本为32000.
* EIP-2/1 通过自杀退款修复协议bug，目前简单的以太传输仅需11664gas
* EIP-2/2 修复了交易的可延展性问题
* EIP-2/3 更多的以“成功/失败”来区分结果，而不是现在的“成功/失败/空合约”的三分法
* EIP-2/4 eliminates the excess incentive to set the timestamp difference to exactly 1 in order to create a block that has slightly higher difficulty and that will thus be guaranteed to beat out any possible forks. This guarantees to keep block time in the 10-20 range and according to simulations restores the target 15 second blocktime \(instead of the current effective 17s\).
* EIP-7 makes it much easier for a contract to store another address as a mutable source of code and ‘’pass through’’ calls to it, as the child code would execute in essentially the same environment \(except for reduced gas and increased callstack depth\) as the parent.
* EIP-8 确保所有运行在以太坊网络上的客户端能够应对将来的升级



