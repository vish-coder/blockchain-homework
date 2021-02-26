# blockchain-homework
blockchain-homework
# Part 1: Blockchain Case Study 

### What is Hive? 
HIVE Blockchain Technologies Ltd. is a growth oriented, TSX.V-listed company building a bridge from the blockchain sector to traditional capital markets. HIVE owns state-of-the-art green energy-powered data centre facilities in Canada, Sweden and Iceland, which produce newly minted digital currencies like Bitcoin and Ethereum continuously on the cloud. Our deployments provide shareholders with exposure to the operating margins of digital currency mining as well as a portfolio of crypto-coins.

### What’s the big idea behind HIVE?
HIVE is a growth oriented, publicly listed company building a bridge from the blockchain sector to traditional capital markets.

Blockchain technology is revolutionizing finance and there are very few ways for investors to gain exposure to businesses in this space.

HIVE is a relatively new public company that uses high powered computing assets to mine cryptocurrencies like Ethereum and Bitcoin on the cloud. Our deployments provide shareholders with exposure to the operating margins of digital currency mining as well as a portfolio of crypto-coins.

### What is HIVE’s business model?
Simply put, HIVE is a cryptocurrency mining firm. We validate transactions on blockchain networks — like Ethereum — for rewards paid in cryptocurrencies. Everyday HIVE earns new crypto coins which it can monetize for revenue and cash flow. HIVE offers shareholders exposure to the operating margins from cryptocurrency mining plus a growing portfolio of coins.

### What are HIVE’s assets?
HIVE owns **state-of-the-art green energy-powered data centre facilities in Canada, Sweden and Iceland,** which produce newly minted digital currencies like Bitcoin and Ethereum continuously on the cloud.

### Why go public on the TSXV?
Being a first mover to list on a major public exchange was a key part of HIVE’s strategy. It provides equity shareholders a way of getting exposure to the crypto world through a traditional investment vehicle. The capital markets have very few options for investors to participate in the blockchain sector, and HIVE provides a unique opportunity to do so. Public markets are a huge untapped opportunity to finance the growth of the blockchain sector and HIVE. We chose the TSX-Venture Exchange in particular because it is a flexible capital formation platform, and at the same time, is one of the most accessible stock exchanges globally.

# Part 2: POA Development Chain.
Welcome to Vishal's MagNet - my first blockchain! 

 how to start the network
 Steps you must follow to experience the entire journey: 

Few initial steps on MyCrytpo: 
 1. Create a wallet, I used a new one just to enjoy the ride! So I went to crypto and I created a wallet using generate wallet. 
 2. I used the Mnemonic phrase to open my new wallet. 
 3. I used a side cheatsheet to track all my work. so I copied the public address of this wallet -> 0x054220BDAb81A1031b6A9B6fAD142aec59B3922d
 4. Next, I went to the "wallet info" tab and I copied the private key on my cheatsheet. (THIS IS VERY IMPORTANT STEP). we will need this key later on when we are mining

Creating the blockchain using GitBash:

## Step 1: Create Genesis

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


## Step 2: Create nodes and initialize
1. To create the nodes use the following statements. In  this project, I have used 2 nodes (node1, node2)  and they love talking ALL DAY ALL NIGHT like the new lovers! 
2. ./geth account new --datadir node1
3. ./geth account new --datadir node2
4. I got a successful message 
5. Then I went to the blockchain tools directory to see there were 2 folders
6. then i initialized my nodes by running following commands
7.  ./geth init magnet.json --datadir node1 ,  ./geth init magnet.json --datadir node2
8. This will initialize the nodes

## Step 3: Firing up our magnet (blockchain): 
1. ./geth --datadir node1 --unlock "0x29a283EB012017DbC30918B73f6Bd3018E0c76C1" --mine --minerthreads 1 - this command starts the node 1 mining
2. copy the enode address 
3. Then use the enode address to make our second node - node 2 - to talk to node 1. 
4. this commmand will start that command - ./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://a1aa4a2e8ce56ad2a2f770f79013ee4cb322907a272a6e26a93ddc97595ed6349b8403f6e994dcf2378dc2d3048ea96e652be27cdc469c773c0f066c374e73f0@127.0.0.1:30303" --ipcdisable
 5. Now magnet is up and running. 

## Step 4: Set up custom network
1. go to mycrytpo 
2. set up the custom network by adding the network name - magnet, network id 999 and the http://127.0.0.1:8545
3. Then connect  to network using private key that is stored in a textpad on local machine (if you forgot to keep it handy, not to worry, use optional step 4)
4. this is optional step if you havent saved your private key. Go go testnet , open your waller with the mnemonic and then copy the private key of your wallet 
5. Open magnet with private key
6. you must see that this wallet is pre funded with huge number of ETH.
7. this is end of this step

## Step 5: Transact on mycrypto:
1. go to view and send
2. copy/paste the node (my address) in "to address " 0x054220BDAb81A1031b6A9B6fAD142aec59B3922d
3. Send any amount from "your" account to "your" account 
4. I am sending 10000000 
5. then you will see that this transaction has been successfully submitted 
6. you can also see the hash on the gitbash in node 1 like below
INFO [02-26|09:14:43.433] Submitted transaction                    fullhash=0x9afd10fe3f7318da73d67788f20e73a98b35f33fc9b7d6c23e8c53c8918edde2 recipient=0x054220BDAb81A1031b6A9B6fAD142aec59B3922d

This concludes the second part of the assignment.  

Please refer to screenshots here https://github.com/vish-coder/blockchain-homework/issues/1


 
 
 
