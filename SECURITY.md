# Security Policy

## Reporting Security Issues

**Do not** create public GitHub issues for security vulnerabilities.

Instead, please report security issues to the maintainers by:
1. Opening a [GitHub Security Advisory](https://github.com/Furs-Tissue/listening-room/security/advisories/new)
2. Or emailing maintainers with details

### What to Include

When reporting a security issue, please include:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if known)

### Timeline

We aim to:
- Acknowledge receipt within 48 hours
- Provide initial assessment within 1 week
- Release a patch within 2 weeks (or timeline agreed with reporter)

## Supported Versions

| Version | Supported          |
|---------|-------------------|
| Latest  | ✅ Supported      |
| Older   | ⚠️ Case-by-case    |

## Security Best Practices for Contributors

When contributing code:
- **Input Validation**: Always validate and sanitize user input
- **Authentication**: Use secure authentication patterns
- **Encryption**: Use strong encryption for sensitive data
- **Dependencies**: Keep dependencies up to date
- **Secrets**: Never commit secrets or credentials
- **SQL Injection**: Use parameterized queries
- **XSS Prevention**: Sanitize output in frontend code
- **CSRF Protection**: Implement CSRF tokens where needed

### Code Review Security Checklist

Reviewers will check for:
- [ ] No hardcoded secrets or credentials
- [ ] Input is properly validated
- [ ] Authorization checks are in place
- [ ] Sensitive data is encrypted
- [ ] Dependencies are secure and up-to-date
- [ ] Common vulnerabilities are addressed (OWASP Top 10)

## Disclosure Policy

- We will work with security researchers responsibly
- We request 90 days before public disclosure
- We will credit researchers (if desired) in the advisory

## Security Headers

Recommended security headers for production deployment:
```
Content-Security-Policy: default-src 'self'
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
Strict-Transport-Security: max-age=31536000; includeSubDomains
```

## Dependencies Security

- Keep dependencies updated regularly
- Monitor for known vulnerabilities using tools like:
  - PHP: Composer's security advisory
  - JavaScript: npm audit, Snyk
  - GitHub's dependabot

## AI Agent Security Considerations

AI agents should:
- Follow the same security practices as human developers
- Not generate code with known security vulnerabilities
- Include security checks in generated code
- Report security findings when discovered
- Respect security embargoes during responsible disclosure

---

**Questions?** Open a discussion or contact maintainers privately.
