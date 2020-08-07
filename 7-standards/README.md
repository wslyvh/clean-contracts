# Standards & Libraries

An intrinsic feature of smart contracts is its composability. Turning every contract into a component and potential building block that others can leverage. A lot of these building blocks exist already and standards ensure the ease of use and development. 

The most well-known standard was created for the emerging token ecosystem and the exchanges serving it: the ERC20 standard.

```
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract ExampleToken is ERC20 {
    constructor(uint256 initialSupply) public ERC20("Example", "XMPL") {
        _mint(msg.sender, initialSupply);
    }
}
```

- Ethereum Improvement Proposals (EIPs) describe standards for the Ethereum platform, including contract standards. [Finalized ERC's](https://eips.ethereum.org/erc#final)
- [OpenZeppelin Contracts](https://openzeppelin.com/contracts/)
