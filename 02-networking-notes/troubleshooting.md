# LAB-002 — DNS troubleshooting record

## Reported problem

The Projects chat describes systemd-resolved's DNS stub listener occupying port 53 during Pi-hole setup. It also describes configuration syntax and file-path corrections, inspection of resolver symlinks, and checking upstream DNS.

The original failing output and final configuration diff are unavailable in the retrieved material. This is a qualified incident summary, not proof of a particular root cause or a reusable configuration fix.

## Supported outcome

The reviewed Windows responses and Pi-hole Query Log establish that client DNS queries subsequently reached Pi-hole and filtering worked. They do not identify exactly which configuration change fixed the earlier conflict.

## Diagnostic checks for a recurrence

These are suggested checks, not captured troubleshooting output:

```bash
sudo ss -lntup
systemctl status systemd-resolved --no-pager
resolvectl status
readlink -f /etc/resolv.conf
cat /etc/resolv.conf
sudo pihole status
ip route
```

Identify the process and bind address using port 53, distinguish a local resolver stub from Pi-hole's intended listener, and confirm the guest retains a working upstream resolver. Do not blindly disable services or replace resolv.conf based on this historical summary. Record the before/after configuration and retest DNS from both Ubuntu and Windows.

If local DNS works but Windows queries fail, check the explicit server address, VM Host-Only adapter, guest listener, and firewall. If a domain is not blocked, compare blocklist membership, configured blocking mode, and the application's log.

## Evidence to retain next time

- Exact error and relevant listener output.
- Reviewed before/after resolver settings and symlink target.
- Service state and allowed/blocked tests after the change.
- Matching client log entries and reboot persistence results.

Exclude passwords and unrelated DNS history.
