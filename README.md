# Bitcoin-Linux-Build

```
add-apt-repository --update -y ppa:ubuntu-toolchain-r/test
apt update
apt install build-essential autoconf bsdmainutils pkg-config libtool libboost-dev libevent-dev gcc-11 g++-11 g++ autotools-dev libicu-dev libbz2-dev libboost-all-dev
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-11 11
update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-11 11
git clone https://github.com/bitcoin/bitcoin.git
cd bitcoin
cmake -B build -DENABLE_WALLET=OFF
cmake --build build --target bitcoind bitcoin-cli
cd ~/bitcoin/build/bin
./bitcoind -version
./bitcoin-cli -version
cp --preserve=mode,ownership,timestamps ~/bitcoin/build/bin/bitcoind "$(which bitcoind)"
cp --preserve=mode,ownership,timestamps ~/bitcoin/build/bin/bitcoin-cli "$(which bitcoin-cli)"
```
