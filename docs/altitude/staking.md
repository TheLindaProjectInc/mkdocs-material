# Staking
Staking is the process whereby you put your Metrixcoins in a Metrix wallet (Altitude or MyStakingWallet) and get rewarded in Metrix for holding them in your wallet. Staking contributes to the blockchain by creating blocks.

## Requirements
* The coins in your wallet need to be there for at least 960    confirmations to mature, this will take approximatily 24 hours.
* Your wallet has to be fully synched with a decent amount of connections.
* Your wallet must be unlocked for staking.
* Your system time has to be correct, and synched with https://time.is/.

## Staking process
* When a wallet stake occurs, the stake payment will be added to the balance of the staking input which was rewarded by the blockchain.
* After a successful stake, the coins require 960 confirmations to re-mature, the staking input which received the stake becomes unspendable for this period of time.
* If the balance of this address is > 1 million Metrix then the stake process will split the coins into 2 inputs, each of these inputs will then stake separately on the same wallet address.
* The smaller stake inputs will take more time to gain weight to re-stake, but will follow the same process as above, again splitting if their value is > 1 million.
* If you have a staking input smaller than 500.000 Metrix the wallet will combine this input with another one when a stake is received.

## Things to note
* Sending coins from a wallet will interrupt the staking process of any inputs chosen to fulfill the total amount to send. These interrupted inputs will require 960 confirmations to remature. It is also likely that any coins of these inputs not sent out will be returned on a new wallet change address.


## Staking rewards and deflationary staking model
* The current staking reward is 10% annually, this wil remain so until October 2022
* From October 2022 to October 2026 staking rewards are reduced to 5%
* From October 2026 to October 2032 staking rewards are reduced to 2%
* From October 2032 the staking rewards are reduced to 1% untill maximum supply is reached.

## Coin control
On the new chain (October 2020) coin control is not recommended. The coins become spendable after 960 confirmations after receiving a stake, if you coincontrol to combine them they will need another 960 confirmations before they are mature, this will cost you approximatily another 24 hours without staking. 
