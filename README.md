# FarmPoTFull Smart Contract

The FarmPoTFull contract is a sophisticated and versatile staking smart contract that offers users the opportunity to stake their ERC20 tokens, earn interest, and participate in a dynamic referral rewards program. This contract is designed to ensure security, transparency, and flexibility in managing staked funds, interest accrual, and reward distribution.

## Features

- **Staking Mechanism**: Users can deposit their ERC20 tokens into the contract, effectively locking them for a predetermined period. During this time, staked tokens generate interest based on a carefully calibrated algorithm.

- **Vesting and Gradual Reward Distribution**: The contract's innovative vesting mechanism ensures that rewards are distributed gradually over the vesting period. This design prevents a sudden influx of rewards, promoting long-term user engagement and stability.

- **Referral Rewards**: The FarmPoTFull contract introduces an advanced referral rewards system. Users can refer others to the platform, and based on the level of referrals and staking activities, referrers are eligible to receive rewards. The multi-level structure of this referral program encourages network growth and engagement.

- **Secure and Reentrancy-Proof**: To safeguard user assets, the contract includes built-in security measures. The ReentrancyGuard modifier is implemented to prevent reentrancy attacks, ensuring the contract operates as intended.

- **Customizable Parameters**: This contract is designed with flexibility in mind. Key parameters, such as deposit tax rates, minimum deposit amounts, referral reward levels, and even vesting periods, can be configured to suit the platform's specific needs.

## Prerequisites

- Node.js and npm
- Truffle: Install with `npm install -g truffle`
- Solidity Compiler: Truffle requires a compatible compiler version.

## Deployment

1. Clone this repository: `git clone <repository_url>`
2. Navigate to the project directory: `cd FarmPoTFull`
3. Install project dependencies: `npm install`
4. Configure Truffle: Modify the `truffle-config.js` file to specify your network settings.
5. Compile the contract: `truffle compile`
6. Deploy the contract: `truffle migrate --network <network_name>`

## Usage

1. Interact with the deployed contract using Truffle console or scripts.
2. Deposit tokens to stake and start earning interest.
3. Refer friends and others to the platform to earn referral rewards.
4. Claim your rewards after the vesting period has passed.
5. Explore additional contract functions as needed.

## Detailed Explanation of Key Functions

### deposit(uint256 amount, address referAddress) public

Users can initiate a deposit of ERC20 tokens, effectively entering the staking program. Additionally, users can provide a referral address during the deposit process. This function calculates the potential interest based on the locked amount and initializes the user's staking details.

### claimRewards() external

Users can claim their available rewards using this function. The contract takes into account the vesting period and applies a withdrawal tax to ensure a responsible and gradual distribution of rewards.

### doubleUp() external

Users who have accumulated a sufficient level of interest can use this function to double their initial deposit. This feature provides an added incentive for users to remain engaged in the platform.

### getContractBalance() public view returns (uint256)

Provides a snapshot of the current balance of ERC20 tokens held within the contract.

### calculatePayout(address caller) public view returns (uint256)

This function calculates the potential payout for a given user based on their initial deposit and the duration of their staking.

### Multi-Level Referral Functions

The FarmPoTFull contract includes a sophisticated referral structure that spans multiple levels. For example, functions like `getLevel1Reffers(address userAddress)` and `getLevel2Reffers(address userAddress)` return arrays of addresses representing users who were referred by the specified user. This hierarchical approach encourages users to refer others and creates a network effect.

## Contributing

Contributions to this project are warmly welcomed! If you encounter issues, have suggestions, or wish to contribute enhancements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Disclaimer: It is essential to review and thoroughly test the contract before deploying it in a production environment. Understand the contract's functionality and potential implications fully.
# FarmPot-Investment-Protocol-Contract
