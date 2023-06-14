# ETHassessment_Barsabal
# Creating a Token in ETH
 This Solidity program is a simple token generator program that utilizes the basic functions of solidity through creating and running token transactions in Ethereum. The purpose of this project is to help new users understand the functionalities of running a program in Solidity see through how it works.

## Description

This program uses the basic functions of Solidity and shows how it runs through creating or distributing tokens to accounts. Basically, Solidity is a programming language that is used for producing smart contracts (programs that are stored on a blockchain) inside the Ethereum blockchain. This program contains functions that varies through the user's expense, in which they will be able to generate values of tokens and return it's balances to the existing amount of the user's account. They will be able to edit values on multiple addresses or tokens through adding and subtracting their amounts. This program will serve as an overview of how Ethereum Blockchain works inside the Solidity programming language.

## Getting Started

### Where to Access

To run this program, you can use Remix, which is an online Solidity IDE. To get started and use the code provided, go to the Remix website at https://remix.ethereum.org/.

### Executing program

Once inside the IDE, click on the "+" button on the left-hand sidebar to create a new file inside the existing Workspace, or create a new workspace for yourself depending on how you want to use it. After that Save the file with a .sol extension at the end (e.g. IamHandsome.sol). Copy and paste the following code into the file:
```
contract MyToken {

    // public variables here
    string public tokenName = "Thirdy";
    string public tokenAbbrv = "3rdy";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public remainder;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        remainder[_address] += _value;
    }

    // burn function
    function burn (address _address ,uint _value) public {
        if (remainder[_address] >= _value) {
        totalSupply -= _value;
        remainder[_address] -= _value;
    }
  }
}
```
* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button
* After a successful compilation, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar just below the Solidity Compiler tab. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.
* From there, you will be able to see the contract deployed and be able to transact values from the mint function (used for adding tokens) , burn function (used for subtracting the amount of tokens inside the address , and the remainder function (displays the current deposited amount of your tokens)

## Authors

Contributors names and contact info

Benito Barsabal
@bmbarsabal@gmail.com


## License

This project is licensed under the Benito M. Barsabal III License - see the LICENSE.md file for details
