## Startup & First Launch

In order to startup metrixd, use the following:

```
./metrixd -daemon
```
Additional options can be specified in ~/.metrixcoin/metrix.conf, you can add `-staking=false` to the commandline or `-staking=0` in the metrix.conf file to disable staking. This may be required if you plan on using this wallet as a service.

Afterwards, you can check the status of the Metrix node:

```
./metrix-cli getblockchaininfo
```
It will show a block count. when the block count matches the latest block on our block explorer: https://explorer.metrixcoin.com that means that the node is synchronized. If it shows 0 blocks and 0 connections for more than a few minutes, contact Metrix staff for help. Syncing the blockchain will take around 10-30 minutes depending on connection speed

In order to shut down the node, simply use:
```
./metrix-cli stop
```
!!! warning
    NOTE: `-staking=false` disables automatic staking in the wallet. This is **HIGHLY RECOMMENDED** for exchanges or wallet services that rely on availability of the coins. Staking can make an unpredictable amount of coins unaccessible for 960 blocks (~24 hours) and so it is recommended that exchanges and wallets that provide a service do not participate in staking.
