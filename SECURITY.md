# Security Policy

## Supported Versions

The following versions of VeritasChain Protocol (VCP) are currently supported with security updates:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take the security of VeritasChain Protocol seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### How to Report

**Please do NOT report security vulnerabilities through public GitHub issues.**

Instead, please report them via email to:

📧 **security@veritaschain.org**

If you prefer encrypted communication, please contact us first to obtain our PGP key.

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

| Action | Timeline |
| ------ | -------- |
| Initial response | Within 48 hours |
| Status update | Within 7 days |
| Vulnerability assessment | Within 14 days |
| Fix development | Depends on severity |
| Public disclosure | After fix is released |

### What to Expect

1. **Acknowledgment**: We will acknowledge receipt of your vulnerability report within 48 hours.

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
