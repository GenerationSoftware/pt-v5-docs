# Claimer
[Git Source](https://github.com/GenerationSoftware/pt-v5-claimer/blob/main/src/Claimer.sol)


## State Variables
### prizePool

```solidity
PrizePool public immutable prizePool;
```


### decayConstant

```solidity
SD59x18 public immutable decayConstant;
```


### targetPrice

```solidity
uint256 public immutable targetPrice;
```


## Functions
### constructor


```solidity
constructor(PrizePool _prizePool, UD2x18 _priceDeltaScale, uint256 _targetPrice);
```

### claimPrizes


```solidity
function claimPrizes(
    IVault _vault,
    address[] calldata _winners,
    uint8[] calldata _tiers,
    uint256 _minFees,
    address _feeRecipient
) external returns (uint256);
```
**Returns**

|Name|Type|Description|
|----|----|-----------|
|`<none>`|`uint256`|Fees earned|


### estimateFees


```solidity
function estimateFees(uint256 _claimCount) external returns (uint256);
```

### _estimateFees


```solidity
function _estimateFees(uint256 _claimCount) internal returns (uint256);
```

