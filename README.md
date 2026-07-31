# Agentic Commerce Gateway

> AI-powered fraud detection and trust verification gateway for autonomous shopping agents.

## 🚀 Overview

Agentic Commerce Gateway is a seller-side security layer built for the future of AI-driven commerce. As autonomous shopping agents begin making purchases on behalf of users, merchants need a reliable way to verify these agents before completing transactions.

This project screens AI buying agents, evaluates their trustworthiness, verifies sales receipts against on-chain settlement records, and autonomously flags or blocks suspicious transactions.

Instead of replacing existing payment systems, the gateway acts as an intelligent verification layer between the buyer's AI agent and the merchant's checkout.

---

## ✨ Features

- 🤖 AI Agent Identity Verification
- 🔒 Trust Score Calculation
- 📦 Order Risk Analysis
- 🧾 Receipt vs Settlement Verification
- 🚩 Automatic Fraud Detection
- ⛔ Agent Blacklisting
- 📊 Seller Dashboard
- 🛒 Mock Merchant Store (NovaGear)

---

## 🏗️ Architecture

```
AI Shopping Agent
        │
        ▼
Agentic Commerce Gateway
        │
 ┌──────────────┐
 │ Screen Agent │
 └──────────────┘
        │
        ▼
Compute Trust Score
        │
        ▼
Decision Engine
Approve / Hold / Decline
        │
        ▼
Verify Receipt
        │
        ▼
Flag or Block Agent
        │
        ▼
Seller Dashboard
```

---

## 🔄 Workflow

1. AI agent places an order.
2. Gateway validates the agent's identity and signature.
3. Trust score is calculated using:
   - Reputation
   - Purchase history
   - Order anomalies
   - Velocity checks
4. Order is approved, held, or declined.
5. Receipt is verified against settlement records.
6. Any mismatch automatically flags the order.
7. Suspicious agents are blacklisted.
8. Dashboard updates seller analytics.

---

## 🛠 MCP Tools

| Tool | Purpose |
|------|---------|
| `list_products` | Retrieve available products |
| `place_agent_order` | Simulate AI agent purchase |
| `screen_agent` | Verify agent identity |
| `compute_trust_score` | Calculate fraud risk |
| `verify_receipt` | Compare receipt with settlement record |
| `flag_order` | Mark suspicious orders |
| `blocklist_agent` | Block fraudulent agents |
| `get_sales_dashboard` | Seller analytics dashboard |

---

## 📁 Project Structure

```
src/
│
├── fixtures/
│   ├── products.json
│   ├── agents.json
│   ├── orders.json
│   ├── registry.json
│   └── onchain-records.json
│
├── tools/
│
├── widgets/
│
└── gateway/
```

---

## 📊 Demo Scenarios

### ✅ Trusted Purchase

A verified AI shopping agent purchases a product successfully after passing all trust checks.

---

### 🚫 Fraudulent Agent

A spoofed AI agent attempts a bulk purchase.

The gateway detects:

- Invalid signature
- Low reputation
- Suspicious order size

The order is rejected and the agent is blacklisted.

---

### 🔍 Tampered Receipt

A transaction appears legitimate, but the receipt differs from the settlement record.

The gateway detects the mismatch, flags the order, and updates the dashboard.

---

## 📈 Dashboard

The seller dashboard provides:

- Orders by AI agents
- Approved vs declined transactions
- Flagged orders
- Blacklisted agents
- Revenue protected
- Trust score insights

---

## 💡 Why Agentic Commerce Gateway?

As AI agents become capable of purchasing products autonomously, traditional fraud prevention methods are no longer sufficient.

This gateway enables merchants to:

- Trust autonomous buyers
- Reduce fraudulent transactions
- Verify settlement integrity
- Protect revenue
- Maintain a seamless checkout experience

---

## 🛠 Tech Stack

- TypeScript
- NitroStack SDK
- NitroCloud
- MCP (Model Context Protocol)
- JSON Fixtures
- AI-powered Decision Logic

---

## Future Improvements

- ACP protocol integration
- AP2 and MPP support
- Live blockchain verification
- Multi-merchant support
- Real payment gateway integration
- Advanced behavioral anomaly detection

---

## License

MIT License
