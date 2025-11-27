# Security Policy

This project is static, zero-dependency, and contains no backend services.  
Security considerations are minimal but still important.

---

## Reporting Issues

If you discover a potential vulnerability:

1. Do **not** open a public issue.  
2. Email the project maintainer directly.  
3. Provide a clear description and steps to reproduce.

The project owner will review the report and respond promptly.

---

## Scope

Valid security concerns include:

- Cross-site scripting introduced through HTML changes
- Unsafe external links
- Insecure inline scripts
- Misuse of browser APIs
- JavaScript that violates the data-only rule and affects user state

Because the project has no backend:

- No authentication is involved  
- No server-side code exists  
- No dependencies or package CVEs apply  

Keep contributions strictly aligned with the D7460N Architecture to avoid accidental security regressions.
