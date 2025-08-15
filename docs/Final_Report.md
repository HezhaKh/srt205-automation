## CIS Ubuntu – Final Summary

**Scope:** Single host `db_node01` audited and hardened using Ansible roles `cis_ubuntu` and `audit_compliance`.

**Key Controls Implemented:**
- Password aging (`/etc/login.defs`) and complexity (`/etc/security/pwquality.conf`)
- SSH hardening via drop-in (`/etc/ssh/sshd_config.d/10-ansible.conf`) with:
  - `PermitRootLogin no`, `PasswordAuthentication no`, `MaxAuthTries 4`,
  - `ClientAliveInterval 300`, `ClientAliveCountMax 3`, `LogLevel VERBOSE`
- Kernel hardening (`ASLR`, core dumps, `ptrace_scope`)
- Logging services (`auditd`, `rsyslog`) enabled and active
- Firewall (`ufw`) active with default deny inbound and SSH allowed
- Time sync: `systemd-timesyncd` enabled/active
- `cron/at` restrictions: only root allowed
- Sudo logging to `/var/log/sudo.log` (drop-in validated)

**Evidence:**
- Audit log: `docs/evidence/ubuntu_audit_<timestamp>.log`
- Enforce log: `docs/evidence/ubuntu_enforce_<timestamp>.log`
- Compliance report: `reports/compliance_report_db_node01_<date>.md` (No non-compliance detected)

**Idempotency Results:** Subsequent runs show zero drift (`ok` state, minimal `changed`).

**Challenges & Fixes:**
- Report initially wrote to remote → fixed with `delegate_to: localhost`.
- Jinja templating with mixed result/list types → normalized to line lists in `audit_compliance`.
- Robust SSHD parsing (context `-C`, lowercase, regex-safe extraction) eliminated false positives.

**Improvements (future):**
- Add GitHub Actions to run `ansible-lint` and `--syntax-check`.
- Optional CI fail gate when `non_compliant_items` > 0.
