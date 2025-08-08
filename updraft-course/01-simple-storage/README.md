
# 01-simple-storage

### Few formalities of solidity smart contract

- // SPDX-License-Identifier: MIT
- pragma solidity version;
- contract NameOfTheContract {}
    (In camel case)

### WAYS TO WRITE SOLIDITY VERSION
- exact version: ```0.8.18;```
- this or above: ```^0.8.18;```
- in-between these 2 versions: ```>=0.8.0 <0.9.0;```

#### WAYS TO DECLARE VARIABLES AND THEIR DEFAULT VALUES

---
1. uint for unsigned integers takes uint8, uint16, uint32, uint64, uint128, uint256.
But if you dont write bytes, it takes uint256 by default. Same with the int for signed.

- Default Value for all uint and int = 0;
- initialize -> ```uint256 myNumber = 23;```

---

2. Boolean is simply 'bool',
- Default value for bool is false,
- initialize -> ```bool isItDone = true;```
---
3. String 
- ```string myFirstString  = "Hello Solidity!"```
---
4. Struct
- ``` solidity
    struct Person{
        uint256 aNumber;
        string name;
    } 
    ```
---
5. Arrays
- declaration: ```Person[] public listOfPeople;```
- usage: ```listOfPeople.push(dataToBePushed)```
---

### WRITE FUNCTIONS
---
```function functionName(dataType dataName) public {}```

```function functionName2 (string memory name) {}```

the heap memory things ned to be pass as argument with ```memory``` or ```call``` keyword. Since they are temporary and die with the function call.
---
### VISIBILITY KEYWORDS
---
- public: for everyone, anywhere
- private: for inside of the contract
- internal: for inside and derived contracts
- external: only for otherside.
---
### MISCELLENEOUS KEYWORDS
---
When you don't want to change the state of the data on-chain:
- view: when you just want to return a variable.
- pure: when you want to return a fixed value, nothing derived.
---
### MAPPING
---
declaration: ```mapping(string => uint256) public stringToNumber```

usage: ```stringToNumber[putStringHere] = uint256-NumberVariable```

this maps a string to a uint256 number, that will be connected 



