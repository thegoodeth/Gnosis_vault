# 🔐 Gnosis Vault — Secure Safe{Wallet} Dashboard

[![Vercel Deployment](https://img.shields.io/badge/deployed-vercel-%2300C7B7)](https://safe-vault-f44t.vercel.app)
[![License](https://img.shields.io/github/license/Safe-Wallet-Custom-Secure-dApp/Gnosis_vault)](LICENSE)
[![GitHub Actions](https://github.com/Safe-Wallet-Custom-Secure-dApp/Gnosis_vault/actions/workflows/main.yml/badge.svg)](../../actions)

---

**Gnosis Vault** is a custom Safe{Wallet}-native dashboard built for decentralized transaction governance and secure multi-owner coordination.

> Built by [@thegoodeth](https://github.com/thegoodeth12) — Powered by [Reown](https://reown.com) and [Safe (Gnosis)](https://safe.global)

---

## 🌐 Live App

**🔗 [https://safe-vault-f44t.vercel.app](https://safe-vault-f44t.vercel.app)**  
Main Safe Address: `0xAfD5f60aA8eb4F488eAA0eF98c1C5B0645D9A0A0`

---

## ✨ Features

- 🧾 **Real-time Safe info**: owners, threshold, balances
- 🧠 **GitHub Automation**: propose & sign via PR comments
- 📡 **Discord Webhooks**: real-time transaction updates
- ⚙️ **Multi-chain & multi-Safe support**
- 🔧 **Admin controls** for signers and thresholds
- 📜 **Transaction history + queue viewer**

---

## 🛠️ Quick Setup

### 🔧 Prerequisites

- Node.js v18+
- Yarn / npm
- Vercel or Docker (for deployment)

### 🚀 Run Locally

```bash
git clone https://github.com/Safe-Wallet-Custom-Secure-dApp/Gnosis_vault.git
cd Gnosis_vault

# Install dependencies
yarn install

# Create your .env file
cp .env.example .env

Update .env with:
REOWN_API_KEY=your_reown_api_key
APPKIT_WEBHOOK_URL=https://appkit-lab.reown.com/library/multichain-all/
SAFE_ADDRESS=0xAfD5f60aA8eb4F488eAA0eF98c1C5B0645D9A0A0
CHAIN_ID=42161

🧪 Development
yarn dev

📦 Deployment

This project is pre-configured for Vercel.

vercel --prod

Or self-host using Docker:

docker build -t gnosis-vault .
docker run -p 3000:3000 gnosis-vault

🔔 GitHub & Discord Integration
	•	✅ Auto-create Safe transaction proposals from GitHub Actions or PR comments
	•	✅ Notify via Discord webhook when proposals are created, signed, or executed
	•	🔒 GitHub App and custom webhook runner support

⸻

📁 Project Structure

📦 Gnosis_vault/
 ┣ 📂 components/         # UI components
 ┣ 📂 dashboard/          # Safe data renderers
 ┣ 📂 github/             # GitHub Action & PR logic
 ┣ 📂 hooks/              # Safe data + wallet logic
 ┣ 📂 pages/              # App routes
 ┣ 📂 utils/              # Safe utilities
 ┣ 📜 safe.config.ts      # Safe & chain configuration
 ┣ 📜 README.md
 ┣ 📜 .env.example
 ┗ 📜 vercel.json

🧩 Extensions (Planned)
	•	✅ Proposal Queue with GitHub PR link
	•	✅ Signer Log (last signed TXs)
	•	🚧 Telegram Mini App export
	•	🚧 Safe Bundler Integration
	•	🚧 Cross-Safe proposal forwarding

⸻

🤝 Contributing

PRs welcome! For onboarding:
	•	Setup .env
	•	Fork this repo
	•	Open a PR with clear title & purpose
	•	Link your Safe signer address in PR description

⸻

📜 License

MIT © 2025 @thegoodeth — See LICENSE

⸻

Built with love for Safe{Wallet} owners who care about governance, security, and transparency.

---

### ✅ 2. Optional: **Release Artifacts**

If you'd like to attach zipped binaries to your GitHub Release:

#### Build + zip the project:
```bash
yarn build
zip -r gnosis-vault-v0.1.0.zip .next public package.json README.md
