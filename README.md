# 🔎 Web Reconnaissance Lab

## 📌 Project Overview

This project demonstrates a basic web reconnaissance workflow using commonly available cybersecurity tools.

The objective is to collect publicly available information about an authorized domain and document the findings.

### Tools Used

* WHOIS
* WhatWeb
* nslookup
* curl
* wafw00f
* DNSRecon
* Kali Linux

---

## 🎯 Learning Objectives

By completing this lab, I learned how to:

1. Identify domain registration information.
2. Fingerprint web technologies.
3. Resolve domain names to IP addresses.
4. Inspect HTTP response headers.
5. Identify the presence of a Web Application Firewall (WAF).
6. Enumerate publicly available DNS records.
7. Document reconnaissance findings professionally.

---

# 🧪 Tasks

## Task 1 — WHOIS

### Objective

Find publicly available domain registration information.

### Command

```bash
whois example.com
```

### Information to observe

* Registrar
* Registration date
* Expiration date
* Name servers
* Domain status
* Registrant information, where publicly available

### Evidence

Save the output to:

```text
results/whois.txt
```

---

# Task 2 — WhatWeb

## Objective

Identify technologies used by the target website.

### Command

```bash
whatweb https://example.com
```

### Information to observe

* Web server
* CMS
* JavaScript frameworks
* Web technologies
* Cookies
* Programming languages
* Security-related headers

### Evidence

Save the output to:

```text
results/whatweb.txt
```

---

# Task 3 — nslookup

## Objective

Resolve the domain name to its IP address.

### Command

```bash
nslookup example.com
```

You can also query specific DNS records:

```bash
nslookup -type=A example.com
```

```bash
nslookup -type=MX example.com
```

```bash
nslookup -type=NS example.com
```

### Evidence

Save the output to:

```text
results/nslookup.txt
```

---

# Task 4 — curl

## Objective

Inspect the HTTP response headers returned by the web server.

### Command

```bash
curl -I https://example.com
```

### Information to observe

Look for:

* HTTP status code
* Server
* Content-Type
* Location
* Set-Cookie
* Strict-Transport-Security
* Content-Security-Policy
* X-Frame-Options
* X-Content-Type-Options

### Evidence

Save the output to:

```text
results/curl-headers.txt
```

---

# Task 5 — WAFW00F

## Objective

Determine whether the website appears to be protected by a Web Application Firewall.

### Command

```bash
wafw00f https://example.com
```

### Information to observe

The tool may identify:

* Whether a WAF is present
* The WAF vendor, if detectable
* Detection confidence or supporting indicators

### Evidence

Save the output to:

```text
results/wafw00f.txt
```

> Note: WAF detection is not always conclusive. A result indicating that no WAF was detected does not prove that the site has no WAF.

---

# Task 6 — DNSRecon

## Objective

Enumerate publicly available DNS information.

### Command

```bash
dnsrecon -d example.com
```

### Information to observe

Depending on the target and DNS configuration, results may include:

* A records
* AAAA records
* MX records
* NS records
* SOA records
* TXT records
* CNAME records

### Evidence

Save the output to:

```text
results/dnsrecon.txt
```

---

# 📊 Findings Summary

After completing the tasks, document the results in the following table.

| Task | Tool     | Finding                                       |
| ---- | -------- | --------------------------------------------- |
| 1    | WHOIS    | Registrar and domain registration information |
| 2    | WhatWeb  | Detected web technologies                     |
| 3    | nslookup | Domain/IP resolution                          |
| 4    | curl     | HTTP response headers                         |
| 5    | WAFW00F  | WAF detection result                          |
| 6    | DNSRecon | Public DNS records                            |

---

# 📝 Final Report

The reconnaissance exercise provided an overview of the target's publicly observable infrastructure.

The assessment covered:

* Domain registration information
* Web technology fingerprinting
* DNS resolution
* HTTP headers
* WAF detection
* DNS record enumeration

These techniques demonstrate how publicly available information can be collected during the reconnaissance phase of a security assessment.

---

# ⚠️ Ethical Considerations

Only perform reconnaissance against systems that you own or have explicit authorization to assess.

Do not attempt to bypass security controls, exploit vulnerabilities, access restricted information, or disrupt services.

This project focuses on information gathering and documentation.

---

# 🧠 Skills Demonstrated

* Linux command-line usage
* Cybersecurity reconnaissance
* DNS analysis
* Web technology fingerprinting
* HTTP analysis
* WAF identification
* Security documentation
* Technical reporting

---

## Author

**Omotara Oluwadamilare**

Cybersecurity / IT Operations

---

## Disclaimer

This project is intended for educational and authorized security-testing purposes only.
