# xmrig-classic
XMRig is high performance Monero (XMR) CPU miner, with the official full Windows support.
Based on cpuminer-multi with heavy optimizations/rewrites and removing a lot of legacy code.

#### Table of contents
* [Features](#features)
* [Download](#download)
* [Usage](#usage)
* [Build](#build)
* [Common Issues](#common-issues)
* [Donations](#donations)
* [Contacts](#contacts)

## Features
* CryptoNight support for MONERO v8 / Variant 2
* CryptoNight-Lite support for AEON v7 / Variant 1
* It's open source software.

## Download
* Binary releases: https://github.com/myaeon-ru/xmrig-classic/releases
* Git tree: https://github.com/myaeon-ru/xmrig-classic.git
  * Clone with `git clone https://github.com/myaeon-ru/xmrig-classic.git`

## Usage
### Basic example
```
xmrig.exe -o pool.myaeon.ru:3333 -u YOUR_WALLET -p x -k
```
## Build
### Ubuntu (Debian-based distros)
```
sudo apt-get install git build-essential cmake libcurl4-openssl-dev
git clone https://github.com/myaeon-ru/xmrig-classic.git
cd xmrig
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
```
### Optional features
`-DWITH_LIBCPUID=OFF` Disable libcpuid. Auto configuration of CPU after this will be very limited.
`-DWITH_AEON=OFF` Disable CryptoNight-Lite support.

## Common Issues
### HUGE PAGES unavailable
* Run XMRig as Administrator.
* Since version 0.8.0 XMRig automatically enable SeLockMemoryPrivilege for current user, but reboot or sign out still required. [Manual instruction](https://msdn.microsoft.com/en-gb/library/ms190730.aspx).

### Maximum performance checklist
* Idle operating system.
* Do not exceed optimal thread count.
* Use modern CPUs with AES-NI instructuon set.
* Try setup optimal cpu affinity.
* Enable fast memory (Large/Huge pages).

## Donations
* XMR:  `43QVF2gN8kAFwTCDzJNRiU3eMp769x8G5FvRgqsmnznVPXsmCEUVb1kX6v77Zggbh7ACxTx9swiTbPXY2kDxATKDVGGa1NB`
* AEON: `Wmu1v35Bq9zFtSssT3GWjm7Wxpd2dvk7TWgqPPZi9y92hRv3GTKrJLU4oVgPjrjKCbKEShp1HDFmjCcEDT6ykRzt1vVZCCB1G`

## Contacts
* myaeon@ya.com

