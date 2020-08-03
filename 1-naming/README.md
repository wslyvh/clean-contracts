# Naming 

The naming of contracts, functions, or variables should reveal the intention, why it exists, and how it is used. If a name requires comments to explain, then it doesn’t reveal its intent.

Be consistent in your naming throughout your code. Especially when you’re working with a large codebase. Use the same names for abstract concepts, throughout multiple contracts.

Use pronounceable names.

Use searchable names.

## Code Example 

### Yes
```
contract Owned {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    modifier onlyOwner {
        require(msg.sender == owner);
        _;
    }

    function transferOwnership(address newOwner) public onlyOwner {
        owner = newOwner;
    }
}
```

### No
```
contract owned {
    address public o;

    constructor() {
        o = msg.sender;
    }

    modifier oo {
        require(msg.sender == o);
        _;
    }

    function transfer(address newOwner) public oo {
        o = newOwner;
    }
}
```

Reference: [Solidity Style guide](https://solidity.readthedocs.io/en/latest/style-guide.html)