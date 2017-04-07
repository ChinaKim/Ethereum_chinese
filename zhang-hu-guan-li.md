以太坊中，账户扮演了核心角色。账户有两种类型：EOA和合约账户。这里我们集中讨论EOA。

账户中包含被称作状态对象（）的实体。这些实体拥有的状态是：EOA拥有余额，合约账户拥有余额和合约存储。所有账户拥有的状态是以太坊网络状态。

如果我们限制以太坊只允许外部拥有账户，只允许他们之间交易，我们将得到一个“altcoin”系统，该系统比比特币功能更弱，只能交易以太（ether）。

账户代表了外部代理的身份（人类，挖矿节点，自动代理）。账户使用公钥密码为交易签名，这样EVM能够安全地验证交易发送者的身份。

## keyfiles

每个账户由一对秘钥定义，公钥和私钥。账户的索引即它们的地址\(address\)，该地址由公钥的后20个字节衍生而来。私钥/地址组成对，编码成一个keyfile文件。keyfile是JSON格式字符串。keyfile的重要部分--私钥，总是加密的。它由你创建账户时输入的密码加密。keyfile可以在你的以太坊节点数据目录下的keystore目录找到。请确保经常备份keyfile。详见：[Backup and restore accounts](http://www.ethdocs.org/en/latest/account-management.html#backup-and-restore-accounts)

创建一个秘钥等于创建一个账户：

* 不要告诉任何人
* 无需同步区块链
* 无需运行客户端
* 甚至无需连接网络

当然你的新账户不会有任何以太\(Ether\)。但它仅属于你，没有你的账户和密码，任何人都不能访问。

在以太坊节点上转移整个目录或单个keyfile是安全的。

注意：

一旦你从其他节点添加了keyfile到你的节点，账户的顺序会改变。所以确保在您的脚本或代码中没有依赖或改变索引。

## 创建账户

注意：记住你的密码和ref：\`**backup your keyfiles&lt;backup-and-restore-accounts&gt;**\`.从账户中发送交易，你必须同时拥有keyfile和密码。确保备份了keyfile并牢记密码。一旦丢失keyfile或忘记密码，你就完了。

##### 使用geth accout new

如果你安装了geth客户端，创建账户仅仅需要在terminal中输入一行命令：geth account new 

注意你无需使用geth account 命令来运行geth客户端或同步区块。

对于非交互式的使用方式，需要提供密码文件的文本作为参数--password的值，

```
$ geth --password /path/to/password account new
```

显示所有账户：

```
$ geth account list
```

账户的显示按创建时间排列。

##### 使用geth console

为了用geth创建新的账户，我们需要首先连接geth到console模式（通过geth attach连接console到一个已经运行的实例上）



















