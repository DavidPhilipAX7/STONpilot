# STONpilot 🧭

[![License: MIT](https://shields.io)](https://opensource.org)
[![Powered by STON.fi](https://shields.io)](https://ston.fi)
[![Platform: TON](https://shields.io)](https://ton.org)

> **Browse a leaderboard of the most profitable TON traders, select a strategy that matches your risk, and let STONpilot execute every move for you via STON.fi's high-efficiency liquidity pools.**

---

## 💡 The Hook
**STONpilot: The Social Trading & Copy-Trading Layer for TON, powered by STON.fi.**

While STON.fi provides the deep liquidity and technical infrastructure for the TON ecosystem, retail users often struggle with "analysis paralysis"—not knowing which tokens to trade or when. **STONpilot** bridges this gap by adding a social intelligence layer on top of the DEX.

## 🧭 What is STONpilot?
STONpilot is a TON-native copy-trading and social analytics protocol. 

Today, STON.fi is a powerful manual exchange. You swap, you leave. There is no social layer, no way to learn from the best performers, and no way to automate a proven strategy. **STONpilot changes that.** 

We surface the "smart money" on the TON blockchain, rank them by real performance, and let any user automatically mirror their trades—executed instantly through STON.fi’s liquidity pools.

---

## 🚀 Core Features

*   **📊 Smart Money Leaderboard**: Real-time ranking of TON wallets by PnL, win rate, and consistency. Filter by risk (Conservative, Moderate, Aggressive).
*   **🤖 Automated Copy Trading**: Select a top trader and set your allocation. STONpilot mirrors every swap they make via the [STON.fi SDK](https://github.com).
*   **🔗 STON.fi SDK Integration**: All trades are routed through STON.fi for near-zero fees and low slippage.
*   **👤 Trader Profiles**: Verifiable on-chain performance history and community-driven reputation systems.

---

## 🏗️ Architecture Overview

```mermaid
graph TD
    User((User Wallet))
    
    Frontend[STONpilot Frontend<br/>Dashboard + Leaderboard]
    
    subgraph Protocol [STONpilot Protocol Layer]
        direction TB
        Analytics[Wallet Analytics Engine]
        Execution[Copy-Trade Execution Engine]
        Risk[Risk Scoring Module]
    end
    
    SDK[STON.fi SDK<br/>Swap Execution]
    
    Blockchain[(TON Blockchain)]

    User -->|Connects| Frontend
    Frontend -->|Requests| Protocol
    Protocol -->|Calls| SDK
    SDK -->|Executes Swap| Blockchain
    Blockchain -.->|Data Feed| Analytics
    
    style Protocol fill:#f9f9f9,stroke:#333
    style SDK fill:#ffdf00

