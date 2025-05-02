# 📄 Feature Requirements Document (FRD)

### **Project Name:** Cross-exchange Arbitrage Bot(MEV.ver)

### **Date:** 2025-05-02

### **Author:** \[Me]

---

## **1. Project Objective**

An automated Cross-exchange arbitrage bot that operates on the Ethereum mainnet. It continuously monitors token exchange rates across multiple DEXs and executes profitable arbitrage opportunities in real time.

---

## **2. Project Scope**

**In Scope:**

* Token selection.
* Monitor token prices.
* Generate trading paths.
* Profit evaluation.
* Execute transactions.
* Logs.

**Out of Scope:**

* Cross-chain.
* Centralized exchange integration.
* GUI or web interface.
* ..
---

## **3. Functional Requirements**

| ID | Feature                 | Description                                                                                  |
| -- | ----------------------- | -------------------------------------------------------------------------------------------- |
| F1 | Price Aggregation       | Fetch real-time prices from multiple DEXs using RPC or aggregator APIs.                      |
| F2 | Path Generator          | Dynamically construct valid Cross-exchange paths between top tokens (e.g., top 20 by liquidity). |
| F3 | Profit Evaluation       | For each path, calculate expected profit after gas fees and slippage.                        |
| F4 | Trade Executor          | Send atomic swap transactions when expected profit exceeds threshold.                        |
| F5 | Logging                 | Record prices, decisions, transactions, gas usage, and profits.                              |
| F6 | Configurable Parameters | Allow dynamic config (e.g., gas limit, slippage tolerance, profit threshold).                |

---

## **4. Non-Functional Requirements**

| ID | Category        | Requirement                                                               |
| -- | --------------- | ------------------------------------------------------------------------- |
| N1 | Performance     | Total path evaluation and trade decision should complete within 1 second. |
| N2 | Reliability     | Must handle RPC failures and retry gracefully.                            |
| N3 | Security        | Private keys must be securely stored and not hardcoded.                   |
| N4 | Maintainability | Code should follow modular structure for easy strategy updates.           |

---

## **5. API Requirements**

| API Name                         | Provider                     |
| -------------------------------- | ---------------------------- |
| Token Price Feed                 |           |
| Token Price Feed                 |             |
| Swap Execution API               |                      |
| Gas Price Estimation             |   
| Flash Loan Execution             |                     |
| Token Metadata & Decimals Lookup |       |
