# FarmPot-Investment-protocol

PharaohFarmPoTFull
PharaohFarmPoTFull is a smart contract that allows users to make deposits and earn rewards through a referral system. It is implemented in Solidity and includes features such as depositing, withdrawing, claiming rewards, and referral rewards.

Getting Started
To get started with PharaohFarmPoTFull, follow the steps below:

Prerequisites
Make sure you have an Ethereum wallet to interact with the contract.
You will need the address of the CAFToken contract (0xf8e81D47203A594245E36C48e151709F0C19fBe8).
Deployment
Deploy the PharaohFarmPoTFull contract on the Ethereum network.
Set the MIN_DEPOSIT_AMOUNT constant to specify the minimum deposit amount required.
Set the startTime variable to the current timestamp.
Contract Details
The PharaohFarmPoTFull contract includes the following features:

Deposit
Function: deposit(uint256 amount, address referAddress)

Allows users to make a deposit by specifying the deposit amount and referral address.
Validates the deposit amount against the minimum deposit amount.
Transfers the specified amount of CAFToken from the user to the contract.
Calculates the final deposit amount after deducting the deposit tax.
Sets the maximum payout based on the final deposit amount.
Tracks the user's deposit, referral rewards, total referrals, and other relevant information.
Emits the DepositMade and Referred events.
Claim Rewards
Function: claimRewards()

Allows users to claim their available rewards.
Calculates the available rewards based on the user's deposit, referral rewards, and previous double-up rewards.
Calculates the withdrawal tax based on the user's initial deposit percentage.
Updates the user's claimed rewards and previous double-up rewards.
Emits the ClaimedAdjusted event.
Referral Rewards
Function: refer(address referAddress, uint256 amount)

Handles the referral rewards distribution.
Distributes referral rewards to the referrer based on the referral level.
Updates the referrer's total referrals and referral rewards.
Emits the ReferralRewarded and Referred events.
Other Functions
The contract also includes various getter functions to retrieve information such as the user's maximum payout, available rewards, withdrawal tax, and more.

Events
The PharaohFarmPoTFull contract emits the following events:

DepositMade: Indicates that a deposit has been made by a user.
Referred: Indicates that a user has been referred by another user.
ClaimedAdjusted: Indicates the amount of rewards claimed by a user.
WithdrawAdjusted: Indicates the amount of rewards withdrawn by a user.
ReferralRewarded: Indicates the referral rewards given to a user.
Disclaimer
Please note that this README provides a general overview of the PharaohFarmPoTFull contract. It is essential to review the contract's implementation and conduct thorough testing before using it in a production environment.