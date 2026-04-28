# 02 — ECSA Network Penetration Testing Methodology

**Course:** CYB/427 — Security Analyst Threat Testing
**Deliverable:** [`ECSA_Network_Penetration_Testing_Methodology.docx`](./ECSA_Network_Penetration_Testing_Methodology.docx)
**Target:** Luxury Treats (fictional client)

## What's in this document

The completed **EC-Council Certified Security Analyst (ECSA)** Network Penetration Testing methodology template — the structured framework used in industry-standard offensive security training and engagements. The template documents every test step performed against the target, with results captured in a consistent, auditable format.

### Tests documented

The methodology covers external network penetration testing across these test areas:

- **Test 1 — Port Scanning** — discovering live hosts, identifying open ports, mapping services
- **Test 2 — Operating System Fingerprinting** — identifying target OS via service banners and stack behavior
- **Test 3 — Service Enumeration** — querying running services for version and configuration data
- Additional tests per the ECSA template structure

### Sample findings recorded

For each test, the template records:

- The target organization (Luxury Treats — fictional)
- The URL/IP scope (`http://www.luxurytreats.com`, `untangle.example.com` at `172.19.1.24`, lab IPs in `172.19.19.x`)
- Whether the test succeeded
- Tools used (nslookup, nmap)
- The discovered hosts and services

### Identified findings (from this and related labs)

- **Windows Server 2008 R2 / 2012** running on target hosts (out of mainstream support — known-vulnerable)
- **Microsoft IIS 7.5** with known vulnerabilities
- Open ports: **FTP (21/tcp)**, **SMB over NetBIOS (139/tcp)**, **SMB direct (445/tcp)**, **RDP (3389/tcp)**, ephemeral high ports (49152-49157/tcp)
- HTTP traffic on port 80 (no HTTPS)

These findings are translated into actionable recommendations in [`06-recommendations-report`](../06-recommendations-report).

## What this demonstrates

- **Methodology discipline** — using a recognized industry framework (ECSA) rather than ad-hoc testing
- **Documentation rigor** — every test, target, tool, and result captured consistently
- **Tool execution** — actual nmap and nslookup work against authorized lab targets
- **Finding-to-action translation** — the discoveries here directly drive the recommendations in section 06

## Why ECSA matters

EC-Council's Certified Security Analyst certification is one of the standard credentials for working penetration testers. The methodology template used here is the same structure ECSA-certified testers use in real engagements — meaning this work is portable directly into a junior pen test role, not just academic exercise.

## Related deliverables

- [`03-lab-week-1-recon-and-set`](../03-lab-week-1-recon-and-set) — initial reconnaissance phase work
- [`04-lab-week-3-exploitation`](../04-lab-week-3-exploitation) — exploitation of identified services
- [`05-lab-final-internal-pentest`](../05-lab-final-internal-pentest) — internal-network methodology lab
- [`06-recommendations-report`](../06-recommendations-report) — findings translated for client action
