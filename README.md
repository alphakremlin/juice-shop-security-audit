# OWASP Juice Shop — Security Assessment Report

**Type:** Web Application Security / OWASP Top 10
**Site:** juice-shop.herokuapp.com
**Auditor:** Ramone Scott — QA Engineer

## Summary
Full OWASP Top 10 security assessment of OWASP Juice Shop — a deliberately vulnerable Node.js/Angular application used for security training. All 10 OWASP categories assessed.

## OWASP Top 10 Results
| Category | Result |
|---|---|
| A01 Broken Access Control | FAIL |
| A02 Cryptographic Failures | FAIL |
| A03 Injection (SQLi + XSS) | FAIL |
| A04 Insecure Design | FAIL |
| A05 Security Misconfiguration | FAIL |
| A06 Vulnerable Components | FAIL |
| A07 Auth Failures | FAIL |
| A08 Software Integrity | WARN |
| A09 Logging & Monitoring | FAIL |
| A10 SSRF | WARN |

## Critical Findings
- SQL injection on search endpoint — full database readable
- Authentication bypass via SQLi — admin access without credentials
- Stored XSS in product descriptions and reviews
- IDOR on user profiles — any user can modify any other user's data
- Weak JWT signing — token forgery possible
- Stack traces returned in error responses

> Note: OWASP Juice Shop is intentionally vulnerable for educational purposes. All findings are documented from official OWASP Juice Shop vulnerability documentation and verified testing methodology.

---
*Ramone Scott · QA Engineer · Jamaica · Available for freelance audits*
