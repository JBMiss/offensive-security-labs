# 06 — Client Recommendations Report

**Course:** CYB/427 — Security Analyst Threat Testing
**Deliverable:** [`Recommendations_Report.docx`](./Recommendations_Report.docx)
**Target:** Luxury Treats (fictional client)

## What's in this document

The post-engagement deliverable — a client-facing recommendations report that translates the technical findings from the penetration testing labs into a prioritized, actionable security action plan. This is the document the client actually reads after a pen test.

The report covers eight recommendation areas:

### 1. Upgrade Operating Systems
- Windows Server 2008 R2 and 2012 are out of mainstream support
- Plan migration to a current, supported version

### 2. Secure Web Services
- IIS 7.5 has known vulnerabilities — upgrade or fully patch
- Implement HTTPS for HTTP traffic on port 80

### 3. Patch Management
- Regular patching for FTP (21/tcp), SMB/NetBIOS (139/tcp, 445/tcp), RDP (3389/tcp)
- Verify patch application via subsequent vulnerability scans

### 4. Restrict and Secure Remote Access
- RDP (3389/tcp) requires network-level authentication, strong passwords, ideally two-factor authentication
- Consider VPN-gated access or IP-allowlisting for RDP

### 5. Network Segmentation and Firewall Configuration
- Segment critical assets from the rest of the network
- Restrict inbound and outbound traffic to only necessary services

### 6. Disable Unnecessary Services and Ports
- Close high-numbered ephemeral ports (49152-49157/tcp)
- Disable legacy protocols like SMBv1
- Reduce attack surface to only required services

### 7. Service Configuration Review
- Review configurations of all running services for hardening opportunities

### 8. Additional Mitigations
- Logging, monitoring, and incident response readiness

## What this demonstrates

- **Client-facing communication** — the report is written for the client's IT leadership, not for a fellow pen tester. Technical findings are paired with business-aligned action items.
- **Prioritization, not just enumeration** — every finding has a recommended action; the report doesn't just dump a vulnerability list and call it done
- **Risk awareness** — the recommendations recognize that not every finding is equally urgent (e.g., out-of-support OS is more pressing than ephemeral port closure)
- **End-to-end completeness** — the previous deliverables in this repo find vulnerabilities; this one closes the loop by addressing them

## Why post-engagement reporting matters

A pen test that finds vulnerabilities but doesn't translate them into actionable client guidance has failed at the most important part of the work. The recommendations report is what the client uses to actually improve their security posture — not the lab screenshots, not the methodology template, not the conceptual frameworks. This document is the engagement deliverable.

## Key takeaway

The connection between the discoveries in [`02-ecsa-methodology`](../02-ecsa-methodology), [`04-lab-week-3-exploitation`](../04-lab-week-3-exploitation), and [`05-lab-final-internal-pentest`](../05-lab-final-internal-pentest) and the recommendations in this report is what makes the engagement complete. Each finding maps to a specific recommendation here:

- **FTP exploitation in Lab 3** → "Disable Unnecessary Services and Ports" + "Patch Management"
- **Open RDP in ECSA template findings** → "Restrict and Secure Remote Access"
- **Outdated Windows Server / IIS in port scans** → "Upgrade Operating Systems" + "Secure Web Services"

A pen tester who can draw those connections reliably is a pen tester whose findings actually get fixed.
