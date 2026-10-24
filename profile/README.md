<p align="center">
  <img src="https://veritaschain.org/assets/img/logo.png" alt="VeritasChain Protocol" width="180"/>
</p>

<h1 align="center">VeritasChain Standards Organization (VSO)</h1>

<p align="center">
  <strong>VAP / VCP — specifications and research tools for verifiable records</strong><br/>
  <em>"Verify, Don't Trust" — Encoding Trust in the Algorithmic Age</em>
</p>

<p align="center">
  <a href="https://veritaschain.org">🌐 Website</a> •
  <a href="https://veritaschain.org/explorer/app/">🔍 Explorer</a> •
  <a href="https://github.com/veritaschain/vcp-spec">📋 Specification</a> •
  <a href="#-getting-started">⚡ Quick Start</a> •
  <a href="https://veritaschain.org/certified/">Assessment information</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/VCP-v1.2-blue?style=flat-square" alt="VCP Version"/>
  <img src="https://img.shields.io/badge/VCP_spec-GA-blue?style=flat-square" alt="VCP specification GA; not a product certification"/>
  <img src="https://img.shields.io/badge/License-CC%20BY%204.0-green?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Languages-EN%20|%20JA%20|%20ZH-orange?style=flat-square" alt="Languages"/>
</p>

---

## Publication and implementation status

These are separate statuses; publication is not independent validation or certification.

