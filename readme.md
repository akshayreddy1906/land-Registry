# Land Registry Smart Contract

A Solidity smart contract for managing land parcels and ownership records on the blockchain.

Created for the VOIS Foundation's Blockchain Internship Program.

## Features

- Register new land parcels with unique IDs
- Transfer land ownership
- Query land details
- Verify land registration status

## Contract Details

- License: MIT
- Solidity Version: ^0.8.0

## Functions

### registerLand
```solidity
function registerLand(uint256 _id, string memory _location, uint256 _area) public
```
Registers a new land parcel with specified ID, location, and area.

### transferOwnership
```solidity
function transferOwnership(uint256 _id, address _newOwner) public
```
Transfers land ownership to a new address.

### getLand
```solidity
function getLand(uint256 _id) public view returns (uint256, string memory, uint256, address, bool)
```
Returns complete details of a registered land parcel.

### isLandRegistered
```solidity
function isLandRegistered(uint256 _id) public view returns (bool)
```
Checks if particular land is registered.

## Events

- `LandRegistered`: Emitted when new land is registered
- `OwnershipTransferred`: Emitted when land ownership changes

## Data Structure

```solidity
struct Land {
    uint256 id;
    string location;
    uint256 area;
    address owner;
    bool registered;
}
```

## Security Considerations

- Only land owners can transfer ownership
- Duplicate land IDs cannot be registered
- All functions include appropriate access controls

## License

This project is licensed under the MIT License.
