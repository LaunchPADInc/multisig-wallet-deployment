Description
=======
 
 ***Everything contained in this repository is in draft form and subject to change at any time and provided for information purposes only.  LaunchPAD does not guarantee the accuracy of the information contained in this repository and the information is provided “as is” with no representations or warranties, express or implied. This code is owned and copyrighted by LaunchPAD and cannot be used by anyone for any purpose.***
 
 This repository contains the draft source code for the multisigwallet for the Ethereum blockchain. It is being released so that it may be reviewed by the community and deployed and tested by all.

Multisignature Wallet
===================

Smart contracts that comprise of the multisigwallet. The purpose of a multisigwallet is to increase security by requiring multiple parties to agree on transactions before execution. Transactions can be executed only when confirmed by a predefined number of owners.

Features
-------------

- Can hold Ether and all kind of tokens with multisig support
- Easy to use offline signing (cold wallet) support
- Integration with web3 wallets (Metamask, Mist, Parity, etc)
- Transaction data and log decoding, makes transactions more readable
- Interacting with any contracts with UI support
- Hardware wallet support (Ledger Wallet)
- Optional email notifications when an event is triggered or you are required to sign a transaction

Install
-------------
```
git clone https://github.com/LaunchPADInc/multisig-wallet-deployment
cd wallet
npm install
```

Test
-------------
### Run contract tests:
```
npm test
```
### Run interface tests:
```
npm run test-dapp
```

Deploy
-------------
### Deploy multisig wallet:
```
truffle migrate <account1,account2,...,accountN> <requiredConfirmations>
```
### Deploy multisig wallet with daily limit:
```
truffle migrate <account1,account2,...,accountN> <requiredConfirmations> <dailyLimit>
```

Limitations
-------------
This implementation does not allow the creation of smart contracts via multisignature transactions.
Transactions to address 0 cannot be done. Any other transaction can be done.

Security
-------------
All contracts are WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

License
-------------
See LICENSE file
