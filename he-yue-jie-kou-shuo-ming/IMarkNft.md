
## IMarkNft










### BuyMarkOneNFT

```solidity
event BuyMarkOneNFT(address user, address teamAddress, uint256 tokenId, uint256 price)
```

在购买创世NFT时触发,会触发的函数有buyMarkOneNFT


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | NFT接收者 |
| teamAddress | address | 邀请人地址 |
| tokenId | uint256 | nft id |
| price | uint256 | 购买支付的价格 |





### AirdropSevenNFT

```solidity
event AirdropSevenNFT(address user, uint256 tokenId)
```

在兑换钢铁战衣时触发,会触发的函数有getAirdropSevenNFT


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | NFT接收者 |
| tokenId | uint256 | nft id |





### AirdropFortyFourNFT

```solidity
event AirdropFortyFourNFT(address user, uint256 tokenId)
```

在兑换钢铁战甲时触发,会触发的函数有getAirdropFortyFourNFT


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | NFT接收者 |
| tokenId | uint256 | nft id |




### buyMarkOneNFT

```solidity
function buyMarkOneNFT(address teamAddress) external
```

购买钢铁侠创世NFT

_邀请人地址(teamAddress)必须是已经购买过创世NFT的用户地址或者零地址_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| teamAddress | address | 邀请人地址 |




### getAirdropSevenNFT

```solidity
function getAirdropSevenNFT() external
```

领取钢铁战衣NFT

_需要直推用户至少10人才能钢铁战衣NFT_





### getAirdropFortyFourNFT

```solidity
function getAirdropFortyFourNFT() external
```

领取钢铁战甲NFT

_需要直推用户至少6人并且这6人都邀请满10人才能领取钢铁战甲NFT_





### markOnePrice

```solidity
function markOnePrice() external view returns (uint256 markOnePrice)
```

获取钢铁侠创世NFT价格



#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| markOnePrice | uint256 | 钢铁侠创世NFT价格 |



### idoStartTime

```solidity
function idoStartTime() external view returns (uint256 idoStartTime)
```

获取ido开始时间



#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| idoStartTime | uint256 | ido开始时间 |



### deadlineTime

```solidity
function deadlineTime() external view returns (uint256 deadlineTime)
```

获取ido结束时间



#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| deadlineTime | uint256 | ido结束时间 |



### userMap

```solidity
function userMap(address user) external view returns (address superior, uint8 level, uint256 childLv1Count, uint256 childLv2Count, bool receivedAirdrop1, bool receivedAirdrop2)
```

获取ido用户信息


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | 用户地址 |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| superior | address | 上级用户 |
| level | uint8 | 用户等级 0:未购买创世NFT(未参加IDO) >0:已购创世NFT(已参加IDO) |
| childLv1Count | uint256 | 直推用户个数 |
| childLv2Count | uint256 | 直推用户并邀请满10人的个数 |
| receivedAirdrop1 | bool | 是否领取钢铁战衣 |
| receivedAirdrop2 | bool | 是否领取钢铁战甲 |



### totalSupplyMap

```solidity
function totalSupplyMap(uint8 nftType) external view returns (uint256 totalSupply)
```

获取nft已铸造信息


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftType | uint8 | nft类型 0:钢铁侠NFT 1:钢铁战衣 2:钢铁战甲 |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| totalSupply | uint256 | 已铸造数量 |




### MintMarkNFT

```solidity
event MintMarkNFT(address user, uint256 tokenId, uint256 displayId, uint8 nftType, uint256 durability)
```

在铸造NFT时触发,会触发的函数有buyMarkOneNFT,getAirdropSevenNFT


#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| user | address | NFT接收者 |
| tokenId | uint256 | nft id |
| displayId | uint256 | NFT页面展示Id |
| nftType | uint8 | nft类型 0:钢铁侠NFT 1:钢铁战衣 2:钢铁战甲 |
| durability | uint256 | 耐久属性 |



