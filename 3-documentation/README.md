# Documentation & Natspec 

Solidity contracts can have a form of comments that provide rich documentation to others reading the code as well as end-users. This is called the Ethereum Natural Language Specification Format, or NatSpec.

This documentation is segmented into developer-focused messages and end-user-facing messages. These messages may be shown to the end-user (the human) at the time that they will interact with the contract (i.e. sign a transaction).

It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI).

## Code Example 

```
/// @author The Solidity Team
/// @title A simple storage example
contract SimpleStorage {
    uint storedData;

    /// Store `x`.
    /// @param x the new value to store
    /// @dev stores the number in the state variable `storedData`
    function set(uint x) public {
        storedData = x;
    }

    /// Return the stored value.
    /// @dev retrieves the value of the state variable `storedData`
    /// @return the stored value
    function get() public view returns (uint) {
        return storedData;
    }
}
```

Reference: [NatSpec](https://solidity.readthedocs.io/en/latest/natspec-format.html)