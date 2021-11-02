# Image Flake

![Ethereum](https://img.shields.io/badge/-Ethereum-3C3C3D?logo=ethereum&logoColor=fff)
![Solidity](https://img.shields.io/badge/-Solidity-363636?logo=solidity&logoColor=fff)
![IPFS](https://img.shields.io/badge/-IPFS-65C2CB?logo=ipfs&logoColor=fff)  
![React](https://img.shields.io/badge/-React-61dafb?logo=react&logoColor=000)
![Gatsby](https://img.shields.io/badge/-Gatsby-663399?logo=gatsby&logoColor=fff)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178c6?logo=typescript&logoColor=fff)
![tailwindcss](https://img.shields.io/badge/-tailwindcss-06b6d4?logo=tailwind%20css&logoColor=fff)
![Sass](https://img.shields.io/badge/-Sass-cc6699?logo=sass&logoColor=fff)  
![Infura](https://img.shields.io/badge/-Infura-FF6B4A?logoColor=fff)
![MetaMask](https://img.shields.io/badge/-MetaMask-F6851B?logoColor=fff)  

This is the final project of *Block-chain and Digital Currency* course of Zhejiang University.  
*Image Flake* is a NFT (non-fungible token) auction platform Dapp (decentralized application). User of this Dapp can upload, sell and purchase artworks using ETH. The artwork can only be bought in auctions, and the owner of the artwork can start an auction at any time.  
All the persistent data of this app is decentralized. The transaction information is stored on Ethereum chain, and the object files are stored in IPFS.  

![Screenshot_20211102_003421.png](https://i.loli.net/2021/11/02/P1HCk8JY7RUD2vI.png)  

## Usage

### Configuration File
Create configuration file `./front-end/config/eth.yaml`:  
```yaml
contractAddress: "contract_address"  # this can be added later
infura: 
  projectId: "infura_project_id"
  projectSecret: "infura_project_secret"
```
As mentioned above, an Infura project should be created.  

### Truffle and Ganache
Firstly, install Truffle CLI and Ganache GUI. Set up Ganache, which will listen port `8545` on default. You need to click *link truffle projects* button in *Contract* section, and select `./truffle/truffle-config.js`.  Then, run `truffle migrate` in `./truffle` directory. This will compile the contract, and deploy it onto the block-chain created by Ganache.  
In this phase, you will see the deployed contracts in "Contract" section. Copy the address of contract `ImageFlake` to `./front-end/config/eth.yaml`.  

### Front-end
After executed `npm install` in `./front-end` directory, install Gatsby CLI globally using `npm install -g gatsby-cli`, then run `gatsby develop` in `./front-end`.  
A MetaMask extension should be installed in your browser. Set the MetaMask custom port to `8545`, then import some accounts generated by Ganache into MetaMask. Have fun playing with NFT!  