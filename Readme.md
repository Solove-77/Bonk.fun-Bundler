# 🚀 Bonkfun-bundler

**A scalable Solana token bundler & automation toolkit.**  
Create, distribute, and manage tokens and wallets at scale with ease.

---

## 📚 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Quick Start](#quick-start)
- [Configuration](#configuration)
- [Scripts & Usage](#scripts--usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Assets](#assets)
- [Contact](#contact)
- [License](#license)

---

## 📝 Overview

Bonkfun-bundler is a TypeScript-powered toolkit for automating token creation, wallet distribution, and transaction management on Solana. It leverages the Solana, Raydium, and Anchor SDKs for robust, high-scale operations.

---

## ✨ Features

- **Automated Token Creation**: Instantly create new Solana tokens with metadata and launchpad setup.
- **Wallet Distribution**: Mass-generate and fund wallets for airdrops or participation.
- **Automated Buys**: Execute buy instructions across distributed wallets.
- **Address Lookup Table (LUT) Management**: Efficiently batch transactions.
- **Fund Gathering & Wallet Closing**: Collect tokens/SOL and reclaim rent.
- **Jito Fee Wallet Support**: MEV-aware transaction execution.
- **Utility Scripts**: For LUT closing, fund gathering, and status checks.

---

## ⚡ Quick Start

### 1. Prerequisites

- Node.js v18+
- Yarn or npm
- Solana CLI
- Funded Solana wallet

### 2. Install

```bash
yarn install
# or
npm install
```

### 3. Configure

Create a `.env` file in the root directory:

```env
PRIVATE_KEY=...
RPC_ENDPOINT=...
TOKEN_NAME=...
# (See [Configuration](#configuration) for all variables)
```

---

## ⚙️ Configuration

Set these variables in your `.env` file:

- `PRIVATE_KEY`, `RPC_ENDPOINT`, `TOKEN_NAME`, `TOKEN_SYMBOL`, `DESCRIPTION`, `TOKEN_SHOW_NAME`, `TOKEN_CREATE_ON`, `TWITTER`, `TELEGRAM`, `WEBSITE`, `FILE`, `VANITY_MODE`, `SWAP_AMOUNT`, `DISTRIBUTION_WALLETNUM`, `JITO_FEE`, `BUYER_WALLET`, `BUYER_AMOUNT`

> See `constants/constants.ts` for the full list and details.

---

## 🛠️ Scripts & Usage

| Action                | Yarn Command      | npm Command         | Description                                 |
|-----------------------|------------------|---------------------|---------------------------------------------|
| Start main process    | `yarn start`     | `npm run start`     | Token creation, distribution, automation    |
| Gather & close wallets| `yarn gather`    | `npm run gather`    | Collect funds, close wallets                |
| Close LUTs            | `yarn close`     | `npm run close`     | Close address lookup tables                 |
| Check status          | `yarn status`    | `npm run status`    | Wallet & transaction status                 |

---

## 🗂️ Project Structure

- `index.ts` — Main entry (token creation, distribution, automation)
- `src/` — Core logic & utilities
- `gather.ts` — Gather/close wallets
- `closeLut.ts` — Close LUTs
- `status.ts` — Status checks
- `constants/` — Environment & constants
- `executor/` — Transaction execution (Jito/legacy)
- `utils/` — Helper functions

---

## 📦 Dependencies

- `@solana/web3.js`
- `@raydium-io/raydium-sdk`, `@raydium-io/raydium-sdk-v2`
- `@coral-xyz/anchor`
- `@solana/spl-token`
- `axios`, `dotenv`, `js-sha256`, `pino`, `typescript`, etc.

See `package.json` for the full list.

---

## 🖼️ Assets

- Images: `image/` directory (for docs & token metadata)

---

## 💬 Contact

- Discord: **aether_15**
- Telegram: [@Solove](https://t.me/Solove_77)

---

## 🪪 License

[ISC](./LICENSE)
