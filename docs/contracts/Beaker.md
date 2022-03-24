# Beaker









## Methods

### FINALIZATION_PERIOD

```solidity
function FINALIZATION_PERIOD() external view returns (uint256)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### allowance

```solidity
function allowance(address owner, address spender) external view returns (uint256)
```

Gets the allowance of `spender` on behalf of `owner`



#### Parameters

| Name | Type | Description |
|---|---|---|
| owner | address | address that approves `spender` to spend tokens
| spender | address | account that is approved to spend on behalf of `owner`

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | the remaining number of tokens that `spender` will be allowed to spend on behalf of `owner`

### approve

```solidity
function approve(address spender, uint256 amount) external nonpayable returns (bool)
```

Sets `amount` as the allowance of `spender` over the caller&#39;s tokens



#### Parameters

| Name | Type | Description |
|---|---|---|
| spender | address | address that is approved to spend tokens on behalf of `msg.sender`
| amount | uint256 | amount of tokens that `spender` can spend on behalf of `msg.sender`

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean whether the transaction was successful

### balanceOf

```solidity
function balanceOf(address account) external view returns (uint256)
```

Gets the balance of an address



#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | the amount of tokens owned by `account`

### buyoutPrice

```solidity
function buyoutPrice() external view returns (uint256)
```

Get the buyout price of the contract




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | buyout price of the contract

### buyoutVotes

```solidity
function buyoutVotes() external view returns (uint256)
```

Get the buyout votes of the contract




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | buyout votes of the contract

### claimRefund

```solidity
function claimRefund() external nonpayable returns (bool)
```

If funding is unsuccessful, contributors can reclaim their ETH




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### claimTokens

```solidity
function claimTokens(address _beneficiary) external nonpayable returns (bool)
```

Claims LP tokens after the beaker is finalized and the goal has been reached



#### Parameters

| Name | Type | Description |
|---|---|---|
| _beneficiary | address | address to receive the LP tokens

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### contribute

```solidity
function contribute(address _beneficiary) external payable returns (bool)
```

Contributes `msg.value` amount of ETH to the contract, minting a proportional amount of ERC20 LP tokens, and transferring them to the `_beneficiary` 



#### Parameters

| Name | Type | Description |
|---|---|---|
| _beneficiary | address | address to receive the LP tokens

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### decimals

```solidity
function decimals() external view returns (uint256)
```

decimals of the token




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### deposited

```solidity
function deposited(address) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### escrow

```solidity
function escrow() external view returns (address)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### execute

```solidity
function execute(address[] _targets, bytes[] _datas, uint256[] _ethTransfers) external nonpayable returns (bool)
```

Executes arbitrary contract transactions for the outright owner of the contract LP shares



#### Parameters

| Name | Type | Description |
|---|---|---|
| _targets | address[] | list of target addresses
| _datas | bytes[] | list of encoded contract calls
| _ethTransfers | uint256[] | list of ETH amount transfers

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### finalize

```solidity
function finalize() external nonpayable returns (bool)
```

Ends the crowdfunding phase when the fundraising goal is reached or when `endBlock` is reached




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### floor

```solidity
function floor() external view returns (uint256)
```

Get the buyout floor of the contract




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | buyout floor of the contract

### initialize

```solidity
function initialize(address _escrow, address _creator, uint256 _id, uint256 _endBlock, uint256 _goal, uint256 _floor, uint256 _initialBuyoutPrice, address[] _initialTargets, bytes[] _initialDatas, uint256[] _initialEthTransfers, bytes32 _tokenName) external nonpayable returns (bool)
```

Initializes the beaker contract



#### Parameters

| Name | Type | Description |
|---|---|---|
| _escrow | address | address of the escrow contract
| _creator | address | address of the contract deployer
| _id | uint256 | unique identifier of the beaker contract in the factory
| _endBlock | uint256 | block when funding ends
| _goal | uint256 | amount of funds to be raised in wei
| _floor | uint256 | minimum price at which the beaker contract can be bought out
| _initialBuyoutPrice | uint256 | buyout price set by the contract deployer
| _initialTargets | address[] | list of target addresses
| _initialDatas | bytes[] | list of encoded contract calls
| _initialEthTransfers | uint256[] | list of ETH amount transfers
| _tokenName | bytes32 | name of the ERC20 tokens unique to this contract

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### maxSupply

```solidity
function maxSupply() external view returns (uint256)
```

maximum token supply




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### name

```solidity
function name() external view returns (string)
```

Gets the name of the token




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | the name of the token

### owner

```solidity
function owner() external view returns (address)
```

Read the address of the contract owner

*returns the zero address if the contract has no owner*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | address of the contract owner

### sStore

```solidity
function sStore() external pure returns (struct Beaker.Slot)
```

Read the Slot struct out of storage




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | Beaker.Slot | Slot storage struct

### setBuyoutPrice

```solidity
function setBuyoutPrice(uint256 _newBuyoutPrice) external nonpayable returns (bool)
```

Set the address of the contract owner

*only the escrow can call this function*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _newBuyoutPrice | uint256 | the updated buyout price of the contract

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined

### setBuyoutVotes

```solidity
function setBuyoutVotes(uint256 _newBuyoutVotes) external nonpayable returns (bool)
```

Set the number of tokens voting on a buyout price

*only the escrow can call this function*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _newBuyoutVotes | uint256 | the updated number of tokens voting on the buyout price

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | Whether the transaction was successful

### setOwner

```solidity
function setOwner(address _owner) external nonpayable returns (bool)
```

Set the address of the contract owner

*only the escrow can call this function*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _owner | address | address of the contract owner

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful

### symbol

```solidity
function symbol() external view returns (string)
```

Gets the symbol of the token




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | the symbol of the token

### totalSupply

```solidity
function totalSupply() external view returns (uint256)
```

Gets the total token supply




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | the amount of tokens in existence

### transfer

```solidity
function transfer(address recipient, uint256 amount) external nonpayable returns (bool)
```

Moves `amount` tokens from the caller&#39;s account to `recipient`



#### Parameters

| Name | Type | Description |
|---|---|---|
| recipient | address | address receiving the tokens
| amount | uint256 | the amount of tokens to send to `recipient`

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean whether the transaction was successful

### transferFrom

```solidity
function transferFrom(address sender, address recipient, uint256 amount) external nonpayable returns (bool)
```

Moves `amount` tokens from `sender` to `recipient` using the allowance mechanism



#### Parameters

| Name | Type | Description |
|---|---|---|
| sender | address | address that is sending the tokens
| recipient | address | address that is receiving the tokens
| amount | uint256 | amount of tokens to be transferred

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean whether the transaction was successful



## Events

### Approval

```solidity
event Approval(address indexed owner, address indexed spender, uint256 value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| owner `indexed` | address | undefined |
| spender `indexed` | address | undefined |
| value  | uint256 | undefined |

### Contributed

```solidity
event Contributed(address indexed purchaser, address indexed beneficiary, uint256 amount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| purchaser `indexed` | address | undefined |
| beneficiary `indexed` | address | undefined |
| amount  | uint256 | undefined |

### Finalized

```solidity
event Finalized(address indexed sender)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| sender `indexed` | address | undefined |

### Refunded

```solidity
event Refunded(address indexed beneficiary, uint256 weiAmount)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| beneficiary `indexed` | address | undefined |
| weiAmount  | uint256 | undefined |

### Transfer

```solidity
event Transfer(address indexed from, address indexed to, uint256 value)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| from `indexed` | address | undefined |
| to `indexed` | address | undefined |
| value  | uint256 | undefined |



