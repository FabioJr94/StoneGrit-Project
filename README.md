# StoneGrit Protocol - Smart Contracts (Kadena/Pact)

This repository will contain the official Pact smart contracts for the StoneGrit RWA project. Development is scheduled to begin in Q1 2026, following the successful completion of our grant and presale funding rounds.

## Core Contract Architecture

The protocol will consist of several key smart contracts:

### 1. SGT_Token.pact
- **Purpose:** The core fungible token contract for the $SGT token.
- **Standard:** Implements the `fungible-v2` interface.
- **Features:** Fixed total supply, minting/burning controls locked.

### 2. Staking_Pool.pact
- **Purpose:** Manages the staking of $SGT and the distribution of hybrid rewards.
- **Key Functions:**
  - `stake(account, amount)`
  - `unstake(account, amount)`
  - `claimSgtRewards()`: For Bootstrap Rewards (48-month linear emission).
  - `claimUsdcRewards()`: For Real Yield Rewards (from company net income).

### 3. Compliance.pact
- **Purpose:** Implements our regulatory compliance framework based on ERC-3643 principles.
- **Features:**
  - Manages an on-chain KYC whitelist.
  - Utilizes Pact's `guards` to ensure only whitelisted accounts can hold and transact $SGT.

### 4. Community_Acquisition_Model.pact
- **Purpose:** Manages the Community Acquisition Model (CAM) for the stone crusher asset.
- **Features:** Receives a percentage of gross revenue and distributes it to participants.

## Technology Stack
- **Blockchain:** Kadena
- **Language:** Pact

## Development & Audit Roadmap
- **Q1 2026:** Smart Contract Development.
- **Q2 2026:** Internal Testing & Third-Party Security Audit.
- **Q3 2026:** Mainnet Deployment.
