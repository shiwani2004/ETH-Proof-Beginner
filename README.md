# ETH-Proof-Beginner
Summer Training with Metacrafters for Learning Blockchain with Ethereum using Solidity.

# Project Title

Token Simulation: Minting and Burning

## Description

This is a simple project for simulating the development of smart contracts using Remix IDE and the Solidity language for the transaction process of tokens in a blockchain on a local system. The project demonstrates how to create a basic token contract with functionalities to mint (create) and burn (destroy) tokens.

This project provides a basic example of how to create a token on the Ethereum blockchain using Solidity. The contract includes the ability to mint and burn tokens, and it keeps track of token balances for each address. By using public variables and mappings, the contract allows for easy interaction and verification of token details and balances.

## Getting Started

### Installing

* To run the project code, you need an IDE where you can run the Solidity language. One such IDE is the online Remix IDE (https://remix.ethereum.org/), which you can run on any browser of your choice.
* The code in this project can be used by simply copying it to the editor of any IDE where you can run Solidity version 0.8.7.

### Executing program

* How to run the program:
1. Copy the Solidity code provided in the "Final_Assessment" file.
2. Open Remix IDE (https://remix.ethereum.org/).
3. In the Remix IDE, create a new file and paste the copied code into it.
4. Compile the Code by either pressing "Ctrl + S" to compile the code or using the Compile button in the Remix IDE interface.
5. Use the Deploy button in the Remix IDE to deploy the contract to a local Ethereum network or a test network.
6. Use the deployed contract's interface in Remix IDE to call the mint and burn functions with appropriate parameters.
.


```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MyToken {
    // Public variables here
    string public tokenName = "wave";
    string public tokenAbbr = "WAV";
    uint public totalSupply = 0;

    // Mapping variable here
    mapping (address => uint) public balances;

    // Mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function
    function burn(address _address, uint _value) public {
        if(balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```

## Help

If you encounter any issues or have any questions, here are some common solutions:

1. Ensure you are using Solidity version 0.8.7 or later.
2. Check the Remix IDE console for error messages and follow the guidance provided.
3. Make sure the address you are using for minting and burning tokens has sufficient permissions and balance.

## Authors

Contributors names and contact info

Nitish   
mail: nitishkumarveer77@gmail.com


## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
