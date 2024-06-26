# MyToken

This Solidity program demonstrates the creation of a simple ERC20 token using the OpenZeppelin library. It includes basic functionalities such as minting, transferring, and burning tokens. This program is intended for those who are new to Solidity and Ethereum token development, providing a foundation for more advanced token contracts in the future.

## Description

This program defines a smart contract called 'MyToken', which is an ERC20 token with additional functionalities. It leverages OpenZeppelin's implementation of the ERC20 standard and the Ownable contract to restrict certain operations to the contract owner. The key features include:

- **Minting new tokens**: Allows the contract owner to mint new tokens to a specified address.
- **Transferring tokens**: Enables token holders to transfer tokens to other addresses.
- **Burning tokens**: Allows token holders to burn their tokens, reducing the total supply.

## Getting Started

### Executing Program

To run this program, you can use Remix, an online Solidity IDE. Follow these steps to get started:

1. **Go to the Remix website**: [Remix](https://remix.ethereum.org/).

2. **Create a New File**:
   - Click on the "+" icon in the left-hand sidebar.
   - Save the file with a `.sol` extension (e.g., `MyToken.sol`).

3. **Write the Code**:
   - // SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.3.0/contracts/token/ERC20/ERC20.sol";
import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.3.0/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor() ERC20("MyToken", "MTK") {
        _mint(msg.sender, 1000000 * (10 ** uint256(decimals())));
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

    function transfer(address recipient, uint256 amount) public virtual override returns (bool) {
        return super.transfer(recipient, amount);
    }

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }
}

4. **Compile the Code**:
   - Click on the "Solidity Compiler" tab in the left-hand sidebar.
   - Ensure the "Compiler" option is set to "0.8.0" (or another compatible version).
   - Click on the "Compile MyToken.sol" button.

5. **Deploy the Contract**:
   - Click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
   - Select the "MyToken" contract from the dropdown menu.
   - Click on the "Deploy" button.

6. **Interact with the Contract**:
   - Once deployed, you can interact with the contract's functions:
     - `mint`: Mint new tokens to a specified address.
     - `transfer`: Transfer tokens to a recipient.
     - `burn`: Burn tokens to reduce the total supply.

## Authors

- Vikash Kumar Singh

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

