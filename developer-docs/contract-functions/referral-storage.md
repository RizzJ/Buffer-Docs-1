# Referral Storage

### **registerCode**

Public function for setting the user's referral code.

```solidity
function registerCode(string memory _code)
```

### configure

Admin function to set the config for step reduction and discount on the basis of tier

```solidity
function configure(
        uint8[3] calldata _referrerTierStep,
        uint32[3] calldata _referrerTierDiscount // Factor of 1e5
    )
```

### setReferrerTier

Admin function to set referrer's tier

```solidity
function setReferrerTier(address _referrer, uint8 tier)
```
