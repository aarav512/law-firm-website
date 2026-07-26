# Security Policy

## Reporting a Vulnerability

If you believe you have found a security vulnerability in this website, please report it responsibly.

**Do NOT open a public GitHub issue for security vulnerabilities.**

Instead, please email the firm directly with a description of the issue, steps to reproduce, and any relevant proof-of-concept:

- **Email:** srvsharma.adv@gmail.com
- **Phone:** +91 99990 46369

We will acknowledge receipt within 48 hours and aim to provide a substantive response within 5 business days.

## Scope

This security policy applies to the production website of Saurav Sharma & Associates – Lawyers & Solicitors, including:

- The homepage (`index.html`)
- The Our Team page (`team.html`)
- Legal pages (`privacy.html`, `terms.html`, `disclaimer.html`)
- All contact and subscription forms
- Server configuration (`.htaccess`)
- Any deployed Edge Functions or backend services

## Security Measures Implemented

### Server Security
- HTTPS is enforced via 301 redirect from HTTP
- HTTP Strict Transport Security (HSTS) with 2-year max-age, includeSubDomains, preload
- Directory browsing is disabled
- Server signature is hidden
- Sensitive files (`.env`, `.git`, config, backup, log files) are protected from direct access

### Security Headers
- Content-Security-Policy (CSP)
- Strict-Transport-Security (HSTS)
- X-Frame-Options: SAMEORIGIN
- X-Content-Type-Options: nosniff
- Referrer-Policy: strict-origin-when-cross-origin
- Permissions-Policy
- Cross-Origin-Resource-Policy
- Cross-Origin-Opener-Policy
- Cross-Origin-Embedder-Policy

### Form Security
- Client-side and server-side validation
- Input sanitization and output escaping
- XSS protection
- Honeypot anti-spam field (`_gotcha`)
- Client-side rate limiting to prevent submission abuse
- Secure email handling via Formspree

### Repository Security
- `.gitignore` excludes sensitive files, dependencies, and environment files
- No secrets, API keys, or credentials are committed to the repository

## Disclosure Policy

- We request a reasonable disclosure timeline (minimum 90 days) before any public disclosure.
- We commit to acknowledging and addressing valid reports in good faith.
- We will credit reporters (with permission) in release notes once a fix is deployed.

## Preferred Languages

English and Hindi.

## Last Updated

July 2026
