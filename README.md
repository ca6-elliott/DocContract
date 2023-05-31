## Document Contract

The Document Token contract represents a basic token implementation for managing document ownership and transfer.

### Contract Structure

The contract is defined as `DocumentToken` in Solidity version 0.8.0 or higher.

### Token Details

The contract includes the following details for the token:

- `name`: A string representing the name of the token ("Document Token").
- `symbol`: A string representing the symbol of the token ("DOCT").
- `decimals`: An 8-bit unsigned integer representing the number of decimal places for the token.
- `totalSupply`: A `uint256` variable indicating the total supply of tokens.

### Token Ownership and Transfer

The contract manages token ownership and transfer through the following mechanisms:

- `balances`: A mapping that associates addresses with their token balances.
- `allowed`: A nested mapping that tracks the allowed token transfers between addresses.

### Events

The contract emits the following events:

- `Transfer`: Triggered when tokens are transferred from one address to another.
- `Approval`: Triggered when an address approves another address to spend tokens on their behalf.
- `DocumentAdded`: Triggered when a document is added, with the associated owner's address and document hash.

### Functions

The contract provides the following functions:

1. `balanceOf(address owner)`: Retrieves the token balance of a specific address.
2. `transfer(address to, uint256 value)`: Allows a token holder to transfer tokens to another address.
3. `transferFrom(address from, address to, uint256 value)`: Allows a third-party to transfer tokens from one address to another, subject to approval.
4. `approve(address spender, uint256 value)`: Grants approval to a spender to spend a specified amount of tokens on behalf of the owner.
5. `allowance(address owner, address spender)`: Retrieves the amount of tokens approved for spending by a specific spender on behalf of an owner.
6. `addDocument(string memory documentHash)`: Adds a document to the contract, incrementing the token balance and emitting a `DocumentAdded` event.

### Modifiers

The contract includes no modifiers.

### License

The contract is licensed under the MIT License. Refer to the SPDX-License-Identifier at the top of the code for more details.
