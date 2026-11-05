# Week 2 — LAB-002: Pi-hole DNS filtering

**Lab record date:** November 5, 2026  
**Status:** Functional DNS filtering verified from supplied screenshots; no live retest performed during this repository update.

## Objective

Deploy Pi-hole on an Ubuntu VM, test DNS from Windows, and correlate responses with the application's Query Log.

## Architecture

```text
Windows host / DNS test client
       |
       | Explicit DNS queries to <PIHOLE_HOST_ONLY_IP>
       | VirtualBox Host-Only connection
       v
Ubuntu VM / Pi-hole
       |
       | Separate VirtualBox NAT adapter (reported configuration)
       v
Upstream DNS (Cloudflare selected, according to prior chat)
```

The prior chat reports household eero DNS and DHCP were unchanged. Explicit server arguments test Pi-hole directly; they do not prove Windows uses Pi-hole for all DNS traffic. Host-Only plus NAT is not complete isolation.

## Recorded implementation

The Projects chat reports a static Host-Only address, a recovery snapshot, resolution of a systemd-resolved port 53 conflict, Pi-hole installation, and replacement of the generated administrator password. Exact installation commands, resolver diffs, snapshot metadata, and software versions were not supplied in the retrieved turns. These steps are historical reports rather than independently reproduced results.

## Tests

Run in Windows PowerShell, replacing the placeholder with your VM's Host-Only address:

```powershell
nslookup example.com <PIHOLE_HOST_ONLY_IP>
nslookup doubleclick.net <PIHOLE_HOST_ONLY_IP>
```

| Test | Observed result |
|---|---|
| Allowed domain | example.com returned IPv4 and IPv6 answers |
| Blocked domain | doubleclick.net returned 0.0.0.0 and :: |
| Client attribution | Matching Pi-hole log entries identify the Windows Host-Only client |
| Blocklist membership | Linux CLI screenshot shows doubleclick.net matched the StevenBlack hosts list |

See [evidence](evidence.md) for exact source descriptions. Allowed addresses may change; the historical addresses are not acceptance criteria. Block behavior depends on configured blocking mode and list contents.

## Outcome and limits

The two responses plus matching Query Log entries demonstrate allowed and blocked DNS queries from a separate Windows client. This does not establish network-wide filtering, browser DNS-over-HTTPS coverage, every advertising domain being blocked, or permanent service health.

## Next actions

- Preserve a reviewed configuration backup and verify recovery.
- Repeat the allowed/blocked tests after a VM reboot and record results.
- Record actual Ubuntu, VirtualBox, and Pi-hole versions.
- Continue to the [Active Directory plan](../05-active-directory/README.md).
