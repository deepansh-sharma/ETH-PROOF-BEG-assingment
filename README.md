# Create a Token
This is a simple token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

# Description
The goal of this project is to develop a token contract that supports the minting and burning of tokens. The contract will store essential details about the token, such as the token name, token abbreviation, and total supply. It will also maintain a mapping of addresses to token balances.
The contract will be designed to have a flexible supply, enabling the creation of new tokens through a minting process and the destruction of tokens through a burning process.

The contract will include the following features:
1) Token Details: The contract will have public variables to store the token's name, abbreviation, and total supply. These variables will allow users and external systems to easily access information about the token.

2) Balances Mapping: The contract will use a mapping data structure to associate addresses with token balances. Each address will have a corresponding uint value representing the number of tokens held by that address.

3) Mint Function: The contract will provide a mint function that accepts two parameters: an address and a value. This function will increase the total supply by the specified value and increase the balance of the given address by the same amount. The mint function will allow new tokens to be created and distributed to designated addresses.

4) Burn Function: The contract will feature a burn function that works in the opposite manner of the mint function. It will accept an address and a value as parameters. The burn function will verify that the balance of the given address is greater than or equal to the specified value. If the condition is met, it will deduct the value from the total supply and decrease the balance of the address accordingly. The burn function will facilitate the controlled reduction of token supply by destroying existing tokens.

# Getting Started

### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., token.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

```javascript
contract MyToken {
    // public variables here
    string public Tname = "MetaCoin";
    string public Tabbrev = "MC";
    uint public Ttotal = 0;

    // mapping variable here
    mapping(address => uint) public balance;

    // mint function
    function mint(address _address, uint _value) public {
        Ttotal += _value;
        balance[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balance[_address] >= _value) {
            Ttotal -= _value;
            balance[_address] -= _value;
        }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "token"  contract from the dropdown menu,and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "token" contract in the left-hand sidebar, and then click on the "mint" function  Enter address and its value. Finally, click on the "transact" button to execute the function.

Click on the "token" contract in the left-hand sidebar, and then click on the "burn" function  Enter address and its value which you want to delete. Finally, click on the "transact" button to execute the function.

These are sample address which you can use for address attribute 
Address = [0x66B0b1d2930059407DcC30F1A2305435fc37315E, 0x6827b8f6cc60497d9bf5210d602C0EcaFDF7C405];


