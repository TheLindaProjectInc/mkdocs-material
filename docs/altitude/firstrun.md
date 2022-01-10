# Altitude First Run

This is a list of tasks and knowledge we would consider to be essential to your first-run wallet experience. The majority of these tasks relate to securing your wallet and ensuring that you have recovery options available should system failure or wallet corruption occur.

## Dashboard
On the first launch of your Altitude wallet you will be presented with a dashboard.

![firstrun_dashboard.png](/assets/altitude/firstrun_dashboard.png)

On first run the important bits are highlighted. 
- You should have peers connected, if you have less than 10 here you probably have connectivity issues.
- Ensure your wallet is syncronising with the blockchain. This block number should continue to increment as blocks are downloaded.
- Time since last block, is when the last block was received. If fully syncronised, this can change between a few seconds and a few minutes.

> If any of the above items doesn't change for a while, your wallet may have stopped syncing. Check the [Troubleshooting](/Dcoumentation/Altitude/Troubleshooting) section for tips on getting going again.
{.is-warning}

## Language Selection

To display Altitude in your native tongue click **File > Language**.

![language_selection.png](/assets/altitude/language_selection.png)

## Currency Selection

To display Altitude balances in a currency other than MRX click **File > Currency**.

![currency_selection.png](/assets/altitude/currency_selection.png)

## Wallet Security

Your wallet contains the private keys to your funds. So protecting these from both theft and malfunctions is as important as protecting your regular bank details. In the banking industry fund security falls on the issuing bank, in the Crypto world this is all in the hands of the user.

In the case of wallets, you are the only one with access to the private keys, so steps should be takes to ensure their security.

**Encryption**
> Encrypt your wallet!!
{.is-danger}

This is the most fundamental of wallet security steps, and ensures that if your wallet.dat file is obtained, accessing the keys within is not easily possible.

1. Click **Encrypt > Encrypt Wallet**.
2. Enter a complex passphrase and confirm it.
3. Click **Encrypt**.

> Wallet passphrases are used for a lot of wallet functions, so this should be something complex but memorable. A list of random words is generally considered good practice, try and steer away from birthdays, locations, names.
Or maybe try this [Mnemonic generator](https://spacefem.com/mnemonics/)

Once set, the Encrypted icon turns to a green padlock. ![encrypted_padlock.png](/assets/altitude/encrypted_padlock.png)

**Backup**

Taking a backup of the wallet ensures that you have protection in the event of technical issues. PC malfunction, corruption, accidental wallet deletion/overwrites are all things we have seen before. So ensuring a good backup strategy, means your funds are always recoverable.

1. Click **File > Backup Wallet**.
2. Navigate to a directory on the PC. Enter a filename, its a good idea to put a date in this, so you know when it was taken. e.g. 040220_metrix_wallet.dat
3. Click **Save**.

Good backup strategy means keeping this file in a few different places. If you only store it on the local PC, the hard disk fails and is unrecoverable, what good is the backup! Also ensure you have at least one copy externally (USB key/HDD).

> Keep in mind, that if you generate new addresses in the wallet, a new backup should be taken. If you send funds out and receive coins back into a "change" address this also counts as a new address.

**Restoring**

If you have the wallet.dat file then restoration is simple.
1. Close Altitude.
2. Copy the wallet.dat backup into the [Metrix data directory](/Documentation/Altitude/Installation#data_directories). If a wallet.dat already exists in there rename that first.
3. Start Altitude.
4. Ensure you can unlock/relock the wallet.
5. If the blockchain is fully in sync then any coins will already be visible.

> To backup and restore using private keys, please follow the instruction in the Metrix core security section.
{.is-info}
