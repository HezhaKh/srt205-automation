(.venv) hkhoshnoud@miXtile:~/srt205/repo/srt205-project$ ansible-playbook -i inventory/hosts.ini site.yml -e "cis_mode=audit"
sed -n '1,200p' reports/compliance_report_db_node01_$(date +%F).md

PLAY [CIS Ubuntu] ***************************************************************************************************************************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************************************************************************************************************************
[WARNING]: Platform linux on host db_node01 is using the discovered Python interpreter at /usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of that path. See
https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [db_node01]

TASK [cis_ubuntu : Install baseline packages (pwquality, auditd, ufw, rsyslog, unattended-upgrades)] ****************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Audit baseline packages presence] ****************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Record missing baseline packages (audit)] ********************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Configure password aging in /etc/login.defs] *****************************************************************************************************************************************************************
skipping: [db_node01] => (item={'key': 'PASS_MAX_DAYS', 'value': 90}) 
skipping: [db_node01] => (item={'key': 'PASS_MIN_DAYS', 'value': 1}) 
skipping: [db_node01] => (item={'key': 'PASS_WARN_AGE', 'value': 7}) 
skipping: [db_node01]

TASK [cis_ubuntu : Audit password aging values] *********************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Configure pwquality minimums] ********************************************************************************************************************************************************************************
skipping: [db_node01] => (item={'key': 'minlen', 'value': 12}) 
skipping: [db_node01] => (item={'key': 'dcredit', 'value': -1}) 
skipping: [db_node01] => (item={'key': 'ucredit', 'value': -1}) 
skipping: [db_node01] => (item={'key': 'lcredit', 'value': -1}) 
skipping: [db_node01] => (item={'key': 'ocredit', 'value': -1}) 
skipping: [db_node01] => (item={'key': 'retry', 'value': 3}) 
skipping: [db_node01]

TASK [cis_ubuntu : Audit pwquality.conf] ****************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Ensure sudo logging is configured via drop-in] ***************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Ensure sudo log file exists with secure perms] ***************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Audit sudo logging] ******************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Template hardened sshd drop-in] ******************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Audit sshd effective settings] *******************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Normalize sshd audit lines for report] ***********************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Ensure ASLR is enabled] **************************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Restrict core dumps] *****************************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Restrict ptrace_scope] ***************************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Audit kernel/sysctl hardening] *******************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Ensure auditd is enabled and running] ************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Ensure rsyslog is enabled and running] ***********************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Ensure unattended-upgrades service is enabled] ***************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Check UFW status (verbose)] **********************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Reset UFW rules (only when needed)] **************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Set default deny inbound] ************************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Allow SSH port] **********************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Enable UFW (only if inactive)] *******************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Remove cron.deny and at.deny] ********************************************************************************************************************************************************************************
skipping: [db_node01] => (item=/etc/cron.deny) 
skipping: [db_node01] => (item=/etc/at.deny) 
skipping: [db_node01]

TASK [cis_ubuntu : Ensure cron.allow exists and only allows root] ***************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Ensure at.allow exists and only allows root] *****************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Check if /tmp has an fstab entry] ****************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Update /tmp options in /etc/fstab to include nodev,nosuid,noexec] ********************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Remount /tmp with secure options] ****************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Enable and start systemd-timesyncd] **************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Disable/stop chrony if present] ******************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Disable/stop ntp if present] *********************************************************************************************************************************************************************************
skipping: [db_node01]

TASK [cis_ubuntu : Audit UFW status] ********************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Audit cron/at allow/deny] ************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Audit /tmp mount options] ************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Audit time sync services] ************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [cis_ubuntu : Build audit summary (controller-side print)] *****************************************************************************************************************************************************************
ok: [db_node01] => {
    "msg": {
        "cron_at": [
            "-rw------- 1 root root 5 Aug 15 04:38 /etc/at.allow",
            "-rw------- 1 root root 5 Aug 15 04:38 /etc/cron.allow"
        ],
        "login_defs": [
            "PASS_MAX_DAYS\t90",
            "PASS_MIN_DAYS\t1",
            "PASS_WARN_AGE\t7"
        ],
        "missing_packages": [],
        "mode": "audit",
        "pwquality": [
            "minlen = 12",
            "dcredit = -1",
            "ucredit = -1",
            "lcredit = -1",
            "ocredit = -1",
            "retry = 3"
        ],
        "sshd": [],
        "sudo_log": [
            "/etc/sudoers.d/10-logfile:Defaults logfile=/var/log/sudo.log",
            "-rw-r----- 1 root adm 46845 Aug 15 04:50 /var/log/sudo.log"
        ],
        "sysctl": [
            "kernel.randomize_va_space = 2",
            "fs.suid_dumpable = 0",
            "kernel.yama.ptrace_scope = 1"
        ],
        "timesync": [
            "enabled",
            "active",
            "not-found",
            "not-found"
        ],
        "tmp_mount": [],
        "ufw": [
            "Status: active",
            "Logging: on (low)",
            "Default: deny (incoming), allow (outgoing), disabled (routed)",
            "New profiles: skip",
            "",
            "To                         Action      From",
            "--                         ------      ----",
            "22/tcp                     ALLOW IN    Anywhere                  ",
            "22/tcp (v6)                ALLOW IN    Anywhere (v6)             "
        ]
    }
}

TASK [audit_compliance : Ensure report directory exists (controller)] ***********************************************************************************************************************************************************
ok: [db_node01 -> localhost]

TASK [audit_compliance : Initialize non_compliant_items] ************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Normalize audit vars to line lists] ********************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Find SSHD MaxAuthTries line] ***************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Parse SSHD MaxAuthTries (robust)] **********************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Evaluate SSHD controls] ********************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Evaluate sysctl controls] ******************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Evaluate UFW] ******************************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Evaluate sudo logging] *********************************************************************************************************************************************************************************
ok: [db_node01]

