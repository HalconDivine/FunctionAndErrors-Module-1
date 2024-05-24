### UPLIFT 
### Description

You have a contract named Uplift that tracks three parameters: Uniform, Tuition, and Allowance, along with the last update timestamps and the total of these values during the last update. An event is defined to log these updates.

### Requirements

Initialize Values: There should be a function to initialize or set the values of Uniform, Tuition, and Allowance.
Update Values: A function to update these values and emit an event each time they are updated.
Retrieve Values: Functions to retrieve the current values and the last update times for each of the parameters.

### Functions
setValues: A function to set the initial values of Uniform, Tuition, and Allowance.
updateValues: A function to update the values and log the changes with the event.
getValues: Functions to retrieve the current values and the last updated times.

### Getting Started

To interact with this contract, you can deploy it on Remix Ethereum IDE or any Ethereum-compatible blockchain.
1. Open Remix Ethereum IDE.
2. Create a new file and paste the provided Solidity code.
3. Compile the code.
4. Deploy the contract.
5. Interact with the deployed contract by calling its functions.

```solidity
 // SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Uplift {
    uint256 public Uniform;
    uint256 public Tuition;
    uint256 public Allowance;

    uint256 public lastUpdatedUniform;
    uint256 public lastUpdatedTuition;
    uint256 public lastUpdatedAllowance;
    uint256 public totalInLastUpdate;

    // Event to log updates
    event ValuesUpdated(
        uint256 uniform,
        uint256 tuition,
        uint256 allowance,
        uint256 lastUpdatedUniform,
        uint256 lastUpdatedTuition,
        uint256 lastUpdatedAllowance,
        uint256 totalInLastUpdate
    );


```
This is the whole functionality within the code itself and the generalization of how the code will run.

### Authors

Halcon, Divine Louielyn. 
8216021@ntc.edu.ph
