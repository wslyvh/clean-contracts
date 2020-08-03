# Structure & Ordering

Ordering helps readers identify which functions they can call and to find the constructor and fallback definitions easier.

## Code Example 

### Yes

```
contract MyContract {
    constructor() {
        // ...
    }

    receive() external payable {
        // ...
    }

    fallback() external {
        // ...
    }

    // External functions
    // ...

    // External functions that are view
    // ...

    // External functions that are pure
    // ...

    // Public functions
    // ...

    // Internal functions
    // ...

    // Private functions
    // ...
}
```

### No 

```
contract MyContract {

    // External functions
    // ...

    fallback() external {
        // ...
    }
    receive() external payable {
        // ...
    }

    // Private functions
    // ...

    // Public functions
    // ...

    constructor() {
        // ...
    }

    // Internal functions
    // ...
}
```

Reference: [Solidity Style guide](https://solidity.readthedocs.io/en/latest/style-guide.html)