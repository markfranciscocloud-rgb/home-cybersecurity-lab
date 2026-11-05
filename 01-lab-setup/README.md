# Week 1 — Windows, Linux, and VirtualBox inventory

## Objective

Record the host, virtual machine, and networking baseline before adding services.

## Inventory and evidence level

| Component | Recorded configuration | Evidence and qualification |
|---|---|---|
| Host | Dell Precision 3560; Windows 11 Pro; Intel Core i7-1185G7; 32 GB RAM | Reported in the prior Projects chat; hardware and Windows edition screenshots were not available in the retrieved turns, so not independently verified here |
| Windows DNS client | Windows PowerShell using nslookup | Directly visible in reviewed Week 2 screenshot E1 |
| Hypervisor | Oracle VirtualBox | Original Ubuntu setup document; no exact version recorded |
| Linux guest | Ubuntu | Original setup and Linux terminal screenshots |
| Guest release | Ubuntu 26.04.1 LTS | Prior chat report only; confirm with /etc/os-release before treating as independently verified |
| Original VM allocation | 8192 MB RAM, 4 processors, 25 GB disk | Original setup record; current allocation not rechecked |
| Original network | NAT | Original setup record |
| Week 2 network | Host-Only for Windows-to-Pi-hole; separate NAT for outbound access | Prior chat architecture; host-to-server DNS operation corroborated by E1 and E2 |
| Linux hostname | Ubuntu25 | Visible terminal label; a hostname does not establish the OS release |
| Recovery snapshot | Pre-installation snapshot reported | Prior chat only; snapshot inventory not supplied |

The [original Ubuntu setup](../ubuntu-vm-setup.md) and its embedded screenshot links are preserved unchanged. It records installation, updates, networking tools, and password recovery. Its command block mixes prose and commands and is historical evidence, not a script to paste into a terminal. Password recovery applies only to authorized machines. Tool installation notes do not demonstrate completed scanning labs.

## Remaining baseline checks

Capture the following locally and add a short, reviewed inventory summary:

- Windows edition, host model, CPU, and installed memory.
- VirtualBox version, current VM RAM/CPU/disk settings, and adapter modes.
- Ubuntu release from `cat /etc/os-release`, memory from `free -h`, storage from `lsblk`, and routes from `ip route`.
- Snapshot name and creation time, without assuming a snapshot replaces a backup.

These are future checks, not commands executed during this repository update. Exclude serial numbers, product keys, credentials, and unrelated host details.
