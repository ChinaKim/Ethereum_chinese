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

##### 使用Mist 以太坊钱包

不喜欢命令行的人，现在有了GUI界面来操作账户了，这个软件就是Mist以太坊钱包。Mist Ethereum wallet 脱胎于Mist项目。在以太坊基金的支持下发展起来。

注意：Mist钱包目前还是beta版，请谨慎使用。

使用GUI Mist Ethereum wallet创建一个账户在简单不过了。事实上，当你第一次安装这个应用的时候，第一个账户就已经创建好了。

1.下载应用。打开应用将自动同步一份你本机电脑上以太坊区块链副本。  [Download the latest version of the wallet app](https://github.com/ethereum/mist/releases)

2.解压并运行Ethereum-Wallet文件。

3.等待区块链同步完成，按指示操作，这样第一个账户就创建完成。

4.第一次登陆Mist Ethereum 钱包，你会看到安装时创建的账户，默认名称为MAIN ACCOUNT（ETHERBASE）

5.点击ADD ACCOUNT 创建其他账户。

#### 在Mist中创建多重签名的钱包

Mist 以太坊钱包可以使用多重签名来保护你钱包的余额。所谓的多重签名指的是：当从你的账户余额中撤回大额数目时，需要多个账户的授权。在创建多重签名的钱包之前，你需要创建多个账户。

Mist中创建账户很简单。在“Account”一栏，点击“Add Account”，输入密码，确认输入，OK！请创建至少两个账户。第二个账户最好在其他电脑上运行的Mist中创建（理论上来讲，这样更安全）。你仅需要知道你第二个账户的公钥。你的私有账户需要创建多重签名钱包合约，所以它必须和你要生成的多重签名钱包在同一个计算机上。

账户安装设置好后，记得备份（如果不备份的话，一旦计算机崩溃，你的额余额将全部丢失）。点击顶部菜单的“Backup”，选择‘keystore’文件夹，反向点击/选中‘copy’。导航到桌面，点击空白区域选‘paste’。将‘keystore’文件压缩成zip或rar文件，复制到U盘或CD/DVD中，或者上传到云盘保存！

现在你可以添加大约不少于0.0.2个ETH到你的私有账户（启动创建多重签名钱包的那个账户）。这是当您创建多重签名钱包所需的交易费。同样需要额外的1个（或更多）ETH，因为Mist需要这些ETH确保钱包合约交易有足够的gas去执行。所以至少需要1.02个ETH。

当创建一个多重签名钱包时，你需要输入所有与之关联账户的完整地址。建议复制每条地址到一个文本文件中去。每次进入到Mist账户的详情页，在右边栏点击‘copy address’。绝不要手动操作地址，否则很容易出错，那么你的账户余额就有危险了。

准备好创建一个多重签名的钱包吧！在‘Wallet Contracts’一栏下，选择‘Add Wallet Contract’。输入名称，选择私有账户，然后选择‘Multisignature Wallet Contract’。你将会看到如下提示：

“这是一个由X控制的共有账户。你可以每天发送以太\(ether\)到X。超过当日限额的任何交易需要得到X的确认”

Set whatever amount of owners \(accounts\) you are attaching to this multisig wallet, whatever you want for a daily withdrawal limit \(that only requires one account to withdrawal that amount\), and how many owners \(accounts\) are required to approve any withdrawal amount over the daily limit

现在添加先前您复制到文本文档中的账户地址，确认您所有的设置是否正确，点击底部‘create’。然后输入密码，发送交易。之后，在‘Wallet Contracts’部分，显示“creating”。

钱包创建完成后，在屏幕上能看到你的合约地址。选中地址，复制/粘贴到新建文本，命名为Ethereum-Wallet-Address.txt\(或其他名称\),然后保存并将该文本备份。

If you are restoring from backup, simply copy the files inside the ‘Ethereum-keystore-backup’ folder over into the ‘keystore’ folder mentioned in the first section of this walkthrough. FYI, you may need to create the ‘keystore’ folder if it’s a brand new install of Mist on a machine it was never installed on before \(the first time you create an account is when this folder is created\). As for restoring a multisig wallet, instead of choosing ‘Multisignature Wallet Contract’ like we did before when creating it, we merely choose ‘Import Wallet’ instead.

故障排除：

* Mist无法同步。确保你的电脑与NTP服务时间准确，然后重启。
* 同步后，Mist启动了，但是白屏。可能你正在基于Linux的系统上运行视频驱动程序‘xorg’。尝试替代安装制造商的视频驱动程序。
* ‘密码错误’提示。这是当前Mist版本上的一个错误提示。重启Mist问题会得到解决（前提是你输入的密码正确）。

##### 使用Eth







