TASK [audit_compliance : Render compliance report (controller)] *****************************************************************************************************************************************************************
changed: [db_node01 -> localhost]

TASK [audit_compliance : Show report path (controller)] *************************************************************************************************************************************************************************
ok: [db_node01 -> localhost] => {
    "msg": "Report: /home/hkhoshnoud/srt205/repo/srt205-project/reports/compliance_report_db_node01_2025-08-15.md"
}

PLAY RECAP **********************************************************************************************************************************************************************************************************************
db_node01                  : ok=32   changed=1    unreachable=0    failed=0    skipped=19   rescued=0    ignored=0

# CIS Compliance Report for db_node01

**Date:** 2025-08-15
**Mode:** audit










---

## Summary of Security Configurations
- Password Aging: PASS_MAX_DAYS	90, PASS_MIN_DAYS	1, PASS_WARN_AGE	7
- Password Quality: minlen = 12, dcredit = -1, ucredit = -1, lcredit = -1, ocredit = -1, retry = 3
- SSHD Config: port 22, addressfamily any, listenaddress [::]:22, listenaddress 0.0.0.0:22, usepam no, logingracetime 120, x11displayoffset 10, maxauthtries 4, maxsessions 10, clientaliveinterval 300, clientalivecountmax 3, requiredrsasize 1024, streamlocalbindmask 0177, unusedconnectiontimeout none, permitrootlogin no, ignorerhosts yes, ignoreuserknownhosts no, hostbasedauthentication no, hostbasedusesnamefrompacketonly no, pubkeyauthentication yes, kerberosauthentication yes, kerberosorlocalpasswd yes, kerberosticketcleanup yes, gssapiauthentication no, gssapicleanupcredentials yes, gssapikeyexchange no, gssapistrictacceptorcheck yes, gssapistorecredentialsonrekey no, gssapikexalgorithms gss-group14-sha256-,gss-group16-sha512-,gss-nistp256-sha256-,gss-curve25519-sha256-,gss-group14-sha1-,gss-gex-sha1-, passwordauthentication no, kbdinteractiveauthentication no, printmotd no, printlastlog yes, x11forwarding no, x11uselocalhost yes, permittty yes, permituserrc yes, strictmodes yes, tcpkeepalive yes, permitemptypasswords no, compression yes, gatewayports no, usedns no, allowtcpforwarding yes, allowagentforwarding yes, disableforwarding no, allowstreamlocalforwarding yes, streamlocalbindunlink no, fingerprinthash sha256, exposeauthinfo no, debianbanner yes, pidfile /run/sshd.pid, modulifile /etc/ssh/moduli, xauthlocation /usr/bin/xauth, ciphers chacha20-poly1305@openssh.com,aes128-ctr,aes192-ctr,aes256-ctr,aes128-gcm@openssh.com,aes256-gcm@openssh.com, macs umac-64-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-256-etm@openssh.com,hmac-sha2-512-etm@openssh.com,hmac-sha1-etm@openssh.com,umac-64@openssh.com,umac-128@openssh.com,hmac-sha2-256,hmac-sha2-512,hmac-sha1, banner none, forcecommand none, chrootdirectory none, trustedusercakeys none, revokedkeys none, securitykeyprovider internal, authorizedprincipalsfile none, versionaddendum none, authorizedkeyscommand none, authorizedkeyscommanduser none, authorizedprincipalscommand none, authorizedprincipalscommanduser none, hostkeyagent none, kexalgorithms sntrup761x25519-sha512@openssh.com,curve25519-sha256,curve25519-sha256@libssh.org,ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group16-sha512,diffie-hellman-group18-sha512,diffie-hellman-group14-sha256, casignaturealgorithms ssh-ed25519,ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,rsa-sha2-512,rsa-sha2-256, hostbasedacceptedalgorithms ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-ed25519,ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,rsa-sha2-512,rsa-sha2-256, hostkeyalgorithms ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-ed25519,ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,rsa-sha2-512,rsa-sha2-256, pubkeyacceptedalgorithms ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-ed25519,ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,rsa-sha2-512,rsa-sha2-256, loglevel verbose, syslogfacility auth, authorizedkeysfile .ssh/authorized_keys .ssh/authorized_keys2, hostkey /etc/ssh/ssh_host_rsa_key, hostkey /etc/ssh/ssh_host_ecdsa_key, hostkey /etc/ssh/ssh_host_ed25519_key, acceptenv lang, acceptenv lc_*, authenticationmethods any, channeltimeout none, subsystem sftp /usr/lib/openssh/sftp-server , maxstartups 10:30:100, persourcemaxstartups none, persourcenetblocksize 32:128, permittunnel no, ipqos lowdelay throughput, rekeylimit 0 0, permitopen any, permitlisten any, permituserenvironment no, pubkeyauthoptions none
- Sysctl Settings: kernel.randomize_va_space = 2, fs.suid_dumpable = 0, kernel.yama.ptrace_scope = 1
- UFW Status: Status: active; Logging: on (low); Default: deny (incoming), allow (outgoing), disabled (routed)


## Cron & At Restrictions
-rw------- 1 root root 5 Aug 15 04:38 /etc/at.allow
-rw------- 1 root root 5 Aug 15 04:38 /etc/cron.allow


## Time Synchronization
enabled
active
not-found
not-found

## Sudo Logging
/etc/sudoers.d/10-logfile:Defaults logfile=/var/log/sudo.log
-rw-r----- 1 root adm 46845 Aug 15 04:50 /var/log/sudo.log

---

## Non-Compliant Issues
No non-compliance detected.
