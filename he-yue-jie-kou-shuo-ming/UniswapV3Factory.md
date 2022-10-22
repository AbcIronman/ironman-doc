---
Uniswap 兑换合约: v1
---

# UniswapV3Factory
Deploys Uniswap V3 pools and manages ownership and control over pool protocol fees

## 合约信息

bscTestnet： 0xe47BfD6D4CC051d87d7B2489A5a6c84cB2c33702

bsc：0x0F79a7822Bc004da6A195f034563c56D9bBA306A

ABI: [https://github.com/defx-vip/ironman-contract-core/blob/main/abi/MarkOneNft.json](https://github.com/defx-vip/ironman-contract-core/blob/main/abi/MarkOneNft.json)

## Functions
### createPool
``` solidity
  function createPool(
    address tokenA,
    address tokenB,
    uint24 fee
  ) external returns (address pool)
```
Creates a pool for the given two tokens and fee

tokenA and tokenB may be passed in either order: token0/token1 or token1/token0. tickSpacing is retrieved from the fee. The call will revert if the pool already exists, the fee is invalid, or the token arguments are invalid.

Some Markdown text with <span style="color:blue">some *blue* text</span>.

#### Parameters:
| Name        | Type | Description |
| ----------- | -------- | -----------------------------------------------|
| tokenA      | address  | One of the two tokens in the desired pool      |
| tokenB      | address  | The other of the two tokens in the desired pool|
| fee         | uint24   | The desired fee for the pool|

#### Return Values:
| Name        | Type | Description |
| ----------- | -------- | -----------------------------------------------|
| pool        | address   | The address of the newly created pool|
