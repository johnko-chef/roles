# Ace

Host Service  | NIC   | IP Address      | Port
--------------|-------|-----------------|-----
firewall(pf)  |       |                 |
carp(ucarp)   | lagg0 | 192.168.x.2xx   |
sshd          | "     | 192.168.x.120   | 22
ntpd          | "     | "               | 123

Jail Service  | NIC   | IP Address      | Port
--------------|-------|-----------------|-----
dhcpd         | lagg0 | 192.168.x.121   | 67,647,7911,26328
dns           | lo1   | 10.7.7.1        | 192.168.x.201:53
pxe           | "     | 10.7.7.2        | 192.168.x.202:69,80
pkgng         | "     | 10.7.7.3        | 80
freebsdbase   | "     | 10.7.7.4        | 80
git           | "     | 10.7.7.5        | 192.168.x.205:22
log           | "     | 10.7.7.6        | 192.168.x.206:514
ldap          | "     | 10.7.7.7        | 192.168.x.207:389
maria(mysql)  | "     | 10.7.7.8        | 192.168.x.208:3306
smtp(postfix) | "     | 10.7.7.9        | 192.168.x.209:587
crm(odoo)     | "     | 10.7.7.10       | 80
imap(dbmail)  | "     | 10.7.7.11       | 192.168.x.211:993
horde(webmail)| "     | 10.7.7.12       | 80
sslterminator | "     | 10.7.7.13       | 192.168.x.213:443

Optional Jail | NIC   | IP Address      | Port
--------------|-------|-----------------|-----
littlechef    | lo1   | 10.123.234.250  | nat
release.build | "     | 10.123.234.251  | nat
mfsbsd.build  | "     | 10.123.234.252  | nat
