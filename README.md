MiningEnthusiastCoin Core Ver 1.0.0
=========

(Japanese HP)https://miningenthusiastcoin.com/
(English HP)https://miningenthusiastcoin.com/en/

### English

What is MiningEnthusiastCoin 1.0.0?
-------------

MiningEnthusiastCoin is a new blockchain based on VIPSTARCOIN and HTMLCOIN which uses Bitcoin Core and integrates Ethereum based smart contracts. It implements an extensible design which is capable of adding more VMs, enabled primarily through the Account Abstraction Layer, which allows for an account based virtual machine to function on a UTXO based blockchain. 

What is MiningEnthusiastCoin Core?
------------------

MiningEnthusiastCoin Core is our primary mainnet wallet. It implements a full node and is capable of storing, validating, and distributing all history of the MiningEnthusiastCoin network. MiningEnthusiastCoin Core is considered the reference implementation for the MiningEnthusiastCoin network. 

MiningEnthusiastCoin Core currently implements the following:

* Sending/Receiving MiningEnthusiastCoin
* Sending/Receiving MRC20 tokens on the MiningEnthusiastCoin network
* Staking and creating blocks for the MiningEnthusiastCoin network
* Creating and interacting with smart contracts
* Running a full node for distributing the blockchain to other users
* "Prune" mode, which minimizes disk usage
* Regtest mode, which enables developers to very quickly build their own private MiningEnthusiastCoin network for Dapp testing
* Compatibility with the Bitcoin Core set of RPC commands and APIs

Quickstart
----------
### Build on Ubuntu

    This is a quick start script for compiling MiningEnthusiastCoin on Ubuntu

    sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git cmake libboost-all-dev
    sudo apt-get install software-properties-common
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install libdb4.8-dev libdb4.8++-dev

    # If you want to build the Qt GUI:
    sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler

    git clone https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin --recursive
    cd MiningEnthusiastCoin

    # Note autogen will prompt to install some more dependencies if needed
    ./autogen.sh
    ./configure 
    make -j2

### Build on OSX

The commands in this guide should be executed in a Terminal application.
The built-in one is located in `/Applications/Utilities/Terminal.app`.

#### Preparation

Install the OS X command line tools:

`xcode-select --install`

When the popup appears, click `Install`.

Then install [Homebrew](https://brew.sh).

#### Dependencies

    brew install cmake automake berkeley-db4 libtool boost --c++11 --without-single --without-static miniupnpc openssl pkg-config protobuf qt5 libevent imagemagick --with-librsvg

NOTE: Building with Qt4 is still supported, however, could result in a broken UI. Building with Qt5 is recommended.

#### Build MiningEnthusiastCoin Core

1. Clone the MiningEnthusiastCoin source code and cd into `MiningEnthusiastCoin`

        git clone --recursive https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin
        cd MiningEnthusiastCoin

2.  Build MiningEnthusiastCoin Core:

    Configure and build the MiningEnthusiastCoin binaries as well as the GUI (if Qt is found).

    You can disable the GUI build by passing `--without-gui` to configure.

        ./autogen.sh
        ./configure
        make

3.  It is recommended to build and run the unit tests:

        make check

### Run

Then you can either run the command-line daemon using `src/miningenthusiastcoind` and `src/miningenthusiastcoin-cli`, or you can run the Qt GUI using `src/qt/miningenthusiastcoin-qt`

For in-depth description of Sparknet and how to use MiningEnthusiastCoin for interacting with contracts, please see [sparknet-guide](doc/sparknet-guide.md).

License
-------

MiningEnthusiastCoin is GPLv3 licensed.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin/tags) are created
regularly to indicate new official, stable release versions of MiningEnthusiastCoin.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).


### Japanese

MiningEnthusiastCoin 1.0.0とは?
-------------

MiningEnthusiastCoinはBitcoin CoreとEthereumがベースのスマートコントラクトを統合したVIPSTARCOIN及びHTMLCOINをベースとした新しいブロックチェーンです。これは主にアカウント匿名レイヤーを介して有効になっており、より多くのVMを追加できる拡張可能な設計を実装、アカウントベースの仮想マシンをUTXOベースのブロックチェーン上で機能させることができます。

