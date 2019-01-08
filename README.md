ZNode Core (fork of PIVX) integration/staging repository
======================================


### Coin Specs
|   |  |
| --- | ---:|
| Coin Name                   | ZNODE           |
| Ticker                      | ZNDE            |
| Block Time                  | 60 Seconds      |
| Max Coin Supply (PoS Phase) | 48,750,000      |
| Premine                     | 250,000 ZNDE    |
| Max Supply                  | 49,000,000 ZNDE |
| MN Collateral	              | 2,500 ZNDE      |

### additional specs:
|   |  |
| --- | ---:|
| Premine/instamine phase (blocks 2-1,000)| ZNDE |
| Stake Min Age | 60 minutes |
| Maturity | 20 blocks |


### Reward Distribution

| **Block Height**      | **Block Reward** | **Masternode**  | **PoS**   |
|----------------------:|-----------------|-----------------|-----------|
| 1,001-5,000           | **15.5** ZNDE  | **90 %**        | **10 %**  |
| 5,001-7,000           | **3.4** ZNDE   | **90 %**        | **10 %**  |
| 7,001-10,000          | **5.7** ZNDE   | **90 %**        | **10 %**  |
| 10,001-20,000         | **6.2** ZNDE   | **90 %**        | **10 %**  |
| 20,001-30,000         | **6.8** ZNDE   | **71 %**        | **29 %**  |
| 30,001-50,000         | **6.3** ZNDE   | **72 %**        | **28 %**  |
| 50,001-60,000         | **5.7** ZNDE   | **73 %**        | **27 %**  |
| 60,001-70,000         | **5.3** ZNDE   | **74 %**        | **26 %**  |
| 70,001-80,000         | **5** ZNDE     | **75 %**        | **25 %**  |
| 80,001-90,000         | **4** ZNDE     | **76 %**        | **24 %**  |
| 90,001-100,000        | **4.5** ZNDE   | **77 %**        | **23 %**  |
| 100,001-110,000       | **4** ZNDE     | **78 %**        | **22 %**  |
| 110,001-120,000       | **5** ZNDE     | **79 %**        | **21 %**  |
| 120,001-130,000       | **5.5** ZNDE   | **80 %**        | **20 %**  |
| 130,001-140,000       | **6** ZNDE     | **81 %**        | **19 %**  |
| 140,001-150,000       | **6.5** ZNDE   | **82 %**        | **18 %**  |
| 150,001-160,000       | **7** ZNDE     | **83 %**        | **17 %**  |
| 160,001-170,000       | **7.5** ZNDE   | **84 %**        | **16 %**  |
| 170,001-180,000       | **8** ZNDE     | **85 %**        | **15 %**  |
| 180,001-190,000       | **8.5** ZNDE   | **86 %**        | **14 %**  |
| 190,001-200,000       | **9** ZNDE     | **87 %**        | **13 %**  |
| 200,001-210,000       | **9.5** ZNDE   | **88 %**        | **12 %**  |
| 210,001-220,000       | **9** ZNDE     | **89 %**        | **11 %**  |
| 220,001-230,000       | **8** ZNDE     | **90 %**        | **10 %**  |
| 230,001-240,000       | **7** ZNDE     | **90 %**        | **10 %**  |
| 250,001>              | **5** ZNDE     | **90 %**        | **10 %**  |


It is recommended [use the shell script](https://github.com/ZNodes/ZNodes/releases) to install a ZNode Masternode on a Linux server running Ubuntu 14.04, 16.04, 18.04

***

Quick installation of the ZNode daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/ZNodes/ZNode.git
    cd ZNode
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip ZNDEd
    sudo strip ZNDE-cli
    sudo strip ZNDE-tx
    cd ..

Running the daemon:

    ZNDECoind

Stopping the daemon:

    ZNDECoin-cli stop

Demon status:

    ZNDECoin-cli getinfo
    ZNDECoin-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/Znodes/ZNode/releases

P2P port: 27505, RPC port: 27506
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.

