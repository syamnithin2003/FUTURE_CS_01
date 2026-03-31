# Vulnerability Assessment Report

## Website Tested
- Target: http://demo.testfire.net
- Description: A deliberately vulnerable web application (Altoro Mutual) used for cybersecurity learning and testing.

---

## Scope of Testing
This assessment was conducted under a **read-only scope** with ethical practices.

### Included:
- Passive scanning
- Security header analysis
- Service exposure identification
- Client-side inspection

### Excluded:
- Exploitation
- Brute force attacks
- Login bypass attempts
- Denial of Service (DoS)

---

## Tools Used

### 1. Nmap
- Used for port scanning and service detection
- Command:**nmap -sV demo.testfire.net**

### 2. OWASP ZAP (Passive Scan)
- Used to detect security vulnerabilities without active exploitation
- Findings:
- Missing security headers
- CSRF protection issues
- Cookie misconfigurations

### 3. Browser DevTools
- Used for analyzing:
- HTTP headers
- Cookies
- Session handling

---

## Key Findings

- Exposed web services (ports 80, 443, 8080)
- Missing security headers:
- Content Security Policy (CSP)
- HSTS
- X-Frame-Options
- Absence of Anti-CSRF tokens
- Cookie security issues (missing SameSite)
- Server information disclosure

---

## Risk Summary

| Issue                          | Risk Level |
|-------------------------------|------------|
| Exposed Services              | Medium     |
| Missing Security Headers      | Medium     |
| CSRF Vulnerability            | Medium     |
| Cookie Misconfiguration       | Medium     |
| Information Disclosure        | Low        |

---

## Recommendations

- Restrict unnecessary open ports
- Implement CSRF protection tokens
- Add security headers (CSP, HSTS, X-Frame-Options)
- Secure cookies (HttpOnly, Secure, SameSite)
- Hide server information
- Regular security updates and monitoring

---

## Proof of Concept

Screenshots of tool outputs are available in the `Proof of Concept/` folder.

---

## Date
07 March 2026

---

## Created
Yanamadala Syam Nithin  
📧 syamnithin2003@gmail.com

---

## Disclaimer
This project is for educational purposes only. The tested website is intentionally vulnerable.