MiningEnthusiastCoin Coreとは?
------------------

MiningEnthusiastCoin Coreは私たちが主に使うメインネットウォレットです。フルノードを実装し、MiningEnthusiastCoinネットワークのすべての取引履歴などを保存、検証、配布することが可能です。MiningEnthusiastCoin CoreはMiningEnthusiastCoinネットワークのリファレンス実装とみなされます。

MiningEnthusiastCoin Coreは以下を実装しています。

* MiningEnthusiastCoinの送受信
* MiningEnthusiastCoinネットワーク用のMRC20トークンの送受信
* MiningEnthusiastCoinネットワークでのコインのステークとブロックの作成
* スマートコントラクトの作成と利用
* ブロックチェーンを他のユーザーに配布するためのフルノードの実行
* ディスクの使用量を最小限に抑えるプルーンモード
* Regtestネットワーク、開発者はDappテスト用に独自の専用MiningEnthusiastCoinネットワークを非常に迅速に構築できます。
* RPCコマンドとAPIのBitcoin Coreセットとの互換性

クイックスタート
----------
### Ubuntuでビルドする

    MiningEnthusiastCoinをUbuntuでコンパイルするためのクイックスタートスクリプトです。

    sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git cmake libboost-all-dev -y
    sudo apt-get install software-properties-common
    sudo add-apt-repository ppa:bitcoin/bitcoin -y
    sudo apt-get update
    sudo apt-get install libdb4.8-dev libdb4.8++-dev -y

    #Qt GUIウォレットをビルドする場合:
    sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler -y

    git clone https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin --recursive
    cd MiningEnthusiastCoin

    #autogenは必要に応じていくつかの依存関係をインストールするように促します
    ./autogen.sh
    ./configure 
    make -j2

### OS Xでビルドする

このガイドのコマンドは、ターミナルアプリケーションで実行する必要があります。
以下の場所にあります。`/Applications/Utilities/Terminal.app`.

#### 準備

OS Xコマンドラインツールをインストールします。:

`xcode-select --install`

ポップアップが表示されたら、`Install`をクリックします。

次に、[Homebrew](https://brew.sh)をインストールします。

#### 依存関係

    brew install cmake automake berkeley-db4 libtool boost --c++11 --without-single --without-static miniupnpc openssl pkg-config protobuf qt5 libevent imagemagick --with-librsvg

注意：Qt4でのビルドはまだサポートされていますが、UIが壊れる可能性があります。Qt5でビルドすることをお勧めします。

#### MiningEnthusiastCoin Coreをビルドする

1. MiningEnthusiastCoinのソースコードをクローンし、`MiningEnthusiastCoin`を`cd`する

        git clone --recursive https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin
        cd MiningEnthusiastCoin

2. MiningEnthusiastCoin Coreをビルドする:

        MiningEnthusiastCoin CoreとGUI(Qtが見つかった場合)をビルドします。

        configureで`--without-gui`オプションを付け足すことで、GUIビルドを無効にすることができます。

        ./autogen.sh
        ./configure
        make

3. ユニットテストをビルドして実行することをお勧めします。:

        make check

### 実行

`src/miningenthusiastcoind`を実行し、`src/miningenthusiastcoin-cli`を使用することでcoindをコントロールできます。また、Qt GUIウォレットを使う場合は`src/qt/miningenthusiastcoin-qt`を実行してください。

Sparknetの詳細な説明とMiningEnthusiastCoinを使ってスマートコントラクトを使用する方法については、[sparknet-guide](doc/sparknet-guide.md)を見てください。

ライセンス
-------

MiningEnthusiastCoinはGPLv3ライセンスです。

開発プロセス
-------------------

`master`ブランチは定期的に構築され、テストされていますが、完全に安全であることは保証されていません。 [タグ](https://github.com/MiningEnthusiastCoin-Project/MiningEnthusiastCoin/tags)はMiningEnthusiastCoinの正式版、安全版を示すために定期的に作成されます。.

貢献ワークフローは[CONTRIBUTING.md](CONTRIBUTING.md)で説明しています。
