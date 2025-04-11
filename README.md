# 📄 File Notary DApp

This is a simple decentralized application (DApp) that allows users to **notarize** files on the Ethereum blockchain and later **verify** their authenticity. It works by storing the file's SHA256 hash along with a timestamp and the owner's wallet address.

## ⚙️ Features

- 🔐 Connect your MetaMask wallet
- 📝 Notarize any file (PDF, image, document, etc.)
- ✅ Verify if a file has already been notarized
- 📅 View the timestamp and the owner's wallet address

## 🧱 Smart Contract

The smart contract is written in Solidity and deployed locally using Hardhat. It stores file hashes in a mapping to prevent duplicates and allows verification.

```solidity
function notarizeFile(string memory _fileHash) public { ... }
function verifyFile(string memory _fileHash) public view returns (bool, uint256, address) { ... }
```

## 💻 Tech Stack
HTML/CSS/JavaScript

MetaMask + Web3.js

Solidity (Smart Contract)

Hardhat (Local Ethereum Network)

## 🚀 Getting Started
Prerequisites
MetaMask browser extension

Node.js & NPM

Hardhat

## Install & Run
1. Clone the repo:
```
git clone https://github.com/your-username/file-notary-dapp.git
cd file-notary-dapp
```
2. Install Hardhat and dependencies:
```
npm install
```
3. Run Hardhat local blockchain:
```
npx hardhat node
```
4. Deploy the contract:
```
npx hardhat run scripts/deploy.js --network localhost
```
5. Open index.html in your browser with MetaMask connected to localhost:8545.

## 📂 Files to Upload
Make sure you upload the following:
```
file-notary-dapp/
│
├── contracts/
│   └── FileNotary.sol          # Smart contract
├── scripts/
│   └── deploy.js               # Hardhat deployment script
├── index.html                  # Frontend HTML
├── app.js                      # Frontend JS logic
├── style.css (optional)        # CSS if separated
├── README.md                   # This file
├── hardhat.config.js           # Hardhat config
├── package.json                # Dependencies
└── artifacts/, cache/, node_modules/ (auto-generated)
```
✅ Don't forget to update the contract address in app.js after deploying.
