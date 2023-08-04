# SolidityProjectAssessment
# Create a Token

This Solidity program is a simple "Create a Token" program that demonstrates the syntax and functionality of the Solidity programming language to create and burn tokens.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a multiple function's that returns the string "Token Name", "TokenAbbr" and "TotalSupply" Which is initially 0. This program serves as that how to create mint and burn token in Solidity programming, and can be used as a stepping stone for more complex projects in the future.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., CreateAToken.sol). Copy and paste the following code into the file:

    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {
    // public variables here
    string public tokenName = "Mr.India";
    string public tokenAbbrv = "IND";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public tokenCreated;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        tokenCreated[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (tokenCreated[_address] >= _value) {
            totalSupply -= _value;
            tokenCreated[_address] -= _value;
        }
    }
    }

###Getting Started

To deploy and interact with this Token contract, follow the steps below:

Apologies for the confusion. Here are the steps to deploy and interact with the token contract named "Create a Token.sol" on Remix IDE:

Open Remix IDE:

Go to the Remix IDE website: https://remix.ethereum.org/.

1. Create a New File:

   •Click on the "+" icon in the file explorer to create a new file.

   •Name the file "Create A Token.sol" and press Enter.

2. Copy and Paste the Solidity Code:

   •Copy the MyToken contract code provided in the previous responses.

   •Paste the code into the "Create A Token.sol" file.

3. Compile the Contract:

   •In Remix, go to the "Solidity Compiler" tab on the left-hand side.

   •Select the appropriate compiler version (e.g., 0.8.18).

   •Click on "Compile Create A Token.sol" to compile the contract.

4. Deploy the Contract:

   •Go to the "Deploy & Run Transactions" tab on the left-hand side.

5. Deploy the Contract:

   •Choose an Ethereum account to deploy the contract (this will be the contract owner).

   •In the "Deploy" section, click on the "Deploy" button.

   •Confirm the transaction in your Ethereum wallet when prompted.

6. Interact with the Contract:

   •After the contract is successfully deployed, you will see the contract interface on the right-hand side.

8. Mint Tokens (Only for Contract Owner):

   •In the contract interface, locate the "mint" function.

   •Enter the address of the recipient in the "to" field.

   •Enter the number of tokens to mint in the "amount" field.

   •Click on "transact" to mint tokens and assign them to the specified address.

9. Transfer Tokens (Any User):
   
   •In the contract interface, locate the "transfer" function.

   •Enter the recipient's address in the "to" field.

   •Enter the number of tokens to transfer in the "amount" field.

   •Click on "transact" to transfer tokens to the specified address.

10. Burn Tokens (Any User):
    
•In the contract interface, locate the "burn" function.

•Enter the number of tokens to burn in the "amount" field.

•Click on "transact" to burn the specified number of tokens.


Contract Details

Name: The name of the token.

Symbol: The symbol of the token (e.g., XYZ).

Total Supply: The total supply of tokens initially available.

Balance Of: A mapping that tracks the token balance of each address

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
