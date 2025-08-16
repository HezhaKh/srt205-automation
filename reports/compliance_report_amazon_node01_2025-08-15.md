# CIS Compliance Report for amazon_node01

**Date:** 2025-08-15
**Mode:** enforce










---

## Summary of Security Configurations
- Password Aging: UMASK		022, PASS_MAX_DAYS	90, PASS_MIN_DAYS	1, PASS_WARN_AGE	7, UID_MIN                  1000, UID_MAX                 60000, ENCRYPT_METHOD YESCRYPT
- Password Quality: minlen = 12, dcredit = -1, ucredit = -1, lcredit = -1, ocredit = -1, retry = 3
- SSHD Config: port 22, addressfamily any, listenaddress [::]:22, listenaddress 0.0.0.0:22, usepam yes, logingracetime 120, x11displayoffset 10, x11maxdisplays 1000, maxauthtries 4, maxsessions 10, clientaliveinterval 300, clientalivecountmax 3, requiredrsasize 1024, streamlocalbindmask 0177, permitrootlogin no, ignorerhosts yes, ignoreuserknownhosts no, hostbasedauthentication no, hostbasedusesnamefrompacketonly no, pubkeyauthentication yes, kerberosauthentication no, kerberosorlocalpasswd yes, kerberosticketcleanup yes, kerberosuniqueccache no, kerberosusekuserok yes, gssapienablek5users no, gssapiauthentication yes, gssapicleanupcredentials no, gssapikeyexchange no, gssapistrictacceptorcheck yes, gssapistorecredentialsonrekey no, gssapikexalgorithms gss-curve25519-sha256-,gss-nistp256-sha256-,gss-group14-sha256-,gss-group16-sha512-, passwordauthentication no, kbdinteractiveauthentication no, printmotd no, printlastlog yes, x11forwarding no, x11uselocalhost yes, permittty yes, permituserrc yes, strictmodes yes, tcpkeepalive yes, permitemptypasswords no, compression yes, gatewayports no, usedns no, allowtcpforwarding yes, allowagentforwarding yes, disableforwarding no, allowstreamlocalforwarding yes, streamlocalbindunlink no, fingerprinthash SHA256, exposeauthinfo no, pidfile /var/run/sshd.pid, modulifile /etc/ssh/moduli, xauthlocation /usr/bin/xauth, ciphers aes256-gcm@openssh.com,chacha20-poly1305@openssh.com,aes256-ctr,aes128-gcm@openssh.com,aes128-ctr, macs hmac-sha2-256-etm@openssh.com,hmac-sha1-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-512-etm@openssh.com,hmac-sha2-256,hmac-sha1,umac-128@openssh.com,hmac-sha2-512, banner none, forcecommand none, chrootdirectory none, trustedusercakeys none, revokedkeys none, securitykeyprovider internal, authorizedprincipalsfile none, versionaddendum none, authorizedkeyscommand /opt/aws/bin/eic_run_authorized_keys %u %f, authorizedkeyscommanduser ec2-instance-connect, authorizedprincipalscommand none, authorizedprincipalscommanduser none, hostkeyagent none, kexalgorithms curve25519-sha256,curve25519-sha256@libssh.org,ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group14-sha256,diffie-hellman-group16-sha512,diffie-hellman-group18-sha512, casignaturealgorithms ecdsa-sha2-nistp256,sk-ecdsa-sha2-nistp256@openssh.com,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,ssh-ed25519,sk-ssh-ed25519@openssh.com,rsa-sha2-256,rsa-sha2-512, hostbasedacceptedalgorithms ssh-ed25519-cert-v01@openssh.com,ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521-cert-v01@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,rsa-sha2-512-cert-v01@openssh.com,rsa-sha2-256-cert-v01@openssh.com,ssh-rsa-cert-v01@openssh.com,ssh-ed25519,ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,sk-ssh-ed25519@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,rsa-sha2-512,rsa-sha2-256,ssh-rsa, hostkeyalgorithms ecdsa-sha2-nistp256,ecdsa-sha2-nistp256-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521,ecdsa-sha2-nistp521-cert-v01@openssh.com,ssh-ed25519,ssh-ed25519-cert-v01@openssh.com,sk-ssh-ed25519@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,rsa-sha2-256,rsa-sha2-256-cert-v01@openssh.com,rsa-sha2-512,rsa-sha2-512-cert-v01@openssh.com, pubkeyacceptedalgorithms ecdsa-sha2-nistp256,ecdsa-sha2-nistp256-cert-v01@openssh.com,sk-ecdsa-sha2-nistp256@openssh.com,sk-ecdsa-sha2-nistp256-cert-v01@openssh.com,ecdsa-sha2-nistp384,ecdsa-sha2-nistp384-cert-v01@openssh.com,ecdsa-sha2-nistp521,ecdsa-sha2-nistp521-cert-v01@openssh.com,ssh-ed25519,ssh-ed25519-cert-v01@openssh.com,sk-ssh-ed25519@openssh.com,sk-ssh-ed25519-cert-v01@openssh.com,rsa-sha2-256,rsa-sha2-256-cert-v01@openssh.com,rsa-sha2-512,rsa-sha2-512-cert-v01@openssh.com, loglevel VERBOSE, syslogfacility AUTHPRIV, authorizedkeysfile .ssh/authorized_keys, hostkey /etc/ssh/ssh_host_rsa_key, hostkey /etc/ssh/ssh_host_ecdsa_key, hostkey /etc/ssh/ssh_host_ed25519_key, authenticationmethods any, subsystem sftp /usr/libexec/openssh/sftp-server, maxstartups 10:30:100, persourcemaxstartups none, persourcenetblocksize 32:128, permittunnel no, ipqos af21 cs1, rekeylimit 0 0, permitopen any, permitlisten any, permituserenvironment no, pubkeyauthoptions none
- Sysctl Settings: fs.suid_dumpable = 0, kernel.randomize_va_space = 2, net.ipv4.conf.all.accept_redirects = 1, net.ipv4.conf.all.accept_source_route = 0, net.ipv4.conf.all.log_martians = 0, net.ipv4.conf.all.secure_redirects = 1, net.ipv4.conf.all.send_redirects = 1, net.ipv4.conf.default.accept_redirects = 1, net.ipv4.conf.default.accept_source_route = 0, net.ipv4.conf.default.log_martians = 0, net.ipv4.conf.default.secure_redirects = 1, net.ipv4.conf.default.send_redirects = 1, net.ipv4.icmp_echo_ignore_broadcasts = 1, net.ipv4.icmp_ignore_bogus_error_responses = 1, net.ipv4.tcp_syncookies = 1, net.ipv6.conf.all.accept_ra = 1, net.ipv6.conf.all.accept_ra_defrtr = 1, net.ipv6.conf.all.accept_ra_from_local = 0, net.ipv6.conf.all.accept_ra_min_hop_limit = 1, net.ipv6.conf.all.accept_ra_min_lft = 0, net.ipv6.conf.all.accept_ra_mtu = 1, net.ipv6.conf.all.accept_ra_pinfo = 1, net.ipv6.conf.all.accept_ra_rt_info_max_plen = 0, net.ipv6.conf.all.accept_ra_rt_info_min_plen = 0, net.ipv6.conf.all.accept_ra_rtr_pref = 1, net.ipv6.conf.all.accept_redirects = 1, net.ipv6.conf.default.accept_ra = 1, net.ipv6.conf.default.accept_ra_defrtr = 1, net.ipv6.conf.default.accept_ra_from_local = 0, net.ipv6.conf.default.accept_ra_min_hop_limit = 1, net.ipv6.conf.default.accept_ra_min_lft = 0, net.ipv6.conf.default.accept_ra_mtu = 1, net.ipv6.conf.default.accept_ra_pinfo = 1, net.ipv6.conf.default.accept_ra_rt_info_max_plen = 0, net.ipv6.conf.default.accept_ra_rt_info_min_plen = 0, net.ipv6.conf.default.accept_ra_rtr_pref = 1, net.ipv6.conf.default.accept_redirects = 1
- Firewall (firewalld) Status: running; Default zone: public; Services: ssh
## Cron & At Restrictions
== /etc/cron.allow missing ==
== /etc/cron.deny missing ==
== /etc/at.allow missing ==
== /etc/at.deny ==

## /tmp Mount Options
/tmp options: rw,nosuid,nodev,seclabel,nr_inodes=1048576

## Time Synchronization
Timezone=
CanNTP=yes
NTP=yes
NTPSynchronized=yes
chronyd: active

## Sudo Logging
/etc/sudoers.d/10-logfile:1:Defaults logfile=/var/log/sudo.log
---

---

## Non-Compliant Issues
No non-compliance detected.
