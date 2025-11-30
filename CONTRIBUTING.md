# Contributing to VeritasChain Protocol

Thank you for your interest in contributing to the VeritasChain Protocol (VCP)! This document provides guidelines and instructions for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)
- [Community](#community)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to info@veritaschain.org.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** (code snippets, configuration files)
- **Describe the behavior you observed and what you expected**
- **Include relevant logs and error messages**

### Suggesting Enhancements

Enhancement suggestions are welcome! Please provide:

- **A clear and descriptive title**
- **A detailed description of the proposed enhancement**
- **Explain why this enhancement would be useful**
- **List any alternatives you've considered**

### Contributing Code

We welcome code contributions! Areas where you can help:

- **Bug fixes** - Fix reported issues
- **Documentation** - Improve or translate documentation
- **Tests** - Add or improve test coverage
- **Features** - Implement new features (please discuss first)

### Improving Documentation

Documentation improvements are always welcome:

- Fix typos and grammatical errors
- Add missing information
- Improve clarity and readability
- Translate documentation (EN, JA, ZH supported)

## Getting Started

### Prerequisites

Depending on the repository, you may need:

- **Node.js 18+** and npm (for TypeScript projects)
- **Python 3.9+** (for Python projects)
- **MetaTrader 5** (for MQL5 projects)
- **Git** for version control

### Fork and Clone

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
   cd REPOSITORY-NAME
   ```
3. Add the upstream remote:
   ```bash
   git remote add upstream https://github.com/veritaschain/REPOSITORY-NAME.git
   ```

### Install Dependencies

```bash
# For Node.js projects
npm install

# For Python projects
pip install -r requirements.txt
```

## Development Workflow

### Creating a Branch

Create a branch for your changes:

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/issue-description
```

Branch naming conventions:
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation changes
- `refactor/` - Code refactoring
- `test/` - Test additions or modifications

### Making Changes

1. Make your changes in your branch
2. Write or update tests as needed
3. Ensure all tests pass
4. Update documentation if necessary

### Testing

```bash
# TypeScript projects
npm run lint
npm run type-check
npm run test

# Python projects
python -m pytest
```

## Style Guidelines

### TypeScript/JavaScript

- Use **ESLint** and **Prettier** for formatting
- Use TypeScript strict mode
- Prefer `const` over `let`
- Use meaningful variable and function names
- Add JSDoc comments for public APIs

```typescript
/**
 * Creates a new VCP event with the specified parameters.
 * @param eventType - The type of event (SIG, ORD, EXE, etc.)
 * @param payload - The event payload
 * @returns The created VCP event
 */
export function createEvent(eventType: EventType, payload: Payload): VcpEvent {
  // Implementation
}
```

### Python

- Follow **PEP 8** style guide
- Use **Black** for formatting
- Use **type hints** for function signatures
- Add docstrings for public functions

```python
def create_event(event_type: str, payload: dict) -> VcpEvent:
    """
    Creates a new VCP event with the specified parameters.

    Args:
        event_type: The type of event (SIG, ORD, EXE, etc.)
        payload: The event payload

    Returns:
        The created VCP event
    """
    # Implementation
```

### MQL5

- Use descriptive variable names
- Comment complex logic
- Follow MetaQuotes coding standards

### Documentation

- Use **Markdown** for documentation
- Keep line length reasonable (≤120 characters)
- Use headers to organize content
- Include code examples where helpful

## Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Types

- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Code style changes (formatting, etc.)
- `refactor` - Code refactoring
- `test` - Adding or modifying tests
- `chore` - Maintenance tasks
- `ci` - CI/CD changes

### Examples

```
feat(sdk): add Python SDK for VCP event logging

fix(explorer): resolve Merkle proof verification error

docs(readme): add Quick Start section in Japanese

ci: add GitHub Actions workflow for automated testing
```

## Pull Request Process

### Before Submitting

1. **Update your branch** with the latest upstream changes:
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **Ensure all checks pass**:
   - All tests pass
   - Code follows style guidelines
   - Documentation is updated

3. **Write a clear PR description**:
   - What changes were made
   - Why these changes were made
   - Any related issues (use `Fixes #123` to auto-close)

### Review Process

1. A maintainer will review your PR
2. Address any requested changes
3. Once approved, a maintainer will merge your PR

### After Merge

- Delete your feature branch
- Pull the latest changes from upstream

## Community

### Getting Help

- **GitHub Issues** - For bugs and feature requests
- **GitHub Discussions** - For questions and general discussion
- **Email** - info@veritaschain.org

### Stay Connected

- **Website**: https://veritaschain.org
- **GitHub**: https://github.com/veritaschain
- **LinkedIn**: https://linkedin.com/company/110199945

---

## Recognition

Contributors will be recognized in our release notes and on our website. Thank you for helping make VCP better!

---

<p align="center">
  <strong>VeritasChain Standards Organization</strong><br/>
  <em>"Verify, Don't Trust"</em>
</p>
