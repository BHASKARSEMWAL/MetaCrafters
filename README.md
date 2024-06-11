#TestContract

This Solidity program is a simple "TestContract" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works, particularly focusing on using require(), assert(), and revert() statements.

##Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract includes functions that demonstrate the use of require(), assert(), and revert() for enforcing conditions, checking invariants, and handling errors. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

##Getting Started

###Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at Remix IDE.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., TestContract.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract TestContract {
    address public owner;
    uint public count;

    constructor() {
        owner = msg.sender;
        count = 0;
    }

    // Function to demonstrate require()
    function increment() public {
        // Use require to ensure only the owner can increment the count
        require(msg.sender == owner, "Only the owner can increment");
        count += 1;
    }

    // Function to demonstrate assert()
    function incrementBy(uint amount) public {
        // Use require to ensure only the owner can increment the count
        require(msg.sender == owner, "Only the owner can increment");

        // Use assert to check for overflow (not necessary in Solidity 0.8+ due to built-in overflow checks, but shown for illustration)
        uint newCount = count + amount;
        assert(newCount >= count); // This should never fail
        
        count = newCount;
    }

    // Function to demonstrate revert()
    function resetCount(uint newCount) public {
        // Check if the new count is within an acceptable range
        if (newCount > 100) {
            revert("New count must be 100 or less");
        }

        // Use require to ensure only the owner can reset the count
        require(msg.sender == owner, "Only the owner can reset the count");

        count = newCount;
    }
}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile TestContract.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "TestContract" contract from the dropdown menu, and then click on the "Deploy" button.

###Interacting with the Contract
Once the contract is deployed, you can interact with its functions:

Check Initial State: Click on the owner and count variables to see their initial values.
Call increment(): Click the increment button. If the caller is the owner, the count should increase by 1. Check the count variable to see the updated value.
Call incrementBy(uint amount): Enter a value (e.g., 10) in the input box next to incrementBy and click the incrementBy button. If the caller is the owner and no overflow occurs, the count should increase by the specified amount. Check the count variable to see the updated value.
Call resetCount(uint newCount): Enter a value (e.g., 50) in the input box next to resetCount and click the resetCount button. If the caller is the owner and the new count is 100 or less, the count should reset to the specified value. Check the count variable to see the updated value. Enter a value greater than 100 to see the revert in action.

##Authors
Bhaskar Semwal
[ndabhaskar13@gmail.com(E-mail)]

##License
This project is licensed under Bhaskar Semwal License - see the LICENSE.md file for details
