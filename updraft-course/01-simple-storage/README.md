# 01 - Simple Storage

This is a basic smart contract that demonstrates fundamental Solidity concepts like variables, structs, arrays, mappings, and functions.

## What This Contract Does

- Stores and retrieves a `uint256` value (`myFavoriteNumber`)
- Allows adding people with names and favorite numbers
- Maps each person's name to their favorite number

## Key Solidity Concepts

1. Pragma
Used to define the Solidity compiler version:
`pragma solidity 0.8.19;`
// Or: ^0.8.19 — anything >=0.8.19 <0.9.0

2. Variable Types

Unsigned Integers
`uint256 myNumber = 23;` // Default size is uint256
- Other types: uint8, uint16, ..., uint256
- Default value: 0

Booleans
`bool isItDone = true;`
- Default value: false

Strings
`string message = "Hello Solidity!";`

Structs
`struct Person {
    uint256 favoriteNumber;
    string name;
}`

3. Arrays
`Person[] public listOfPeople;`
`listOfPeople.push(Person(_number, _name));`

4. Mappings
`mapping(string => uint256) public nameToFavoriteNumber;`
`nameToFavoriteNumber["Alice"] = 42;`

5. Functions
`function store(uint256 _number) public {
    myFavoriteNumber = _number;
}`

`function retrieve() public view returns (uint256) {
    return myFavoriteNumber;
}`

// `view` = read-only
// `pure` = returns computed values with no state access

## Visibility

- `public` – accessible anywhere
- `private` – only inside this contract
- `internal` – inside and child contracts
- `external` – only callable from outside (not internally)

## Memory vs Storage

- `memory` – temporary, only for function scope (e.g., `strings`, `arrays`)
- `storage` – permanent, writes to blockchain

Example:
`function addPerson(string memory _name, uint256 _number) public {
    ...
}`

## Contract Summary

- `store()`: saves a number
- `retrieve()`: returns the number
- `addPerson()`: saves a person's name and number in array + mapping

## Files

- SimpleStorage.sol – contract code
- README.md – this file
