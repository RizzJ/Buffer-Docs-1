# Buffer Options

### configure

Admin only function used to set config&#x20;

```solidity
function configure(
        uint16 _baseSettlementFeePercentageForAbove,
        uint16 _baseSettlementFeePercentageForBelow,
        uint8[4] calldata _nftTierStep
    )
```

### toggleCreation

Admin only function to pause/Unpause the option creation

```solidity
function toggleCreation()
```

### fees

Returns the fees for buying an option

```solidity
function fees(
        uint256 amount,
        address user,
        bool isAbove,
        string calldata referralCode,
        uint256 traderNFTId
    )
```

### isStrikeValid

Returns true if the strike price at which the trade is opened lies within the slippage bounds

```solidity
function isStrikeValid(
        uint256 slippage,
        uint256 strike,
        uint256 expectedStrike
    )
```

### isInCreationWindow

Checks if the market is open at the time of option creation and execution.

```solidity
function isInCreationWindow(uint256 period)
```

### runInitialChecks

Runs the basic checks for option creation

```solidity
function runInitialChecks(
        uint256 slippage,
        uint256 period,
        uint256 totalFee
    )
```

### getMaxUtilization

Returns max option amount based on the pool's capacity

```solidity
function getMaxUtilization()
```

### checkParams

Runs all the checks on the option parameters and returns the revised amount and fee

```solidity
function checkParams(OptionParams calldata optionParams)
```

### \_getSettlementFeeDiscount

Returns the discount to be applied on settlement fee based on NFT and referrer tiers

```solidity
function _getSettlementFeeDiscount(
        address referrer,
        address user,
        uint256 traderNFTId
    )
```
