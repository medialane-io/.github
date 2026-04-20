![Medialane.io](https://mediolano.xyz/wp-content/uploads/2026/03/medialane-io-launch-starknet-sm01-1-scaled.png)

# Medialane

**The monetization hub of the new creative economy — built on Starknet.**

Medialane is an open protocol and platform infrastructure empowering creators, organizations, and autonomous AI agents to transform intellectual property into new revenue streams. We bridge marketplace dynamics, creator launchpads, smart contract licensing, and decentralized ownership into a unified, permissionless foundation for sustainable value creation.

At its core, Medialane enables **liquid, interoperable, and programmable IP assets** — driving ownership, generating value, and fueling the emergence of autonomous AI agents and Creator Capital Markets. The global intellectual property market stands at **$61 trillion**. Medialane is building the rails.

---

## Mission

> *Fuel the creative economy on the Integrity Web.*

Every creative work deserves a permanent, verifiable record of authorship and a programmable set of rules for how it can be used. Medialane exists to fix what the internet never could: transparent licensing, automatic royalties, and indisputable ownership — without intermediaries, without friction, without compromise.

The Integrity Web is the next phase of the internet — where every transaction is verifiable, every asset is owned by its creator, and every agreement is enforced by code. Medialane is its monetization hub.

---

## Platform

| App | URL | Description |
|---|---|---|
| **Medialane** | [medialane.io](https://medialane.io) | Consumer app — social login, invisible wallet, full creator suite |
| **Medialane Dapp** | [dapp.medialane.io](https://dapp.medialane.io) | Permissionless dApp — Argent, Braavos, Cartridge, Privy |
| **Developer Portal** | [portal.medialane.io](https://portal.medialane.io) | API keys, documentation, usage dashboard, webhooks |
| **Medialane DAO** | [medialane.org](https://medialane.org) | Governance, MDLN token, community treasury |

---

## Open Protocols

Our protocols are **open-source, immutable, permissionless, and censorship-resistant**. Deployed on Starknet, every transaction batch is verified on Ethereum via STARK proofs — no single point of failure, no gatekeepers. Any creator, business, or autonomous AI agent can interact with them directly, without permission or intermediaries.

### Cairo Smart Contracts — Starknet Mainnet

| Contract | Purpose |
|---|---|
| **Medialane-Protocol-ERC721** | Marketplace protocol for NFTs — SNIP-12 signed orders, listings, offers, cart checkout, cancellations |
| **Medialane-Protocol-ERC1155** | Marketplace protocol for multi-edition IP tokens — auctions and secondary markets |
| **Collection-Drop** | ERC721 collection factory — curated NFT drops with configurable mint phases and allowlists |
| **Pop-Protocol** | Proof of Purchase — on-chain receipts, access passes, and fan experiences |
| **NFT-Comments** | On-chain commentary and provenance annotations attached to any NFT |

### Solidity Smart Contract — Ethereum

| Contract | Purpose |
|---|---|
| **Medialane MDLN** | Governance token — 21M fixed supply, Starknet bridge support |

**Key addresses (Starknet Mainnet):**

| Contract | Address |
|---|---|
| Marketplace | `0x04299b51289aa700de4ce19cc77bcea8430bfd1aef04193efab09d60a3a7ee0f` |
| Collection Registry | `0x05c49ee5d3208a2c2e150fdd0c247d1195ed9ab54fa2d5dea7a633f39e4b205b` |
| NFTComments | `0x070edbfa68a870e8a69736db58906391dcd8fcf848ac80a72ac1bf9192d8e232` |

**Order protocol:** All marketplace intents use **SNIP-12 typed data signing** — signed off-chain and settled on-chain in atomic multicalls. Domain: `{ name: "Medialane", version: "1", revision: "1" }`.

---

## Services

### NFT Marketplace
The high-integrity exchange for all tokenized IP assets — ERC721 and ERC1155. Secondary market trading, auctions, and remix licensing with programmable terms enforced by smart contracts. **1% fee** on all transactions. Gas is sponsored — no ETH or STRK required.

- List, buy, and auction IP NFTs
- Make and accept offers
- Cart-based multi-asset checkout
- On-chain provenance and ownership verification
- Remix and derivative licensing with creator approval flows

### Creator Launchpad
Tools for creators to unlock new revenue streams from intellectual property:

| Service | Description |
|---|---|
| **Collection Drop** | ERC721 NFT launches with mint phases and allowlists |
| **NFT Editions** | ERC1155 multi-edition IP tokens — music, art, research, and more |
| **POP Protocol** | Tokenized Proof of Purchase, event access, and fan experiences |
| **IP Commissions** | On-demand creative work with on-chain agreements |
| **IP Club** | Gated creator communities, memberships, and subscriptions |
| **IP Tickets** | Tokenized access and event passes |

### Programmable Licensing
Every IP asset on Medialane carries embedded, on-chain licensing terms — no lawyers required. Creators define how their work is used, shared, remixed, and commercialized. Terms are immutable and enforced by the marketplace contract on every transaction.

**Supported license types:** ARR · CC BY · CC BY-SA · CC BY-NC · CC BY-NC-SA · CC BY-ND · CC0 · Custom

**License attributes embedded in every NFT:**
- Commercial use policy
- Derivative works rules
- **AI Training policy** — one of the first platforms to make AI data use an explicit on-chain attribute
- Geographic scope (worldwide or jurisdiction-specific)
- Royalty percentage (0–100%, enforced on every secondary sale)

**Supported IP types:** Music · Film · Art · Photography · Literature · Gaming · Software · Research · Fashion · Architecture · Design · Other

**Berne Convention compliance** — cryptographic timestamps serving as copyright proof across 181 countries.

### Autonomous AI Agent Infrastructure
Medialane is designed for machine interoperability from day one — on-chain autonomy, ZK proofs, and trustless infrastructure enabling AI agents to own, trade, and license IP without human intermediaries.

---

## Developer Ecosystem

### TypeScript SDK — [`medialane-sdk`](https://github.com/medialane-io/medialane-sdk)

```bash
npm install @medialane/sdk
```

Framework-agnostic SDK for the Medialane protocol and API. Works in Next.js, React, Node.js, and browser environments.

```ts
import { createMedialaneClient } from "@medialane/sdk";

const client = createMedialaneClient({ apiUrl: "...", apiKey: "ml_live_..." });

// Marketplace
const orders = await client.marketplace.getOrders({ status: "ACTIVE" });

// Creator profiles
const profile = await client.api.getCreatorProfile("0x...");

// Collections
const collections = await client.api.getCollectionsByOwner("0x...");
```

Current version: **v0.7.x** · Get an API key at [portal.medialane.io](https://portal.medialane.io)

---

### UI Component Library — [`medialane-ui`](https://github.com/medialane-io/medialane-ui)

```bash
npm install @medialane/ui
```

Shared React component library for all Medialane apps. 23+ components including `TokenCard`, `CollectionCard`, `ListingCard`, `ActivityRow`, `HeroSlider`, discover components, launchpad grids, and motion primitives.

```ts
import uiPreset from "@medialane/ui/preset"; // Tailwind preset
import { TokenCard, CollectionCard, ActivityRow, HeroSlider } from "@medialane/ui";
```

Current version: **v0.4.0** · Peer deps: React 18+, Next 14+, framer-motion, lucide-react

---

## Repository Index

| Repository | Description |
|---|---|
| [`medialane-contracts`](https://github.com/medialane-io/medialane-contracts) | Cairo + Solidity smart contracts — marketplace protocols, collection drops, POP, MDLN token |
| [`medialane-backend`](https://github.com/medialane-io/medialane-backend) | Off-chain API + indexer — Bun · Hono · Prisma · PostgreSQL · starknet.js |
| [`medialane-sdk`](https://github.com/medialane-io/medialane-sdk) | `@medialane/sdk` — TypeScript SDK for the Medialane protocol and API |
| [`medialane-ui`](https://github.com/medialane-io/medialane-ui) | `@medialane/ui` — Shared React component library (23+ components) |
| [`medialane-io`](https://github.com/medialane-io/medialane-io) | [medialane.io](https://medialane.io) — consumer app with social login and invisible wallet |
| [`medialane-dapp`](https://github.com/medialane-io/medialane-dapp) | [dapp.medialane.io](https://dapp.medialane.io) — permissionless dApp for self-custodial users |
| [`medialane-portal`](https://github.com/medialane-io/medialane-portal) | [portal.medialane.io](https://portal.medialane.io) — developer portal, API keys, documentation |
| [`medialane-dao`](https://github.com/medialane-io/medialane-dao) | [medialane.org](https://medialane.org) — DAO governance, MDLN token, community treasury |

---

## Backend Architecture

The Medialane off-chain layer is a single high-performance Bun process with three components:

- **Mirror** — polls Starknet RPC for new blocks, processes on-chain events, writes to PostgreSQL. ~6s polling cadence, 1–3 block lag.
- **Orchestrator** — in-memory worker for metadata jobs: IPFS resolution, stats updates, collection indexing.
- **API** — Hono REST server exposing all platform data to frontends and third-party integrations via `@medialane/sdk`.

---

## Governance — MDLN Token

Medialane is governed by the **Medialane DAO** — a Utah DAO LLC where protocol decisions are made by MDLN token holders, not by any company or venture capital.

| | |
|---|---|
| **Supply** | 21,000,000 MDLN (fixed permanently) |
| **Vesting** | 9-year linear unlock |
| **Allocation** | 100% community treasury — zero VC, zero insider allocation |
| **Network** | Starknet Mainnet · Ethereum (bridge supported) |
| **Governance** | On-chain voting by MDLN holders |

---

## Protocol Principles

| Principle | What it means |
|---|---|
| **Open source** | All protocol contracts are publicly auditable |
| **Immutable** | Deployed contracts cannot be upgraded or altered |
| **Permissionless** | Anyone can interact without approval or registration |
| **Censorship-resistant** | STARK proofs verified on Ethereum; no single point of failure |
| **Trustless** | Smart contracts enforce all agreements — no intermediaries |
| **AI-native** | Designed for autonomous agent interoperability from day one |

---

## Learn More

- [medialane.io/learn](https://medialane.io/learn) — NFTs, Creator Launchpad, Marketplace, Web3 & Starknet, Berne Convention, Programmable Licensing
- [medialane.io/docs](https://medialane.io/docs) — Protocol specification, API reference, community guidelines
- [portal.medialane.io](https://portal.medialane.io) — Get your API key and start building

---

## Medialane DAO

[dao@medialane.org](mailto:dao@medialane.org) · [@integrityweb](https://t.me/integrityweb) · [medialane.org](https://medialane.org)
