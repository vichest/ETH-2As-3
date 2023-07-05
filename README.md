# ETH-2As-3
# ERC20 Token Contract

This is a basic implementation of an ERC20 token contract in Solidity.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Usage

The contract provides an interface (`IERC20`) and an implementation (`ERC20`) for an ERC20 token. 

### Prerequisites

- Solidity compiler version: ^0.8.7

### Interface

The `IERC20` interface defines the following functions:

- `totalSupply()`: Returns the total supply of tokens.
- `balanceOf(address account)`: Returns the token balance of a specified account.
- `transfer(address recipient, uint amount)`: Transfers a specified amount of tokens from the caller's account to the recipient's account.
- `allowance(address owner, address spender)`: Returns the remaining number of tokens that the spender is allowed to spend on behalf of the owner.
- `approve(address spender, uint amount)`: Sets the spender's allowance to a specified amount.
- `transferFrom(address sender, address recipient, uint amount)`: Transfers a specified amount of tokens from the sender's account to the recipient's account, with the allowance mechanism.

### Contract

The `ERC20` contract implements the `IERC20` interface and adds additional functionalities:

- `totalSupply`: A public variable that represents the total supply of tokens.
- `balanceOf`: A mapping that stores the token balance of each address.
- `allowance`: A mapping that stores the allowance of one address for another.
- `name`: A public string variable representing the name of the token.
- `symbol`: A public string variable representing the symbol of the token.
- `decimal`: A public uint variable representing the number of decimal places for the token.
- `onlyAdmin` modifier: A modifier that restricts the execution of certain functions to the contract admin.
- `transfer`: Transfers a specified amount of tokens from the caller's account to the recipient's account.
- `approve`: Sets the spender's allowance to a specified amount.
- `transferFrom`: Transfers a specified amount of tokens from the sender's account to the recipient's account, with the allowance mechanism.
- `mint`: Mints new tokens and adds them to the balance of the admin.
- `burn`: Burns tokens by subtracting them from the balance of the caller.

## Disclaimer

This contract is provided as-is without any warranties or guarantees. Use at your own risk.

