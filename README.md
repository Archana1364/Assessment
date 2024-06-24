# Project: Create a Token
SilverCoin
# Description
The 'MyToken' smart contract is developed in Solidity, a programming language that is utilized for creating smart contracts on the Ethereum network. The following elements are included in the contract:
1. contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
2. contract will have a mapping of addresses to balances (address => uint)
3. contract will have a mint function that takes two parameters: an address and a value.
   The function then increases the total supply by that number and increases the balance of the “sender" address by that amount
4. contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
   It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.
5. Lastly, burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.
# Getting Started
## Executing Program
To run this program, you need an Ethereum development environment. You can use Remix, an online Solidity IDE.
### 1.Open Remix:
Go to the Remix website http://remix.ethereum.org 
### 2.Create a New File:
Click on the "+" icon in the left-hand sidebar and save the file with a '.sol' extension (e.g., 'MyToken.sol'). Copy and paste the following code into the file:
// SPDX-License-Identifier: MIT
pragma solidity^0.8.18;

contract MyToken {

    // Public variables to store the details about the coin
    string public tokenName = "SilverCoin";
    string public tokenAbbrv = "SLV";
    uint public totalSupply = 0;

    // Mapping to store balances of addresses
    mapping(address => uint) public balances;

    // Mint function to increase the total supply and balance of a given address
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function to decrease the total supply and balance of a given address
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

# Author
Archana Budda
