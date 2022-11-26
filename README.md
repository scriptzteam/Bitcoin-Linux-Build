# BitCoin-Linux-Build

```
apt install build-essential autoconf pkg-config libtool
git clone https://github.com/bitcoin/bitcoin.git
cd bitcoin
./autogen.sh
./configure CC=gcc-8 CXX=g++-8 --disable-hardening --without-gui --without-bdb --disable-wallet #this is ours, change as you want..
make
make install
```
