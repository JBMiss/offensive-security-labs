# Offensive Security Labs — Penetration Testing on a Fictional Target

> Hands-on penetration testing labs against a fictional client (Luxury Treats), executing the full ECSA methodology — reconnaissance, social engineering, exploitation, and post-engagement reporting. Real Kali Linux work captured in terminal screenshots.

**Author:** Jesse Missaghian
**Program:** B.S. in Cybersecurity, University of Phoenix
**Course:** CYB/427 — Security Analyst Threat Testing
**Timeline:** February – March 2024
**Lab environment:** Practice Labs / labondemand.com

---

## What this project is

The methodology repos in this portfolio show *how I think* about a pen test. This repo shows *me actually doing one* — running the tools, capturing the output, executing the methodology end-to-end against a fictional client (Luxury Treats) in a controlled lab environment.

The work follows the **EC-Council Certified Security Analyst (ECSA) methodology**, which is the structured framework used in CEH / ECSA certification training. Each phase produces specific deliverables, captured here in their original form.

## Why this matters for a security role

Most junior pen testing job descriptions list the same handful of skills, and this repo demonstrates them with documented evidence:

- **Kali Linux fluency** — terminal screenshots showing tool execution, not just claims of familiarity
- **Reconnaissance and OSINT** — using theHarvester, Netcraft, Whois against an authorized target
- **Social engineering** — using the Social Engineer Toolkit (SET) to clone a target site and harvest credentials
- **Exploitation** — FTP service exploitation, file upload vulnerabilities, BeEF browser hooking
- **Methodology compliance** — completing the ECSA template that documents every test step
- **Post-engagement reporting** — translating findings into a client-facing recommendations report

## The six deliverables

| # | Deliverable | What it shows |
|---|---|---|
| [01](./01-internal-vs-external-pentesting) | **Internal vs External Pen Testing** | Conceptual paper on the two pen test models and when to use each |
| [02](./02-ecsa-methodology) | **ECSA Methodology Template** | Completed Network Penetration Testing methodology document — port scanning, OS fingerprinting, service enumeration |
| [03](./03-lab-week-1-recon-and-set) | **Week 1: Recon & SET** | Social Engineering Toolkit credential harvester against a cloned Luxury Treats login page |
| [04](./04-lab-week-3-exploitation) | **Week 3: FTP Exploitation** | FTP server access, file upload, directory traversal — anonymous-access exploitation |
| [05](./05-lab-final-internal-pentest) | **Final Lab: Internal Pen Test** | Full internal-network methodology lab — service enumeration, BeEF browser exploitation, privilege escalation work (100% completed) |
| [06](./06-recommendations-report) | **Client Recommendations Report** | Post-engagement report translating technical findings into prioritized client action items |

## Tools demonstrated in this repo

**Reconnaissance:** Nmap, theHarvester, Netcraft, Whois, OpenVAS

**Exploitation & Social Engineering:** Metasploit Framework, Social Engineer Toolkit (SET), BeEF (Browser Exploitation Framework), msfvenom

**Service-level testing:** FTP exploitation (anonymous access, file upload, directory listing), SMB/NetBIOS enumeration, RDP analysis

**Methodology framework:** EC-Council Certified Security Analyst (ECSA) Network Penetration Testing template

## A note on the target

All work in this repo was performed against **Luxury Treats** — a fictional company set up by the lab environment specifically for penetration testing exercises. The lab IP space (`172.19.x.x`, `172.20.x.x`) and the labondemand.com lab platform ensure no real-world targets were touched. The course also included an OSINT exercise against a real organization (University of Phoenix), but **that material is not included in this portfolio repo** — publishing detailed reconnaissance and social-engineering attack plans against any real, named entity is poor judgment in a public-portfolio context, even when conducted as authorized academic work.

## How to read this repo

**5 minutes:** read this README and skim [`05-lab-final-internal-pentest`](./05-lab-final-internal-pentest) — the most visually compelling lab screenshots are there.

**15 minutes:** add [`02-ecsa-methodology`](./02-ecsa-methodology) and [`06-recommendations-report`](./06-recommendations-report) — these show the bookends of an engagement (methodology going in, findings coming out).

**30 minutes:** read all six in order. The flow tracks the chronological progression of an ECSA engagement.

---

## About me

Cybersecurity professional based in Fresno, CA, completing my B.S. in Cybersecurity at University of Phoenix and CompTIA Security+ certified. Open to roles in cybersecurity — analyst, SOC, pen testing, network security.

- 🐙 [GitHub: @JBMiss](https://github.com/JBMiss)
- 💼 [LinkedIn: Jesse Missaghian](https://www.linkedin.com/in/jesse-missaghian-b77b4516a)

## Companion portfolio repos

- [Red Cyber Solutions Capstone](https://github.com/JBMiss/red-cyber-solutions-capstone) — security program design (strategic)
- [Wireless Network Security](https://github.com/JBMiss/wireless-network-security) — network design and packet analysis (technical)
- [Pentest Methodology](https://github.com/JBMiss/pentest-methodology) — pre-engagement work (scoping, OSINT, legal)
