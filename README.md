# Ansible Linux Hardening

Idempotent Ansible controls for baseline Linux security and operational hygiene. The project is organized as a reusable role rather than a monolithic playbook.

## Controls represented

- SSH daemon hardening
- Password and authentication defaults
- Audit service enablement
- Time synchronization
- Unnecessary service reduction
- Security-oriented sysctl settings

The defaults are intentionally conservative. Enterprise environments should map controls to their approved CIS/STIG profile and test changes against application requirements before enforcement.

## Run

```bash
ansible-playbook -i inventories/dev/hosts.yml site.yml --check --diff
ansible-playbook -i inventories/dev/hosts.yml site.yml
```
