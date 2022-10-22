---
description: v1
---

# MarkNft

此合约包含了钢铁侠创世NFT、钢铁战衣NFT、钢铁战甲NFT，通过nftType可以区分上述NFT的三种类型。合约兼容ERC721,以下"接口定义"中没有描述ERC721中的事件和函数，查看ERC721方法和事件请前往 [https://docs.openzeppelin.com/contracts/3.x/api/token/erc721](https://docs.openzeppelin.com/contracts/3.x/api/token/erc721)

## 合约信息

bscTestnet： 0xe47BfD6D4CC051d87d7B2489A5a6c84cB2c33702

bsc：0x0F79a7822Bc004da6A195f034563c56D9bBA306A

ABI: [https://github.com/defx-vip/ironman-contract-core/blob/main/abi/MarkOneNft.json](https://github.com/defx-vip/ironman-contract-core/blob/main/abi/MarkOneNft.json)

## Functions <a href="#functions" id="functions"></a>

### buyMarkOneNFT

```solidity
function buyMarkOneNFT(address teamAddress) external;
```

购买钢铁侠创世NFT

邀请人地址(teamAddress)必须是已经购买过创世NFT的用户地址或者零地址。购买创世NFT会扣款用户10USDT，因此请先调用USDT(测试网为UsdtMock)合约的approve函数为本合约授权后才能调用

#### Parameters:

|             |          |                 |
| ----------- | -------- | --------------- |
| **Name**    | **Type** | **Description** |
| teamAddress | address  | 邀请人地址       |

#### Return Values:
