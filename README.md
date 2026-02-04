# # DeferredValueSwap – AI‑Powered Escrow Intelligent Contract for GenLayer

## Overview

`DeferredValueSwap` is an educational Intelligent Contract for the GenLayer Asimov Testnet.  
It implements a **full escrow‑style deal lifecycle** between a sender and a recipient, with:

- **Native GEN deposits** locked in the contract,
- **Stateful lifecycle** (create → activate → finalize / cancel / expire),
- **Optional disputes** with **AI‑based arbitration** using `gl._nondet`,
- **Time‑based deadlines**, protocol fees, blacklisting, and simple reputation.

This repository is intended as **Educational Content** for the GenLayer Builders program and can be used as:

- a reference contract for escrow‑like workflows,
- a starting point for your own marketplace or freelancing dApp,
- a concrete example of using GenLayer’s Intelligent Contract features in practice. ([docs.genlayer.com](https://docs.genlayer.com/developers/intelligent-contracts/introduction))

---

## Contract Idea in One Paragraph

Two parties want to do a deal (for example, a freelance job or a product sale).  
The **sender** locks GEN in this contract as a **deposit**. The **recipient** can activate and later finalize the deal, either by:

- taking a **payout** (funds are released to them), or  
- finalizing as a **certificate** (logical “NFT‑like” state with metadata).

If something goes wrong, either side can open a **dispute**. The dispute can then be resolved either manually by the contract owner or automatically by an **AI arbitrator** that receives the deal context and returns a structured decision.

---

## Repository Structure

```text
.
├── contracts/
│   └── DeferredValueSwap.py   # Full Intelligent Contract source code
├── tutorial.md                # Step‑by‑step textual tutorial with code snippets
├── README.md                  # You are here
└── diagrams/                  # (optional) lifecycle diagrams / visualscontracts-DeferredValueSwap.py
