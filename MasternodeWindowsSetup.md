# Masternode Windows Wallet Setup Guide
## STEP 1: Create Masternode data dir and executable file
1. We need a create folder to masternode files, example `C:\PayDay\MN1`
1. Copy exist executable `PayDayCoin-qt.exe` to this folder, and rename to `PayDayCoin-mn1.exe`
1. Create folder with name `data`
1. Open `notepad`, copy text
```
@echo off
start PayDayCoin-mn1.exe -datadir=./data/
```
and save in masternode folder with name `start.cmd`
## STEP 2: Prepare Masternode Wallet
1. Run script `start.cmd` and wait until wallet is loaded and synchonize
1. Select menu and click on `Help menu` - `Debug window`, see image.
![Image of Yaktocat](https://github.com/PayDayCoinIo/docs/blob/master/images/mn_main.png)
1.