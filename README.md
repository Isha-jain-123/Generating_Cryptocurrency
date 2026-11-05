# Generating Cryptocurrency

A minimal ERC-20 token written in Solidity. The contract creates a token called **DevToken** (symbol **DVT**) and mints 1 000 tokens to the deployer's address.

## Contract

`Token.sol` inherits from the OpenZeppelin `ERC20` base contract, so it comes with the full ERC-20 interface (transfers, allowances, balances, etc.) out of the box.

```solidity
contract DevToken is ERC20 {
    constructor() ERC20("DevToken", "DVT") {
        _mint(msg.sender, 1000 * 10 ** 18);
    }
}
```

## Setup

1. Install [Node.js](https://nodejs.org/) and a Solidity development framework such as [Hardhat](https://hardhat.org/) or [Remix](https://remix.ethereum.org/).
2. Install the OpenZeppelin contracts library:

   ```bash
   npm install @openzeppelin/contracts
   ```

3. Compile and deploy `Token.sol` to a local or test network.

## License

GPL-3.0
