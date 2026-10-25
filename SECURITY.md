# Security Policy

## Supported Versions

This organization-wide policy applies to VSO specifications and first-party code. Repositories may give more specific instructions in their own SECURITY.md (for example [vap-spec](https://github.com/veritaschain/vap-spec/blob/main/SECURITY.md)); where they differ, the repository's policy applies.

Specification versions that receive security-relevant errata:

| Specification | Version | Supported |
| ------------- | ------- | --------- |
| VCP | 1.2.x (Released) | :white_check_mark: |
| VCP | 1.1.x | Known issues recorded; migrate to 1.2 |
| VCP | 1.0.x | :x: |
| VAP | 1.2.0 (Draft 3) | :white_check_mark: |
| CAP | 1.0 (Released) | :white_check_mark: |
| CPP | 1.4 (Released) | :white_check_mark: |

## Reporting a Vulnerability

We take the security of VeritasChain Protocol seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### How to Report

**Please do NOT report security vulnerabilities through public GitHub issues.**

Instead, please report them via email to:

📧 **security@veritaschain.org**

If you need an encrypted exchange, send a non-sensitive initial message so we can agree on a suitable channel. VSO does not currently publish a verified PGP key; availability of a key must not be assumed.

### What to Include

Please include the following information in your report:

- **Type of vulnerability** (e.g., buffer overflow, SQL injection, cross-site scripting)
- **Affected component(s)** (e.g., VCP Explorer API, SDK, Sidecar integration)
- **Full paths of source file(s)** related to the vulnerability (if known)
- **Step-by-step instructions** to reproduce the issue
- **Proof-of-concept or exploit code** (if available)
- **Impact assessment** of the vulnerability
- **Any potential mitigations** you have identified

### Response Timeline

These are operational targets, not a guaranteed service level. Business days mean Monday–Friday, excluding Japanese public holidays (Asia/Tokyo).

| Action | Target |
| ------ | -------- |
| Initial response | Within 2 business days of receipt |
| Status update | Aim for 7 calendar days after acknowledgment |
| Vulnerability assessment | Aim for 14 calendar days after acknowledgment |
| Fix development | Depends on severity |
| Public disclosure | After fix is released |

### What to Expect

1. **Acknowledgment**: We aim to acknowledge receipt of your vulnerability report within 2 business days.

2. **Communication**: We will keep you informed about the progress of addressing the vulnerability.

3. **Assessment**: Our security team will investigate and assess the impact of the reported vulnerability.

4. **Resolution**: We will work on a fix and coordinate the release timeline with you.

5. **Credit**: If you wish, we will publicly acknowledge your responsible disclosure in our release notes.

## Security Best Practices

When implementing VCP in your systems, please follow these security best practices:

### Cryptographic Requirements

- **Ed25519 Signatures**: Use only compliant Ed25519 implementations
- **SHA-256 Hash Chains**: Ensure proper hash chain validation
- **Merkle Proofs**: Verify RFC 6962 compliance for all Merkle tree operations
- **Key Management**: Store private keys securely, never in source code or public repositories

### API Security

- Use HTTPS for all API communications
- Implement proper authentication and authorization
- Rate limit API requests to prevent abuse
- Validate all input data before processing

### Data Protection

- Encrypt sensitive data at rest and in transit
- Implement proper access controls
- Maintain audit logs for all security-relevant operations
- Follow GDPR, MiFID II, and other applicable regulations

## Security Updates

Security updates are released as needed. To stay informed:

- ⭐ **Star** and **Watch** our repositories on GitHub
- 📧 Subscribe to security announcements at info@veritaschain.org
- 🌐 Visit https://veritaschain.org for the latest updates

## Scope

This security policy applies to the following repositories:

- [vcp-spec](https://github.com/veritaschain/vcp-spec) - VCP Specification
- [vcp-explorer-api](https://github.com/veritaschain/vcp-explorer-api) - Explorer API
- [vcp-explorer-gui](https://github.com/veritaschain/vcp-explorer-gui) - Explorer GUI
- [vcp-sdk-spec](https://github.com/veritaschain/vcp-sdk-spec) - SDK Specification
- [vcp-sidecar-guide](https://github.com/veritaschain/vcp-sidecar-guide) - Sidecar Integration Guide
- [vcp-site](https://github.com/veritaschain/vcp-site) - Official Website

## Acknowledgments

We appreciate the security research community's efforts in helping us maintain the security of VeritasChain Protocol. Responsible disclosure helps protect our users and the broader ecosystem.

---

<p align="center">
  <strong>VeritasChain Standards Organization</strong><br/>
  <em>"Verify, Don't Trust"</em>
</p>
