<h1>Token creation on local hardhat network </h1>

This Solidity program is a simple "Token creation" program that demonstrates the basic syntax and functionality of a Token which can be deployed with the help of a smart contract on a local hardhat network. The purpose of this program is to write a contract for a token on a local hardhat network and make transactions 
via Metamask wallet connected to the local hardhat network.

<h2>Description</h2>
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This program has a contract named MyToken. The contract has a token with 3 most basic functions- Transfer, Burn and Mint. Mint function will increment token amount in an account balance of the address specified and add it to the total supply while burn function will destroy the mentioned amount of tokens from the total supply. Transfer enables a user to tranfer any amount of token from his account address to another. Burn and Transfer function can be performed by any user, however the mint function can only be performed by the token owner. The token is created via a smart contract on a local hardhat network. This program serves as a simple and straightforward Token creation, and making transactions with the token on Metamask wallet. This can be used as a stepping stone for more complex tokens in the future.

<h2>Getting Started</h2>
<h3>Executing program</h3>
1. To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

2. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ABC.sol). 
   Copy the code  which you can find in the file named MyFirstToken.sol attached in this github repository, annd paste it into the file created by you.

3. To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" version is set to "0.8.0" (or later), and then 
   click on the "Compile Token.sol" button.

4. Once the code is compiled, Open a project where you have setup ready to start a local hardhat network. Go to the terminal and run the command
```
npx hardhat node
```
   it will start a hardhat network on your local machine. And provide you a list of addresses with public and private keys that you can use to 
   interact with the smart contract. Or import them to metamask wallet. Each accouont will be loaded with 10000 Eth balance.

5. Come back to Remix IDE. Switch to deploy and transactions tab choose the environment Injected Provider. It will connect you to the metamask wallet.
   Make sure you have an account imported from the local hardhat network. And the network is the network which you have created and your account
   should have 10000 ETH balance if you haven't made any transactions before.

6. Now, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token" contract from the dropdown 
   menu, and set the token name, symbol and initial balane for your token and then click on the "Deploy" button.

7. Once the contract is deployed, you can interact with it by calling the Burn, Mint and Transfer functions. Click on TotSupl to see the total supply which
8. should 
   now be set to 1000. Similary you can click on Name, Owner and Symbol to see the token name Token symbol and Owner address respectively. Token address
   should be same as the address shown in your metamask wallet.

Now call functions one by one check balance of an address, value of total supply and mint coin to some address, burn tokens or tranfer token to some address. 
You can import another account from your local hardhat network and try to run those functions. Before that you should transfer some token to this address so 
that this account address have enough token balane to interact with it. If it doesn't then it will throw you an error and probably you have to refresh the 
whole page and start the process again from beginning. While running those functions you will notice you can only run burn and transfer function with this 
account and if you try to run mint function it will throw you an error. It is just because of the implmentation of the modifier OnlyOwner where it checks 
weather this account address is the contract owner or not.

<h2>Author</h2>
Anjan Gorai

email: aneriomcpronier@gmail.com

<h2>License</h2>
This project is licensed under the MIT License.
