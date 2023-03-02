# Option Router

### initiateTrade

Public function for users to initialize their trades.

```solidity
function initiateTrade(
        uint256 totalFee,
        uint256 period,
        bool isAbove,
        address targetContract,
        uint256 expectedStrike,
        uint256 slippage,
        bool allowPartialFill,
        string memory referralCode,
        uint256 traderNFTId
    )
```

### cancelQueuedTrade

Public function for users to cancel their trades.

```solidity
function cancelQueuedTrade(uint256 queueId)
```

### resolveQueuedTrades

Function for keepers to open/cancel the queued trades

```solidity
function resolveQueuedTrades(OpenTradeParams[] calldata params)
```

### unlockOptions

Function for keepers to close the expired trades

```solidity
function unlockOptions(CloseTradeParams[] calldata optionData)
```

### setContractRegistry

Admin function to set/unset the asset pairs for trading

```solidity
function setContractRegistry(address targetContract, bool register)
```

### setKeeper

Admin function to set/unset keepers

```solidity
function setKeeper(address _keeper, bool _isActive)
```

### setInPrivateKeeperMode

Admin function to set/unset private keeper mode

```solidity
function setInPrivateKeeperMode() external onlyRole(DEFAULT_ADMIN_ROLE)
```
