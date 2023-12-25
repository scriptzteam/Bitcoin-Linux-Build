# Bitcoin-Linux-Build

```
add-apt-repository --update -y ppa:ubuntu-toolchain-r/test
apt update
apt install build-essential autoconf bsdmainutils pkg-config libtool libboost-dev libevent-dev gcc-11 g++-11 g++ autotools-dev libicu-dev libbz2-dev libboost-all-dev
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-11 11
update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-11 11
git clone https://github.com/bitcoin/bitcoin.git
cd bitcoin
./autogen.sh
./configure --disable-hardening --without-gui --without-bdb --disable-wallet #this is ours, change as you want..
make clean
make
make install
```
