DefiEdge is liquidity management platform built on top of Uniswap V3. A fund/asset manager can launch a strategy to manage his personal or user's funds, earning the LP fees.

The smart contracts allows anyone to be an strategy manager and earn performance and management fee for managing other's liquidity. Everytime user deposits the funds to the DefiEdge strategy, he gets the share tokens as liquidity representation.

**DefiEdge has following major components**

0. Share Tokens
   - Everytime the user deposits funds into specific strategy, strategy will mint the shares proportional to the liquidity added by the user. The starting price of the share token would be \$100.
   - DefiEdge uses Uniswap TWAP for calculating the share price
1. Swap
   - Swap between tokens in the pool using 1inch.
2. Rebalance
   - The liquidity can be rebalanced to new ticks using one click
3. Hold
   - If the market is volatile and the manager is not able to make the decision, DefiEdge lets the manager hold the funds into the contract.
4. Performance Fees
   - Manager on DefiEdge can charge performance fees. The performance fees are debited from the fees earned in the Uniswap V3 pool of the users assets. A small portion of perfomance fees go to the protocol if the protocol fee is enabled.
5. Management Fees
   - The smart contracts also allows the managers to take upfront fees. A portion of it will also go the the protocol if the protocol fees are enabled.

### Scope

| Contract                                         | Clock |
| ------------------------------------------------ | ----- |
| contracts/base/TwapStrategyBase.sol              | 87    |
| contracts/base/TwapStrategyManager.sol           | 150   |
| contracts/base/UniswapV3TwapLiquidityManager.sol | 218   |
| contracts/libraries/TwapOracleLibrary.sol        | 183   |
| contracts/libraries/TwapShareHelper.sol          | 139   |
| contracts/DefiEdgeTwapStrategy.sol               | 176   |
| contracts/DefiEdgeTwapStrategyDeployer.sol       | 19    |
| contracts/DefiEdgeTwapStrategyFactory.sol        | 151   |
| **Total**                                        | 2016  |
