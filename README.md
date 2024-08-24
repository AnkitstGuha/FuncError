# FuncError
## Overview

In Solidity, error handling is crucial for ensuring that smart contracts behave as expected. Three common mechanisms for error handling are `require`, `revert`, and `assert`. Each serves a distinct purpose and is used in different scenarios.

## `require()`

The `require` statement is used to validate conditions before executing further code. If the condition fails, it reverts the transaction and provides an error message. This is typically used to check inputs, validate conditions before executing code, and ensure that the state of the contract is correct.

### Example

```solidity
function requireStatement(uint number) public pure {
    require(number > 0, "Number must be greater than zero.");
}
```

## Revert()
- revertStatement(): This function takes a number as a parameter and includes an example of using the revert() statement. 
- If the number is zero, it triggers a revert with the message "Number is odd". It causes EVM to set all changes made to their initial stage.
```solidity
function revertStatement(uint number) public pure {
    if (number == 0) {
        revert("Number must not be zero.");
    }
}
```
## Assert()
- assertStatement(): This function takes a number as a parameter and demonstrates the usage of the assert() statement. It checks if the number is within the range of 0 to 99 (both inclusive).
- Mostly used to find internal error and check for the given condition.
```solidity
function assertStatement(uint number) public pure {
    assert(number >= 0 && number <= 99);
}

```
