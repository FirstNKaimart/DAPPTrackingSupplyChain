// General Write-up

Summary: This project was meant allow different actors (roles) to interact with the product through
supply chain. This way we can utilize the blockchain technology to control and verify the authenticity 
of the product from it origin through to its customer.

// Libraries

Libraries that uses in this project are node js, truffle, web3 and truffle-hdwallet-provider which is a npm module.
NodeJs is a server-side platform built on JavaScript Engine. It is a cross-platform runtime environment for developing server-side
and networking applications. NodeJS comes with NPM (Node Package Manager) modules or dependencies which we can install from it website.
Truffle is smart contract development environment which provide testing framework and asset pipeline for blockchain using EVM (Ethereum Virtual Machine)
Using truffle to compile, migrate smart contract aswell as testing smart contract makes workflow much simplier while working on this project.
Truffle also comes with Ganache which is a personal blockchain for Ethereum development use to deploy contract, develop and run tests. 
Web3 is a collection of libraries that allow developers to interact with local or remote ethereum node using HTTP, IPC or WebSocket.
Using Web3 to connect and interact with the smart contract through frontend application. We can provide JSON ABI file for the web3 to 
identify our deployed smart contract as well as connect to Metamask on our browser.

node version: v13.12.0
truffle version : v4.1.14
web3 version: -
truffle-hdwallet-provider for deploying to test network through infura

// Contract and Transaction Hashes
Transaction ID: 0x3cd4e29bf3d8d83280dcc0c5aa22a6b8847b90a12642205736d6fe4dcafb14ad
https://rinkeby.etherscan.io/tx/0x3cd4e29bf3d8d83280dcc0c5aa22a6b8847b90a12642205736d6fe4dcafb14ad

Contract address: 0x1A6550eCbd10bb5A0b3dAAf7514F9Cbf4db269EA
https://rinkeby.etherscan.io/address/0x1a6550ecbd10bb5a0b3daaf7514f9cbf4db269ea

// Steps for testing and front end
// Testing
run on terminal
 ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"

on another terminal run
truffle migrate --reset

then run 
truffle test

// Front-end
run in terminal
npm run dev

If testing dapp on localhost:8545
use these Private Keys to test out to functionality

Available Accounts
==================
(0) 0x27D8D15CbC94527cAdf5eC14B69519aE23288B95 (100 ETH) // Contract Owner
(1) 0x018C2daBef4904ECbd7118350A0c54DbeaE3549A (100 ETH) // Farmer 
(2) 0xCe5144391B4aB80668965F2Cc4f2CC102380Ef0A (100 ETH) // Distributor
(3) 0x460c31107DD048e34971E57DA2F99f659Add4f02 (100 ETH) // Retailer
(4) 0xD37b7B8C62BE2fdDe8dAa9816483AeBDBd356088 (100 ETH) // Consumer

Private Keys
==================
(0) 0x9137dc4de37d28802ff9e5ee3fe982f1ca2e5faa52f54a00a6023f546b23e779
(1) 0x18911376efeff48444d1323178bc9f5319686b754845e53eb1b777e08949ee9b
(2) 0xf948c5bb8b54d25b2060b5b19967f50f07dc388d6a5dada56e5904561e19f08b
(3) 0xfad19151620a352ab90e5f9c9f4282e89e1fe32e070f2c618e7bc9f6d0d236fb
(4) 0x19d1242b0a3f09e1787d7868a4ec7613ac4e85746e95e447797ce36962c7f68b

First step use Contract Owner Account to add Farmer, Distributor, Retailer, Consumer addresses 
to Roles. 
Using addFarmer(), addDistributor(), addRetailer(), addConsumer()
Then use Farmer Contract to add new product into the system.
Farmer then use Click Harvest Button to insert new product to the system.
After that whenever Farmer finish processing the product, farmer can click Process Button
to change the state of which the product is currently at to Processed.
Farmer then have options to Pack using Pack button after done packing the product, and set for Sale 
to sell the product to Distributor.
Distributor accounts can choose to buy from the farmer by input the UPC code and click Buy button.
After brought the product Distributors can Ship them to the Retailers using Ship Button.
Retailers after received the product from the Distributors set the product Status to received.
Consumers can choose to purchase received products from the retailers buy input UPC and click Purchase Button. 

To check authenticity of the product input UPC in the Product Overview Section and click Fetch Data 1 and Fetch Data 2
The information about Product authenticity will be shown at the bottom of Product Authenticity Section.





