# DNS TXT Record Lookup Commands

This document provides a **quick reference** for querying **SPF, DKIM, and DMARC** records using `dig` (Mac/Linux) and `nslookup` (Windows).

## Command Reference

### 🔍 DKIM & DMARC Lookup Commands
- `dig TXT foo.bar._domainkey.example.com` – Look up DKIM TXT records
- `dig TXT _dmarc.example.org` – Look up DMARC TXT records
- `dig +short TXT _dmarc.domain.com` – Look up DMARC TXT records with a short response

### 🖥️ Windows `nslookup` Commands
- `nslookup` – Start `nslookup` interactive mode
- `set type=txt` – Set query type to TXT records
- `nslookup -type=txt domain.com` – Query TXT records for a domain
- `nslookup -type=txt _dmarc.domain.com` – Look up DMARC records
- `nslookup -type=txt _domainkey.domain.com` – Look up DKIM records

### 🖥️ Mac/Linux `dig` Commands
- `dig txt domain.com` – Look up TXT records
- `dig txt _dmarc.domain.com` – Query DMARC TXT records
- `dig txt selector._domainkey.domain.com` – Query DKIM TXT records
- `dig txt _spf.domain.com` – Look up SPF TXT records
- `dig +short txt domain.com` – Get a short TXT record response

---

## 📊 Comparison Table for Key Lookups

| Record  | Windows Command Line                        | Mac OS Terminal                         |
|---------|--------------------------------------------|-----------------------------------------|
| **SPF**  | `nslookup -type=txt domain.com`           | `dig txt domain.com`                    |
| **DKIM** | `nslookup` → `set q=txt` → `selector._domainkey.domain.com` | `dig txt s
