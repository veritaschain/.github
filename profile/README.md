<p align="center">
  <img src="https://veritaschain.org/assets/img/logo.png" alt="VeritasChain Standards Organization (VSO)" width="180"/>
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
| **VAP-LAP — Legal AI Profile** | **Proposed domain profile**; individual Internet-Draft `-05`. [Overview and AILEX product/use-case reference](https://veritaschain.org/vap/lap/). |
| **SDK interfaces and reference code** | [Interface specification](https://github.com/veritaschain/vcp-sdk-spec) and [VCP v1.1 reference implementation](https://github.com/veritaschain/vcp-rta-reference) are published. An [offline core for VCP v1.2](https://github.com/veritaschain/vcp-sdk) (v0.1.0, pre-release, first-party; Python, TypeScript, MQL5) is published on GitHub only. None of these is a certified SDK or a package-registry distribution. See the package-availability notice below. |
| **Explorer** | [API](https://github.com/veritaschain/vcp-explorer-api) and [GUI](https://github.com/veritaschain/vcp-explorer-gui) repositories are published; consult each repository's implementation status and setup instructions. |
| **Research implementation and reproduction kit** | **Experimental and unadopted**. Kit `b1af0dc`; subject `c8ccf97`. Internal validation is recorded; **independent third-party reproduction has not been established**. |

The [September 2026 implementation disclosure](https://github.com/veritaschain/vap-spec#implementation-status-mandatory-disclosure)
reports zero external implementations and zero Evidence Packs accepted in proceedings.
**Correction — 24 October 2026:** the earlier commercial contract figure has not
been substantiated by reconciliation with primary records and is withdrawn from
current public claims pending review. This does not establish a count of zero.
See the [dated correction](https://github.com/veritaschain/vap-spec/blob/main/disclosures/2026-10-24-commercial-contracts.md).
Commercial service activity is separate from external implementations,
independent validation and accepted Evidence Packs.

**Integrity review — 24 October 2026:** VCP v1.1/v1.2 alignment with VAP v1.2
is under review; full conformance has not been established. The
[technical-errata](https://github.com/veritaschain/vcp-spec/pull/3) and
[normative-change](https://github.com/veritaschain/vcp-spec/pull/4) drafts are
unadopted proposals, not an issued repair or a production-validation result.

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

## VAP-LAP — Legal AI Profile (proposed)

VAP-LAP proposes a domain profile for legal AI workflows, including consultation,
document drafting, fact checking and human review. The published proposal is
[draft-ailex-vap-legal-ai-provenance-05][lap-draft]
(26 October 2026; profile version 0.6.0).

Explore the [English overview][lap-en], [日本語][lap-ja] or [中文][lap-zh],
and the [proposal overview on GitHub][lap-github].
[AILEX is introduced as a product and use-case reference][ailex-reference]
for legal practice workflows. The overview explains the proposed profile's
registration and implementation status; product availability does not establish conformance.

[lap-draft]: https://datatracker.ietf.org/doc/draft-ailex-vap-legal-ai-provenance/05/
[lap-en]: https://veritaschain.org/vap/lap/
[lap-ja]: https://veritaschain.org/vap/lap/ja/
[lap-zh]: https://veritaschain.org/vap/lap/zh/
[lap-github]: https://github.com/veritaschain/vap-spec/blob/main/proposals/legal-ai-profile/README.md
[ailex-reference]: https://veritaschain.org/vap/lap/#ailex

---

## 📄 Academic Reference (Preprint)

Kamimura, T. (2025).  
*Hybrid Post-Quantum Signatures for Tamper-Evident Audit Trails:  
Formal Security Analysis and Design Trade-offs.*  
Zenodo. https://zenodo.org/records/17920524

> This paper presents a research-oriented cryptographic design and formal security analysis;  
> it is **not** a finalized protocol specification.

---

## 📜 Internet-Drafts (IETF)

The following five VSO individual Internet-Drafts are active in the IETF Datatracker (checked 2026-10-25).
None has been adopted by an IETF Working Group.

| Draft | Revision | Expires |
| --- | --- | --- |
| [`draft-kamimura-vap-framework`](https://datatracker.ietf.org/doc/draft-kamimura-vap-framework/) | -02 (2026-10-24) | 2027-04-27 |
| [`draft-kamimura-scitt-vcp`](https://datatracker.ietf.org/doc/draft-kamimura-scitt-vcp/) | -05 (2026-10-24) | 2027-04-27 |
| [`draft-kamimura-rats-behavioral-evidence`](https://datatracker.ietf.org/doc/draft-kamimura-rats-behavioral-evidence/) | -02 (2026-07-21) | 2027-01-22 |
| [`draft-kamimura-scitt-refusal-events`](https://datatracker.ietf.org/doc/draft-kamimura-scitt-refusal-events/) | -04 (2026-10-24) | 2027-04-27 |
| [`draft-vso-cpp-core`](https://datatracker.ietf.org/doc/draft-vso-cpp-core/) | -04 (2026-10-24) | 2027-04-27 |

Individual submissions are works in progress. They are not RFCs or IETF-endorsed
standards and have no formal standing in the IETF standards process.

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
| **Hash Chain** | Optional PrevHash linking of events at every tier since VCP v1.1 (RECOMMENDED for Gold and Platinum, VCP v1.2 HCH-002); Merkle batching and external anchoring are required at every tier |
| **Digital Signatures** | Ed25519 signatures bind signed bytes to a key under the verifier's trust policy |
| **Merkle Proofs** | RFC 6962 construction is required by VCP §6.2.1; the published builder and proof examples have known discrepancies under review. See the [pinned observations](https://github.com/veritaschain/vap-spec/blob/9fa5fbc68075079b4599e16940e9078db976cd59/experiments/vcp-v1.2-integrity-alignment/README.md) |
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

For producing and verifying VCP v1.2 events offline, use
[vcp-sdk](https://github.com/veritaschain/vcp-sdk) (v0.1.0, pre-release), installed
from its GitHub repository; its README lists what it does and does not check, and
a `VALID` result from it is not a conformance claim. For the v1.1 SDK interfaces,
start with the [SDK interface specification](https://github.com/veritaschain/vcp-sdk-spec)
or the [Python reference implementation](https://github.com/veritaschain/vcp-rta-reference).
For the Explorer API, follow its [local setup and implementation status](https://github.com/veritaschain/vcp-explorer-api#quick-start).
Official installation instructions will be added after package publication and
publisher verification.

---

## 📦 Repositories

| Repository | Description | For |
|------------|-------------|-----|
| [**vap-spec**](https://github.com/veritaschain/vap-spec) | VAP framework, Draft 3; common requirements and current disclosures | Framework/profile reviewers |
| [**cap-spec**](https://github.com/veritaschain/cap-spec) | Content profile; VAP mapping draft published, conformance unestablished | Content provenance implementers |
| [**cpp-spec**](https://github.com/veritaschain/cpp-spec) | Capture profile; VAP conformance unestablished | Capture provenance implementers |
| [**vcp-spec**](https://github.com/veritaschain/vcp-spec) | 📋 Official VeritasChain Protocol (VCP) Specification (canonical, versioned) | Protocol implementers |
| [**vcp-sdk-spec**](https://github.com/veritaschain/vcp-sdk-spec) | 🛠️ SDK Interface (TypeScript/Python/MQL5) | SDK developers |
| [**vcp-sdk**](https://github.com/veritaschain/vcp-sdk) | 🧰 Offline core for VCP v1.2 (Python/TypeScript/MQL5); v0.1.0 pre-release, first-party, not certified | Implementers, auditors |
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

See [CONTRIBUTING.md](https://github.com/veritaschain/.github/blob/main/CONTRIBUTING.md) for guidelines.

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
