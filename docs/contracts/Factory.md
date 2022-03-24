# Factory









## Methods

### accountBeakers

```solidity
function accountBeakers(address) external view returns (uint256)
```

mapping to retreive the id of the beaker contract by its creator



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### beakerCount

```solidity
function beakerCount() external view returns (uint256)
```

the number of deployed beakers contracts




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

### computeBeakerAddress

```solidity
function computeBeakerAddress(address _creator, uint256 _beakerId) external view returns (address instance)
```

Computes deploying beaker contract address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _creator | address | undefined
| _beakerId | uint256 | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| instance | address | undefined

### createBeaker

```solidity
function createBeaker(uint256 _endBlock, uint256 _goal, uint256 _floor, uint256 _initialBuyoutPrice, address[] _initialTargets, bytes[] _initialDatas, uint256[] _initialEthTransfers, bytes32 _tokenName) external nonpayable returns (address beaker)
```

Creates a new beaker contract



#### Parameters

| Name | Type | Description |
|---|---|---|
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
| beaker | address | The address of the deployed beaker contract

### escrow

```solidity
function escrow() external view returns (address)
```

escrow contract address




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### getBeaker

```solidity
function getBeaker(uint256) external view returns (address)
```

mapping to retrieve a beaker contract using its ID



#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### governance

```solidity
function governance() external view returns (address)
```

protocol governance address




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### implementation

```solidity
function implementation() external view returns (address)
```

reference contract address for clones




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined

### isPaused

```solidity
function isPaused() external view returns (bool)
```

whether the factory is paused




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined

### setEscrow

```solidity
function setEscrow(address _newEscrow) external nonpayable returns (bool)
```

Sets the escrow contract address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _newEscrow | address | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean whether the transaction was successful

### setImplementation

```solidity
function setImplementation(address _implementation) external nonpayable returns (bool)
```

Sets the current beaker implementation address



#### Parameters

| Name | Type | Description |
|---|---|---|
| _implementation | address | undefined

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean whether the transaction was successful

### togglePause

```solidity
function togglePause() external nonpayable returns (bool)
```

toggles the pausing of beaker contract creation




#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | boolean Whether the transaction was successful



## Events

### BeakerCreated

```solidity
event BeakerCreated(address indexed deployer, uint256 id)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| deployer `indexed` | address | undefined |
| id  | uint256 | undefined |



