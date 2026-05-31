<p align="center">
  <img src="https://veritaschain.org/assets/img/logo.png" alt="VeritasChain Protocol" width="180"/>
</p>

<h1 align="center">VeritasChain Protocol (VCP)</h1>

<p align="center">
  <strong>The Global Audit Standard for Algorithmic Trading</strong><br/>
  <em>"Verify, Don't Trust" — Encoding Trust in the Algorithmic Age</em>
</p>

<p align="center">
  <a href="https://veritaschain.org">🌐 Website</a> •
  <a href="https://veritaschain.org/explorer/app/">🔍 Explorer</a> •
  <a href="https://github.com/veritaschain/vcp-spec">📋 Specification</a> •
  <a href="#-quick-start-5-minutes">⚡ Quick Start</a> •
  <a href="https://veritaschain.org/certified/">✅ Get Certified</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/VCP-v1.2-blue?style=flat-square" alt="VCP Version"/>
  <img src="https://img.shields.io/badge/Status-Production%20Ready-brightgreen?style=flat-square" alt="Status"/>
  <img src="https://img.shields.io/badge/License-CC%20BY%204.0-green?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Languages-EN%20|%20JA%20|%20ZH-orange?style=flat-square" alt="Languages"/>
</p>

---

## 📄 Academic Reference (Preprint)

Kamimura, T. (2025).  
*Hybrid Post-Quantum Signatures for Tamper-Evident Audit Trails:  
Formal Security Analysis and Design Trade-offs.*  
Zenodo. https://zenodo.org/records/17920524

> This paper presents a research-oriented cryptographic design and formal security analysis;  
> it is **not** a finalized protocol specification.

---

## 📜 Internet-Draft (IETF – in preparation)

An Internet-Draft is in preparation to propose VCP as a
SCITT-aligned auditability profile for algorithmic trading systems.

*Status:* Draft in progress (not yet submitted to IETF Datatracker)

- Working title: **SCITT Profile for Verifiable Trading Audit Trails**
- Target WG: **IETF SCITT (Security Area)**

---

## 📌 Canonical Specification

The canonical (normative) specification of VeritasChain Protocol (VCP)
is maintained in the following repository and directory structure:

```text
vcp-spec/
 └─ spec/
    ├─ v1.2/   (current)
    ├─ v1.1/   (legacy)
    └─ v1.0/   (legacy)
```
All other formats (HTML, PDF, translations) are non-normative.

---

## AI Decision Auditability Benchmark (v1.0)

A vendor-neutral benchmark for evaluating the **auditability and evidence quality** of AI and algorithmic decision systems.

- Designed for audit, assurance, and compliance teams  
- 10 criteria / 20-point evaluation scale  
- Minimal assessment executable in ~3 hours  
- Aligned with EU AI Act (Articles 12, 13, 14, 17) and MiFID II / RTS requirements  

Canonical reference (released v1.0):  
https://github.com/veritaschain/vcp-spec/tree/main/benchmark

Theoretical foundation (preprint):  
Why Open Cryptographic Standards Matter for AI Auditability  
https://zenodo.org/records/17947483


## 📖 What is VCP?

**VeritasChain Protocol (VCP)** is the world's first open standard for creating **immutable, cryptographically verifiable audit trails** in algorithmic and AI-driven trading systems.

### The Problem

In 2024-2025, the proprietary trading industry faced a crisis:
- **$450M+** in trader payouts frozen
- **80-100** prop firms collapsed or suspended operations
- **Zero** standardized way to verify trading records

### The Solution

VCP provides a universal audit format that enables:

| Capability | Description |
|------------|-------------|
| **Hash Chain** | SHA-256 linked events create tamper-evident audit trails |
| **Digital Signatures** | Ed25519 signatures prove event authenticity |
| **Merkle Proofs** | RFC 6962-compliant proofs for external verification |
| **Regulatory Alignment** | EU AI Act, MiFID II, SEC/FINRA, FCA ready |

---

## ⚡ Quick Start (5 Minutes)

### Python

```bash
pip install veritaschain
```

```python
from veritaschain import VcpLogger, create_event
import os

# Initialize
logger = VcpLogger(
    endpoint="https://api.veritaschain.org/v1",
    api_key=os.environ["VCP_API_KEY"]
)

# Log a trading signal
event = create_event("SIG", {
    "venue_id": "MT5_DEMO",
    "symbol": "EURUSD",
    "account_id": "demo_account",
    "vcp_gov": {
        "algo_id": "my-strategy-v1",
        "confidence_score": "0.85"
    }
})

logger.log(event)
logger.flush()
print(f"✅ Logged: {event.header.event_id}")
```

### TypeScript

```bash
npm install @veritaschain/sdk
```

