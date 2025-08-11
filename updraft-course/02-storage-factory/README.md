# 02 - Storage Factory

A smart contract that deploy another smart contract.

---

## Storagefactory.sol
Imports SimpleStorage contract.
use **sfStore** function takes one input to save 2 numbers: 
- Index Number,
- Storage Number

saved the array of numbers it to the state using `store()` function.

Use another function **sfGet()** to retrieve the number using the index number.
It uses `retrieve()` function to get the number from index.

## SimpleStorage.sol
This file hold many contracts.
SimpleStorage was named imported to the StorageFactory.sol
---
`store()` takes one input and have `virtual` keyword on.
`retrieve()` used for retrieving the stored number.
`addPerson()` it adds person struct that contains `string name` and `uint256 favoriteNumber`, pushed onto an array. map it to index.

## AddFiveStorage.sol
It import SimpleStorage contract from SimpleStorage.sol.
`AddFiveStorage()`: Overrides store() function of SimpleStorage with `override` keyword.
It adds 5 to the input number.

---