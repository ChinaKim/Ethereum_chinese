以太坊个版本对应：

| Client |
| :--- |


|  | Language | Developers | Latest release |
| :--- | :--- | :--- | :--- |
| [go-ethereum](http://www.ethdocs.org/en/latest/ethereum-clients/go-ethereum/index.html#go-ethereum) | Go | [Ethereum Foundation](https://ethereum.org/foundation) | [go-ethereum-v1.4.18](https://github.com/ethereum/go-ethereum/releases/tag/v1.4.18) |
| [Parity](http://www.ethdocs.org/en/latest/ethereum-clients/parity/index.html#parity) | Rust | [Ethcore](https://ethcore.io/) | [Parity-v1.4.0](https://github.com/ethcore/parity/releases/tag/v1.4.0) |
| [cpp-ethereum](http://www.ethdocs.org/en/latest/ethereum-clients/cpp-ethereum/index.html#cpp-ethereum) | C++ | [Ethereum Foundation](https://ethereum.org/foundation) | [cpp-ethereum-v1.3.0](https://github.com/bobsummerwill/cpp-ethereum/releases/tag/v1.3.0) |
| [pyethapp](http://www.ethdocs.org/en/latest/ethereum-clients/pyethapp/index.html#pyethapp) | Python | [Ethereum Foundation](https://ethereum.org/foundation) | [pyethapp-v1.5.0](https://github.com/ethereum/pyethapp/releases/tag/v1.5.0) |
| [ethereumjs-lib](http://www.ethdocs.org/en/latest/ethereum-clients/ethereumjs-lib/index.html#ethereumjs-lib) | Javascript | [Ethereum Foundation](https://ethereum.org/foundation) | [ethereumjs-lib-v3.0.0](https://github.com/ethereumjs/ethereumjs-lib/releases/tag/v3.0.0) |
| [Ethereum\(J\)](http://www.ethdocs.org/en/latest/ethereum-clients/ethereumj/index.html#ethereum-j) | Java | [&lt;ether.camp&gt;](http://www.ether.camp/) | [ethereumJ-v1.3.1](https://github.com/ethereum/ethereumj/releases/tag/1.3.1) |
| [ruby-ethereum](http://www.ethdocs.org/en/latest/ethereum-clients/ruby-ethereum/index.html#ruby-ethereum) | Ruby | [Jan Xie](https://github.com/janx/) | [ruby-ethereum-v0.9.6](https://rubygems.org/gems/ruby-ethereum/versions/0.9.6) |
| [ethereumH](http://www.ethdocs.org/en/latest/ethereum-clients/ethereumh/index.html#ethereumh) | Haskell | [BlockApps](http://www.blockapps.net/) | no Homestead release yet |



## 我该如何安装？

大部分用户只需安装[Mist / Ethereum Wallet](https://github.com/ethereum/mist)。

Mist捆绑在[go-ethereum](http://www.ethdocs.org/en/latest/ethereum-clients/go-ethereum/index.html#go-ethereum) 和[cpp-ethereum](http://www.ethdocs.org/en/latest/ethereum-clients/cpp-ethereum/index.html#cpp-ethereum) 中，如果你运行的以太坊命令行客户端，当Mist启动时，它会使用绑定的客户端（默认geth）同步区块。如果你想用Parity使用Mist，或者在私有网络中运行Mist，只需在启动Mist之前先启动节点，这样Mist就会连接到你的节点，而不是仅仅启动它自己。

如果你是想挖矿，那么Mist是不够的，具体见[Mining](http://www.ethdocs.org/en/latest/mining.html#mining) 部分。









































