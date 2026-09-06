# Hardening Control Mapping

This role demonstrates how enterprise Linux controls can be expressed as idempotent configuration rather than one-off shell changes.

| Area | Control | Automation |
|---|---|---|
| SSH | Disable direct root login | templated sshd config |
| SSH | Restrict authentication retries | templated sshd config |
| Audit | Ensure auditd is enabled | service task |
| Kernel | Disable IPv4 source routing | sysctl task |
| Time | Install chrony | package task |

## Production approach

Before enforcing a control, map it to the organization's approved CIS/STIG baseline, test it in non-production, document exceptions, and preserve a rollback path. Security baselines should be versioned and peer reviewed like application code.
