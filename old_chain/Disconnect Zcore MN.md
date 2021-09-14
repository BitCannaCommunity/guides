Instructions to discconnect a ZCore Cold MN and convert it in a FullNode.

# Disconnect your ZCORE MN

Disconnecting your ZCORE masternode from the network might sometimes be difficult. This guide helps you through the steps to get it done.

## Start
Update to the latest build as can be found on https://www.bitcanna.io/wallets/.

### Scenario’s:
Two scenario’s:

1. QT runs in the background with MN on a ZCORE node
2. QT is switched off, starting required to access wallet

If you have scenario 1, go to the scenario 1 part below.
If you have scenario 2, scroll down to the scenario 2 part.

### Scenario 1. QT runs in the background with MN on a ZCORE node
First step is to get the private key of your address:

![](https://i.imgur.com/hmG9Nt4.png)

![](https://i.imgur.com/8CTGyNl.png)

Save your private key in a safe and secure place!

Afterwards you can close the wallet to continue:

![](https://i.imgur.com/0krRQaY.png)

Continue with the steps below.

### Scenario 2. QT is switched off, starting required to access wallet
First of all, create a copy of the wallet.dat:

![](https://i.imgur.com/Xt8vf4L.png)

Delete the masternode.conf before the wallet is started:

![](https://i.imgur.com/Ui8IQRu.png)

Add the line “staking=0” to the bitcanna.conf file (this will prevent the wallet from staking as soon as it is not a masternode anymore):

![](https://i.imgur.com/N4aUauL.png)

![](https://i.imgur.com/5rdtRah.png)

Start the qt:

![](https://i.imgur.com/e0FtNCL.png)

Make sure you have enabled coin control to give you the option to bundle all masternode rewards before you continue. Go to Settings > Options:

![](https://i.imgur.com/C9i1Hd3.png)

Go to the Wallet tab and make sure the tickbox before “Enable coin control features” is activated:

![](https://i.imgur.com/SZjSGad.png)

Now you can go to the Send tab of the wallet and use the “Inputs” button:

![](https://i.imgur.com/3E7zTbK.png)

Here you can select all the various inputs, but make sure you do not select the masternode output (100.000 BCNA in size):

![](https://i.imgur.com/9WEI7CA.png)

![](https://i.imgur.com/dSuENT6.png)

After that, select all coins in the wallet and send them to another address (or to the same, that works as well since the UTXO for your coins will be different. The MN on ZCORE will not be valid anymore since the UTXO used there is different).
NOTE: in some occassions the wallet crashes. In that case, delete the wallet.dat, replace it with the copy made earlier (make sure you always have one copy stored safely) and restart the wallet.

After sending the masternode output towards the wallet or to another wallet, the MN is deactivated. No new mints will be won. The tokens can now also easily be swapped.
