Masternode Setup Guide:
1.	We have a PayDay wallet with minimum 2000 coins.
2.	We have a linux server, maybe a VDS.
3.	We have a compiled daemon of PayDayd
4.	Start a daemon with command: PayDayd –daemon
5.	At first run we get a message:
Error: To use the "-daemon" option, you must set a rpcpassword in the configuration file:
/home/user/.PayDay/PayDay.conf
It is recommended you use the following random password: rpcuser=PayDayrpc rpcpassword=6XQ1TuMu8CXJrtz3bqijoN32evSAaEa7jSpFQkXgDuFy (you do not need to remember this password)
The username and password MUST NOT be the same.

6.	Now we copy two lines in configuration .PayDay/PayDay.conf in home directory
7.	Use a like text editor to edit file

 
8.	Save file and exit from editor.
9.	Run daemon with command below and have output: PayDayd –daemon
 
10.	When get address with command:
PayDayd getaddressesbyaccount ""
 
11.	So now send 2000 coins to this address from our wallet.

12.	Open a ssh terminal then put command below, to setup a masternode PayDayd masternode genkey
 
13.	Copy this key to clipboard, need to be paste in configuration file.
14.	Open .PayDay/PayDay.conf and insert this lines in file
masternode=1 masternodeprivkey=<this_priv_key> masternodesoftlock=1
Where masternodeprivkey a key generated above.
 
 
15.	Save configuration file and restart a daemon:
PayDayd stop and
PayDayd -daemon
16.	After send coins, need a some confirmations to activate masternode. Put command to show status of masternode:
PayDayd masternode debug

17.	After confirmations, answer to previous command is show that masternode active

And in wallet we show masternode in Mastenode List
