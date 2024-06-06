# MyToken

This Solidity program is a simple "MyToken" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.


## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "Hello World!". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
      string public tokenName="META";
      string public tokenAbbrv="MTA";
      uint public totalSupply=0;

    // mapping variable here
        mapping(address => uint) public balances;
    // mint function

    function mint(address _address,uint _value) public{
        totalSupply +=_value;
        balances[_address] +=_value;
    }
    // burn function
    function burn (address _address,uint _value) public{
        if(balances[_address] >=_value){
            totalSupply -= _value;
            balances[_address] -=_value;
        }
    }
}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.
Once the contract is deployed, we will simply paste the address to our Mint function as a address Parameter as well as a Value into  it....after it we simply check the totalSupply and balances.

## Authors

Bhaskar Semwal 
[ndabhaskar13@gmail.com(E-mail)]


## License

This project is licensed under the Bhaskar Semwal License - see the LICENSE.md file for details
