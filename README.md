# On-Chain Voting Governance (DAO)

This repository provides an expert-level framework for building decentralized autonomous organizations (DAOs). It utilizes a "Governor" model where voting power is proportional to the number of governance tokens held by a user.

### Core Mechanisms
* **Proposal Lifecycle:** Proposals move from Pending -> Active -> Succeeded (or Defeated) -> Queued -> Executed.
* **Delegation:** Users can delegate their voting power to representatives without transferring their tokens.
* **Quorum & Thresholds:** Customizable settings for minimum participation and proposal creation requirements.
* **Timelock Integration:** Includes a delay between a successful vote and execution to allow users to exit if they disagree with the outcome.

### How to Use
1. Deploy the `GovernanceToken.sol` to distribute voting power.
2. Deploy the `Timelock.sol` to hold the DAO's treasury or administrative rights.
3. Deploy `GovernorContract.sol` to manage the logic.
4. Transfer ownership of the target assets to the Timelock.

### Security
Uses OpenZeppelin's standardized governance modules to ensure protection against double-voting and flash-loan attacks.