| Item | Confirmed public status |
| --- | --- |
| **VeritasChain Protocol (VCP)** | Finance profile; **v1.2 specification GA, 2026-07-06**. See the [canonical specification and known issues](https://github.com/veritaschain/vcp-spec). This does not establish production suitability of every implementation. |
| **Verifiable AI Provenance Framework (VAP)** | **v1.2 Draft 3**. See the [framework repository](https://github.com/veritaschain/vap-spec). An individual Internet-Draft is not IETF adoption. |
| **SDK interfaces and reference code** | [Interface specification](https://github.com/veritaschain/vcp-sdk-spec) and [VCP v1.1 reference implementation](https://github.com/veritaschain/vcp-rta-reference) are published. They are not a verified, complete VCP v1.2 SDK package distribution. See the package-availability notice below. |
| **Explorer** | [API](https://github.com/veritaschain/vcp-explorer-api) and [GUI](https://github.com/veritaschain/vcp-explorer-gui) repositories are published; consult each repository's implementation status and setup instructions. |
| **Research implementation and reproduction kit** | **Experimental and unadopted**. Kit `b1af0dc`; subject `c8ccf97`. Internal validation is recorded; **independent third-party reproduction has not been established**. |

The [September 2026 implementation disclosure](https://github.com/veritaschain/vap-spec#implementation-status-mandatory-disclosure)
reports zero external implementations and zero Evidence Packs accepted in proceedings.
It separately reports ten paid service contracts held by the operating company.
This is a dated self-disclosure, not a fresh contract audit; service contracts are
not external implementations, independent validation, or accepted Evidence Packs.

### Unadopted research implementation and reproduction kit

[**Download the fixed research kit and preserved execution evidence**](https://github.com/veritaschain/vap-spec/releases/tag/research-kit-b1af0dc-20261024).
The distribution preserves the tested ZIP, SHA-256 checksums, complete internal CI
outputs and workflow logs separately from the specification release series.
It evaluates submitted evidence and a synthetic mock gate / OS-isolation experiment.
It does not modify current VAP v1.2, the existing verifier, gate, OS experiment or K3.

The internal record reports 27 package tests plus 138 existing regression tests,
and matching results for 16 OS, 15 gate and 14 verifier cases. These are internal
checks, not an independent reproduction, a certified product, or a claim that all
real-world actions are observed or blocked. Use the fixed [English instructions](https://github.com/veritaschain/vap-spec/blob/b1af0dc9d368b466bf74e7c1b2a6808fb41949ae/reproduction/os-isolation/README.md)
or [日本語手順](https://github.com/veritaschain/vap-spec/blob/b1af0dc9d368b466bf74e7c1b2a6808fb41949ae/reproduction/os-isolation/RUN-ja.md).

---

## 📄 Academic Reference (Preprint)

Kamimura, T. (2025).  
*Hybrid Post-Quantum Signatures for Tamper-Evident Audit Trails:  
Formal Security Analysis and Design Trade-offs.*  
Zenodo. https://zenodo.org/records/17920524

> This paper presents a research-oriented cryptographic design and formal security analysis;  
> it is **not** a finalized protocol specification.

---

## 📜 Internet-Draft (IETF)

VCP's SCITT profile for verifiable audit trails in algorithmic trading is published
in the IETF Datatracker as an **active individual Internet-Draft**.

- Document: [`draft-kamimura-scitt-vcp-03`](https://datatracker.ietf.org/doc/draft-kamimura-scitt-vcp/)
- Revision date: **2026-07-21**
- Status: **Active Internet-Draft (individual)**; not adopted by any IETF Working Group.

This individual submission is a work in progress, is not an RFC or an IETF-endorsed
standard, and has no formal standing in the IETF standards process.

---

## 📌 Canonical Specification

The canonical (normative) specification of VeritasChain Protocol (VCP)
is maintained in the following repository and directory structure:

```text
vcp-spec/
 └─ spec/
    ├─ v1.2/   (current specification, GA)
    ├─ v1.1/   (legacy)
    └─ v1.0/   (legacy)
```
The [canonical v1.2 specification](https://github.com/veritaschain/vcp-spec/blob/main/spec/v1.2/VCP-Specification-v1_2_en.md)
is the **GA specification**, following the merge of the
[GA cutover PR](https://github.com/veritaschain/vcp-spec/pull/1).
See the [canonical repository](https://github.com/veritaschain/vcp-spec) for release artifacts and known issues.

All other formats (HTML, PDF, translations) are non-normative.

---

## AI Decision Auditability Benchmark (v1.0)

A vendor-neutral benchmark for evaluating the **auditability and evidence quality** of AI and algorithmic decision systems.

- Designed for audit, assurance, and compliance teams  
- 10 criteria / 20-point evaluation scale  
- Includes published regulatory mappings; these do not establish legal compliance

Canonical reference (released v1.0):  
https://github.com/veritaschain/vcp-spec/tree/main/benchmark

Theoretical foundation (preprint):  
Why Open Cryptographic Standards Matter for AI Auditability  
https://zenodo.org/records/17947483


## 📖 What is VCP?

**VeritasChain Protocol (VCP)** is an open specification for **tamper-evident,
cryptographically verifiable audit trails** in algorithmic and AI-driven trading systems.
It is the finance profile of VAP.

Given the required evidence, trusted keys and anchoring assumptions, a third party
can check alterations to recorded evidence and omissions relative to an anchored,
committed set. Valid signatures do not establish that every real-world action was
observed, that a record is factually true, or that the action was authorized.
VAP itself does not prevent AI misconduct or recover actions that were never recorded.

### The Problem

An evaluator may receive records without enough evidence to check their integrity,
ordering or relationship to a committed set. The design goal is to make those
checks explicit, including the conditions under which evidence is insufficient.

### The Solution

VCP defines record structures and verification requirements, including:

| Capability | Description |
|------------|-------------|
| **Hash Chain** | SHA-256 linked events create tamper-evident audit trails |
| **Digital Signatures** | Ed25519 signatures bind signed bytes to a key under the verifier's trust policy |
| **Merkle Proofs** | RFC 6962-compliant proofs for external verification |
| **Evidence assessment** | Specification mappings support review; they do not establish regulatory approval or legal compliance |

---

## ⚡ Getting Started

### SDK package availability — not verified

As checked on **2026-10-22 (JST)**, the public npm registry returned 404 for
`@veritaschain/sdk`, and PyPI returned 404 for `veritaschain`. These names are
not currently verified public VSO SDK releases. Do not install packages under
these names based on older examples; availability alone would not establish
VSO ownership or authenticity.

The PyPI package `vcp-sdk` belongs to **Value Context Protocol**, a separate
project. It is not a substitute for the VeritasChain Protocol (VCP) SDK.

Start with the [SDK interface specification](https://github.com/veritaschain/vcp-sdk-spec)
or the [Python reference implementation](https://github.com/veritaschain/vcp-rta-reference).
For the Explorer API, follow its [local setup and implementation status](https://github.com/veritaschain/vcp-explorer-api#quick-start).
Official installation instructions will be added after package publication and
publisher verification.

---

## 📦 Repositories

| Repository | Description | For |
|------------|-------------|-----|
| [**vcp-spec**](https://github.com/veritaschain/vcp-spec) | 📋 Official VeritasChain Protocol (VCP) Specification (canonical, versioned) | Protocol implementers |
| [**vcp-sdk-spec**](https://github.com/veritaschain/vcp-sdk-spec) | 🛠️ SDK Interface (TypeScript/Python/MQL5) | SDK developers |
| [**vcp-explorer-api**](https://github.com/veritaschain/vcp-explorer-api) | 🔍 Explorer API; [GUI maintained separately](https://github.com/veritaschain/vcp-explorer-gui) | Verification & audit |
| [**vcp-rta-reference**](https://github.com/veritaschain/vcp-rta-reference) | 🧪 Non-certified reference implementation (audit trail demo) | Evaluation, PoC |
| [**vcp-sidecar-guide**](https://github.com/veritaschain/vcp-sidecar-guide) | 🔌 MT4/MT5/cTrader Integration | Platform integrators |
| [**vcp-site**](https://github.com/veritaschain/vcp-site) | 🌐 Official Website | - |
| [**vcp-market-intelligence**](https://github.com/veritaschain/vcp-market-intelligence) | 📊 Industry Reports | Business stakeholders |

---

## Assessment program status

Consult the [assessment program information](https://veritaschain.org/certified/),
[policies](https://veritaschain.org/vso/policies/) and [CAB registry](https://veritaschain.org/certified/cab/)
for current published information. No launch date is asserted here.
The [current VAP repository disclosure](https://github.com/veritaschain/vap-spec#what-this-repository-is--is-not)
explains that the listed CAB, VeritasChain Co., Ltd., operates VSO and is not
independent of the scheme owner. Specification publication, reference code and
internal research tests do not establish independent certification.

VCP tier requirements belong to the canonical VCP specification. Regulatory
mappings are explanatory material, not regulator endorsement or a guarantee of compliance.

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
| LinkedIn | [VeritasChain Co., Ltd.](https://linkedin.com/company/110199945) |

---

<p align="center">
  <strong>VeritasChain Standards Organization (VSO)</strong><br/>
  <em>Maintainer of VAP and VeritasChain Protocol (VCP)</em><br/><br/>
  © 2025-2026 VeritasChain Standards Organization (VSO).
</p>
