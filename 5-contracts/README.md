# Contracts & Data structures

Clear separation of your contracts and data storage is important, due to the contract’s immutability. If you want to add logic or deploy new contracts, you want to be able to utilize the existing data structures. Separating the two can be done by storage contracts. We’ll cover these in more detail in another blog post.

A common pattern is by using Eternal Storage. This is a smart contract that only contains data, sort of a key/value store, and no other business logic. This is similar to a database in a more traditional web application.

```
contract EternalStorage {

    mapping(bytes32 => uint) uIntStorage;
    mapping(bytes32 => address) addressStorage;

    function getUint(bytes32 _key) external view returns(uint) {
        return uIntStorage[_key];
    }

    function getAddress(bytes32 _key) external view returns(address) {
        return addressStorage[_key];
    }

    function setUint(bytes32 _key, uint _value) external {
        uIntStorage[_key] = _value;
    }

    function setAddress(bytes32 _key, address _value) external {
        addressStorage[_key] = _value;
    }

    function deleteUint(bytes32 _key) external {
        delete uIntStorage[_key];
    }

    function deleteAddress(bytes32 _key) external {
        delete addressStorage[_key];
    }
}
```

