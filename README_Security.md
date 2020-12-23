# SnowSwap Security Review by Quantstamp

Link: https://hackmd.io/@9GUQpanJRF6cloQ0fwyPFw/r1_ctUuqv

## Follow-up to individual QSPs
1. Wrong version of the contracts were initially sent to QS. This issue has been resolved. 
2. We can’t fix a deployed contract but we as a team have agreed not to make any reductions to the A parameters. If any updates are made by a byzantine entity there is a timelock period so vulnerability will not be immediate (will take 3 days). For future contracts we will use the latest version of Curve’s stableswap.vy which includes a ramp_A() method that fixes this issue. 
3. We tested this contract extensively on both testnets and mainnet and are satisfied with the comprehensiveness of our testing, especially since the contract in question has been battle-tested by hundreds of millions in deposits via multiple protocols without issues. 
4. Can be ignored, nothing new will be done with oUSD until vulns are fixed. We are only keeping the pool on the website so people can unstake. 
5. This issue was previously raised by users and we resolved it by adding an exit function which allows the user to unstake without claiming. 

6. OUSD related -- no longer relevant 
7. Added input validation where necessary 
8. OUSD related -- no longer relevant 
9. This functionality existed in an undeployed release candidate of the contracts and has since been removed. In any case, StakingRewardsFactory deals only with the rewardToken, and does not touch user funds at any point. 
10. Pragma has been locked to 0.5.16 for StakingRewardsFactory.sol
