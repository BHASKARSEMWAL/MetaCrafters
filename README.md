# ELECTIONS

This Solidity program i.e. "ELECTIONS" is a simple program that demonstrates Use of Error Handling Functions in Solidity programming language. The purpose of this program is to provide the use of Error Handling Functions i.e. require(), assert(), revert().

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a two different functions which checks whether an individual is Eligible for Voting or not. This program serves as a simple and straightforward introduction to Error Handling in Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Elections.sol). Copy and paste the following code into the file:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

contract Elections{

    function isEligible(uint age) public  pure  returns(string memory){
        require(age>=18,"Candidate is NOT eligible for Voting this year");
        return "Eligible for Voting";
    }

    function checking(uint age)public pure returns(string memory){
        bool result;
        assert(age>=18);
        result=true;

        if(result==true){
            return "YES";
        }
        revert("NOT ELIGIBLE");
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile Elections.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Elections" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the Checking & isEligible functions. Click on the "Elections" contract in the left-hand sidebar, and then click on the "Checking" and "isEligible" functions. Finally, click on the "transact" button to execute the function and retrieve the "Eligible" or "Not Eligible" message.

## Authors

Bhaskar Semwal   
ndabhaskar13@gmail.com(E-mail)


## License

This project is licensed under Bhaskar Semwal License - see the LICENSE.md file for details
