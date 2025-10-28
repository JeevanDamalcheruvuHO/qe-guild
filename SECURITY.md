# Security Policy

## Supported Versions

This repository contains documentation, templates, and tooling guidance for the Home Office QE Guild. Security updates are applied to the latest version only.

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| Older   | :x:                |

## Reporting a Vulnerability

The QE Guild takes security seriously. If you discover a security vulnerability in our templates, documentation, or tooling recommendations, please report it responsibly.

### What to Report

Please report:
- **Template vulnerabilities** - Security issues in code templates
- **Dependency vulnerabilities** - Outdated or vulnerable dependencies in examples
- **Documentation issues** - Guidance that could lead to insecure implementations
- **Credential exposure** - Any accidentally committed secrets or credentials
- **CI/CD security issues** - Vulnerabilities in our GitHub Actions workflows

### How to Report

**Do NOT open a public GitHub issue for security vulnerabilities.**

Instead, please report security issues privately to:

**Email:** qe-guild-leads@homeoffice.gov.uk

**Subject Line:** `[SECURITY] Brief description of the issue`

**Include:**
1. **Description** - Clear explanation of the vulnerability
2. **Impact** - Potential security impact and affected components
3. **Steps to Reproduce** - How to reproduce the issue
4. **Affected Files** - Which templates, docs, or workflows are affected
5. **Suggested Fix** - If you have a recommendation (optional)

### Response Timeline

- **Acknowledgement:** Within 2 business days
- **Initial Assessment:** Within 5 business days
- **Fix Timeline:** Depends on severity
  - Critical: 1-3 days
  - High: 1 week
  - Medium: 2 weeks
  - Low: Next scheduled release

### Disclosure Policy

- We will acknowledge your report within 2 business days
- We will keep you informed of our progress
- Once the issue is resolved, we will credit you (if desired) in the fix announcement
- We request that you do not publicly disclose the issue until we have released a fix

## Security Best Practices for Contributors

When contributing to this repository:

### ✅ Do
- Review templates for common security issues before submission
- Use `.env.example` files with placeholder values only
- Add sensitive files to `.gitignore`
- Keep dependencies up to date
- Follow principle of least privilege in examples
- Include security considerations in documentation
- Use environment variables for sensitive configuration

### ❌ Don't
- Commit real credentials, API keys, or secrets
- Include real production URLs or internal endpoints
- Hard-code passwords or tokens in examples
- Ignore Dependabot security alerts
- Use outdated or vulnerable dependencies
- Commit `.env` files
- Include PII (Personally Identifiable Information) in examples

## Security in Templates

All templates in this repository should follow these security principles:

### 1. Credential Management
- Never hard-code credentials
- Use environment variables
- Provide `.env.example` with placeholders
- Include `.gitignore` to prevent credential commits

### 2. Dependency Security
- Pin dependency versions
- Regular updates via Dependabot
- Avoid dependencies with known CVEs
- Minimal dependency footprint

### 3. Authentication Best Practices
- Demonstrate secure authentication patterns
- Support SSO/Enterprise auth where applicable
- Avoid basic auth in production examples
- Show token refresh patterns

### 4. Data Handling
- No real PII in test data
- Demonstrate data sanitisation
- Show secure data storage patterns
- Include data cleanup after tests

### 5. CI/CD Security
- Don't expose secrets in logs
- Use GitHub Secrets for sensitive data
- Limit workflow permissions (principle of least privilege)
- Review third-party actions for security

## Security Checklist for Template Submissions

Before submitting a template, verify:

- [ ] No credentials or secrets committed
- [ ] `.env.example` provided (not `.env`)
- [ ] `.gitignore` includes sensitive files
- [ ] Dependencies are current and have no known CVEs
- [ ] Authentication examples follow best practices
- [ ] No real PII in test data
- [ ] CI/CD workflows don't expose secrets
- [ ] Security considerations documented in README

## Known Security Considerations

### Tool-Specific Guidance

**Postman (Not Approved)**
- Avoid Postman due to cloud sync security concerns
- Use Bruno instead (file-based, no cloud sync)

**Cloud Services**
- Be cautious with cloud-based tools
- Verify data residency requirements
- Check HO compliance before recommending

**Open Source Dependencies**
- Regular security scanning via Dependabot
- Avoid unmaintained packages
- Review package permissions

## Security Resources

### For Contributors
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [Home Office Security Guidance](https://www.gov.uk/government/organisations/home-office)

### For Template Users
- Each template's README includes security considerations
- See `/docs/standards/security-guidelines.md` (when created)
- Review tool-specific security documentation

## Security Review Process

Templates undergo security review before approval:

1. **Automated Scanning** - Dependabot, CodeQL (future)
2. **Manual Review** - CODEOWNERS review for security issues
3. **Ongoing Monitoring** - Dependabot alerts, periodic reviews
4. **Community Reports** - Security vulnerability reports from users

## Questions?

For non-security questions about templates or tools, use:
- GitHub Issues
- GitHub Discussions
- Email: qe-guild-leads@homeoffice.gov.uk

For security issues, always use the private reporting method above.

---

**Last Updated:** October 2025  
**Next Review:** January 2026
