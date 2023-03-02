# Liquidity Pool

### setHandler

Admin function to set handlers

```solidity
function setHandler(address _handler, bool _isActive)

```

### setMaxLiquidity

Admin function to set max liquidity

```solidity
function setMaxLiquidity(uint256 _maxLiquidity)

```

### Provide

Public function to add liquidity

```solidity
function provide(uint256 tokenXAmount, uint256 minMint)

```

### provideForAccount

Handler only function to add liquidity for an account

```solidity
function provideForAccount(
        uint256 tokenXAmount,
        uint256 minMint,
        address account
    )
```

### Withdraw

Public function to remove liquidity

```solidity
function withdraw(uint256 tokenXAmount) 
```

### withdrawForAccount

Handler only function to remove liquidity for an account

```solidity
function withdrawForAccount(uint256 tokenXAmount, address account)

```

### toTokenX

Returns tokenX equivalent of a certain amount BLP

```solidity
function toTokenX(uint256 amount)
```

### getUnlockedLiquidity

Returns available liquidity

```solidity
function getUnlockedLiquidity(address account)
```

### shareOf

Returns provider's share in tokenX

```solidity
function shareOf(address account)
```

### availableBalance

Returns the amount of tokenX available for withdrawals

```solidity
function availableBalance()
```

### totalTokenXBalance

Returns the total balance of tokenX provided to the pool

```solidity
function totalTokenXBalance()
```
