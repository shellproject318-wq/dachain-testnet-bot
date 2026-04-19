# DAC Inception — Daily Testnet Bot

Automated daily activities for [DAC Inception](https://inception.dachain.io/activity) testnet.

**Chain:** DAC Quantum Chain (ID: 21894)
**RPC:** `https://rpctest.dachain.tech`
**Explorer:** `https://exptest.dachain.tech`

---

## Activities

| # | Action | Description |
|---|--------|-------------|
| 1 | 🚰 Faucet | Claim free DACC (requires X or Discord linked) |
| 2 | 📦 Crate | Open daily Quantum Crate → earn QE |
| 3 | 💸 TX | Self-transfer transactions → earn TX badges |
| 4 | 🔥 Burn | Burn DACC → Quantum Energy (QE) |
| 5 | 🔄 Sync | Sync all activity to API |

## Badges (Auto-earned)

| Badge | Requirement | QE Reward |
|-------|------------|-----------|
| Sign In | First login | 25 |
| First Crate | Open 1 crate | 25 |
| First Transaction | Send 1 tx | 50 |
| Getting Started | Send 3 tx | 25 |
| 10 Transactions | Send 10 tx | 100 |
| 50 Transactions | Send 50 tx | 250 |
| First Drip | Claim faucet 1x | 25 |
| Regular | Claim faucet 10x | 50 |
| Daily Streak | 3/7/14/21/30 days | 50–1000 |
| QE milestones | 500+ total QE | 50–5000 |

---

## Setup

### 1. Clone Repositories

```bash
git clone https://github.com/shellproject318-wq/dachain-testnet-bot.git
cd dachain-testnet-bot

# Install dependencies
npm install
```

### 2. Wallet Keys

Create `pk.txt` in the project directory — one private key per line:

```bash
# Single wallet
echo "0xYOUR_PRIVATE_KEY_HERE" > pk.txt

# Multi-wallet
echo "0xWALLET_1_KEY" > pk.txt
echo "0xWALLET_2_KEY" >> pk.txt
echo "0xWALLET_3_KEY" >> pk.txt
```

> ⚠️ Never share or commit `pk.txt`!

### 3. Prerequisites per Wallet

Each wallet must have:
- ✅ Connected at [inception.dachain.io](https://inception.dachain.io) at least once
- ✅ Linked Twitter (X) or Discord for faucet
- ✅ Some DAC balance for txs and burn (claim faucet first)

---

## Usage

### Single Run
```bash
node bot.js --once
```

### Loop Mode (every 10 min)
```bash
node bot.js
```

### Cron Mode (4x daily: 00:00, 06:00, 12:00, 18:00 UTC)
```bash
node bot.js --cron
```
