# txdecoder

**txdecoder.xyz** helps you decode on-chain transactions across **Ethereum, Solana, BNB Chain, and Base** into a **single unified, human-readable schema**.

Instead of dealing with raw logs, instruction bytes, or chain-specific formats, txdecoder normalizes everything into a clean data structure that is easy to query, index, and analyze.

🌐 Powered by **https://txdecoder.xyz**

---

## 🚀 Playground (Try it now)

👉 **[https://txdecoder.xyz/#public](https://txdecoder.xyz/#public)**

Paste a transaction hash from any supported chain and instantly see:

- Raw on-chain data
- Decoded actions (swap, transfer, mint, borrow…)
- Unified, human-readable schema output

No setup. No SDK. Just on-chain data → readable structure.

Decoded data for Swap transaction on ethereum
<img width="1133" height="699" alt="image" src="https://github.com/user-attachments/assets/e2bbaaf7-aabc-4c23-8a94-cb2adab4e33d" />


Decoded data for Lending transaction on Solana
<img width="901" height="693" alt="image" src="https://github.com/user-attachments/assets/5999250e-b05b-4ede-a7de-49bca26bf246" />


## API documents
**https://txdecoder.gitbook.io/docs/api-documentations/decode-transaction-api**

## ✨ Why txdecoder?

Decoding on-chain transactions is painful because:

- Each chain has **different execution models**
- Data is scattered across:
  - Logs
  - Instructions
  - Internal calls
  - Program-specific layouts
- Output is **not human-readable**
- Cross-chain analytics becomes extremely hard

**txdecoder solves this by converting raw transactions into a single unified schema.**

---

## 🔗 Supported Chains

| Chain       | Status |
|------------|--------|
| Ethereum   | ✅ |
| BNB Chain  | ✅ |
| Base       | ✅ |
| Solana    | ✅ |

---

## 🧠 What txdecoder does

txdecoder takes a raw on-chain transaction and produces:

- **High-level actions** (swap, transfer, mint, borrow, liquidate…)
- **Normalized entities**
  - user
  - protocol
  - pool / market
  - token
- **Unified fields** across all chains
- **Human-readable semantics**

---

## 🧩 Unified Schema (Example)

```json
{
            "type": "LENDING",
            "protocol": "Morpho",
            "source": "Morpho",
            "action": "repay",
            "participants": [
                {
                    "address": "0x9fb1750Da6266a05601855bb62767eBC742707B1",
                    "type": "signer"
                },
                {
                    "address": "0x9fb1750Da6266a05601855bb62767eBC742707B1",
                    "type": "repayer"
                },
                {
                    "address": "0x4095F064B8d3c3548A3bebfd0Bbfd04750E30077",
                    "type": "initiator"
                }
            ],
            "pool_id": "0xBBBBBbbBBb9cC5e90e3b3Af64bdAF62C37EEFFCb",
            "tokens": [
                {
                    "address": "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48",
                    "name": "USD Coin",
                    "symbol": "USDC",
                    "decimals": 6,
                    "amount": "264463759538",
                    "ui_amount": "264463.759538"
                }
            ],
            "value_usd": 264463.759538,
            "extra_data": {
                "shares": "246984185247671317"
            },
            "log_index": 89,
            "block_number": 23187124,
            "block_hash": "0x0226dfc0c5ab0b5cc331d94bbda20664e28ce8aa730777a9855d42c7cd79ccae",
            "tx_hash": "0xf74e5042eb57b5cd0e308e8b3108c9a0d631514829aeee728e40e61564ced0ba",
            "timestamp": 1755751139
        },
