# Assessment
# Project: Create a Token
## Description
A basic Ethereum smart contract for a unique token can be found in this repository. The contract tracks address balances and performs standard operations like minting and burning tokens.
## Contract Details
The smart contract includes the following features:
### 1.Token Details:
Public variables to store the token name, abbreviation, and total supply.
### 2.Balances:
A mapping of addresses to their token balances
### 3.Mint Function:
A function that increases the total supply of tokens.
### 4.Burn Function:
A function that decreases the total supply of tokens.
## Functions
### Mint Funtion
function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
        }
### Burn Function
function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
## Usage
utilize Solidity and Ethereum smart contracts with caution. To utilize this contract, deploy it to the Ethereum network and use the functions to mint or burn tokens as needed.
## Author
Archana Budda
