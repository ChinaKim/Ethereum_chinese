什么是以太币（ether）？

以太币是以太坊所使用的货币。它是用来购买EVM的计算力的。它通过购买gas来间接使用。

以太币有自己的度量系统。每个面额单位有自己的名字。最小面额（以太币的基准单位）称作Wei。下面是以太币的面额之间关系：

| Unit |
| :--- |


|  | Wei Value | Wei |
| :--- | :--- | :--- |
| **wei** | 1 wei | 1 |
| **Kwei \(babbage\)** | 1e3 wei | 1,000 |
| **Mwei \(lovelace\)** | 1e6 wei | 1,000,000 |
| **Gwei \(shannon\)** | 1e9 wei | 1,000,000,000 |
| **microether \(szabo\)** | 1e12 wei | 1,000,000,000,000 |
| **milliether \(finney\)** | 1e15 wei | 1,000,000,000,000,000 |
| **ether** | 1e18 wei | 1,000,000,000,000,000,000 |

##### 获取以太币

想要获取以太币，你需要按如下去做：

* 成为以太坊矿工
* 使用集中或无信任服务与交换货币
* 按[http://shapeshift.io/](http://shapeshift.io/) 中API指示，使用[Mist Ethereum GUI Wallet](https://github.com/ethereum/mist/releases) 购买以太币

##### 无需信任服务（Trustless services）

以太坊平台是一个特殊的无须信任服务的智能合约。所谓无需信任服务，指的是在货币交易中不需要第三方信任担保。

这样的项目有：

[BTCrelay](http://btcrelay.org/)

* * [More information](https://medium.com/@ConsenSys/taking-stock-bitcoin-and-ethereum-4382f0a2f17)
    \(about ETH/BTC 2-way peg without modifying bitcoin code\).
  * [BTCrelay audit](http://martin.swende.se/blog/BTCRelay-Auditing.html)
* [EtherEx decentralised exchange](https://etherex.org/).

集中交易市场列表：

| Exchange |
| :--- |


|  | Currencies |
| :--- | :--- |
| Poloniex | BTC |
| Kraken | BTC, USD, EUR, CAD, GBP |
| Gatecoin | BTC, EUR |
| Bitfinex | BTC, USD |
| Bittrex | BTC |
| Bluetrade | BTC, LTC, DOGE |
| HitBTC | BTC |
| Livecoin | BTC |
| Coinsquare | BTC |
| Bittylicious | GBP |
| BTER | CNY |
| Yunbi | CNY |
| Metaexchange | BTC |

固定利率交易所：

| Exchange |
| :--- |


|  | Currencies |
| :--- | :--- |
| [Shapeshift](http://www.ethdocs.org/en/latest/shapeshift.io) | BTC, LTC, DOGE, Other |
| [Bity](https://bity.com/) | BTC, USD, EUR, CHF |

##### 交易与价格分析

[ETH markets exhaustive listing by volume on coinmarketcap](https://coinmarketcap.com/currencies/ethereum/#markets)

* Aggregating realtime stats of major ETH markets:
  * [Tradeblock](https://tradeblock.com/ethereum)
  * [EthereumWisdom](http://ethereumwisdom.com/)
  * [Cryptocompare](https://www.cryptocompare.com/coins/eth/overview)
  * [Coinmarketcap](https://coinmarketcap.com/currencies/ethereum/)

## Online wallets, paper wallets, and cold storage

下面是生态系统的连接结合：

Mist Ethereum Wallet

* * [Releases to download](https://github.com/ethereum/mist/releases)
  * [Mist Ethereum Wallet developer preview](https://blog.ethereum.org/2015/09/16/ethereum-wallet-developer-preview/)
    * foundation blog post
  * [How to easily set up the Ethereum Mist wallet!](https://www.youtube.com/watch?v=Z6lE0Ctaeqs)
    * Tutorial by Tommy Economics
* Kryptokit Jaxx
  * [Jaxx main site](http://jaxx.io/)
  * [Mobile release](http://favs.pw/first-ethereum-mobile-app-released/#.VsHn_PGPL5c)
* Etherwall
  * [Etherwall website](http://www.etherwall.com/)
  * [Etherwall source](https://github.com/almindor/etherwall)
* MyEtherWallet
  * [MyEtherWallet website](https://www.myetherwallet.com/)
  * [MyEtherWallet source](https://github.com/kvhnuke/etherwallet/)
  * [Chrome extension](http://sebfor.com/myetherwallet-chrome-extension-release/)
* Cold storage
  * [Icebox](https://github.com/ConsenSys/icebox)
    by
    [ConsenSys](https://consensys.net/)
    * Cold storage based on lightwallet with HD wallet library integrated.
  * [Reddit discussion 1](https://www.reddit.com/r/ethereum/comments/45uvmy/offline_cold_storage_question/offline_cold_storage_question)
  * [How to setup a cold storage wallet](https://www.reddit.com/r/ethereum/comments/48wfbv/eli5_how_to_setup_a_cold_storage_wallet_as/)
* Hardware wallet
  * [reddit discussion 2](https://www.reddit.com/r/ethereum/comments/45siaq/hardware_wallet/)
  * [reddit discussion 3](https://www.reddit.com/r/ethereum/comments/4521o4/crowdfunding_ethereum_hardware_cold_storage_wallet/)
* Brain wallet
  * brain wallets are not safe, do not use them.
    [https://www.reddit.com/r/ethereum/comments/45y8m7/brain\_wallets\_are\_now\_generally\_shunned\_by/](https://www.reddit.com/r/ethereum/comments/45y8m7/brain_wallets_are_now_generally_shunned_by/)
  * Extreme caution with brain wallets. Read the recent controversy:
    [https://reddit.com/r/ethereum/comments/43fhb5/brainwallets](https://reddit.com/r/ethereum/comments/43fhb5/brainwallets)
    vs
    [http://blog.ether.camp/post/138376049438/why-brain-wallet-is-the-best](http://blog.ether.camp/post/138376049438/why-brain-wallet-is-the-best)
* Misc
  * [Kraken Wallet Sweeper Tool](https://www.kraken.com/ether)
    * Pre-sale wallet import
  * [Recommended ways to safely store ether](http://ethereum.stackexchange.com/questions/1239/what-is-the-recommended-way-to-safely-store-ether)
  * [How to buy and store ether](http://sebfor.com/how-to-buy-and-store-ether/)
  * [A laymen’s intro into brute forcing and why not to use brain wallets](http://www.fastcompany.com/3056651/researchers-find-a-crack-that-drains-supposedly-secure-bitcoin-wallets)
  * [Pyethsaletool](https://github.com/ethereum/pyethsaletool/blob/master/README.md)
  * [Account vs wallet](https://www.reddit.com/r/ethereum/comments/47j3r5/eli5_accounts_vs_wallet_contracts_on_mist/)

##### 发送以太币

以太坊钱包支持通过图形界面来发送以太币。

以太币同样可以通过geth控制台来交易。

```
> var sender = eth.accounts[0];
> var receiver = eth.accounts[1];
> var amount = web3.toWei(0.01, "ether")
> eth.sendTransaction({from:sender, to:receiver, value: amount})
```

更多以太币交易信息，请看：[Account Types, Gas, and Transactions](http://www.ethdocs.org/en/latest/contracts-and-transactions/account-types-gas-and-transactions.html#account-types-gas-and-transactions)

在加密货币领域，以太坊是独一无二的，而以太币则是其货币价值的体现，我们通常称作‘gas’。除了交易费用，gas也是每个网络请求的核心部分，发送者需要为计算力的消耗支付费用。gas的花费是动态计算的。基于请求的体积和复杂度乘以当前gas的价格。Its value as a cryptofuel has the effect of increasing the stability and long-term demand for ether and Ethereum as a whole. For more information, see[Account Types, Gas, and Transactions](http://www.ethdocs.org/en/latest/contracts-and-transactions/account-types-gas-and-transactions.html#account-types-gas-and-transactions)

## Gas and ether

gas可以看做是网络资源的固定成本。你希望发送交易的真实成本总是相同的，所以你不希望Gas被调整，但货币通常是波动的。

所以，取而代之的是，我们发行了ether，它的价值是变化的。如果ether的价格上涨，已ether为单位的Gas价格会下降，保证gas的真是成本一致。

与Gas相关的术语有多个：Gas Price、Gas Cost、Gas Limit和Gas Fees。Gas背后的原则是保证在以太网上的交易或计算成本是稳定的。

* Gas Cost：计算成本的一个静态值。本意上Gas的真实价值应该永远不变，所以该值也是不变的。
* Gas Price：依据其他货币如Ether计算出来的Gas成本。如果其他货币有波动，为了保持gas价值的稳定，Gas Price也会上下浮动。Gas Price由多少用户打算花费以及进程节点能接受多少来平衡得出价格。
* Gas Limit：每个节点上能使用的最大Gas量，这取决于计算负载，交易体积，区块大小。随着时间推移，矿工可以慢慢改变该值。
* Gas Fee：运行特定交易或程序（也称合约）所需Gas的有效数量。某个区块的Gas Fee通常取决于计算载荷，交易体积和区块大小。gas fee是支付给矿工的。



