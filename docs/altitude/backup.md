Each public address on the blockchain has a unique key to access it. This is the **Private key**. When you hold this key you can access that public address at any time and place as long as you have a proper wallet.

## Obtain a private key
To obtain a private key you have to execute the following steps.

* First copy the public address for which you want to retrieve the private key.
* Fully unlock your encrypted wallet. Go to **Encrypt -> Unlock wallet** and unlock your wallet. Uncheck for **Unlock for staking only**.

![fully_unlock.png](/assets/altitude/fully_unlock.png)

* Now go to **Tools -> Debug console**
* Type **dumpprivkey ***yourwalletaddresshere***** and hit enter. For example:

![dumpprivkey.jpg](/assets/altitude/dumpprivkey.jpg)

* Copy the output and keep it somewhere save. This is the private key of the entered public address.

> **CAUTION!** Never share your private keys! People having access to your private key, can obtain access to your wallet and can steal your coins.

## Import a private key
The importprivkey command assists you with importing a wallet address into a new wallet.dat file. This can be usefull incase your wallet.dat get's corrupted or after a system failure.

The steps below describe how you can import a private key into an excisting wallet.

* Make sure your wallet is fully unlocked. Go to **Encrypt -> Unlock wallet** and unlock your wallet. Uncheck for **Unlock for staking only**.
* Go to **Tools -> Debug Console** 
* Type following command: importprivkey **yourprivatekeyhere**. For example:

![importprivkey.jpg](/assets/altitude/importprivkey.jpg)

* after the cursor returns close altitude and reopen it to see the imported address.



