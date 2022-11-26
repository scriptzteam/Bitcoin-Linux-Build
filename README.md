# BitCoin-Linux-Build

```
apt install build-essential autoconf pkg-config libtool libboost-dev libevent-dev
git clone https://github.com/bitcoin/bitcoin.git
cd bitcoin
./autogen.sh
./configure --disable-hardening --without-gui --without-bdb --disable-wallet #this is ours, change as you want..
make
make install
```
