# DGPv2 Migration

## About the DGPv2 migration
The DGPv2 migration is the mandatory process which all DGPv1 governors must perform to retrieve their collateral and enroll in the DGPv2 contracts. The reason for this migration is to fix bugs found within the DGPv1 contracts, unfortunately on the MainNet, causing a subsidy distribution error before the bug could be temporarily patched in [Metrix Core v4.0.9.1](https://github.com/TheLindaProjectInc/Metrix/releases/tag/4.0.9.1) fixing the subsidy error caused by the bug.

[Metrix Core v4.1.0.0](https://github.com/TheLindaProjectInc/Metrix/releases/tag/4.1.0.0) introduces MIP3, which will activate once miners have signaled they have updated to the new version, approving the upgrade to DGPv2. Once MIP3 is active this will signal to miners that DGPv2 should be used instead of DGPv1. DGPv1 will no longer be used to process block rewards or provide blockchain parameters to the miners, however can still process contract calls, like to unenroll. 

DGPv2 on top of solving bugs in the DGP contracts, allows for greater functionality in terms of what types accounts can participate as governors. Smart contracts can now participate as governors, that allow the potential for things like delegated governors and more, which were not a possibility in the DGPv1 contracts.

### Issues solved in DGPv2
- Use new Solidity compiler allowing any bugfixes and optimizations benefits
- Allow both externally owned accounts and smart contracts to enroll as a governor
- Convert `transfer` methods to `call` to allow gas forwarding
- Fallback for failed governor subsidy reward (burn)
- Fallback for failed governor collateral return (sent to Budget contract where governors can handle the failure via proposal)
- Fallback for failed budget settlement (burn)
- Check if lastreward > 0 also when checking governor winner


## Migrating to DGPv2 via CLI or Debug Console

Migrating from DGPv1 to DGPv2 requires 2 steps:
- Unenroll from DGPv1
- Enroll in DGPv2

This can be done using the `sendtocontract` method using metrix-cli or from the debug console in the Altitude or QT MetrixCoin wallets

### Unenroll from DGPv1

First we will call `unenroll(bool)` on the DGPv1 contract using false as the parameter, by abi encoding the data we will get `fba713970000000000000000000000000000000000000000000000000000000000000000`. 

This transaction doesn't need to send any MRX so we use 0 for the value.

We should be able to use the minimum gas limit 250000 and gas price 0.00005. 

The governor needs to sign the transaction, so replace `<GOVERNOR ADDRESS>` with our governor's address. 

We will use true for both broadcast and return change to sender.

```
sendtocontract "0000000000000000000000000000000000000089" "fba713970000000000000000000000000000000000000000000000000000000000000000" 0 250000 0.00005 <GOVERNOR ADDRESS> true true
```


### Enroll in DGPv2

Next we will call `enroll()` on the DGPv2 contract which takes no parameters, by abi encoding the data we will get `e65f2a7e`.

This transaction needs to send a value of 7500000 MRX as collateral.

We should be able to use the minimum gas limit 250000 and gas price 0.00005.

The governor needs to sign the transaction, so replace `<GOVERNOR ADDRESS>` with our governor's address. 

We will use true for both broadcast and return change to sender.
```
sendtocontract "42d98057e271b08a20c0959665e9499a3c00e371" "e65f2a7e" 7500000 250000 0.00005 <GOVERNOR ADDRESS> true true
```


## FAQ
### Why is the migration manual?

Due to the nature of the bug found in the DGPv1 contracts, DGPv1 governors can never be unenrolled automatically. DGPv1 governors can be unenrolled at any time by calling the contracts.

### Will I need to wait for my governor to mature again?

**Yes!** Enrolling in the DGPv2 contracts will require all new governors to wait for 1920 blocks (~48 hours) to receive governor rewards and 26880 blocks (~28 days) to be eligible to vote on budget proposals or DGP blockchain parameter updates.


### What happens to any DGPv1 proposals?

Any DGPv1 proposals that have not passed or been completed will need to be re-created in the DGPv2 contracts. 








