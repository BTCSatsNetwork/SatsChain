> To set up a directory for Foundry with Git, ensure the directory is empty and not linked to another Git branch. Use the git init command in the directory to create a new Git repository, which allows Foundry to work correctly. This process is crucial for proper version control and integration with Foundry.

## Initialize the foundry directory
```
forge init 
```
## Install an open-source solidity repo
```
forge install OpenZeppelin/openzeppelin-contracts
```
## Open the directory by vs-code
```
code .
```
## Modify "Counter.sol"
1. Rename the file to "TokenTest.sol"
2. Modify the "TokenTest.sol" code as follows:
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.13;
import "lib/openzeppelin-contracts/contracts/token/ERC20/ERC20.sol";

contract TokenTest is ERC20 {
    constructor() ERC20("SatsChain", "SatsChain") {
        _mint(msg.sender, 1000 * 10 ** 18);
    }
} 
```
## Modify "Counter.s.sol"
1. Rename the file to "TokenTest.s.sol"

2. Modify the "TokenTest.s.sol" code as follows:
```
// SPDX-License-Identifier: UNLICENSED
// scripts/DeployContract.s.sol
pragma solidity ^0.8.13;

import "forge-std/Script.sol";
import "../src/TokenTest.sol";

contract DeployContract is Script {
    function run() public returns(TokenTest){
        vm.startBroadcast();
        TokenTest tokenTest = new TokenTest(/* constructor arguments */);
        vm.stopBroadcast();
        return tokenTest; 
    }
}
```
## Delete "test.sol"
It's optional. You may adjust the code accordingly.

## Add a ".env" File
```
ETH_RPC_URL=
PRIVATE_KEY=
VERIFIER_URL=https://scan-canary-test-api.bevm.io/api
```
## Activate ".env"
```
source .env
```
## Deploy and verify  your contract
> When utilizing SatsChain Mainnet, to align the Solidity version correctly, you may insert "solc_version = "0.8.13" " into the "foundry.toml" file within the "[profile.default]" section. This adjustment may require you to modify certain dependencies.

```
forge script script/TokenTest.s.sol --rpc-url $ETH_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --verifier blockscout --verifier-url $VERIFIER_URL
```
Afterward, the current status is provided beneath.


