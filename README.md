# Metacrafters_ETH-PROOF-Beginner-EVM
The `MyToken` smart contract is an ERC20-like token in Solidity. It manages the token name, symbol, total supply, and address balances. The `mint` function creates tokens, and the `burn` function destroys them, adjusting balances and total supply.

Certainly! Here is a detailed description for the `README.md` file of your GitHub repository:

# MyToken Smart Contract

This repository contains the Solidity code for the `MyToken` smart contract. The contract implements a basic ERC20-like token with minting and burning functionalities. Below are the key features and functionalities provided by this smart contract.

## Contract Details

### Public Variables
- **name**: The name of the token, set to "MyToken".
- **symbol**: The symbol or abbreviation of the token, set to "MTK".
- **totalSupply**: The total supply of tokens in existence, initialized to 0.

### Mapping
- **balances**: A mapping from addresses to their respective token balances. This allows the contract to keep track of how many tokens each address owns.

### Functions

#### mint
```solidity
function mint(address to, uint256 amount) public
```
- **Description**: Mints new tokens and assigns them to the specified address.
- **Parameters**:
  - `to`: The address to which the minted tokens will be assigned.
  - `amount`: The number of tokens to mint.
- **Behavior**:
  - Increases the `totalSupply` by the specified `amount`.
  - Increases the balance of the specified address by the same `amount`.

#### burn
```solidity
function burn(address from, uint256 amount) public
```
- **Description**: Burns (destroys) tokens from the specified address.
- **Parameters**:
  - `from`: The address from which the tokens will be burned.
  - `amount`: The number of tokens to burn.
- **Behavior**:
  - Ensures the balance of the specified address is greater than or equal to the `amount` to be burned.
  - Decreases the `totalSupply` by the specified `amount`.
  - Decreases the balance of the specified address by the same `amount`.

## Example Usage
1. **Minting Tokens**: To mint tokens to an address, call the `mint` function with the recipient's address and the amount of tokens to mint.
2. **Burning Tokens**: To burn tokens from an address, call the `burn` function with the address from which to burn and the amount of tokens to be burned. Ensure the address has a sufficient balance before calling this function.


### Prerequisites
- Solidity ^0.8.18
- An Ethereum wallet like [MetaMask](https://metamask.io/)


### Deploying
Deploy the contract using Remix IDE or any other Ethereum development framework.
