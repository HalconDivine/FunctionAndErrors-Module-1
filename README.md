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
    // state variables
    uint256 public Uniform;
    uint256 public Tuition;
    uint256 public allowance;

    // function to set reimbursement amounts
    function setReimbursement(uint256 _Uniform, uint256 _Tuition, uint256 _allowance) public {
        require(_Uniform > 0 || _Tuition > 0 || _allowance > 0, "Please enter amount");

        Uniform = _Uniform;
        Tuition = _Tuition;
        allowance = _allowance;
    }

    function assertTotalAmount() public view returns (uint256) {
        uint256 totalAmount = Uniform + Tuition + allowance;
        // Ensure the total amount is greater than 0
        assert(totalAmount > 0);
        return totalAmount;
    }

    // Function to revert if no amounts are set
    function revertIfNoAmount() public view {
        if (Uniform == 0 && Tuition == 0 && allowance == 0) {
            revert("Please enter amount");
        }
    }
}

```
