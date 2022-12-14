
# Optimism City Pathfinder smart contract project bootstrapped with Foundry + Hardhat

## Use with Foundry

Make sure to install foundry locally first: https://book.getfoundry.sh/getting-started/installation

```
git clone https://github.com/atlantis-world-core/op-pathfinder-contract.git
cd op-pathfinder-contract
forge install
```
### Test

```
forge test -vv --gas-report
```

### Deploy

```
forge create src/AWOptimismCityPathfinder.sol:AWOptimismCityPathfinder --rpc-url <RPC_URL> --private-key <PRIVATE_KEY> --legacy --gas-limit 10000000
```

### Verify
```
forge verify-contract --chain-id <chain_id> --num-of-optimizations 1000000 --watch --compiler-version v0.8.15+commit.e14f2714 <the_contract_address> src/AWOptimismCityPathfinder.sol:AWOptimismCityPathfinder <your_etherscan_api_key>
```

### Send transaction

```
cast send <CONTRACT_ADDRESS> "airdrop(address)()" <ADDRESS> --rpc-url <RPC_URL> --private-key <PRIVATE_KEY> --legacy --gas 1000000
```

## Use with Hardhat

```
npm ci
npm run test
```