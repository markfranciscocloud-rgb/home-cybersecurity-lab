# LAB-002 — Evidence register

Reviewed November 5, 2026 from attachments recovered from the Projects chat. Originals remain in that chat; raw screenshots are not committed here. The following is a transcription of observed results, not a new execution log.

## E1 — Windows DNS responses

Source: image(20261105-174438).png  
SHA-256: `F5C82F8865EA2D8123CDD3A95D1BD26B6FAFDF54984CF224EECFFD4644AE550E`

PowerShell shows explicit nslookup requests to the same Pi-hole server. doubleclick.net returns `::` and `0.0.0.0`. example.com returns two IPv6 and two IPv4 answers. The server is identified as pi.hole. Lab addresses are represented by role aliases in the report.

## E2 — Pi-hole Query Log

Source: image(20261105-174618).png  
SHA-256: `B4F7DA8A9C786D96684F77CA0156C30CBBD4167CEB9C01AD451DE7AA9D46B0C2`

| Displayed timestamp | Domain | Type | Observed handling |
|---|---|---|---|
| 2026-11-05 10:42:49 | doubleclick.net | A and AAAA | Red rows with blocked icons |
| 2026-11-05 10:43:03 | example.com | A and AAAA | Green rows with allowed handling |

All four entries show the same Windows Host-Only client. The interface shows Active status. Times are copied from the screenshot; the dashboard timezone was not established. The Allow and Deny buttons offer actions and are not the current handling status.

## E3 — Blocklist query

Source: image(20261105-174133).png, visually reviewed.

`sudo pihole query doubleclick.net` reports one matching list: StevenBlack's hosts list, marked block. Membership alone would not prove enforcement; E1 and E2 provide that confirmation.

## Historical reports without direct evidence in this review

The prior assistant described successful ping, FTL listening on TCP/UDP 53, snapshot creation, password rotation, and resolver configuration repairs. These are retained as reported context. Original terminal logs/configuration diffs for those events were not verified here. Do not reconstruct missing output or mark those checks as newly passed.
