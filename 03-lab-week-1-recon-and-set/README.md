# 03 — Lab Week 1: Reconnaissance & Social Engineer Toolkit

**Course:** CYB/427 — Security Analyst Threat Testing
**Lab platform:** Practice Labs / labondemand.com
**Module:** Social Engineering Penetration Testing Methodology
**Target:** Luxury Treats (fictional, lab-resident)

## What this lab covered

The first hands-on lab focused on **social engineering reconnaissance and credential harvesting** — the parts of an engagement that exploit the human layer of security rather than the technical layer. Specifically:

1. **Setup** — Kali Linux external network instance configured against the lab target
2. **Site cloning** — using Social Engineer Toolkit (SET) to clone the legitimate Luxury Treats login page
3. **Credential harvester deployment** — running the SET credential harvester to capture form submissions
4. **Successful credential capture** — POST credentials extracted from a victim browser session

## Screenshots

Selected lab screenshots showing actual tool execution:

| File | What it shows |
|---|---|
| `screenshot_kali_login.png` | Kali Linux external-network instance, lab environment confirmed |
| `screenshot_set_clone_target.png` | SET cloning `http://www.luxurytreats.com` — webattack credential harvester configured for IP `192.168.0.7` |
| `screenshot_set_credentials_captured.png` | Successful credential capture — POST data showing `txt_email=adam` and `txt_password=diamond` from a victim authentication attempt against the cloned page |

## What this demonstrates

- **SET fluency** — choosing the right SET attack module (webattack → site cloner → credential harvester) and configuring it correctly
- **Understanding of the social engineering attack chain** — clone → host → lure → capture
- **Practical evidence** — terminal output and successful POST capture aren't conceptual; they're proof of execution

## Why this matters

Social engineering attacks are responsible for a significant majority of real-world breaches — including the DNC breach analyzed in [section 01](../01-internal-vs-external-pentesting). A pen tester who can't execute the human-layer side of an engagement is missing the most consequential attack vector in modern security.

This lab is the foundational version of that skill — using SET to clone a site and capture credentials. In a real engagement, this would be paired with a phishing-email lure and a typo-domain hosting setup; the lab environment substitutes those external pieces with the controlled `192.168.0.7` host.

## A note on what's included

The course material for this week also included reconnaissance and social-engineering planning against a real organization (University of Phoenix). That material is **deliberately excluded** from this portfolio because publishing detailed attack plans against a named real entity — even when conducted as authorized academic exercise — is poor judgment in a public-portfolio context. The lab work captured here against the fictional Luxury Treats target demonstrates the same skills with no third-party risk.

## Related deliverables

- [`02-ecsa-methodology`](../02-ecsa-methodology) — the structured methodology these lab activities fit into
- [`04-lab-week-3-exploitation`](../04-lab-week-3-exploitation) — exploitation work that follows reconnaissance
