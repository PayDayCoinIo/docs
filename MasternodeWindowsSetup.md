# Masternode Windows Wallet Setup Guide
## STEP 1: Create Masternode data dir and executable file
1. We need a create folder to masternode files, example `C:\PayDay\MN1`
1. Copy exist executable `PayDayCoin-qt.exe` to this folder, and rename to `PayDayCoin-mn1.exe`
1. In masternode folder `C:\PayDay\MN1\` create new folder with name `data`
1. Open `notepad`, copy text below
```
@echo off
start PayDayCoin-mn1.exe -datadir=./data/
```
and save in masternode folder with name `start.cmd`
## STEP 2: Prepare Masternode Wallet
1. Run script `start.cmd` and wait until wallet is loaded and synchonize
1. Select menu and click on `Help menu` - `Debug window`, see image.
![Masternode Main](https://github.com/PayDayCoinIo/docs/blob/master/images/mn_main.png)
1. In opened window select tab Console
![Masternode Debug](https://github.com/PayDayCoinIo/docs/blob/master/images/mn_debug.png)
1. Type command `getaddressesbyaccount ""` and we see answer same as:
```
[
    "MUs9swsjpSqp9K2UrVu5u8fDiaSSNtkUXt"
]
```
1. Then open a main windows Wallet with coins and send 20000 in one transaction to address in answer abowe.
1. Wait until 1 confirmation is accepted.
1. After this, return to Masternode Wallet Debug console and type command `masternode genkey`, answer same as:
```
3orrHCsSefKX1bPdzWNw4DoGgxSTGjTfb3RMW5wJk6NCyYDa1cB
```
Copy this key to some place, example new file in notepad.
1. Then put command `masternode outputs` in Debug console, answer same as:
```
{
    "e8f62a66e132e24f13dd5556e61b003ec25ef069170b218b9222d434d288ccbe" : "1"
}
```
1. Copy first hash, this is output txhash of your transaction, second - output index, copy this in notepad
1. Now close Debug window and change tab to Masternodes - My Master Nodes. Click button Create..., see image.
![Masternode AddNode](https://github.com/PayDayCoinIo/docs/blob/master/images/mn_addnode.png)
1. 