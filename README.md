MyToken
This Solidity program demonstrates the creation of a simple ERC20 token using the OpenZeppelin library. It includes basic functionalities such as minting, transferring, and burning tokens. This program is intended for those who are new to Solidity and Ethereum token development, providing a foundation for more advanced token contracts in the future.

Description
This program defines a smart contract called 'MyToken', which is an ERC20 token with additional functionalities. It leverages OpenZeppelin's implementation of the ERC20 standard and the Ownable contract to restrict certain operations to the contract owner. The key features include minting new tokens, transferring tokens, and burning tokens to reduce the total supply.

Getting Started
Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at Remix.

Create a New File:

Click on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension (e.g., MyToken.sol).

After writing the code-
Compile the Code:

Click on the "Solidity Compiler" tab in the left-hand sidebar.
Ensure the "Compiler" option is set to "0.8.0" (or another compatible version).
Click on the "Compile MyToken.sol" button.
Deploy the Contract:

Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
Select the "MyToken" contract from the dropdown menu.
Click on the "Deploy" button.
Interact with the Contract:

Once deployed, you can interact with the contract's functions:
mint: Mint new tokens to a specified address.
transfer: Transfer tokens to a recipient.
burn: Burn tokens to reduce the total supply.


Authors
Vikash Kumar Singh
