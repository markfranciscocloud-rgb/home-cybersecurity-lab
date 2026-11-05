# Next lab — Windows Server and Active Directory

**Status:** Planned. No domain controller, domain join, or Group Policy results have been verified.

## Objective

Build a small Windows domain in VirtualBox and document identity administration.

## Proposed sequence

1. Verify available memory/storage and supported installation media before choosing VM allocations.
2. Create a dedicated lab network and recovery baseline; keep household DHCP/DNS unchanged.
3. Install Windows Server and record its version and configuration.
4. Configure a lab domain controller and DNS.
5. Add an authorized Windows client VM and verify domain join.
6. Create test users and security groups with least privilege.
7. Apply a simple Group Policy and capture its effective result.
8. Test sign-in, name resolution, policy application, and recovery.

## Evidence required

A network diagram, reviewed inventory, DNS and join results, test account/group examples, and policy validation. Use disposable lab accounts and omit credentials and product keys.

## Following labs

- [Authorized scanning and remediation](../03-vulnerability-scanning/README.md)
- [Log investigation and incident response](../04-incident-response/README.md)

Choose detailed settings when the lab begins; these steps are plans, not executed changes.
