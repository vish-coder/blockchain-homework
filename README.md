# blockchain-homework
blockchain-homework
Welcome to Vishal's MagNet - my first blockchain! 

 how to start the network
 Steps you must follow to experience the entire journey: 

Few initial steps on MyCrytpo: 
 1. Create a wallet, I used a new one just to enjoy the ride! So I went to crypto and I created a wallet using generate wallet. 
 2. I used the Mnemonic phrase to open my new wallet. 
 3. I used a side cheatsheet to track all my work. so I copied the public address of this wallet -> 0x054220BDAb81A1031b6A9B6fAD142aec59B3922d
 4. Next, I went to the "wallet info" tab and I copied the private key on my cheatsheet. (THIS IS VERY IMPORTANT STEP). we will need this key later on when we are mining

Creating the blockchain using GitBash:

Step 1: Create Genesis

1. Go to the directory where geth(blockchain) tools are present(C:\Users\visha\geth-alltools-windows-amd64-1.9.25-e7872729)
2. GitBash to this directory
3. Type ./puppeth -> This is the start of creating the Genesis
4. Provide a cool network name, such as magnet (Magical Network) 
5. Key in option 2 to configure new genesis
6. and then option 1 to "Create new Genesis from scratch" 
7. Then choose option 2  Clique - proof-of-authority because this what the assignment/homework asks for
8. just hit enter to default the seconds block must take
9. Accounts to seal -> your wallet -> 0x **(054220BDAb81A1031b6A9B6fAD142aec59B3922d)** skip the Ox part from your wallet. Just copy the rest and paste it here
10. Press enter to skip adding more account that can seal 
11. Prefund your wallet by entering 054220BDAb81A1031b6A9B6fAD142aec59B3922d in the next prompt and then hit enter to skip other accounts
12. Just hit enter to use default precompiling address
13. VERY IMP key in an unused chain ID -> 888
14. You will then get a message that INFO [02-25|18:18:21.946] Configured new genesis block
15. Proceed to export the genesis settings by opting number 2 
16. number 2 again to export genesis config and just hit enter to use default directory 
17. Now use CTRL+C to exit and we are now ready to add nodes to our chain, YAY!!!!





 
 
 
