# Irys CLI Guide 📔

The **Irys CLI** is a command-line tool for interacting with **[Irys](https://irys.xyz/)**, a decentralized data availability layer that lets you upload, manage, and retrieve data (files, JSON, metadata, etc.) on-chain or off-chain with permanent storage guarantees.

---

## 📌 Device/System Requirements 💻
No specific requirements — works on any minimal device.

---

## ⚙️ Install All Required Dependencies

```bash
sudo apt-get update && sudo apt-get upgrade -y
```
```
sudo apt install curl iptables build-essential git wget lz4 jq make protobuf-compiler cmake gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev screen ufw -y
```

**📥 Install Node.js & npm**

*For Linux:*
```
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && sudo apt install -y nodejs
```

*For Mac*
```
brew install node
```

*check version*
```
node -v
npm -v
```

**🚀 CLI Installation**
```
sudo npm i -g @irys/cli
```

**Verify installation:**
```
irys
```

**🔑 Parameters & Their Usage**

| Option           | Description                                                       |
| ---------------- | ----------------------------------------------------------------- |
| `-n`             | The network to check, `mainnet` or `devnet`, defaults to mainnet. |
| `-t`             | The [token](https://docs.irys.xyz/build/d/features/supported-tokens) to use when funding.                                    |
| `-w`             | Your private key (without `0x`).                                  |
| `--tags`         | Tags to include, format `<file_name> <file_format>`.              |
| `--provider-url` | [RPC URL](https://chainlist.org/) to use.                                                   |



**💸 Fund Your Wallet [Testnet/Devnet]**
```
irys fund 1000000 \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --provider-url RPC_URL
```

*👉 Take faucet: [Ethereum Sepolia Faucet](https://sepolia-faucet.pk910.de/)*

*(If using another chain, take faucet of that network.)*

*Replace PRIVATE_KEY with your actual credential (without 0x)*

*Replace RPC_URL with your selected network RPC* https://sepolia.drpc.org/

*💡 The fund amount is in wei.*



**📊 Check Balance**
```
irys balance WALLET_ADDRESS \
  -t ethereum \
  -n devnet \
  --provider-url RPC_URL
```

*Replace WALLET_ADDRESS with your actual wallet address*

*Replace RPC_URL with your selected RPC*


**📂 Upload a File**
```
irys upload FILE_NAME \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --tags FILE_NAME FILE_FORMAT \
  --provider-url RPC_URL
```
*Replace FILE_NAME with your file name*

*Replace PRIVATE_KEY with your credential*

*Replace FILE_FORMAT (e.g. jpg, png)*

*Replace RPC_URL with your selected network RPC*



**🔗 Community**

✔️ Join Telegram for updates: [Crypto Syndicate](https://t.me/CryptoSyndicate07?utm_source=chatgpt.com)

If you face any issue:

DM me on Telegram
