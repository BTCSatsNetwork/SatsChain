# SatsChain

SatsChain is a Bitcoin Layer-2 Network developed based on the BEVM Stack, fully compatible with the Ethereum Virtual Machine (EVM).

## Table of Contents

- [SatsChain](#satschain)
  - [Table of Contents](#table-of-contents)
  - [Quick Start](#quick-start)
    - [Overview](#overview)
    - [Network Configuration](#network-configuration)
  - [SatsChain Bridge](#satschain-bridge)
  - [Build Decentralized Apps](#build-decentralized-apps)
    - [Fee Calculation](#fee-calculation)
    - [Smart Contracts](#smart-contracts)
    - [Integrations](#integrations)
    - [Libraries](#libraries)
  - [Run a SatsChain Node](#run-a-satschain-node)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)

## Quick Start

### Overview

SatsChain leverages the security of Bitcoin while providing the scalability and flexibility of a Layer-2 solution. It is designed to support a wide range of decentralized applications (DApps) with low transaction costs and fast confirmation times.

### Network Configuration

To configure your network to connect to SatsChain, use the following parameters:

- **Network Name**: SatsChain
- **RPC URL**:
  - RPC:  `https://rpc-satschain-1.bevm.io`
  - Websocket: `wss://rpc-satschain-1.bevm.io`
- **Chain ID**: 11521
- **Currency Symbol**: `SATS`
- **Block Explorer URL**: `http://scan-satschain.bevm.io/`

For more detailed configuration instructions, please refer to the [Metamask Setup Guide](docs/setup-metamask.md).


## SatsChain Bridge

The SatsChain Bridge enables seamless asset transfers between Bitcoin and SatsChain. This bridge ensures that assets can be securely and efficiently moved, facilitating interoperability between the networks.

- **Bridge Documentation**: [SatsChain Bridge Guide](https://github.com/BTCSatsNetwork/SatsChain-Bridge)
- **Supported Assets**: Bitcoin (BTC), Sats (SATS), and other ERC-20 tokens.

## Build Decentralized Apps

### Fee Calculation

Transaction fees on SatsChain are calculated using sats (BRC-20) tokens. The gas fees are designed to be minimal, ensuring cost-effective transactions.


### Smart Contracts

SatsChain supports smart contracts fully compatible with the Ethereum Virtual Machine (EVM). You can deploy your existing Ethereum contracts with minimal modifications.

For detailed instructions on deploying smart contracts, please refer to the following guides:
* [Deploy Smart Contract Guide](docs/deploy-smart-contract.md)
* [Foundry Guide](docs/foundry.md)
* [Deploy & Verify by Foundry](docs/deploy-verfify-by-foundry.md)

### Integrations

Integrate SatsChain with various services and platforms to enhance your DApp's functionality.

- **Wallets**: MetaMask, Trust Wallet, etc.
- **Oracles**: Chainlink, Band Protocol, etc.

### Libraries

Utilize a range of libraries to facilitate development on SatsChain:

- **Web3.js**: JavaScript library for interacting with the SatsChain.
- **Ethers.js**: A complete Ethereum library and wallet implementation.
- **OpenZeppelin**: Secure smart contract library.

## Run a SatsChain Node

Running a SatsChain node allows you to participate directly in the network, helping to validate transactions and secure the blockchain.

### Prerequisites

- **Hardware Requirements**: Minimum 4 CPU cores, 8GB RAM, 256GB SSD

- **Software Requirements**: Latest version of Docker, Git

### Installation

To run a SatsChain node, follow the instructions in the [Run Node Guide](docs/run-node.md).

------

Thank you for your interest in SatsChain. We look forward to your contributions and feedback.
