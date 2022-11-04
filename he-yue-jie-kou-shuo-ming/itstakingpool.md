# ITStakingPool

此合约用于IT挖矿充值和提现

## 合约信息

bscTestnet：0x85631D304d8F4F613eED7184211C2a45e9D3BF3A

bsc：

abi： [https://github.com/defx-vip/ironman-contract-core/blob/main/abi/ITStakingPool.json](https://github.com/defx-vip/ironman-contract-core/blob/main/abi/ITStakingPool.json)

## Functions <a href="#functions" id="functions"></a>

### bindUser(绑定用户)

```solidity
function bindUser(address teamAddress) external;
```

绑定用户

邀请人地址(teamAddress)必须是已经购买过算力的地址或者顶级帐号地址

#### Parameters:

|             |          |                 |
| ----------- | -------- | --------------- |
| **Name**    | **Type** | **Description** |
| teamAddress | address  | 邀请人地址           |

### deposit(购买算力)

```solidity
function deposit(uint256 amount) external;
```

购买算力

用户需要先绑定邀请人后才能购买算力。购买算里会扣款用户对应的IT代币，因此请先调用IT合约的approve函数为本合约授权后才能调用

#### Parameters:

|          |          |                 |
| -------- | -------- | --------------- |
| **Name** | **Type** | **Description** |
| amount   | uint256  | 购买数量            |

### withdrawal(提现)

```solidity
function withdrawal(uint256 amount) external payable;
```

用户提现

调用函数时需要发送0.03个bnb用作手续费。

#### Parameters:

|          |          |                 |
| -------- | -------- | --------------- |
| **Name** | **Type** | **Description** |
| amount   | uint256  | 提现数量            |

### userList(获取用户信息)

```solidity
function userList(address user) external view returns(
    address superior,
    uint256 stakingAmount,
    uint256 earnedAmount
);
```

获取用户信息

#### Parameters:

|          |          |                 |
| -------- | -------- | --------------- |
| **Name** | **Type** | **Description** |
| user     | address  | 用户地址            |

#### **Return Values:**

|               |          |                 |
| ------------- | -------- | --------------- |
| **Name**      | **Type** | **Description** |
| superior      | address  | 邀请人地址           |
| stakingAmount | uint256  | 已购买的算力力         |
| earnedAmount  | uint256  | 已提现             |
