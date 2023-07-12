# MyToken
This is a simple token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

## Requirements
### The contract has public variables that store the details about the coin:
 1) TName: A string representing the name of the token.
 2) Tabbrv: A string representing the abbreviation of the token.
 3) TSupply: An unsigned integer representing the total supply of the token.

### The contract has a mapping of addresses to balances:
balances: A mapping that associates addresses with their corresponding token balances.
The contract has a mint function that increases the total supply and the balance of the "sender" address by a given value:

### mint Function -
mint: Creates new tokens and assigns them to a specified address.

Parameters:
_address: The address to which the tokens will be minted.
_value: The amount of tokens to be minted.

Actions:
Increase the totalSupply by _value.
Increase the balance of the _address by _value.
The contract has a burn function that decreases the total supply and the balance of the "sender" address by a given value:

### burn function -
burn: Destroys existing tokens by reducing the total supply and the balance of a specified address.

Parameters:
_address: The address from which the tokens will be burned.
_value: The amount of tokens to be burned.

Actions:
Check if the balance of the _address is greater than or equal to _value.
If true, decrease the totalSupply by _value.
Decrease the balance of the _address by _value.
Usage
Deploy the MyToken contract to a supported Ethereum network.

These are sample address which you can use for address attribute 
Address = [0x66B0b1d2930059407DcC30F1A2305435fc37315E, 0x6827b8f6cc60497d9bf5210d602C0EcaFDF7C405];

License
This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.
