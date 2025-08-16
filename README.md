# SRT205 CIS Hardening Project

This repo applies a minimal CIS-style hardening baseline to:
- **Ubuntu** (group: `ubuntu`) using UFW
- **Amazon Linux 2** (group: `amazon`) using firewalld / dnf-automatic

It also generates Markdown compliance reports and JSON evidence.

### How to run
**Inventory:** `inventory/hosts.ini`

**Modes:**
- Audit (no changes):
  `ansible-playbook -i inventory/hosts.ini site.yml -e "cis_mode=audit"`
- Enforce (apply hardening where missing):
  `ansible-playbook -i inventory/hosts.ini site.yml -e "cis_mode=enforce"`

**Artifacts:**
- Compliance reports are generated on the controller: `./reports/compliance_report_<host>_<date>.md`
- Logs (suggested): `./docs/evidence/*.log`

**Idempotency:** All tasks are idempotent; re-running should yield `ok`/`skipping` with no drift.

**Selective runs (tags):**
- SSH only: `--tags ssh`
- Auth/sudo: `--tags auth`
- Kernel/sysctl: `--tags sysctl`
- Services (auditd/rsyslog/ufw/time): `--tags services`
- Reporting: handled by `audit_compliance` at the end of the play
