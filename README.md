# Home Cybersecurity Lab

## Purpose

This repository documents my home cybersecurity lab as I build practical skills in networking, Linux, Windows administration, and security analysis.

## Current progress

Updated November 5, 2026. This is a learning portfolio; planned tools and labs are not completed experience.

| Week | Lab | Status |
|---|---|---|
| 1 | [Windows, Linux, and VirtualBox inventory](01-lab-setup/README.md) | Ubuntu setup recorded; inventory evidence and remaining checks identified |
| 2 | [LAB-002: Pi-hole DNS filtering](02-networking-notes/LAB-002-pihole-dns-filtering.md) | Allowed and blocked DNS responses and Query Log visually verified |
| Next | [Windows Server and Active Directory](05-active-directory/README.md) | Planned |
| Future | [Vulnerability scanning](03-vulnerability-scanning/README.md) | Objective recorded; no scan results supplied |
| Future | [Incident response](04-incident-response/README.md) | Planned |

## Repository map

- `01-lab-setup/`: inventory and setup notes.
- `02-networking-notes/`: DNS lab, validation evidence, and troubleshooting.
- `03-vulnerability-scanning/`: original objective and future validation plan.
- `04-incident-response/`: planned log investigation.
- `05-active-directory/`: next lab and completion criteria.
- `screenshots/`: evidence index and screenshot handling.
- `archive/original/`: unchanged copies of every original file, including the earlier README.
- [Original Ubuntu setup](ubuntu-vm-setup.md): retained at its existing URL.

## Environment and demonstrated skills

Windows is the DNS test client; Ubuntu runs Pi-hole inside Oracle VirtualBox. A Host-Only connection carries test queries, with a separate NAT adapter for guest outbound access. See the [inventory](01-lab-setup/README.md) for the evidence level of each configuration detail.

Demonstrated: DNS validation, blocklist inspection, application log review, Windows/Linux command use, and virtualization documentation. The earlier lab record also describes resolver troubleshooting; its exact configuration diff is unavailable.

Kali Linux, a separate Windows client VM, vulnerable targets, Nmap scan results, Wireshark captures, Nessus/OpenVAS, and Active Directory are future work unless evidence is added.

## Rules of engagement

All scanning and testing will be performed only on systems I own or have explicit permission to test. This lab is for legal, ethical, educational use only. Do not expose a recursive DNS service or lab administration interface to the Internet.

## Progress log

### 2026-04-28
- Created GitHub repository and started documentation (original recorded date).

### 2026-11-05
- Organized existing files into navigable directories while preserving all original content.
- Documented Week 1 inventory with source qualifications.
- Verified Week 2 screenshots showing allowed and blocked DNS requests and matching Pi-hole logs.
- Defined [next labs](05-active-directory/README.md).

## Evidence and publication

The [evidence index](screenshots/README.md) distinguishes direct screenshot review, historical records, and pending checks. No credentials, resolver configuration secrets, or unrelated browsing logs are included. Public examples use `<PIHOLE_HOST_ONLY_IP>` and `<WINDOWS_HOST_ONLY_IP>`; substitute your own lab addresses. Private lab addresses are not credentials.
