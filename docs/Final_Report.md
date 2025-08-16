## CIS Ubuntu and amazon – Final Summary

**Project:** CIS-style Baseline for Ubuntu & Amazon Linux 2

## Scope & Approach

- Implemented separate hardening roles:
  - `cis_ubuntu` (UFW, pwquality, login.defs, sshd, sysctl, timesync, unattended-upgrades)
  - `cis_amazon` (firewalld, pwquality, login.defs, sshd, sysctl, chronyd, dnf-automatic)
- Common reporting via `audit_compliance` role:
  - Enforces and/or audits a minimal sysctl baseline and critical file permissions
  - Writes JSON to `/var/tmp/audit_compliance_report.json`
  - Renders controller-side Markdown into `reports/`

**Key Controls Implemented:**
- Completed without task failures.
- **Noncompliant sysctl items detected (4):**
  - `net.ipv4.conf.all.send_redirects`
  - `net.ipv4.conf.default.send_redirects`
  - `net.ipv4.conf.default.accept_source_route`
  - `fs.suid_dumpable` (actual: `2`)
- UFW active; SSH allowed on 22/tcp; defaults deny incoming, allow outgoing.
- Evidence and report written under `docs/evidence/` and `reports/`.

### Amazon Linux 2 group (`-l amazon`, mode: **enforce**)
- Completed without task failures.
- **No remaining sysctl drift** (12 checked, 0 noncompliant).
- firewalld enabled; chronyd active; auto-updates configured via `dnf-automatic`.
- Evidence and report written under `docs/evidence/` and `reports/`.

## Remediation Notes (amazon)
- Switch to enforce to remediate automatically:
```bash
  ansible-playbook -i inventory/hosts.ini site.yml -e "cis_mode=enforce" -l amazon
```

**Evidence:**
- Audit log: `docs/evidence/amazon_audit_<timestamp>.log`
- Enforce log: `docs/evidence/amazon_enforce_<timestamp>.log`
- Compliance report: `reports/compliance_report_db_node01_<date>.md` (No non-compliance detected)

**Idempotency Results:** Subsequent runs show zero drift (`ok` state, minimal `changed`).

**Challenges & Fixes:**
- Report initially wrote to remote → fixed with `delegate_to: localhost`.
- Jinja templating with mixed result/list types → normalized to line lists in `audit_compliance`.
- Robust SSHD parsing (context `-C`, lowercase, regex-safe extraction) eliminated false positives.
