# nova-blockchain-academy-project
# SafeCode 🔒 – Blockchain-Based QR Trust Verification System

## Context
This project was developed as the **final assessment for the Nova SBE Blockchain Academy (5 ECTS)**, an intensive hybrid program on blockchain fundamentals, platforms (Ethereum/Polygon), smart contracts, governance, and business applications — completed January–February 2026.

## Problem Statement
Traditional QR codes lack built-in authenticity verification, making them vulnerable to:
- **QR code phishing (quishing)** – criminals overlay malicious codes on legitimate ones  
- **Counterfeit goods** – fake products bearing copied QR codes  
- **Fraud and malware** – 20–25% of phishing attacks now use QR codes, costing organizations $4.8M+ per breach on average  

**Business impact**: Brands face reputational damage and loss of trust; consumers face financial losses and safety risks, especially in pharmaceuticals and luxury goods sectors.

## Proposed Solution
**SafeCode** is a blockchain-anchored trust verification system that stores cryptographic proofs of authentic QR codes on a public ledger (Polygon L2). When users scan a code, the system:
1. Queries the blockchain to verify the QR hash is registered and valid  
2. Checks on-chain status (active, revoked, consumed, recalled)  
3. Returns a **traffic-light verification signal**:
   - 🟢 **Green** = verified and legitimate  
   - 🟡 **Yellow** = suspicious / ambiguous  
   - 🔴 **Red** = invalid or revoked  

## Data and Architecture
- **On-chain**: QR hash (cryptographic fingerprint), issuer wallet address, status flag (active/sold/consumed/recall)  
- **Off-chain (IPFS/Oracle)**: Product metadata, images, batch details, user manuals  
- **Platform**: Polygon (Ethereum L2) for low gas fees, high speed, and Ethereum security  
- **Smart contract**: Manages QR lifecycle, role-based minting (only authorized issuers), anti-cloning logic  
- **Frontend**: Mobile app for issuers (mint QR codes) and verifiers (scan and validate)  

## Key Insights and Outcomes
- **Mapped current-state QR vulnerabilities**: reactive blacklists, visual inspection failures, no cryptographic root of trust  
- **Designed "to-be" process**: immutable on-chain registry, real-time verification, transparency via public ledger  
- **Identified stakeholders**: brands/manufacturers (reduce fraud 70–90%), consumers (protection against quishing), infrastructure providers (Polygon, IPFS, wallets)  
- **Proposed KPIs**: verification accuracy >99%, <3-second scan-to-verification time, measurable fraud reduction for pilot brands  
- **Assessed risks**: smart contract vulnerabilities (mitigated via audits), oracle reliability (redundancy + hash verification), low adoption (pilot programs, network effects)  
- **Governance model**: phased from founder-led (pre-launch) → user feedback + board (launch) → issuer board + potential user DAO (scale)  
- **Regulatory compliance**: GDPR-friendly (no personal data on-chain), outside MiCA scope (no tradable tokens), consumer protection via transparent verification signals  

## Implementation Roadmap
1. **MVP**: Smart contract on Polygon, QR scanner app, basic issuer interface, security audit  
2. **Version 1**: Institutional dashboards, analytics, role management, pilot integrations with brands  
3. **Full Product**: Reputation systems, token incentives, loyalty mechanisms, strategic partnerships  

## Full Report
**Complete project documentation (21 pages):**  
Available in this repository as `SafeCode-Project-Blockchain-Academy.pdf` or via [Google Docs link](https://docs.google.com/document/d/1Xoj5xyMDtYg6ZhZ3XdO3idoDRwFmAOqN3qz7wGw2_5M).

## Technologies
Blockchain: Polygon (Ethereum L2) | Storage: IPFS | Smart Contracts: Solidity | Frontend: Mobile app (Web3 integration) | Oracles: Off-chain metadata bridge

---

**Author:** Augusto Wen  
**Program:** Nova SBE Blockchain Academy, Jan–Feb 2026  
**Portfolio:** [github.com/Wancing](https://github.com/Wancing)
