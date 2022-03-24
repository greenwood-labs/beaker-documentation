# BeakerERC20









## Methods

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

### decimals

```solidity
function decimals() external view returns (uint256)
```

decimals of the token




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

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



