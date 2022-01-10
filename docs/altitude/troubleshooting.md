# Troubleshooting

This is a list of common issues we see. In some cases the fixes detailed below will address a range of wallet & syncronisation issues.

> Prior to performing any troubleshooting fixes, its always best to ensure you have a current backup of the wallet.dat. you can manually copy this from the [Metrix data directory](/altitude/install#data-directories), or use the backup facility **File > Backup Wallet** in Altitude.
{.is-danger}


> If your still getting issues after trying some of these, please **Report a Bug** using the links below.
>  Help us squash those bugs [Metrix Core](https://github.com/TheLindaProjectInc/metrix/issues) | [Altitude](https://github.com/TheLindaProjectInc/altitude/issues)
{.is-info}

## Core Stopped Unexpectedly
![core_stopped.png](/assets/altitude/core_stopped.png)

This is a dialog displayed when Altitude detects that the core has crashed.
In most cases this is when initially starting the client, and in most cases it's due to the core being unable to load the local copy of the blockchain. 
The reasons for being unable to load the local blockchain are various and many. But the quick fix for all is normally the same.

- Remove the local blockchain and resync.

Fixing this normally consists of performing the following steps.

1. 	If you are running Altitude v3.0.5 or newer. Click the Recovery Tools button then click **Resync Blockchain** this should remove your local blockchain files and start resynchronizing from block 0.
2. If Step 1 fails to fix the issue, you can manually perform the same steps. Navigate to the [metrix data directory](/altitude/install#data-directories).
3. Delete the blocks & chainstate folders.
4. Start altitude. The wallet will now start synchronizing from block 0


## Initialising Core

![inititialising_error.png](/assets/altitude/inititialising_error.png)

An issue experienced most commonly after a Core update.

2 options to fix this.

**Within Altitude**

- Click **Tools** > **Wallet Repair** > **Reinstall Metrix Core**

**Manually**

1. Close the wallet (Altitude) check it's also not still running in the system tray.
2. Delete [Altitude data directory](/altitude/install#data-directories)\Clients\metrixd.exe. (**metrixd** for Linux and MacOS clients)
3. Start Altitude.


## Staking Icon Incorrect
![staking_not_staking.png](/assets/altitude/staking_not_staking.png)

Not a common issue, the wallet advises staking is active but the staking icon in the bottom left is Red.

Simply closing Altitude(Also exit in tray) and reopening it normally fixes this issue.



## The wallet is not staking

If it takes really long before you receive a stake in altitude 3.0.5 or newer and you are in doubt if the wallet is working correctly there are a few options you can check and do yourself.

First of all make sure your system time is in synch with https://time.is/

If this is not the problem there is a really small possibility you are on a sidechain, to fix this you have to delete the local blockchain files end let the wallet resynch. There are 2 ways to do this.

#### In altitude 

Go to Tools-->Wallet repair--> Resync Blockchain

#### Manually
1.	Close altitude, also in system tray.
2.	Go to the [Metrix data directory](/altitude/install#data-directories) and remove the folders “blocks” and “chainstate”
3.	Open altitude and let it synch

Once synchronized the wallet should work correctly.

### Notes
* Small inputs of 500k Metrix or less just take really long to stake, it is not common that it is a wallet issue if they are not staking in a few weeks.
* This fix will not affect the amount of confirmations on your inputs so you won’t lose any stake time.
* Do not expect the wallet to stake immediately or even in a few days after the fix, it will just stake as normal.

## No Peers
When altitude is stuck on "waiting for peers" there is a fairly simple solution


* Close altitude and go to the [metrix data directory](/altitude/install#data-directories), remove the peers.dat file in the metrixcoin folder. Start altitude.



