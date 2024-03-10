# polymer-dev-testnet

Follow my steps, copy and paste the codes one by one

## Start here

````
sudo apt update -y && sudo apt upgrade -y
sudo apt-get install git -y
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings
````

continue in here

````
sudo nano /etc/apt/sources.list.d/nodesource.list
````

We are in the file, now paste this and then CTRL+X + Y then Enter ( save and exit )
````
# deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_ jammy main
````

continue on the main screen 

````
sudo apt update -y && sudo apt upgrade -y
sudo apt-get install -y nodejs
````

## polymer set up

````
git clone https://github.com/sarox0987/polymerlab-ibc-app-solidity.git
cd polymerlab-ibc-app-solidity
````

## just and forge's set up

````
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to /usr/local/bin
curl -L https://foundry.paradigm.xyz | bash
source /root/.bashrc
foundryup
forge build
````

## Required steps
1-Create new testnet wallet in Metamask and copy it's key
2- Create Alchemy account 
3- Create Optimism Sepolia and Base Sepolia App ( copy their's key only - not RPC keys- first key )
4- Get faucet for both
[Op - Sepolia Faucet](https://www.alchemy.com/faucets/optimism-sepolia)
[Base - Sepolia Faucet](https://www.alchemy.com/faucets/base-sepolia)

enter env file
````
nano .env
````
Fill this parts :


>    PRIVATE_KEY_1 = Metamask private key

>    OP_ALCHEMY_API_KEY = Optimism API Key

>    BASE_ALCHEMY_API_KEY = BaseAPI Key

CTRL+X +Y and Enter

## create channels

````
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
npm install
just install
just do-it
````

use this code if you couldnt install just and got error, otherwise skip this step
````
wget -qO - 'https://proget.makedeb.org/debian-feeds/prebuilt-mpr.pub' | gpg --dearmor | sudo tee /usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg 1> /dev/null
echo "deb [arch=all,$(dpkg --print-architecture) signed-by=/usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg] https://proget.makedeb.org prebuilt-mpr $(lsb_release -cs)" | sudo tee /etc/apt/sources.list.d/prebuilt-mpr.list
sudo apt update
````

You should be good after running just do-it code. Codes will run and it will say " You are done" at the end.
Take ss and send it to their discord. 

[Discord]([https://pages.github.com/](https://discord.com/invite/hvMQp4qcM6)https://discord.com/invite/hvMQp4qcM6)

send your proof to this channel :  [Proof](https://discord.com/channels/839903468750635039/1213267408370794506)


## If you get error : 
First of all make sure you have eth both sepolia chains. If you have testnet tokens then use this codes
````
npx hardhat clean
just do-it 
````

till you see you are done.
