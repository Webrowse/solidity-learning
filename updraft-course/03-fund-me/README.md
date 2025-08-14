# 03 - Fund-me

## What it does?

It is a crowd funding contract. Where anyone can deposit into the smart contract. But only the owner can withdraw.

## Conditions: 

The deposited $ETH should worth more than $5.

## File Management?

We have FundMe.sol that controls the main contract.
It checked
- if deposited fund is more than $5
- if owner is the one who is withdrawing

handles error.

Handles the recieve and callback function.

---

We created a library named PriceConverter.sol. 

It will identify the current conversion rates via chainlink.

