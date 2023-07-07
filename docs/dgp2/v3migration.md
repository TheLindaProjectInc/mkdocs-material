# DGPv3 Migration

## About the DGPv3 migration
The DGPv3 migration is the mandatory process which all DGPv1 or v2 governors must perform to retrieve their collateral and enroll in the DGPv3 contracts. The reason for this migration is to fix bugs found within the DGPv1 & DGPv2 contracts. Unfortunately this bug was discovered on the MainNet, causing EVM transactions to be delayed significantly and the mempool to fill up.

[Metrix Core v4.2.0.0](https://github.com/TheLindaProjectInc/Metrix/releases/tag/4.2.0.0) introduces [MIP5](https://github.com/TheLindaProjectInc/MIPs/blob/main/mip-5.md), which will activate once miners have signaled they have updated to the new version, approving the upgrade to DGPv3. Once MIP5 is active this will signal to the network that DGPv3 should be used instead of DGPv2. DGPv2 will no longer be used to process block rewards or provide blockchain parameters of the network, however can still process contract calls, like to unenroll. 

---


# Migrating to DGPv3
Migrating from DGPv2 to DGPv3 requires 2 steps:
- Unenroll from DGPv2
- Enroll in DGPv3

## MSW

### Unenroll from v2

Use the v2 unenrollment button present in the application. This will only show up if your blockchain is in sync and you have a governer registered on the old contract.

### Enroll in v3

This can only be done once MIP5 is active and the activation block has passed. Attempting to enroll earier via the GUI will result in re-enrolling into DGPv2. For this reason the enrollment button will be disabled until DGPv3 is active on the network.

---

## Altitude

### Unenroll from v2

Use the v2 unenrollment button present in the application. This will only show up if your blockchain is in sync and you have a governer registered on the old contract.

### Enroll in v3

This can only be done once MIP5 is active and the activation block has passed. Attempting to enroll earier via the GUI will result in re-enrolling into DGPv2. For this reason the enrollment button will be disabled until DGPv3 is active on the network.

---

## Migrating to DGPv3 via CLI or Debug Console

Migrating from DGPv2 to DGPv3 requires 2 steps:
- Unenroll from DGPv2
- Enroll in DGPv3

This can be done using the `sendtocontract` method using metrix-cli or from the debug console in the Altitude or QT MetrixCoin wallets

#### Unenroll from DGPv2

First we will call `unenroll(bool)` on the DGPv1 contract using false as the parameter, by abi encoding the data we will get `fba713970000000000000000000000000000000000000000000000000000000000000000`. 

This transaction doesn't need to send any MRX so we use 0 for the value.

We should be able to use the minimum gas limit 250000 and gas price 0.00005. 

The governor needs to sign the transaction, so replace `<GOVERNOR ADDRESS>` with our governor's address. 

We will use true for both broadcast and return change to sender.

```
sendtocontract "13a5933a1b786e8016178656145e36eccd0221f6" "fba713970000000000000000000000000000000000000000000000000000000000000000" 0 250000 0.00005 <GOVERNOR ADDRESS> true true
```


#### Enroll in DGPv3

Next we will call `enroll()` on the DGPv2 contract which takes no parameters, by abi encoding the data we will get `e65f2a7e`.

This transaction needs to send a value of 7500000 MRX as collateral.

We should be able to use the minimum gas limit 250000 and gas price 0.00005.

The governor needs to sign the transaction, so replace `<GOVERNOR ADDRESS>` with our governor's address. 

We will use true for both broadcast and return change to sender.
```
sendtocontract "73e6c0383dceed1583eb6a4b2aa9253020cb2b18" "e65f2a7e" 7500000 250000 0.00005 <GOVERNOR ADDRESS> true true
```

## FAQ

### Will I need to wait for my governor to mature again?

**Yes!** Enrolling in the DGPv3 contracts will require all new governors to wait for 1920 blocks (~48 hours) to receive governor rewards and 26880 blocks (~28 days) to be eligible to vote on budget proposals or DGP blockchain parameter proposals.


### What happens to any DGPv2 proposals?

Any DGPv1 proposals that have not passed or been completed will need to be re-created in the DGPv3 contracts. 