```typescript
import { createLogger, createEvent } from '@veritaschain/sdk';

const logger = createLogger({
  endpoint: 'https://api.veritaschain.org/v1',
  apiKey: process.env.VCP_API_KEY!
});

const event = createEvent('ORD', {
  venueId: 'EXCHANGE_01',
  symbol: 'BTCUSD',
  accountId: 'trader_123',
  vcpTrade: {
    orderId: 'ord_001',
    side: 'BUY',
    price: '42150.50',
    quantity: '0.5'
  }
});

await logger.log(event);
console.log(`✅ Logged: ${event.header.eventId}`);
```

### Verify with Explorer API

```bash
# Get Merkle proof (no server trust required)
curl -H "Authorization: Bearer $VCP_API_KEY" \
  https://explorer.veritaschain.org/api/v1/events/{event_id}/proof
```

📚 **Full Examples:** [Python SDK Guide](https://github.com/veritaschain/vcp-sdk-spec/blob/main/examples/python/) | [Explorer API Guide](https://github.com/veritaschain/vcp-explorer-api/blob/main/docs/API_QUICKSTART.md)

---

## 📦 Repositories

| Repository | Description | For |
|------------|-------------|-----|
| [**vcp-spec**](https://github.com/veritaschain/vcp-spec) | 📋 Official VeritasChain Protocol (VCP) Specification (canonical, versioned) | Protocol implementers |
| [**vcp-sdk-spec**](https://github.com/veritaschain/vcp-sdk-spec) | 🛠️ SDK Interface (TypeScript/Python/MQL5) | SDK developers |
| [**vcp-explorer-api**](https://github.com/veritaschain/vcp-explorer-api) | 🔍 Explorer GUI & API | Verification & audit |
| [**vcp-rta-reference**](https://github.com/veritaschain/vcp-rta-reference) | 🧪 Non-certified reference implementation (audit trail demo) | Evaluation, PoC |
| [**vcp-sidecar-guide**](https://github.com/veritaschain/vcp-sidecar-guide) | 🔌 MT4/MT5/cTrader Integration | Platform integrators |
| [**vcp-site**](https://github.com/veritaschain/vcp-site) | 🌐 Official Website | - |
| [**vcp-market-intelligence**](https://github.com/veritaschain/vcp-market-intelligence) | 📊 Industry Reports | Business stakeholders |

---

## 🏅 Certification Tiers

| Tier | Target | Precision | Signature |
|------|--------|-----------|-----------|
| 🥈 **Silver** | Retail traders, small prop firms | MILLISECOND | Delegated (VCC) |
| 🥇 **Gold** | Institutional traders, mid-size firms | MICROSECOND | Self-signed Ed25519 |
| 🏆 **Platinum** | HFT firms, exchanges | NANOSECOND | HSM-backed |

**→ [Get VC-Certified](https://certified.veritaschain.org)**

---

## 🌍 Regulatory Alignment

| Region | Regulation | VCP Module |
|--------|------------|------------|
| 🇪🇺 EU | AI Act, MiFID II | VCP-GOV, VCP-TRADE |
| 🇺🇸 US | SEC, FINRA, CAT | VCP-TRADE, VCP-RISK |
| 🇬🇧 UK | FCA | VCP-TRADE |
| 🌏 APAC | MAS, JFSA, SFC | All modules |

---

## 🛣️ Roadmap

| Phase | Status | Description |
|-------|--------|-------------|
| **1. Standardization** | ✅ Complete | VCP Spec, SDKs, Explorer |
| **2. Platformization** | 🚧 In Progress | VeritasChain Cloud (VCC) |
| **3. Certification** | 📅 Q1 2025 | VC-Certified program launch |
| **4. Universalization** | 📅 Future | Blockchain anchoring, PQC |

---

## 🤝 Contributing

We welcome contributions from the community!

- 🐛 **Issues:** Report bugs or request features
- 💬 **Discussions:** Ask questions, share ideas
- 🔧 **Pull Requests:** Contribute code or docs

See [CONTRIBUTING.md](https://github.com/veritaschain/vcp-spec/blob/main/CONTRIBUTING.md) for guidelines.

---

## 📞 Contact

| Channel | Link |
|---------|------|
| Website | [veritaschain.org](https://veritaschain.org) |
| Email | [info@veritaschain.org](mailto:info@veritaschain.org) |
| Technical | [technical@veritaschain.org](mailto:technical@veritaschain.org) |
| LinkedIn | [VeritasChain Inc.](https://linkedin.com/company/110199945) |

---

<p align="center">
  <strong>VeritasChain Standards Organization (VSO)</strong><br/>
  <em>Independent, vendor-neutral standards body for algorithmic trading auditability</em><br/><br/>
  © 2025-2026 VeritasChain Standards Organization (VSO).
</p>
