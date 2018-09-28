# Masternode Setup Guide
1. install git    
``` sudo apt-get -y install git ```
1. goto home directory   
``` cd ``` 
1. fetch sources   
``` git clone https://github.com/PayDayCoinIo/Binaries.git ```
1. go to fetched sources   
``` cd Binaries ```
1. Type command to install and configure masternode
``` ./linux_install masternode ```
1. After node is configured, your keys and masternode info saved in   
``` ~/masternode_info.txt ```   
to some secure place. 
1. So now send *20 000* coins to Masternode address which has been saved in masternode_info.txt
1. after coins sent, some confirmations necessary, to that masternode will activated. Enter command to display status of masternode:   
``` pdd masternode debug ```
1. after confirmations has been done, command output, which entered in previous step, will displayed that masternode is active   

And in the wallet we will saw masternode in Mastenode List
