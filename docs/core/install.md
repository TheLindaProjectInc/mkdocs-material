## Setup

You can download a pre-built version of Metrix from our Github Release page:

[Releases](https://github.com/TheLindaProjectInc/Metrix/releases/)

Simply extract the .tar.gz linux-64bit archive. In the "bin" directory will be the two programs of interest, `metrixd` and `metrix-cli`

If you choose to compile it yourself instead, follow these steps on Ubuntu:

Install packages if needed:

```
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git cmake libboost-all-dev libgmp3-dev
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev

git clone https://github.com/TheLindaProjectInc/metrix --recursive
cd metrix

# Note autogen will prompt to install some more dependencies if needed
./autogen.sh
./configure 
make -j2
```

Afterwards, in the "src" directory, there will be two programs of interest, `metrixd` and `metrix-cli`.


Build instruction for other OS variations can be found in the main [Github](https://github.com/TheLindaProjectInc/Metrix/tree/master/doc)
